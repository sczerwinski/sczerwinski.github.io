---
title: flatMap - Kotlin utilities
---

[Kotlin utilities](../index.html) / [it.czerwinski.kotlin.util](index.html) / [flatMap](./flat-map.html)

# flatMap

`inline fun <L, R, T> `[`LeftProjection`](-left-projection/index.html)`<`[`L`](flat-map.html#L)`, `[`R`](flat-map.html#R)`>.flatMap(transform: (`[`L`](flat-map.html#L)`) -> `[`Either`](-either/index.html)`<`[`T`](flat-map.html#T)`, `[`R`](flat-map.html#R)`>): `[`Either`](-either/index.html)`<`[`T`](flat-map.html#T)`, `[`R`](flat-map.html#R)`>`

Maps value of this [Left](-left/index.html) to a new [Either](-either/index.html) using [transform](flat-map.html#it.czerwinski.kotlin.util$flatMap(it.czerwinski.kotlin.util.LeftProjection((it.czerwinski.kotlin.util.flatMap.L, it.czerwinski.kotlin.util.flatMap.R)), kotlin.Function1((it.czerwinski.kotlin.util.flatMap.L, it.czerwinski.kotlin.util.Either((it.czerwinski.kotlin.util.flatMap.T, it.czerwinski.kotlin.util.flatMap.R)))))/transform).

### Parameters

`transform` - Function transforming a [Left](-left/index.html) to an [Either](-either/index.html).

**Return**
[Either](-either/index.html) mapped using [transform](flat-map.html#it.czerwinski.kotlin.util$flatMap(it.czerwinski.kotlin.util.LeftProjection((it.czerwinski.kotlin.util.flatMap.L, it.czerwinski.kotlin.util.flatMap.R)), kotlin.Function1((it.czerwinski.kotlin.util.flatMap.L, it.czerwinski.kotlin.util.Either((it.czerwinski.kotlin.util.flatMap.T, it.czerwinski.kotlin.util.flatMap.R)))))/transform) or this object if this is a [Right](-right/index.html).

`inline fun <L, R, T> `[`RightProjection`](-right-projection/index.html)`<`[`L`](flat-map.html#L)`, `[`R`](flat-map.html#R)`>.flatMap(transform: (`[`R`](flat-map.html#R)`) -> `[`Either`](-either/index.html)`<`[`L`](flat-map.html#L)`, `[`T`](flat-map.html#T)`>): `[`Either`](-either/index.html)`<`[`L`](flat-map.html#L)`, `[`T`](flat-map.html#T)`>`

Maps value of this [Right](-right/index.html) to a new [Either](-either/index.html) using [transform](flat-map.html#it.czerwinski.kotlin.util$flatMap(it.czerwinski.kotlin.util.RightProjection((it.czerwinski.kotlin.util.flatMap.L, it.czerwinski.kotlin.util.flatMap.R)), kotlin.Function1((it.czerwinski.kotlin.util.flatMap.R, it.czerwinski.kotlin.util.Either((it.czerwinski.kotlin.util.flatMap.L, it.czerwinski.kotlin.util.flatMap.T)))))/transform).

### Parameters

`transform` - Function transforming a [Right](-right/index.html) to an [Either](-either/index.html).

**Return**
[Either](-either/index.html) mapped using [transform](flat-map.html#it.czerwinski.kotlin.util$flatMap(it.czerwinski.kotlin.util.RightProjection((it.czerwinski.kotlin.util.flatMap.L, it.czerwinski.kotlin.util.flatMap.R)), kotlin.Function1((it.czerwinski.kotlin.util.flatMap.R, it.czerwinski.kotlin.util.Either((it.czerwinski.kotlin.util.flatMap.L, it.czerwinski.kotlin.util.flatMap.T)))))/transform) or this object if this is a [Left](-left/index.html).

