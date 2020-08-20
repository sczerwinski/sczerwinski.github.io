---
title: Some.asSequence - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Some](index.html) / [asSequence](./as-sequence.html)

# asSequence

`fun asSequence(): `[`Sequence`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)`<`[`T`](index.html#T)`>`

Overrides [Option.asSequence](../-option/as-sequence.html)

Returns a sequence that wraps this [Option](../-option/index.html) returning its value if it is defined,
or an empty sequence if the option is empty.

**Return**
A sequence that wraps this [Option](../-option/index.html) returning its value if it is defined,
or an empty sequence if the option is empty.

**Since**
1.1

