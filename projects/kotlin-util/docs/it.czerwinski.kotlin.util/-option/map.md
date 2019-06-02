---
title: Option.map - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [map](./map.html)

# map

`inline fun <R> map(transform: (`[`T`](index.html#T)`) -> `[`R`](map.html#R)`): `[`Option`](index.html)`<`[`R`](map.html#R)`>`

Maps value of a [Some](../-some/index.html) using [transform](map.html#it.czerwinski.kotlin.util.Option$map(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.map.R)))/transform) or returns the same [None](../-none/index.html).

### Parameters

`transform` - Function transforming value of a [Some](../-some/index.html).

**Return**
[Some](../-some/index.html) with a value mapped using [transform](map.html#it.czerwinski.kotlin.util.Option$map(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.map.R)))/transform) or this object if this is a [None](../-none/index.html).

