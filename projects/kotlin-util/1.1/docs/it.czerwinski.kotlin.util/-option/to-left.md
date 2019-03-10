---
title: Option.toLeft - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [toLeft](./to-left.html)

# toLeft

`inline fun <R> toLeft(right: () -> `[`R`](to-left.html#R)`): `[`Either`](../-either/index.html)`<`[`T`](index.html#T)`, `[`R`](to-left.html#R)`>`

Returns a [Right](../-right/index.html) containing the given argument [right](to-left.html#it.czerwinski.kotlin.util.Option$toLeft(kotlin.Function0((it.czerwinski.kotlin.util.Option.toLeft.R)))/right) if this is empty,
or a [Left](../-left/index.html) containing this option's value if it is defined.

### Parameters

`right` - Producer of the fallback [Right](../-right/index.html) value.

`R` - The type of the [Right](../-right/index.html) value.

**Return**
a [Right](../-right/index.html) containing the given argument [right](to-left.html#it.czerwinski.kotlin.util.Option$toLeft(kotlin.Function0((it.czerwinski.kotlin.util.Option.toLeft.R)))/right) if this is empty,
or a [Left](../-left/index.html) containing this option's value if it is defined.

