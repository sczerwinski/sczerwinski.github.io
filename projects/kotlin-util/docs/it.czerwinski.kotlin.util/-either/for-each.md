---
title: Either.forEach - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Either](index.html) / [forEach](./for-each.html)

# forEach

`inline fun forEach(action: (`[`R`](index.html#R)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Runs [action](for-each.html#it.czerwinski.kotlin.util.Either$forEach(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, kotlin.Unit)))/action) if this is a [Right](../-right/index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Left](../-left/index.html).

### Parameters

`action` - Action to be run on a [Right](../-right/index.html).

**Since**
1.3

