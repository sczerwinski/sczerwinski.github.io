---
title: AdvancedPath.arcTo - Android Graphics Utilities
---

[Android Graphics Utilities](../../index.html) / [it.czerwinski.android.graphics](../index.html) / [AdvancedPath](index.html) / [arcTo](./arc-to.html)

# arcTo

`open fun arcTo(cx: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f, cy: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` = 0f, radius: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, startAngle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, sweepAngle: `[`Float`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, forceMoveTo: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Appends the specified arc of a circle to the path as a new contour.

If the start of the path is different from the path's current last point,
an automatic `lineTo()` is added to connect the current contour to the
start of the arc.

If the path is empty, a `moveTo()` is added with the first point of the arc.

### Parameters

`cx` - The x-coordinate of the center of the circle.

`cy` - The x-coordinate of the center of the circle.

`radius` - The radius of the circle.

`startAngle` - Starting angle of the arc measured in degrees.

`sweepAngle` - Sweep angle of the arc measured in degrees.

`forceMoveTo` - Set to `true`, if a `moveTo()` should always be added before the arc,
    instead of a `lineTo()`.