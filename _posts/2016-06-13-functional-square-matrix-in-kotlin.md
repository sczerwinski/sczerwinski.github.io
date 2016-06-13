---
title: Functional Square Matrix in Kotlin
mobileTitle: Functional Square Matrix…
layout: post
abstract: How to create a simple functional square matrix in Kotlin programming language
keywords: kotlin,functional,programming,matrix,affine,transformations
---

Working with OpenGL and 3D graphics requires [affine transformations](https://en.wikipedia.org/wiki/Affine_transformation) and transformation matrix.

So called _normal matrix_ used to transform normals:
$$\boldsymbol{N} = \big(\boldsymbol{A}^{-1}\big)^\mathrm{T} = \big(\boldsymbol{A}^\mathrm{T}\big)^{-1}$$

Could be done in vertex shader, but it would use too much GPU. It would be calculated for each vertex.

```glsl
mat4 normalMatrix = transpose(inverse(modelViewMatrix));
```

It is enough to calculate normal matrix for each frame only once.

There is an ugly code on
[GrepCode](http://grepcode.com/file/repository.grepcode.com/java/ext/com.google.android/android/4.0.1_r1/android/opengl/Matrix.java#Matrix.invertM%28float%5B%5D%2Cint%2Cfloat%5B%5D%2Cint%29).

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
