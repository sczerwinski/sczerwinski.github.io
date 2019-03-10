---
title: Success.toEither - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](index.html) / [toEither](./to-either.html)

# toEither

`fun toEither(): `[`Either`](../-either/index.html)`<`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`, `[`T`](index.html#T)`>`

Overrides [Try.toEither](../-try/to-either.html)

Converts this [Try](../-try/index.html) to [Either](../-either/index.html).

**Return**
[Left](../-left/index.html) if this is [Failure](../-failure/index.html) or [Right](../-right/index.html) if this is [Success](index.html).

