---
title: set - Android Graphics Utilities
---

[Android Graphics Utilities](../../index.html) / [it.czerwinski.android.graphics](../index.html) / [android.graphics.Path](index.html) / [set](./set.html)

# set

`inline fun Path.set(close: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` = false, init: Path.() -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Clear any lines and curves from this path, making it empty,
and applies a new path defined in [init](set.html#it.czerwinski.android.graphics$set(android.graphics.Path, kotlin.Boolean, kotlin.Function1((android.graphics.Path, kotlin.Unit)))/init) function.

### Parameters

`close` - Set to `true` if the path should be closed upon completion.

`init` - Function initializing a new path.