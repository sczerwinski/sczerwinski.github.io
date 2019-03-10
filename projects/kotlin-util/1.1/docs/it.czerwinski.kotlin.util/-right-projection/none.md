---
title: RightProjection.none - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [RightProjection](index.html) / [none](./none.html)

# none

`inline fun none(predicate: (`[`R`](index.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns `false` if the [predicate](none.html#it.czerwinski.kotlin.util.RightProjection$none(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) is met by the value if this is [Right](../-right/index.html) or `true` otherwise.

### Parameters

`predicate` - Predicate function.

**Return**
`false` if the [predicate](none.html#it.czerwinski.kotlin.util.RightProjection$none(kotlin.Function1((it.czerwinski.kotlin.util.RightProjection.R, kotlin.Boolean)))/predicate) is met by the value if this is [Right](../-right/index.html) or `true` otherwise.

**Since**
1.1

