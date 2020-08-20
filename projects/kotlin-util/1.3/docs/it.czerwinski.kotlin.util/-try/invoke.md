---
title: Try.invoke - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [invoke](./invoke.html)

# invoke

`inline operator fun <T> invoke(callable: () -> `[`T`](invoke.html#T)`): `[`Try`](index.html)`<`[`T`](invoke.html#T)`>`

Creates a new [Try](index.html) based on the result of the [callable](invoke.html#it.czerwinski.kotlin.util.Try.Companion$invoke(kotlin.Function0((it.czerwinski.kotlin.util.Try.Companion.invoke.T)))/callable).

### Parameters

`callable` - A callable operation.

**Return**
An instance of [Success](../-success/index.html) or [Failure](../-failure/index.html), depending on whether the operation.

