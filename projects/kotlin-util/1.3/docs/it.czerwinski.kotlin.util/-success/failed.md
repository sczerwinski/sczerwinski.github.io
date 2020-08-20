---
title: Success.failed - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](index.html) / [failed](./failed.html)

# failed

`val failed: `[`Try`](../-try/index.html)`<`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`>`

Overrides [Try.failed](../-try/failed.html)

Returns a [Success](index.html) with an exception it this is a [Failure](../-failure/index.html) or a [Failure](../-failure/index.html) if this is a [Success](index.html).

**Return**
A [Success](index.html) with an exception it this is a [Failure](../-failure/index.html) or a [Failure](../-failure/index.html) if this is a [Success](index.html).

