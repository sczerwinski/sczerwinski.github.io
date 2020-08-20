---
title: Try.toEither - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [toEither](./to-either.html)

# toEither

`abstract fun toEither(): `[`Either`](../-either/index.html)`<`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`, `[`T`](index.html#T)`>`

Converts this [Try](index.html) to [Either](../-either/index.html).

**Return**
[Left](../-left/index.html) if this is [Failure](../-failure/index.html) or [Right](../-right/index.html) if this is [Success](../-success/index.html).

