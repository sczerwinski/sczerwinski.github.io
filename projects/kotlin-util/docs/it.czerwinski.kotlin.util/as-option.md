---
title: asOption - Kotlin utilities
---

[Kotlin utilities](../index.html) / [it.czerwinski.kotlin.util](index.html) / [asOption](./as-option.html)

# asOption

`fun <T> `[`T`](as-option.html#T)`?.asOption(): `[`Option`](-option/index.html)`<`[`T`](as-option.html#T)`>`

Returns [Some](-some/index.html) if this is not `null` or [None](-none/index.html) if this is `null`.

### Parameters

`T` - Type of the nullable value.

**Return**
[Some](-some/index.html) if this is not `null` or [None](-none/index.html) if this is `null`.

