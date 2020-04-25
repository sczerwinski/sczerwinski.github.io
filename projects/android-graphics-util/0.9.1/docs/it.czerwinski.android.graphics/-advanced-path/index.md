---
title: AdvancedPath - Android Graphics Utilities
---

[Android Graphics Utilities](../../index.html) / [it.czerwinski.android.graphics](../index.html) / [AdvancedPath](./index.html)

# AdvancedPath

`open class AdvancedPath : Path`

An extension of the `Path` class, providing means of building advanced shapes.

### Constructors

| [&lt;init&gt;](-init-.html) | `AdvancedPath()`<br>An extension of the `Path` class, providing means of building advanced shapes. |

### Functions

| [addCircleSector](add-circle-sector.html) | `open fun addCircleSector(cx: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f, cy: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f, radius: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, startAngle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, sweepAngle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, inset: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Adds a closed circle sector contour to the path. |
| [addRingSector](add-ring-sector.html) | `open fun addRingSector(cx: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f, cy: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f, radius: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, startAngle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, sweepAngle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, thickness: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, inset: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Adds a closed ring sector (annulus sector) contour to the path. |
| [arcTo](arc-to.html) | `open fun arcTo(cx: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f, cy: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f, radius: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, startAngle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, sweepAngle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, forceMoveTo: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Appends the specified arc of a circle to the path as a new contour. |

### Extension Functions

| [set](../set.html) | `fun <T : Path> `[`T`](../set.html#T)`.set(close: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false, init: `[`T`](../set.html#T)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Clear any lines and curves from this path, making it empty, and applies a new path defined in [init](../set.html#it.czerwinski.android.graphics$set(it.czerwinski.android.graphics.set.T, kotlin.Boolean, kotlin.Function1((it.czerwinski.android.graphics.set.T, kotlin.Unit)))/init) function. |

