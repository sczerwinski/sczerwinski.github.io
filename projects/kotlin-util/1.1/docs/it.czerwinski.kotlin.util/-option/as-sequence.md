---
title: Option.asSequence - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [asSequence](./as-sequence.html)

# asSequence

`abstract fun asSequence(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`T`](index.html#T)`>`

Returns a sequence that wraps this [Option](index.html) returning its value if it is defined,
or an empty sequence if the option is empty.

**Return**
A sequence that wraps this [Option](index.html) returning its value if it is defined,
or an empty sequence if the option is empty.

**Since**
1.1

