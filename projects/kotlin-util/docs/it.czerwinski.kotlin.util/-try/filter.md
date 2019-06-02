---
title: Try.filter - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [filter](./filter.html)

# filter

`abstract fun filter(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](index.html)`<`[`T`](index.html#T)`>`

Returns the same [Success](../-success/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.Try$filter(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The same [Success](../-success/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.Try$filter(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).

