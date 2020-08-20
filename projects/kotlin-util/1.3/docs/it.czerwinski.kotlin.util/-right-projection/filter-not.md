---
title: RightProjection.filterNot - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [RightProjection](index.html) / [filterNot](./filter-not.html)

# filterNot

`inline fun filterNot(predicate: (`[`R`](index.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Either`](../-either/index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>?`

Returns the same [Right](../-right/index.html) if the [predicate](filter-not.html#it.czerwinski.kotlin.util.RightProjection$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns `null`.

### Parameters

`predicate` - Predicate function.

**Return**
The same [Right](../-right/index.html) if the [predicate](filter-not.html#it.czerwinski.kotlin.util.RightProjection$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns `null`.

