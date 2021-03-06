---
title: Success.forEach - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](index.html) / [forEach](./for-each.html)

# forEach

`fun forEach(action: (`[`T`](index.html#T)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)

Overrides [Try.forEach](../-try/for-each.html)

Runs [action](../-try/for-each.html#it.czerwinski.kotlin.util.Try$forEach(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Unit)))/action) if this is a [Success](index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Failure](../-failure/index.html).

### Parameters

`action` - Action to be run on a value of a [Success](index.html).