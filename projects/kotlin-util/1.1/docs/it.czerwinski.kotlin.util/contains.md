---
title: contains - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../index.html) / [it.czerwinski.kotlin.util](index.html) / [contains](./contains.html)

# contains

`operator fun <T> `[`Option`](-option/index.html)`<`[`T`](contains.html#T)`>.contains(element: `[`T`](contains.html#T)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)

Tests whether the [Option](-option/index.html) contains the given [element](contains.html#it.czerwinski.kotlin.util$contains(it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.contains.T)), it.czerwinski.kotlin.util.contains.T)/element).

### Parameters

`element` - An element to be tested.

**Return**
`true` if the [element](contains.html#it.czerwinski.kotlin.util$contains(it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.contains.T)), it.czerwinski.kotlin.util.contains.T)/element) is equal to the value of this [Some](-some/index.html), or `false` otherwise.

