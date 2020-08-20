---
title: Option.flatMap - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [flatMap](./flat-map.html)

# flatMap

`inline fun <R> flatMap(transform: (`[`T`](index.html#T)`) -> `[`Option`](index.html)`<`[`R`](flat-map.html#R)`>): `[`Option`](index.html)`<`[`R`](flat-map.html#R)`>`

Maps value of a [Some](../-some/index.html) to a new [Option](index.html) using [transform](flat-map.html#it.czerwinski.kotlin.util.Option$flatMap(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.Option.flatMap.R)))))/transform) or returns the same [None](../-none/index.html).

### Parameters

`transform` - Function transforming value of a [Some](../-some/index.html) to an [Option](index.html).

**Return**
[Option](index.html) returned by [transform](flat-map.html#it.czerwinski.kotlin.util.Option$flatMap(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.Option.flatMap.R)))))/transform) or this object if this is a [None](../-none/index.html).

