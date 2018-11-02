---
title: Success.toOption - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](index.html) / [toOption](./to-option.html)

# toOption

`fun toOption(): `[`Option`](../-option/index.html)`<`[`T`](index.html#T)`>`

Overrides [Try.toOption](../-try/to-option.html)

Converts this [Try](../-try/index.html) to [Option](../-option/index.html).

**Return**
[None](../-none/index.html) if this is [Failure](../-failure/index.html) or [Some](../-some/index.html) if this is [Success](index.html).

