---
title: recover - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../index.html) / [it.czerwinski.kotlin.util](index.html) / [recover](./recover.html)

# recover

`inline fun <T> `[`Try`](-try/index.html)`<`[`T`](recover.html#T)`>.recover(rescue: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`T`](recover.html#T)`): `[`Try`](-try/index.html)`<`[`T`](recover.html#T)`>`

Returns this [Try](-try/index.html) if this is a [Success](-success/index.html) or a [Try](-try/index.html) created for the [rescue](recover.html#it.czerwinski.kotlin.util$recover(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recover.T)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.recover.T)))/rescue) operation if this is a [Failure](-failure/index.html).

### Parameters

`rescue` - Function creating a new value from the exception of a [Failure](-failure/index.html).

**Return**
This [Try](-try/index.html) if this is a [Success](-success/index.html) or a [Try](-try/index.html) created for the [rescue](recover.html#it.czerwinski.kotlin.util$recover(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recover.T)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.recover.T)))/rescue) operation if this is a [Failure](-failure/index.html).

