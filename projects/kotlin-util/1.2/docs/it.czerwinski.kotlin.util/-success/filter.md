---
title: Success.filter - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](index.html) / [filter](./filter.html)

# filter

`fun filter(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](../-try/index.html)`<`[`T`](index.html#T)`>`

Overrides [Try.filter](../-try/filter.html)

Returns the same [Success](index.html) if the [predicate](../-try/filter.html#it.czerwinski.kotlin.util.Try$filter(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The same [Success](index.html) if the [predicate](../-try/filter.html#it.czerwinski.kotlin.util.Try$filter(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).

