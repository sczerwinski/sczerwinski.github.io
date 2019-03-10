---
title: Failure.forEach - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Failure](index.html) / [forEach](./for-each.html)

# forEach

`fun forEach(action: (`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Overrides [Try.forEach](../-try/for-each.html)

Runs [action](../-try/for-each.html#it.czerwinski.kotlin.util.Try$forEach(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Unit)))/action) if this is a [Success](../-success/index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Failure](index.html).

### Parameters

`action` - Action to be run on a value of a [Success](../-success/index.html).