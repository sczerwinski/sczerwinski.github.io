---
title: Option.all - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [all](./all.html)

# all

`inline fun all(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns the result of applying the [predicate](all.html#it.czerwinski.kotlin.util.Option$all(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) to the value if this is [Some](../-some/index.html)
or `true` if this is [None](../-none/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The result of applying the [predicate](all.html#it.czerwinski.kotlin.util.Option$all(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) to the value if this is [Some](../-some/index.html)
or `true` if this is [None](../-none/index.html).

