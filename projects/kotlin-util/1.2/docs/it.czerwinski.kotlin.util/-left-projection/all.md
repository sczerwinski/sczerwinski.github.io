---
title: LeftProjection.all - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [LeftProjection](index.html) / [all](./all.html)

# all

`inline fun all(predicate: (`[`L`](index.html#L)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns the result of applying the [predicate](all.html#it.czerwinski.kotlin.util.LeftProjection$all(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) to the value if this is [Left](../-left/index.html)
or `true` if this is [Right](../-right/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The result of applying the [predicate](all.html#it.czerwinski.kotlin.util.LeftProjection$all(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) to the value if this is [Left](../-left/index.html)
or `true` if this is [Right](../-right/index.html).

