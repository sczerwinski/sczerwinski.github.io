---
title: RightProjection.filterIsInstance - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [RightProjection](index.html) / [filterIsInstance](./filter-is-instance.html)

# filterIsInstance

`inline fun <reified T> filterIsInstance(): `[`Either`](../-either/index.html)`<`[`L`](index.html#L)`, `[`T`](filter-is-instance.html#T)`>?`

Returns the same [Right](../-right/index.html) casted to type [T](filter-is-instance.html#T) if it is [T](filter-is-instance.html#T). Otherwise returns `null`.

### Parameters

`T` - Required type of the optional value.

**Return**
The same [Right](../-right/index.html) casted to type [T](filter-is-instance.html#T) if it is [T](filter-is-instance.html#T). Otherwise returns `null`.

