---
title: Either.filterNotToOption - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Either](index.html) / [filterNotToOption](./filter-not-to-option.html)

# filterNotToOption

`inline fun filterNotToOption(predicate: (`[`R`](index.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Option`](../-option/index.html)`<`[`Either`](index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>>`

Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) if the [predicate](filter-not-to-option.html#it.czerwinski.kotlin.util.Either$filterNotToOption(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, kotlin.Boolean)))/predicate) is not satisfied for the value.
Otherwise returns [None](../-none/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
[Some](../-some/index.html) containing the same [Right](../-right/index.html) if the [predicate](filter-not-to-option.html#it.czerwinski.kotlin.util.Either$filterNotToOption(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, kotlin.Boolean)))/predicate) is not satisfied for the value.
Otherwise returns [None](../-none/index.html).

**Since**
1.3

