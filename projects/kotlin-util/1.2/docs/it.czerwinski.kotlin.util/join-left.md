---
title: joinLeft - Kotlin utilities
---

[Kotlin utilities](../index.html) / [it.czerwinski.kotlin.util](index.html) / [joinLeft](./join-left.html)

# joinLeft

`fun <L, R> `[`Either`](-either/index.html)`<`[`Either`](-either/index.html)`<`[`L`](join-left.html#L)`, `[`R`](join-left.html#R)`>, `[`R`](join-left.html#R)`>.joinLeft(): `[`Either`](-either/index.html)`<`[`L`](join-left.html#L)`, `[`R`](join-left.html#R)`>`

Returns this if this is [Right](-right/index.html). Otherwise returns value of [Left](-left/index.html).

Requires [Left](-left/index.html) to be an [Either](-either/index.html).

**Return**
This if this is [Right](-right/index.html). Otherwise returns value of [Left](-left/index.html).

