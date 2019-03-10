---
title: Some.asIterable - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Some](index.html) / [asIterable](./as-iterable.html)

# asIterable

`fun asIterable(): `[`Iterable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)`<`[`T`](index.html#T)`>`

Overrides [Option.asIterable](../-option/as-iterable.html)

Returns an iterable that wraps this [Option](../-option/index.html) returning its value if it is defined,
or an empty iterable if the option is empty.

**Return**
An iterable that wraps this [Option](../-option/index.html) returning its value if it is defined,
or an empty iterable if the option is empty.

**Since**
1.1

