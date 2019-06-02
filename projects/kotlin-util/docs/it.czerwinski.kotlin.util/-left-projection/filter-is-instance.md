---
title: LeftProjection.filterIsInstance - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [LeftProjection](index.html) / [filterIsInstance](./filter-is-instance.html)

# filterIsInstance

`inline fun <reified T> filterIsInstance(): `[`Either`](../-either/index.html)`<`[`T`](filter-is-instance.html#T)`, `[`R`](index.html#R)`>?`

Returns the same [Left](../-left/index.html) casted to type [T](filter-is-instance.html#T) if it is [T](filter-is-instance.html#T). Otherwise returns `null`.

### Parameters

`T` - Required type of the optional value.

**Return**
The same [Left](../-left/index.html) casted to type [T](filter-is-instance.html#T) if it is [T](filter-is-instance.html#T). Otherwise returns `null`.

