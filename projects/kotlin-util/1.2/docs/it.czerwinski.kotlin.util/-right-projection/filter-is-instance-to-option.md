---
title: RightProjection.filterIsInstanceToOption - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [RightProjection](index.html) / [filterIsInstanceToOption](./filter-is-instance-to-option.html)

# filterIsInstanceToOption

`inline fun <reified T> filterIsInstanceToOption(): `[`Option`](../-option/index.html)`<`[`Either`](../-either/index.html)`<`[`L`](index.html#L)`, `[`T`](filter-is-instance-to-option.html#T)`>>`

Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) casted to type [T](filter-is-instance-to-option.html#T) if it is [T](filter-is-instance-to-option.html#T). Otherwise returns [None](../-none/index.html).

### Parameters

`T` - Required type of the optional value.

**Return**
[Some](../-some/index.html) containing the same [Right](../-right/index.html) casted to type [T](filter-is-instance-to-option.html#T) if it is [T](filter-is-instance-to-option.html#T). Otherwise returns [None](../-none/index.html).

