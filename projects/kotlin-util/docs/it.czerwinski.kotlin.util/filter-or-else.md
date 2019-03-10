---
title: filterOrElse - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../index.html) / [it.czerwinski.kotlin.util](index.html) / [filterOrElse](./filter-or-else.html)

# filterOrElse

`inline fun <L, R> `[`LeftProjection`](-left-projection/index.html)`<`[`L`](filter-or-else.html#L)`, `[`R`](filter-or-else.html#R)`>.filterOrElse(predicate: (`[`L`](filter-or-else.html#L)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, zero: () -> `[`R`](filter-or-else.html#R)`): `[`Either`](-either/index.html)`<`[`L`](filter-or-else.html#L)`, `[`R`](filter-or-else.html#R)`>?`

Returns the same [Left](-left/index.html) if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.LeftProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.L, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.R)))/predicate) is satisfied for the value,
`Right(zero)` if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.LeftProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.L, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.R)))/predicate) is not satisfied for the value,
or the same [Right](-right/index.html) if this is [Right](-right/index.html).

### Parameters

`predicate` - Predicate function.

`zero` - Provider of the value used if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.LeftProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.L, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.R)))/predicate) is not satisfied.

**Return**
The same [Left](-left/index.html) if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.LeftProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.L, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.R)))/predicate) is satisfied for the value,
`Right(zero)` if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.LeftProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.L, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.R)))/predicate) is not satisfied for the value,
or the same [Right](-right/index.html) if this is [Right](-right/index.html).

**Since**
1.2

`inline fun <L, R> `[`RightProjection`](-right-projection/index.html)`<`[`L`](filter-or-else.html#L)`, `[`R`](filter-or-else.html#R)`>.filterOrElse(predicate: (`[`R`](filter-or-else.html#R)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, zero: () -> `[`L`](filter-or-else.html#L)`): `[`Either`](-either/index.html)`<`[`L`](filter-or-else.html#L)`, `[`R`](filter-or-else.html#R)`>?`

Returns the same [Right](-right/index.html) if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.RightProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.R, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.L)))/predicate) is satisfied for the value,
`Left(zero)` if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.RightProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.R, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.L)))/predicate) is not satisfied for the value,
or the same [Left](-left/index.html) if this is [Left](-left/index.html).

### Parameters

`predicate` - Predicate function.

`zero` - Provider of the value used if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.RightProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.R, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.L)))/predicate) is not satisfied.

**Return**
The same [Right](-right/index.html) if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.RightProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.R, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.L)))/predicate) is satisfied for the value,
`Left(zero)` if the [predicate](filter-or-else.html#it.czerwinski.kotlin.util$filterOrElse(it.czerwinski.kotlin.util.RightProjection((it.czerwinski.kotlin.util.filterOrElse.L, it.czerwinski.kotlin.util.filterOrElse.R)), kotlin.Function1((it.czerwinski.kotlin.util.filterOrElse.R, kotlin.Boolean)), kotlin.Function0((it.czerwinski.kotlin.util.filterOrElse.L)))/predicate) is not satisfied for the value,
or the same [Left](-left/index.html) if this is [Left](-left/index.html).

**Since**
1.2

