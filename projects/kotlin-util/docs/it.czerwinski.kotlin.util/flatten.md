---
title: flatten - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../index.html) / [it.czerwinski.kotlin.util](index.html) / [flatten](./flatten.html)

# flatten

`fun <T> `[`Try`](-try/index.html)`<`[`Option`](-option/index.html)`<`[`T`](flatten.html#T)`>>.flatten(): `[`Option`](-option/index.html)`<`[`T`](flatten.html#T)`>`

Extracts an [Option](-option/index.html) nested in the [Try](-try/index.html) to a not nested [Option](-option/index.html).

**Return**
[Option](-option/index.html) nested in a [Success](-success/index.html) or [None](-none/index.html) if this is a [Failure](-failure/index.html).

`fun <T> `[`Option`](-option/index.html)`<`[`Try`](-try/index.html)`<`[`T`](flatten.html#T)`>>.flatten(): `[`Option`](-option/index.html)`<`[`T`](flatten.html#T)`>`

Returns [Some](-some/index.html) if this [Some](-some/index.html) contains a [Success](-success/index.html). Otherwise returns [None](-none/index.html).

**Return**
[Some](-some/index.html) if this [Some](-some/index.html) contains a [Success](-success/index.html). Otherwise returns [None](-none/index.html).

`fun <T> `[`Option`](-option/index.html)`<`[`Iterable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)`<`[`T`](flatten.html#T)`>>.flatten(): `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`T`](flatten.html#T)`>`

Returns nested [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html) if this is [Some](-some/index.html). Otherwise returns an empty [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html).

**Return**
Nested [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html) if this is [Some](-some/index.html). Otherwise returns an empty [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html).

`fun <T> `[`Option`](-option/index.html)`<`[`Option`](-option/index.html)`<`[`T`](flatten.html#T)`>>.flatten(): `[`Option`](-option/index.html)`<`[`T`](flatten.html#T)`>`

Transforms a nested [Option](-option/index.html) to a not nested [Option](-option/index.html).

**Return**
[Option](-option/index.html) nested in a [Some](-some/index.html) or [None](-none/index.html) if this option is empty.

`fun <T> `[`Try`](-try/index.html)`<`[`Try`](-try/index.html)`<`[`T`](flatten.html#T)`>>.flatten(): `[`Try`](-try/index.html)`<`[`T`](flatten.html#T)`>`

Transforms a nested [Try](-try/index.html) to a not nested [Try](-try/index.html).

**Return**
[Try](-try/index.html) nested in a [Success](-success/index.html) or this object if this is a [Failure](-failure/index.html).

