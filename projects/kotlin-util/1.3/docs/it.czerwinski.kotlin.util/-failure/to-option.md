---
title: Failure.toOption - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Failure](index.html) / [toOption](./to-option.html)

# toOption

`fun toOption(): `[`Option`](../-option/index.html)`<`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`>`

Overrides [Try.toOption](../-try/to-option.html)

Converts this [Try](../-try/index.html) to [Option](../-option/index.html).

**Return**
[None](../-none/index.html) if this is [Failure](index.html) or [Some](../-some/index.html) if this is [Success](../-success/index.html).

