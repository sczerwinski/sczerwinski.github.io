---
title: Either.all - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Either](index.html) / [all](./all.html)

# all

`inline fun all(predicate: (`[`R`](index.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns the result of applying the [predicate](all.html#it.czerwinski.kotlin.util.Either$all(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, kotlin.Boolean)))/predicate) to the value if this is [Right](../-right/index.html)
or `true` if this is [Left](../-left/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The result of applying the [predicate](all.html#it.czerwinski.kotlin.util.Either$all(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, kotlin.Boolean)))/predicate) to the value if this is [Right](../-right/index.html)
or `true` if this is [Left](../-left/index.html).

**Since**
1.3

