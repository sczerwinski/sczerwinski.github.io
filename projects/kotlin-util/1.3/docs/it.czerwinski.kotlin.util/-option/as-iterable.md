---
title: Option.asIterable - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [asIterable](./as-iterable.html)

# asIterable

`abstract fun asIterable(): `[`Iterable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)`<`[`T`](index.html#T)`>`

Returns an iterable that wraps this [Option](index.html) returning its value if it is defined,
or an empty iterable if the option is empty.

**Return**
An iterable that wraps this [Option](index.html) returning its value if it is defined,
or an empty iterable if the option is empty.

**Since**
1.1

