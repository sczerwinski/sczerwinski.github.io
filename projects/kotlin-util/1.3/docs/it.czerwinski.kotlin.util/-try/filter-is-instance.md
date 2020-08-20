---
title: Try.filterIsInstance - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [filterIsInstance](./filter-is-instance.html)

# filterIsInstance

`inline fun <reified R> filterIsInstance(): `[`Try`](index.html)`<`[`R`](filter-is-instance.html#R)`>`

Returns the same [Success](../-success/index.html) casted to type [R](filter-is-instance.html#R) if it is [R](filter-is-instance.html#R). Otherwise returns a [Failure](../-failure/index.html).

### Parameters

`R` - Required type of the optional value.

**Return**
The same [Success](../-success/index.html) casted to type [R](filter-is-instance.html#R) if it is [R](filter-is-instance.html#R). Otherwise returns a [Failure](../-failure/index.html).

