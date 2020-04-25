---
title: it.czerwinski.android.graphics - Android Graphics Utilities
---

[Android Graphics Utilities](../index.html) / [it.czerwinski.android.graphics](./index.html)

## Package it.czerwinski.android.graphics

Graphics Utilities for Android.

### Types

| [AdvancedPath](-advanced-path/index.html) | An extension of the `Path` class, providing means of building advanced shapes.`open class AdvancedPath : `[`Path`](https://developer.android.com/reference/android/graphics/Path.html) |

### Extensions for External Classes

| [android.graphics.Canvas](android.graphics.-canvas/index.html) |  |
| [android.graphics.Rect](android.graphics.-rect/index.html) |  |
| [android.graphics.RectF](android.graphics.-rect-f/index.html) |  |
| [kotlin.Float](kotlin.-float/index.html) |  |
| [kotlin.Int](kotlin.-int/index.html) |  |

### Properties

| [DOUBLE_PI](-d-o-u-b-l-e_-p-i.html) | A `Float` value equal to double pi constant.`const val DOUBLE_PI: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) |
| [FULL_ANGLE](-f-u-l-l_-a-n-g-l-e.html) | A `Float` value equal to full angle in measured in degrees.`const val FULL_ANGLE: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) |
| [PI](-p-i.html) | A `Float` value equal to pi constant.`const val PI: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) |
| [RIGHT_ANGLE](-r-i-g-h-t_-a-n-g-l-e.html) | A `Float` value equal to right angle in measured in degrees.`const val RIGHT_ANGLE: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) |
| [STRAIGHT_ANGLE](-s-t-r-a-i-g-h-t_-a-n-g-l-e.html) | A `Float` value equal to straight angle in measured in degrees.`const val STRAIGHT_ANGLE: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) |

### Functions

| [hsvColor](hsv-color.html) | Creates a color with the given hue, saturation and value.`fun hsvColor(hue: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, saturation: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, value: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`): `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [mixColors](mix-colors.html) | Returns an `Int` value representing a color being a result of mixing `color1` and `color2` with the specified ratio.`fun mixColors(color1: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, color2: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, ratio: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = .5f): `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [set](set.html) | Clear any lines and curves from this path, making it empty, and applies a new path defined in `init` function.`fun <T : `[`Path`](https://developer.android.com/reference/android/graphics/Path.html)`> T.set(close: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false, init: T.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) |

