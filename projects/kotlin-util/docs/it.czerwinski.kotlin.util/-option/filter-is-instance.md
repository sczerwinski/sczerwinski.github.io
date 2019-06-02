---
title: Option.filterIsInstance - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [filterIsInstance](./filter-is-instance.html)

# filterIsInstance

`inline fun <reified R> filterIsInstance(): `[`Option`](index.html)`<`[`R`](filter-is-instance.html#R)`>`

Returns the same [Some](../-some/index.html) casted to type [R](filter-is-instance.html#R) if it is [R](filter-is-instance.html#R). Otherwise returns a [None](../-none/index.html).

### Parameters

`R` - Required type of the optional value.

**Return**
The same [Some](../-some/index.html) casted to type [R](filter-is-instance.html#R) if it is [R](filter-is-instance.html#R). Otherwise returns a [None](../-none/index.html).

