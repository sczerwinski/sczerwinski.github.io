---
title: Try.forEach - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [forEach](./for-each.html)

# forEach

`abstract fun forEach(action: (`[`T`](index.html#T)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Runs [action](for-each.html#it.czerwinski.kotlin.util.Try$forEach(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Unit)))/action) if this is a [Success](../-success/index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Failure](../-failure/index.html).

### Parameters

`action` - Action to be run on a value of a [Success](../-success/index.html).