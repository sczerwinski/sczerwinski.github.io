---
title: Success.flatMap - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](index.html) / [flatMap](./flat-map.html)

# flatMap

`fun <R> flatMap(transform: (`[`T`](index.html#T)`) -> `[`Try`](../-try/index.html)`<`[`R`](flat-map.html#R)`>): `[`Try`](../-try/index.html)`<`[`R`](flat-map.html#R)`>`

Overrides [Try.flatMap](../-try/flat-map.html)

Maps value of a [Success](index.html) to a new [Try](../-try/index.html) using [transform](../-try/flat-map.html#it.czerwinski.kotlin.util.Try$flatMap(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.flatMap.R)))))/transform) or returns the same [Try](../-try/index.html) if this is a [Failure](../-failure/index.html).

### Parameters

`transform` - Function transforming value of a [Success](index.html) to a [Try](../-try/index.html).

**Return**
[Try](../-try/index.html) returned by [transform](../-try/flat-map.html#it.czerwinski.kotlin.util.Try$flatMap(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.flatMap.R)))))/transform) or this object if this is a [Failure](../-failure/index.html).

