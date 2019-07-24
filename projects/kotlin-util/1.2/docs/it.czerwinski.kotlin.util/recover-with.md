---
title: recoverWith - Kotlin utilities
---

[Kotlin utilities](../index.html) / [it.czerwinski.kotlin.util](index.html) / [recoverWith](./recover-with.html)

# recoverWith

`inline fun <T> `[`Try`](-try/index.html)`<`[`T`](recover-with.html#T)`>.recoverWith(rescue: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`Try`](-try/index.html)`<`[`T`](recover-with.html#T)`>): `[`Try`](-try/index.html)`<`[`T`](recover-with.html#T)`>`

Returns this [Try](-try/index.html) if this is a [Success](-success/index.html) or a [Try](-try/index.html) created by the [rescue](recover-with.html#it.czerwinski.kotlin.util$recoverWith(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recoverWith.T)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recoverWith.T)))))/rescue) function if this is a [Failure](-failure/index.html).

### Parameters

`rescue` - Function creating a new [Try](-try/index.html) from the exception of a [Failure](-failure/index.html).

**Return**
This [Try](-try/index.html) if this is a [Success](-success/index.html) or a [Try](-try/index.html) created by the [rescue](recover-with.html#it.czerwinski.kotlin.util$recoverWith(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recoverWith.T)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recoverWith.T)))))/rescue) function if this is a [Failure](-failure/index.html).

