---
title: RightProjection.map - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [RightProjection](index.html) / [map](./map.html)

# map

`inline fun <T> map(transform: (`[`R`](index.html#R)`) -> `[`T`](map.html#T)`): `[`Either`](../-either/index.html)`<`[`L`](index.html#L)`, `[`T`](map.html#T)`>`

Maps value of this [Right](../-right/index.html) using [transform](map.html#it.czerwinski.kotlin.util.RightProjection$map(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, it.czerwinski.kotlin.util.RightProjection.map.T)))/transform).

### Parameters

`transform` - Function transforming a [Right](../-right/index.html).

**Return**
[Right](../-right/index.html) mapped using [transform](map.html#it.czerwinski.kotlin.util.RightProjection$map(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, it.czerwinski.kotlin.util.RightProjection.map.T)))/transform) or this object if this is a [Left](../-left/index.html).

