---
title: Success.filterOrElse - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](index.html) / [filterOrElse](./filter-or-else.html)

# filterOrElse

`fun filterOrElse(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, throwable: (`[`T`](index.html#T)`) -> `[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`): `[`Try`](../-try/index.html)`<`[`T`](index.html#T)`>`

Overrides [Try.filterOrElse](../-try/filter-or-else.html)

Returns the same [Success](index.html) if the [predicate](../-try/filter-or-else.html#it.czerwinski.kotlin.util.Try$filterOrElse(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)), kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Throwable)))/predicate) is satisfied for the value.
Otherwise returns a [Failure](../-failure/index.html) containing the given [throwable](../-try/filter-or-else.html#it.czerwinski.kotlin.util.Try$filterOrElse(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)), kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Throwable)))/throwable).

### Parameters

`predicate` - Predicate function.

`throwable` - Function providing a throwable to be used when the [predicate](../-try/filter-or-else.html#it.czerwinski.kotlin.util.Try$filterOrElse(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)), kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Throwable)))/predicate) is not satisfied.

**Return**
The same [Success](index.html) if the [predicate](../-try/filter-or-else.html#it.czerwinski.kotlin.util.Try$filterOrElse(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)), kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Throwable)))/predicate) is satisfied for the value.
Otherwise returns a [Failure](../-failure/index.html) containing the given [throwable](../-try/filter-or-else.html#it.czerwinski.kotlin.util.Try$filterOrElse(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)), kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Throwable)))/throwable).

**Since**
1.2

