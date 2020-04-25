---
title: set - Android Graphics Utilities
---

[Android Graphics Utilities](../index.html) / [it.czerwinski.android.graphics](index.html) / [set](./set.html)

# set

`inline fun <T : `[`Path`](https://developer.android.com/reference/android/graphics/Path.html)`> T.set(close: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false, init: T.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Clear any lines and curves from this path, making it empty,
and applies a new path defined in `init` function.

**Example:**

``` kotlin
path.set(close = true) {
    moveTo(0f, 0f)
    lineTo(10f, 0f)
    lineTo(10f, 10f)
    lineTo(0f, 10f)
}
```

### Parameters

`close` - Set to `true` if the path should be closed upon completion.

`init` - Function initializing a new path.

**Receiver**
The path.

