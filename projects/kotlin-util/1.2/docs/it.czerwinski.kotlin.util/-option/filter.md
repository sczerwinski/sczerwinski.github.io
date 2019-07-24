---
title: Option.filter - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [filter](./filter.html)

# filter

`inline fun filter(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Option`](index.html)`<`[`T`](index.html#T)`>`

Returns the same [Some](../-some/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.Option$filter(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [None](../-none/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The same [Some](../-some/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.Option$filter(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [None](../-none/index.html).

