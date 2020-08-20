---
title: Try.transform - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [transform](./transform.html)

# transform

`inline fun <R> transform(successTransform: (`[`T`](index.html#T)`) -> `[`Try`](index.html)`<`[`R`](transform.html#R)`>, failureTransform: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`Try`](index.html)`<`[`R`](transform.html#R)`>): `[`Try`](index.html)`<`[`R`](transform.html#R)`>`

Transforms a [Success](../-success/index.html) using [successTransform](transform.html#it.czerwinski.kotlin.util.Try$transform(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))))/successTransform) or a [Failure](../-failure/index.html) using [failureTransform](transform.html#it.czerwinski.kotlin.util.Try$transform(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))))/failureTransform).

### Parameters

`successTransform` - Function transforming value of a [Success](../-success/index.html) to a new [Try](index.html).

`failureTransform` - Function transforming exception from a [Failure](../-failure/index.html) to a new [Try](index.html).

**Return**
New [Try](index.html) being a result of a transformation of a [Success](../-success/index.html) with [successTransform](transform.html#it.czerwinski.kotlin.util.Try$transform(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))))/successTransform)
or a [Failure](../-failure/index.html) with [failureTransform](transform.html#it.czerwinski.kotlin.util.Try$transform(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))))/failureTransform).

