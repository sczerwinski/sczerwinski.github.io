---
title: LeftProjection.filter - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [LeftProjection](index.html) / [filter](./filter.html)

# filter

`inline fun filter(predicate: (`[`L`](index.html#L)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Either`](../-either/index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>?`

Returns the same [Left](../-left/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.LeftProjection$filter(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns `null`.

### Parameters

`predicate` - Predicate function.

**Return**
The same [Left](../-left/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.LeftProjection$filter(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns `null`.

