---
title: Option.none - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [none](./none.html)

# none

`inline fun none(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns `false` if the [predicate](none.html#it.czerwinski.kotlin.util.Option$none(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) is met by the value if this is [Some](../-some/index.html) or `true` otherwise.

### Parameters

`predicate` - Predicate function.

**Return**
`false` if the [predicate](none.html#it.czerwinski.kotlin.util.Option$none(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) is met by the value if this is [Some](../-some/index.html) or `true` otherwise.

**Since**
1.1

