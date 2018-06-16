---
title: Option.invoke - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [invoke](./invoke.html)

# invoke

`operator fun <T> invoke(value: `[`T`](invoke.html#T)`?): `[`Option`](index.html)`<`[`T`](invoke.html#T)`>`

Returns [Some](../-some/index.html) if the [value](invoke.html#it.czerwinski.kotlin.util.Option.Companion$invoke(it.czerwinski.kotlin.util.Option.Companion.invoke.T)/value) is not `null` or [None](../-none/index.html) if the [value](invoke.html#it.czerwinski.kotlin.util.Option.Companion$invoke(it.czerwinski.kotlin.util.Option.Companion.invoke.T)/value) is `null`.

### Parameters

`value` - Nullable value.

`T` - Type of the optional value.

**Return**
[Some](../-some/index.html) if the [value](invoke.html#it.czerwinski.kotlin.util.Option.Companion$invoke(it.czerwinski.kotlin.util.Option.Companion.invoke.T)/value) is not `null` or [None](../-none/index.html) if the [value](invoke.html#it.czerwinski.kotlin.util.Option.Companion$invoke(it.czerwinski.kotlin.util.Option.Companion.invoke.T)/value) is `null`.

