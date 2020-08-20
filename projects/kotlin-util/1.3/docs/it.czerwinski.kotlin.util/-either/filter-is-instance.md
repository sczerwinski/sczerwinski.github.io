---
title: Either.filterIsInstance - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Either](index.html) / [filterIsInstance](./filter-is-instance.html)

# filterIsInstance

`inline fun <reified T> filterIsInstance(): `[`Either`](index.html)`<`[`L`](index.html#L)`, `[`T`](filter-is-instance.html#T)`>?`

Returns the same [Right](../-right/index.html) casted to type [T](filter-is-instance.html#T) if it is [T](filter-is-instance.html#T). Otherwise returns `null`.

### Parameters

`T` - Required type of the optional value.

**Return**
The same [Right](../-right/index.html) casted to type [T](filter-is-instance.html#T) if it is [T](filter-is-instance.html#T). Otherwise returns `null`.

**Since**
1.3

