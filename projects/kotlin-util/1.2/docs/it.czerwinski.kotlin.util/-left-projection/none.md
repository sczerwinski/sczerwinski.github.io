---
title: LeftProjection.none - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [LeftProjection](index.html) / [none](./none.html)

# none

`inline fun none(predicate: (`[`L`](index.html#L)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns `false` if the [predicate](none.html#it.czerwinski.kotlin.util.LeftProjection$none(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) is met by the value if this is [Left](../-left/index.html) or `true` otherwise.

### Parameters

`predicate` - Predicate function.

**Return**
`false` if the [predicate](none.html#it.czerwinski.kotlin.util.LeftProjection$none(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) is met by the value if this is [Left](../-left/index.html) or `true` otherwise.

**Since**
1.1

