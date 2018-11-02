---
title: Failure.failed - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Failure](index.html) / [failed](./failed.html)

# failed

`val failed: `[`Try`](../-try/index.html)`<`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`>`

Overrides [Try.failed](../-try/failed.html)

Returns a [Success](../-success/index.html) with an exception it this is a [Failure](index.html) or a [Failure](index.html) if this is a [Success](../-success/index.html).

**Return**
A [Success](../-success/index.html) with an exception it this is a [Failure](index.html) or a [Failure](index.html) if this is a [Success](../-success/index.html).

