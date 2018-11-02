---
title: RightProjection.any - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [RightProjection](index.html) / [any](./any.html)

# any

`inline fun any(predicate: (`[`R`](index.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns the result of applying the [predicate](any.html#it.czerwinski.kotlin.util.RightProjection$any(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) to the value if this is [Right](../-right/index.html)
or `false` if this is [Left](../-left/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The result of applying the [predicate](any.html#it.czerwinski.kotlin.util.RightProjection$any(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) to the value if this is [Right](../-right/index.html)
or `false` if this is [Left](../-left/index.html).

