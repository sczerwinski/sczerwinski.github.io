---
title: it.czerwinski.android.graphics - Android Graphics Utilities
---

[Android Graphics Utilities](../index.html) / [it.czerwinski.android.graphics](./index.html)

## Package it.czerwinski.android.graphics

Graphics Utilities for Android.

### Types

| [AdvancedPath](-advanced-path/index.html) | `open class AdvancedPath : Path`<br>An extension of the `Path` class, providing means of building advanced shapes. |
| [BuildConfig](-build-config/index.html) | `class BuildConfig`<br>`class BuildConfig` |

### Extensions for External Classes

| [android.graphics.Canvas](android.graphics.-canvas/index.html) |  |
| [android.graphics.Rect](android.graphics.-rect/index.html) |  |
| [android.graphics.RectF](android.graphics.-rect-f/index.html) |  |
| [kotlin.Float](kotlin.-float/index.html) |  |

### Properties

| [DOUBLE_PI](-d-o-u-b-l-e_-p-i.html) | `const val DOUBLE_PI: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)<br>A `Float` value equal to double pi constant. |
| [FULL_ANGLE](-f-u-l-l_-a-n-g-l-e.html) | `const val FULL_ANGLE: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)<br>A `Float` value equal to full angle in measured in degrees. |
| [PI](-p-i.html) | `const val PI: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)<br>A `Float` value equal to pi constant. |
| [RIGHT_ANGLE](-r-i-g-h-t_-a-n-g-l-e.html) | `const val RIGHT_ANGLE: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)<br>A `Float` value equal to right angle in measured in degrees. |
| [STRAIGHT_ANGLE](-s-t-r-a-i-g-h-t_-a-n-g-l-e.html) | `const val STRAIGHT_ANGLE: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)<br>A `Float` value equal to straight angle in measured in degrees. |

### Functions

| [mixColors](mix-colors.html) | `fun mixColors(color1: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, color2: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, ratio: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = .5f): `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>Returns an `Int` value representing a color being a result of mixing [color1](mix-colors.html#it.czerwinski.android.graphics$mixColors(kotlin.Int, kotlin.Int, kotlin.Float)/color1) and [color2](mix-colors.html#it.czerwinski.android.graphics$mixColors(kotlin.Int, kotlin.Int, kotlin.Float)/color2) with the specified [ratio](mix-colors.html#it.czerwinski.android.graphics$mixColors(kotlin.Int, kotlin.Int, kotlin.Float)/ratio). |
| [set](set.html) | `fun <T : Path> `[`T`](set.html#T)`.set(close: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false, init: `[`T`](set.html#T)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Clear any lines and curves from this path, making it empty, and applies a new path defined in [init](set.html#it.czerwinski.android.graphics$set(it.czerwinski.android.graphics.set.T, kotlin.Boolean, kotlin.Function1((it.czerwinski.android.graphics.set.T, kotlin.Unit)))/init) function. |

