---
title: Failure.filterNot - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Failure](index.html) / [filterNot](./filter-not.html)

# filterNot

`fun filterNot(predicate: (`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](../-try/index.html)`<`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`>`

Overrides [Try.filterNot](../-try/filter-not.html)

Returns the same [Success](../-success/index.html) if the [predicate](../-try/filter-not.html#it.czerwinski.kotlin.util.Try$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [Failure](index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The same [Success](../-success/index.html) if the [predicate](../-try/filter-not.html#it.czerwinski.kotlin.util.Try$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [Failure](index.html).

