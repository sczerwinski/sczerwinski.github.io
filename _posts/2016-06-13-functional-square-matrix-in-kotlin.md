---
disqusid: functional-square-matrix-in-kotlin
title: Functional Square Matrix in Kotlin
mobileTitle: Functional Square Matrix…
layout: post
abstract: How to create a simple functional square matrix in Kotlin programming language
keywords: kotlin,functional,programming,matrix,affine,transformations,3d,opengl
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
[normals](https://en.wikipedia.org/wiki/Normal_(geometry)) should be transformed using a normal matrix $$\boldsymbol{N}$$:

$$\boldsymbol{N} = \big(\boldsymbol{A}^{-1}\big)^\mathrm{T} = \big(\boldsymbol{A}^\mathrm{T}\big)^{-1}$$

This calculation could be done in a vertex shader:

```glsl
mat4 normalMatrix = transpose(inverse(modelViewMatrix));
```

However, this would mean that the GPU should perform the same operation for each vertex.
It is better to calculate normal matrix once per each frame using CPU instead.


**Draft:**

Unfortunately, [typical algorithm](http://grepcode.com/file/repository.grepcode.com/java/ext/com.google.android/android/4.0.1_r1/android/opengl/Matrix.java#Matrix.invertM%28float%5B%5D%2Cint%2Cfloat%5B%5D%2Cint%29)
is ugly.

## Functional square matrix

Let's create a class which represents a square matrix of a specific `size` with `elements`:

```kotlin
class SquareMatrix(val size:Int, private val elements: (Int, Int) -> Float) {
	operator fun get(row: Int, col: Int): Float {
		require(row in 0..size - 1) { "Row ${row} out of bounds: 0..${size - 1}" }
		require(col in 0..size - 1) { "Column ${col} out of bounds: 0..${size - 1}" }
		return elements(row, col)
	}
}
```

Example: identity matrix

```kotlin
fun identity(size: Int) = SquareMatrix(size) { row, col ->
	if (row == col) 1f else 0f
}
```

## Transpose

https://en.wikipedia.org/wiki/Transpose

This one's easy:

```kotlin
fun transpose(): SquareMatrix = SquareMatrix(size) { row, col -> this[col, row] }
```

## Inverse

Inverse:
$$\boldsymbol{A}^{-1} = \dfrac{1}{\mathrm{det}(\boldsymbol{A})} \mathrm{adj}(\boldsymbol{A})$$

### Determinant

First, let's calculate the determinant.

For a 1×1 matrix:

$$\mathrm{det}(\boldsymbol{A}) = \boldsymbol{A}_{1,1}$$

For bigger matrix:

$$\mathrm{det}(\boldsymbol{A}) = \sum_{j=1}^n a_{i,j} C_{i,j}$$

```kotlin
val det: Float by lazy {
	if (size == 1) this[0, 0]
	else (0..size - 1).map { item -> this[0, item] * comatrix[0, item] }.sum()
}
```

### Cofactors and comatrix

Cofactor is:
$$C_{i,j} = (-1)^{i+j} M_{i,j}$$

```kotlin
private val comatrix: SquareMatrix by lazy {
	SquareMatrix(size) { row, col -> cofactor(row, col) }
}
```

```kotlin
private fun cofactor(row: Int, col: Int): Float =
		minor(row, col) * if ((row + col) % 2 == 0) 1f else -1f
```

### Minor

Minor $$M_{i,j}$$ is a determinant of a submatrix created by removing _i_-th row and _j_-th column from the original matrix.

```kotlin
private fun minor(row: Int, col: Int): Float = sub(row, col).det
```

```kotlin
private fun sub(delRow: Int, delCol: Int) = SquareMatrix(size - 1) { row, col ->
	this[if (row < delRow) row else row + 1, if (col < delCol) col else col + 1]
}
```

### Adjugate matrix

Finally, adjugate matrix:
$$\mathrm{adj}(\boldsymbol{A}) = \boldsymbol{C}^\mathrm{T}$$

```kotlin
val adj: SquareMatrix by lazy { comatrix.transpose() }
```

### Putting everything together

```kotlin
fun inverse(): SquareMatrix = SquareMatrix(size) { row, col -> adj[row, col] / det }
```

Full implementation of `SquareMatrix` can be downloaded from [GitHub Gist](https://gist.github.com/sczerwinski/3d98549ebb8c48f7b4b38e898e30fb30).
