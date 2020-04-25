---
title: mixColors - Android Graphics Utilities
---

[Android Graphics Utilities](../index.html) / [it.czerwinski.android.graphics](index.html) / [mixColors](./mix-colors.html)

# mixColors

`fun mixColors(color1: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, color2: `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, ratio: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = .5f): `[`Int`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)

Returns an `Int` value representing a color being a result of mixing `color1` and `color2`
with the specified ratio.

### Parameters

`color1` - `Int` value representing first color.

`color2` - `Int` value representing second color.

`ratio` - Colors mixing ratio.
    If this value is equal to 0.0, the result will be equal to `color1`.
    If this value is equal to 1.0, the result will be equal to `color2`.

**Return**
`Int` value representing mixed color.

