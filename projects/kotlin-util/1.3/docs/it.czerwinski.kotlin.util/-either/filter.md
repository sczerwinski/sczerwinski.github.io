---
title: Either.filter - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Either](index.html) / [filter](./filter.html)

# filter

`inline fun filter(predicate: (`[`R`](index.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Either`](index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>?`

Returns the same [Right](../-right/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.Either$filter(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns `null`.

### Parameters

`predicate` - Predicate function.

**Return**
The same [Right](../-right/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.Either$filter(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns `null`.

**Since**
1.3

