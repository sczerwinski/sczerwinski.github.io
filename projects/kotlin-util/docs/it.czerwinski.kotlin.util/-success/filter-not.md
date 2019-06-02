---
title: Success.filterNot - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](index.html) / [filterNot](./filter-not.html)

# filterNot

`fun filterNot(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](../-try/index.html)`<`[`T`](index.html#T)`>`

Overrides [Try.filterNot](../-try/filter-not.html)

Returns the same [Success](index.html) if the [predicate](../-try/filter-not.html#it.czerwinski.kotlin.util.Try$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The same [Success](index.html) if the [predicate](../-try/filter-not.html#it.czerwinski.kotlin.util.Try$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).

