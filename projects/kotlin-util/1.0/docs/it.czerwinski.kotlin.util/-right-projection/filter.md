---
title: RightProjection.filter - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [RightProjection](index.html) / [filter](./filter.html)

# filter

`inline fun filter(predicate: (`[`R`](index.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Either`](../-either/index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>?`

Returns the same [Right](../-right/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.RightProjection$filter(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns `null`.

### Parameters

`predicate` - Predicate function.

**Return**
The same [Right](../-right/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.RightProjection$filter(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns `null`.

