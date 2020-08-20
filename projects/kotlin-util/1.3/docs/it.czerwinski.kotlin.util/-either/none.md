---
title: Either.none - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Either](index.html) / [none](./none.html)

# none

`inline fun none(predicate: (`[`R`](index.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns `false` if the [predicate](none.html#it.czerwinski.kotlin.util.Either$none(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, kotlin.Boolean)))/predicate) is met by the value if this is [Right](../-right/index.html) or `true` otherwise.

### Parameters

`predicate` - Predicate function.

**Return**
`false` if the [predicate](none.html#it.czerwinski.kotlin.util.Either$none(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, kotlin.Boolean)))/predicate) is met by the value if this is [Right](../-right/index.html) or `true` otherwise.

**Since**
1.3

