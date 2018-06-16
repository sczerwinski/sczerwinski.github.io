---
title: filterNotNull - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../index.html) / [it.czerwinski.kotlin.util](index.html) / [filterNotNull](./filter-not-null.html)

# filterNotNull

`fun <L, R> `[`LeftProjection`](-left-projection/index.html)`<`[`L`](filter-not-null.html#L)`?, `[`R`](filter-not-null.html#R)`>.filterNotNull(): `[`Either`](-either/index.html)`<`[`L`](filter-not-null.html#L)`, `[`R`](filter-not-null.html#R)`>?`

Returns the same [Left](-left/index.html) if its value is not `null`. Otherwise returns `null`.

**Return**
The same [Left](-left/index.html) if its value is not `null`. Otherwise returns `null`.

`fun <L, R> `[`RightProjection`](-right-projection/index.html)`<`[`L`](filter-not-null.html#L)`, `[`R`](filter-not-null.html#R)`?>.filterNotNull(): `[`Either`](-either/index.html)`<`[`L`](filter-not-null.html#L)`, `[`R`](filter-not-null.html#R)`>?`

Returns the same [Right](-right/index.html) if its value is not `null`. Otherwise returns `null`.

**Return**
The same [Right](-right/index.html) if its value is not `null`. Otherwise returns `null`.

`fun <T> `[`Try`](-try/index.html)`<`[`T`](filter-not-null.html#T)`?>.filterNotNull(): `[`Try`](-try/index.html)`<`[`T`](filter-not-null.html#T)`>`

Returns the same [Success](-success/index.html) if its value is not `null`. Otherwise returns a [Failure](-failure/index.html).

**Return**
The same [Success](-success/index.html) if its value is not `null`. Otherwise returns a [Failure](-failure/index.html).

