---
title: Failure.map - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Failure](index.html) / [map](./map.html)

# map

`fun <R> map(transform: (`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`) -> `[`R`](map.html#R)`): `[`Try`](../-try/index.html)`<`[`R`](map.html#R)`>`

Overrides [Try.map](../-try/map.html)

Maps value of a [Success](../-success/index.html) using [transform](../-try/map.html#it.czerwinski.kotlin.util.Try$map(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.map.R)))/transform) or returns the same [Try](../-try/index.html) if this is a [Failure](index.html).

### Parameters

`transform` - Function transforming value of a [Success](../-success/index.html).

**Return**
[Try](../-try/index.html) with a value mapped using [transform](../-try/map.html#it.czerwinski.kotlin.util.Try$map(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.map.R)))/transform) or this object if this is a [Failure](index.html).

