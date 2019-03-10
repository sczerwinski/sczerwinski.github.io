---
title: Option.any - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [any](./any.html)

# any

`inline fun any(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Returns the result of applying the [predicate](any.html#it.czerwinski.kotlin.util.Option$any(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) to the value if this is [Some](../-some/index.html)
or `false` if this is [None](../-none/index.html).

### Parameters

`predicate` - Predicate function.

**Return**
The result of applying the [predicate](any.html#it.czerwinski.kotlin.util.Option$any(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Boolean)))/predicate) to the value if this is [Some](../-some/index.html)
or `false` if this is [None](../-none/index.html).

