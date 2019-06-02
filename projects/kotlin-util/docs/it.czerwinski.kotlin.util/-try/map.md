---
title: Try.map - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [map](./map.html)

# map

`abstract fun <R> map(transform: (`[`T`](index.html#T)`) -> `[`R`](map.html#R)`): `[`Try`](index.html)`<`[`R`](map.html#R)`>`

Maps value of a [Success](../-success/index.html) using [transform](map.html#it.czerwinski.kotlin.util.Try$map(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.map.R)))/transform) or returns the same [Try](index.html) if this is a [Failure](../-failure/index.html).

### Parameters

`transform` - Function transforming value of a [Success](../-success/index.html).

**Return**
[Try](index.html) with a value mapped using [transform](map.html#it.czerwinski.kotlin.util.Try$map(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.map.R)))/transform) or this object if this is a [Failure](../-failure/index.html).

