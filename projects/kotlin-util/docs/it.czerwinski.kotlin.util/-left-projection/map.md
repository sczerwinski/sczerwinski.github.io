---
title: LeftProjection.map - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [LeftProjection](index.html) / [map](./map.html)

# map

`inline fun <T> map(transform: (`[`L`](index.html#L)`) -> `[`T`](map.html#T)`): `[`Either`](../-either/index.html)`<`[`T`](map.html#T)`, `[`R`](index.html#R)`>`

Maps value of this [Left](../-left/index.html) using [transform](map.html#it.czerwinski.kotlin.util.LeftProjection$map(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, it.czerwinski.kotlin.util.LeftProjection.map.T)))/transform).

### Parameters

`transform` - Function transforming a [Left](../-left/index.html).

**Return**
[Left](../-left/index.html) mapped using [transform](map.html#it.czerwinski.kotlin.util.LeftProjection$map(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, it.czerwinski.kotlin.util.LeftProjection.map.T)))/transform) or this object if this is a [Right](../-right/index.html).

