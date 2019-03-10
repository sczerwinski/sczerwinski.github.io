---
title: Try.flatMap - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [flatMap](./flat-map.html)

# flatMap

`abstract fun <R> flatMap(transform: (`[`T`](index.html#T)`) -> `[`Try`](index.html)`<`[`R`](flat-map.html#R)`>): `[`Try`](index.html)`<`[`R`](flat-map.html#R)`>`

Maps value of a [Success](../-success/index.html) to a new [Try](index.html) using [transform](flat-map.html#it.czerwinski.kotlin.util.Try$flatMap(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.flatMap.R)))))/transform) or returns the same [Try](index.html) if this is a [Failure](../-failure/index.html).

### Parameters

`transform` - Function transforming value of a [Success](../-success/index.html) to a [Try](index.html).

**Return**
[Try](index.html) returned by [transform](flat-map.html#it.czerwinski.kotlin.util.Try$flatMap(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.flatMap.R)))))/transform) or this object if this is a [Failure](../-failure/index.html).

