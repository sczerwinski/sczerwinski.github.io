---
title: None.asSequence - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [None](index.html) / [asSequence](./as-sequence.html)

# asSequence

`fun asSequence(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`>`

Overrides [Option.asSequence](../-option/as-sequence.html)

Returns a sequence that wraps this [Option](../-option/index.html) returning its value if it is defined,
or an empty sequence if the option is empty.

**Return**
A sequence that wraps this [Option](../-option/index.html) returning its value if it is defined,
or an empty sequence if the option is empty.

**Since**
1.1

