---
title: joinRight - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../index.html) / [it.czerwinski.kotlin.util](index.html) / [joinRight](./join-right.html)

# joinRight

`fun <L, R> `[`Either`](-either/index.html)`<`[`L`](join-right.html#L)`, `[`Either`](-either/index.html)`<`[`L`](join-right.html#L)`, `[`R`](join-right.html#R)`>>.joinRight(): `[`Either`](-either/index.html)`<`[`L`](join-right.html#L)`, `[`R`](join-right.html#R)`>`

Returns this if this is [Left](-left/index.html). Otherwise returns value of [Right](-right/index.html).

Requires [Right](-right/index.html) to be an [Either](-either/index.html).

**Return**
This if this is [Left](-left/index.html). Otherwise returns value of [Right](-right/index.html).

