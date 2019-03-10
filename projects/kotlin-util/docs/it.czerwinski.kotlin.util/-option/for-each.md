---
title: Option.forEach - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [forEach](./for-each.html)

# forEach

`inline fun forEach(action: (`[`T`](index.html#T)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Runs [action](for-each.html#it.czerwinski.kotlin.util.Option$forEach(kotlin.Function1((it.czerwinski.kotlin.util.Option.T, kotlin.Unit)))/action) if this is a [Some](../-some/index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is [None](../-none/index.html).

### Parameters

`action` - Action to be run on a value of a [Some](../-some/index.html).