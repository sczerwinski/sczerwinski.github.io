---
title: withRadialTranslation - Android Graphics Utilities
---

[Android Graphics Utilities](../../index.html) / [it.czerwinski.android.graphics](../index.html) / [android.graphics.Canvas](index.html) / [withRadialTranslation](./with-radial-translation.html)

# withRadialTranslation

`inline fun Canvas.withRadialTranslation(distance: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, angle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, block: Canvas.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Wraps the specified [block](with-radial-translation.html#it.czerwinski.android.graphics$withRadialTranslation(android.graphics.Canvas, kotlin.Float, kotlin.Float, kotlin.Function1((android.graphics.Canvas, kotlin.Unit)))/block) in a call to `Canvas.withTranslation()`
with the specified radial coordinates.

### Parameters

`distance` - Translation distance.

`angle` - Translation angle in degrees.

`block` - A block of instructions to be executed with the specified translation.