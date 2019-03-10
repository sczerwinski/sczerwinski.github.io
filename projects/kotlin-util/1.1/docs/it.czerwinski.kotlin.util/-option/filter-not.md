---
title: Option.filterNot - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [filterNot](./filter-not.html)

# filterNot

`inline fun filterNot(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Option`](index.html)`<`[`T`](index.html#T)`>`

Returns the same [Some](../-some/index.html) if the [predicate](filter-not.html#it.czerwinski.kotlin.util.Option$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [None](../-none/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The same [Some](../-some/index.html) if the [predicate](filter-not.html#it.czerwinski.kotlin.util.Option$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [None](../-none/index.html).

