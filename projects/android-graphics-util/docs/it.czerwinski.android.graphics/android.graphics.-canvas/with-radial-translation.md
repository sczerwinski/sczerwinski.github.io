---
title: withRadialTranslation - Android Graphics Utilities
---

[Android Graphics Utilities](../../index.html) / [it.czerwinski.android.graphics](../index.html) / [android.graphics.Canvas](index.html) / [withRadialTranslation](./with-radial-translation.html)

# withRadialTranslation

`inline fun `[`Canvas`](https://developer.android.com/reference/android/graphics/Canvas.html)`.withRadialTranslation(distance: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, angle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, block: `[`Canvas`](https://developer.android.com/reference/android/graphics/Canvas.html)`.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Wraps the specified `block` in a call to `Canvas.withTranslation()`
with the specified radial coordinates.

**Example:**

``` kotlin
canvas.withRadialTranslation(
    distance = 10.0f,
    angle = 30.0f
) {
    drawRect(rect, paint)
}
```

### Parameters

`distance` - Translation distance.

`angle` - Translation angle in degrees.

`block` - A block of instructions to be executed with the specified translation.

**Receiver**
The canvas.

