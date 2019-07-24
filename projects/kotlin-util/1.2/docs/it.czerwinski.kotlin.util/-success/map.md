---
title: Success.map - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](index.html) / [map](./map.html)

# map

`fun <R> map(transform: (`[`T`](index.html#T)`) -> `[`R`](map.html#R)`): `[`Try`](../-try/index.html)`<`[`R`](map.html#R)`>`

Overrides [Try.map](../-try/map.html)

Maps value of a [Success](index.html) using [transform](../-try/map.html#it.czerwinski.kotlin.util.Try$map(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.map.R)))/transform) or returns the same [Try](../-try/index.html) if this is a [Failure](../-failure/index.html).

### Parameters

`transform` - Function transforming value of a [Success](index.html).

**Return**
[Try](../-try/index.html) with a value mapped using [transform](../-try/map.html#it.czerwinski.kotlin.util.Try$map(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.map.R)))/transform) or this object if this is a [Failure](../-failure/index.html).

