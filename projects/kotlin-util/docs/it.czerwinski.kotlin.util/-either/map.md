---
title: Either.map - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Either](index.html) / [map](./map.html)

# map

`inline fun <T> map(transform: (`[`R`](index.html#R)`) -> `[`T`](map.html#T)`): `[`Either`](index.html)`<`[`L`](index.html#L)`, `[`T`](map.html#T)`>`

Maps value of this [Right](../-right/index.html) using [transform](map.html#it.czerwinski.kotlin.util.Either$map(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.map.T)))/transform).

### Parameters

`transform` - Function transforming a [Right](../-right/index.html).

**Return**
[Right](../-right/index.html) mapped using [transform](map.html#it.czerwinski.kotlin.util.Either$map(kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.map.T)))/transform) or this object if this is a [Left](../-left/index.html).

**Since**
1.3

