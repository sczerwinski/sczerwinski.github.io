---
title: LeftProjection.filterToOption - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [LeftProjection](index.html) / [filterToOption](./filter-to-option.html)

# filterToOption

`inline fun filterToOption(predicate: (`[`L`](index.html#L)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Option`](../-option/index.html)`<`[`Either`](../-either/index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>>`

Returns [Some](../-some/index.html) containing the same [Left](../-left/index.html) if the [predicate](filter-to-option.html#it.czerwinski.kotlin.util.LeftProjection$filterToOption(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) is satisfied for the value.
Otherwise returns [None](../-none/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
[Some](../-some/index.html) containing the same [Left](../-left/index.html) if the [predicate](filter-to-option.html#it.czerwinski.kotlin.util.LeftProjection$filterToOption(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) is satisfied for the value.
Otherwise returns [None](../-none/index.html).

