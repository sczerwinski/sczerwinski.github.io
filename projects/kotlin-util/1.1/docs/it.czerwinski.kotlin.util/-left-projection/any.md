---
title: LeftProjection.any - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [LeftProjection](index.html) / [any](./any.html)

# any

`inline fun any(predicate: (`[`L`](index.html#L)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns the result of applying the [predicate](any.html#it.czerwinski.kotlin.util.LeftProjection$any(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) to the value if this is [Left](../-left/index.html)
or `false` if this is [Right](../-right/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The result of applying the [predicate](any.html#it.czerwinski.kotlin.util.LeftProjection$any(kotlin.Function1((it.czerwinski.kotlin.util.LeftProjection.L, kotlin.Boolean)))/predicate) to the value if this is [Left](../-left/index.html)
or `false` if this is [Right](../-right/index.html).

