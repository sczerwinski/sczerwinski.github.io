---
title: LeftProjection.filterIsInstanceToOption - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [LeftProjection](index.html) / [filterIsInstanceToOption](./filter-is-instance-to-option.html)

# filterIsInstanceToOption

`inline fun <reified T> filterIsInstanceToOption(): `[`Option`](../-option/index.html)`<`[`Either`](../-either/index.html)`<`[`T`](filter-is-instance-to-option.html#T)`, `[`R`](index.html#R)`>>`

Returns [Some](../-some/index.html) containing the same [Left](../-left/index.html) casted to type [T](filter-is-instance-to-option.html#T) if it is [T](filter-is-instance-to-option.html#T). Otherwise returns [None](../-none/index.html).

### Parameters

`T` - Required type of the optional value.

**Return**
[Some](../-some/index.html) containing the same [Left](../-left/index.html) casted to type [T](filter-is-instance-to-option.html#T) if it is [T](filter-is-instance-to-option.html#T). Otherwise returns [None](../-none/index.html).

