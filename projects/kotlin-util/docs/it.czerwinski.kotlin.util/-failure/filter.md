---
title: Failure.filter - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Failure](index.html) / [filter](./filter.html)

# filter

`fun filter(predicate: (`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](../-try/index.html)`<`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`>`

Overrides [Try.filter](../-try/filter.html)

Returns the same [Success](../-success/index.html) if the [predicate](../-try/filter.html#it.czerwinski.kotlin.util.Try$filter(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [Failure](index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The same [Success](../-success/index.html) if the [predicate](../-try/filter.html#it.czerwinski.kotlin.util.Try$filter(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [Failure](index.html).

