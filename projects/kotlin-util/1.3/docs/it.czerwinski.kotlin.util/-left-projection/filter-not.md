---
title: LeftProjection.filterNot - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [LeftProjection](index.html) / [filterNot](./filter-not.html)

# filterNot

`inline fun filterNot(predicate: (`[`L`](index.html#L)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Either`](../-either/index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>?`

Returns the same [Left](../-left/index.html) if the [predicate](filter-not.html#it.czerwinski.kotlin.util.LeftProjection$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns `null`.

### Parameters

`predicate` - Predicate function.

**Return**
The same [Left](../-left/index.html) if the [predicate](filter-not.html#it.czerwinski.kotlin.util.LeftProjection$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns `null`.

