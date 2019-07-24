---
title: RightProjection.filterNotToOption - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [RightProjection](index.html) / [filterNotToOption](./filter-not-to-option.html)

# filterNotToOption

`inline fun filterNotToOption(predicate: (`[`R`](index.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Option`](../-option/index.html)`<`[`Either`](../-either/index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>>`

Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) if the [predicate](filter-not-to-option.html#it.czerwinski.kotlin.util.RightProjection$filterNotToOption(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) is not satisfied for the value.
Otherwise returns [None](../-none/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
[Some](../-some/index.html) containing the same [Right](../-right/index.html) if the [predicate](filter-not-to-option.html#it.czerwinski.kotlin.util.RightProjection$filterNotToOption(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) is not satisfied for the value.
Otherwise returns [None](../-none/index.html).

