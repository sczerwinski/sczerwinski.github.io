---
disqusid: functional-square-matrix-in-kotlin
title: Functional Square Matrix in Kotlin
mobileTitle: Functional Square Matrix…
layout: post
abstract: How to create a simple functional square matrix in Kotlin programming language
keywords: kotlin,functional,programming,matrix,affine,transformations,inverse,inversion,adjugate,cofactor,comatrix,determinant,traspose,transposition,3d,opengl
---

## A little theory: Affine transformations

Working with OpenGL and 3D graphics would be impossible without
[affine transformations](https://en.wikipedia.org/wiki/Affine_transformation),
which in general can be represented as:

$$\vec{y} = \boldsymbol{A} \vec{x} + \vec{a}$$

where $$\vec{a}$$ is a translation vector, and $$\boldsymbol{A}$$ is a matrix representation
of a [linear map](https://en.wikipedia.org/wiki/Linear_map).

The same transformation can also be represented by a single multiplication
of an augmented matrix (also called an _affine transformation matrix_) and an augmented vector:

$$
\begin{bmatrix}\vec{y}\\1\end{bmatrix} = \left[\begin{array}{ccc|c}
  & \boldsymbol{A} & & \vec{a} \\
  0 & … & 0 & 1
\end{array}\right] \begin{bmatrix}\vec{x}\\1\end{bmatrix}
$$

So in 3D space, an augmented matrix is a 4×4 matrix, while an augmented vector consists of 4 coordinates: $$(x, y, z, 1)$$.

Using this representation, we can compose affine transformations by simply multiplying augmented matrices: 

$$
\begin{bmatrix}\vec{y}\\1\end{bmatrix} = \left[\begin{array}{ccc|c}
  & \boldsymbol{A} & & \vec{a} \\
  0 & … & 0 & 1
\end{array}\right] \left[\begin{array}{ccc|c}
  & \boldsymbol{B} & & \vec{b} \\
  0 & … & 0 & 1
\end{array}\right] \begin{bmatrix}\vec{x}\\1\end{bmatrix}
$$

## The problem: Normal matrix

While matrix multiplication is a relatively simple operation, computing a so called _normal matrix_ can be quite challenging.

If a 3D model is transformed using an augmented matrix $$\boldsymbol{A}$$,
the [normals](https://en.wikipedia.org/wiki/Normal_(geometry)) should be transformed using a normal matrix $$\boldsymbol{N}$$:

$$\boldsymbol{N} = \big(\boldsymbol{A}^{-1}\big)^\mathrm{T} = \big(\boldsymbol{A}^\mathrm{T}\big)^{-1}$$

This calculation could be done in a vertex shader:

```glsl
mat4 normalMatrix = transpose(inverse(modelViewMatrix));
```

However, this would mean that the GPU should perform the same operation for each vertex.
It is better to calculate normal matrix only once per each frame with the CPU instead.

Unfortunately, a typical implementation of
[matrix inversion](http://grepcode.com/file/repository.grepcode.com/java/ext/com.google.android/android/4.0.1_r1/android/opengl/Matrix.java#Matrix.invertM%28float%5B%5D%2Cint%2Cfloat%5B%5D%2Cint%29)
is long and hard to understand.

## Functional square matrix

A nice and clear algorithm for matrix inversion is recursive.
Since multiple matrices will be created in the course of the calculation, it is better to avoid copying matrix entries every time.
So I have decided to use a functional approach to the problem.

Let's create a class representing a square matrix of a specific size, the elements of which are defined by a function `(Int, Int) -> Float`:

```kotlin
class SquareMatrix(val size:Int, private val elements: (Int, Int) -> Float) {
	operator fun get(row: Int, col: Int): Float {
		require(row in 0..size - 1) { "Row ${row} out of bounds: 0..${size - 1}" }
		require(col in 0..size - 1) { "Column ${col} out of bounds: 0..${size - 1}" }
		return elements(row, col)
	}
}
```

The `elements` function returns a matrix element at the specific row and column, e.g. identity matrix of a requested size can be defined like this:

```kotlin
fun identity(size: Int) = SquareMatrix(size) { row, col ->
	if (row == col) 1f else 0f
}
```

Now, let's try to define some operations on the matrix.

### Matrix transposition

The [transpose](https://en.wikipedia.org/wiki/Transpose) of a matrix can be created by simply switching indices of the rows and the columns:

$$\left[\boldsymbol{A}^\mathrm{T}\right]_{i,j} = \left[\boldsymbol{A}\right]_{j,i}$$

So the method can be defined as follows:

```kotlin
fun transpose(): SquareMatrix = SquareMatrix(size) { row, col -> this[col, row] }
```

Note that the transpose does not copy entries of the original matrix, but rather refers to them.

### Determinant

Before starting any further calculations, we will need the [determinant](https://en.wikipedia.org/wiki/Determinant)
of the matrix.

Let's start with the simplest case of a (rather degenerated) 1×1 matrix.
It seems impossible to infer from the definition (determinant is defined for 2×2 and larger matrices),
but let's look at some properties of the determinant.
For _n_×_n_ matrices:

$$\mathrm{det}(\boldsymbol{I}_n) = 1$$

$$\mathrm{det}(c\boldsymbol{A}) = c^n \mathrm{det}(\boldsymbol{A})$$

On the other hand, for any 1×1 matrix $$\boldsymbol{A}$$:

$$\boldsymbol{A} = a_{1,1} \boldsymbol{I}_1$$

Therefore:

$$
\mathrm{det}(\boldsymbol{A}) =
\mathrm{det}(a_{1,1} \boldsymbol{I}_1) =
\left(a_{1,1}\right)^1 \mathrm{det}(\boldsymbol{I}_1) =
a_{1,1} \cdot 1 =
a_{1,1}$$

For a _n_×_n_ matrix, determinant can be defined as a sum of all elements in the first row
of the matrix multiplied by respective cofactors:

$$\mathrm{det}(\boldsymbol{A}) = \sum_{j=1}^n a_{1,j} C_{1,j}$$

So the determinant can be defined like this:

```kotlin
val det: Float by lazy {
	if (size == 1) this[0, 0]
	else (0..size - 1).map { item -> this[0, item] * comatrix[0, item] }.sum()
}
```

Lazily initialized value is used instead of a function,
to prevent the same determinant from being calculated multiple times.

### Cofactors and comatrix

A comatrix is just a matrix of _cofactors_:

```kotlin
private val comatrix: SquareMatrix by lazy {
	SquareMatrix(size) { row, col -> cofactor(row, col) }
}
```

A cofactor is a _first minor_ of the matrix multiplied by $$(-1)^{i+j}$$,
where $$i$$ and $$j$$ are indices of matrix row and column:

$$C_{i,j} = (-1)^{i+j} M_{i,j}$$

```kotlin
private fun cofactor(row: Int, col: Int): Float =
		minor(row, col) * if ((row + col) % 2 == 0) 1f else -1f
```

### First minor

A first minor $$M_{i,j}$$ is a determinant of a submatrix created by removing
_i_-th row and _j_-th column from the original matrix.

```kotlin
private fun minor(row: Int, col: Int): Float = sub(row, col).det
```

```kotlin
private fun sub(delRow: Int, delCol: Int) = SquareMatrix(size - 1) { row, col ->
	this[if (row < delRow) row else row + 1, if (col < delCol) col else col + 1]
}
```

Obviously, recalculation of indices of the row and the column could be extracted into a separate method.
However, to avoid excessive complication of the code, I decided to leave it the way it is.

As you may notice, the algorithm for calculation of determinant used in `SquareMatrix` is recursive.
But since in 3D graphics only 4×4 matrices are used, nested method calls will not cause stack overflow.

### Adjugate matrix

Having implemented the determinant, we can now calculate the [adjugate matrix](https://en.wikipedia.org/wiki/Adjugate_matrix),
which is simply a transpose of the comatrix:

$$\mathrm{adj}(\boldsymbol{A}) = \boldsymbol{C}^\mathrm{T}$$

```kotlin
val adj: SquareMatrix by lazy { comatrix.transpose() }
```

### Matrix inversion

And finally, we can put together matrix inversion:

$$\boldsymbol{A}^{-1} = \dfrac{1}{\mathrm{det}(\boldsymbol{A})} \mathrm{adj}(\boldsymbol{A})$$

```kotlin
fun inverse(): SquareMatrix = SquareMatrix(size) { row, col -> adj[row, col] / det }
```

---

Full implementation of `SquareMatrix` can be downloaded at
[GitHub Gist](https://gist.github.com/sczerwinski/3d98549ebb8c48f7b4b38e898e30fb30).

---