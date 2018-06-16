---
title: filterNotNullToOption - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../index.html) / [it.czerwinski.kotlin.util](index.html) / [filterNotNullToOption](./filter-not-null-to-option.html)

# filterNotNullToOption

`fun <L, R> `[`LeftProjection`](-left-projection/index.html)`<`[`L`](filter-not-null-to-option.html#L)`?, `[`R`](filter-not-null-to-option.html#R)`>.filterNotNullToOption(): `[`Option`](-option/index.html)`<`[`Either`](-either/index.html)`<`[`L`](filter-not-null-to-option.html#L)`, `[`R`](filter-not-null-to-option.html#R)`>>`

Returns [Some](-some/index.html) containing the same [Left](-left/index.html) if its value is not `null`. Otherwise returns [None](-none/index.html).

**Return**
[Some](-some/index.html) containing the same [Left](-left/index.html) if its value is not `null`. Otherwise returns [None](-none/index.html).

`fun <L, R> `[`RightProjection`](-right-projection/index.html)`<`[`L`](filter-not-null-to-option.html#L)`, `[`R`](filter-not-null-to-option.html#R)`?>.filterNotNullToOption(): `[`Option`](-option/index.html)`<`[`Either`](-either/index.html)`<`[`L`](filter-not-null-to-option.html#L)`, `[`R`](filter-not-null-to-option.html#R)`>>`

Returns [Some](-some/index.html) containing the same [Right](-right/index.html) if its value is not `null`. Otherwise returns [None](-none/index.html).

**Return**
[Some](-some/index.html) containing the same [Right](-right/index.html) if its value is not `null`. Otherwise returns [None](-none/index.html).

