---
title: Try.filterNot - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [filterNot](./filter-not.html)

# filterNot

`abstract fun filterNot(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](index.html)`<`[`T`](index.html#T)`>`

Returns the same [Success](../-success/index.html) if the [predicate](filter-not.html#it.czerwinski.kotlin.util.Try$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The same [Success](../-success/index.html) if the [predicate](filter-not.html#it.czerwinski.kotlin.util.Try$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).

