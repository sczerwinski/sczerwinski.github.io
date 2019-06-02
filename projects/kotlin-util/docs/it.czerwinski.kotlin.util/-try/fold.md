---
title: Try.fold - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [fold](./fold.html)

# fold

`inline fun <R> fold(successTransform: (`[`T`](index.html#T)`) -> `[`R`](fold.html#R)`, failureTransform: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`R`](fold.html#R)`): `[`R`](fold.html#R)

Transforms a [Success](../-success/index.html) using [successTransform](fold.html#it.czerwinski.kotlin.util.Try$fold(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.fold.R)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try.fold.R)))/successTransform) or a [Failure](../-failure/index.html) using [failureTransform](fold.html#it.czerwinski.kotlin.util.Try$fold(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.fold.R)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try.fold.R)))/failureTransform).

### Parameters

`successTransform` - Function transforming value of a [Success](../-success/index.html) to a new [Try](index.html).

`failureTransform` - Function transforming exception from a [Failure](../-failure/index.html) to a new [Try](index.html).

**Return**
Result of applying [successTransform](fold.html#it.czerwinski.kotlin.util.Try$fold(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.fold.R)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try.fold.R)))/successTransform) on [Success](../-success/index.html) or [failureTransform](fold.html#it.czerwinski.kotlin.util.Try$fold(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.fold.R)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try.fold.R)))/failureTransform) on [Failure](../-failure/index.html).

