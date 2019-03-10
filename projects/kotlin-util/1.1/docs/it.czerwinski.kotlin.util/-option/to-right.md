---
title: Option.toRight - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [toRight](./to-right.html)

# toRight

`inline fun <L> toRight(left: () -> `[`L`](to-right.html#L)`): `[`Either`](../-either/index.html)`<`[`L`](to-right.html#L)`, `[`T`](index.html#T)`>`

Returns a [Left](../-left/index.html) containing the given argument [left](to-right.html#it.czerwinski.kotlin.util.Option$toRight(kotlin.Function0((it.czerwinski.kotlin.util.Option.toRight.L)))/left) if this is empty,
or a [Right](../-right/index.html) containing this option's value if it is defined.

### Parameters

`left` - Producer of the fallback [Left](../-left/index.html) value.

`L` - The type of the [Left](../-left/index.html) value.

**Return**
a [Left](../-left/index.html) containing the given argument [left](to-right.html#it.czerwinski.kotlin.util.Option$toRight(kotlin.Function0((it.czerwinski.kotlin.util.Option.toRight.L)))/left) if this is empty,
or a [Right](../-right/index.html) containing this option's value if it is defined.

