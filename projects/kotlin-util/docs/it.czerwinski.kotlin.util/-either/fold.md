---
title: Either.fold - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Either](index.html) / [fold](./fold.html)

# fold

`inline fun <T> fold(leftTransform: (`[`L`](index.html#L)`) -> `[`T`](fold.html#T)`, rightTransform: (`[`R`](index.html#R)`) -> `[`T`](fold.html#T)`): `[`T`](fold.html#T)

Transforms [Left](../-left/index.html) with [leftTransform](fold.html#it.czerwinski.kotlin.util.Either$fold(kotlin.Function1((it.czerwinski.kotlin.util.Either.L, it.czerwinski.kotlin.util.Either.fold.T)), kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.fold.T)))/leftTransform) or [Right](../-right/index.html) with [rightTransform](fold.html#it.czerwinski.kotlin.util.Either$fold(kotlin.Function1((it.czerwinski.kotlin.util.Either.L, it.czerwinski.kotlin.util.Either.fold.T)), kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.fold.T)))/rightTransform).

### Parameters

`leftTransform` - Function transforming [Left](../-left/index.html) value.

`rightTransform` - Function transforming [Right](../-right/index.html) value.

**Return**
Result of applying [leftTransform](fold.html#it.czerwinski.kotlin.util.Either$fold(kotlin.Function1((it.czerwinski.kotlin.util.Either.L, it.czerwinski.kotlin.util.Either.fold.T)), kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.fold.T)))/leftTransform) on [Left](../-left/index.html) or [rightTransform](fold.html#it.czerwinski.kotlin.util.Either$fold(kotlin.Function1((it.czerwinski.kotlin.util.Either.L, it.czerwinski.kotlin.util.Either.fold.T)), kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.fold.T)))/rightTransform) on [Right](../-right/index.html).

