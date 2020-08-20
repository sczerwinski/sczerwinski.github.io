---
title: getOrElse - Kotlin utilities
---

[Kotlin utilities](../index.html) / [it.czerwinski.kotlin.util](index.html) / [getOrElse](./get-or-else.html)

# getOrElse

`inline fun <L, R> `[`Either`](-either/index.html)`<`[`L`](get-or-else.html#L)`, `[`R`](get-or-else.html#R)`>.getOrElse(default: () -> `[`R`](get-or-else.html#R)`): `[`R`](get-or-else.html#R)

Gets value of this [Right](-right/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.Either((it.czerwinski.kotlin.util.getOrElse.L, it.czerwinski.kotlin.util.getOrElse.R)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.R)))/default) value if this is [Left](-left/index.html).

### Parameters

`default` - Default value provider.

**Return**
Value of this [Right](-right/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.Either((it.czerwinski.kotlin.util.getOrElse.L, it.czerwinski.kotlin.util.getOrElse.R)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.R)))/default).

**Since**
1.3

`inline fun <L, R> `[`LeftProjection`](-left-projection/index.html)`<`[`L`](get-or-else.html#L)`, `[`R`](get-or-else.html#R)`>.getOrElse(default: () -> `[`L`](get-or-else.html#L)`): `[`L`](get-or-else.html#L)

Gets value of this [Left](-left/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.LeftProjection((it.czerwinski.kotlin.util.getOrElse.L, it.czerwinski.kotlin.util.getOrElse.R)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.L)))/default) value if this is [Right](-right/index.html).

### Parameters

`default` - Default value provider.

**Return**
Value of this [Left](-left/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.LeftProjection((it.czerwinski.kotlin.util.getOrElse.L, it.czerwinski.kotlin.util.getOrElse.R)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.L)))/default).

`inline fun <L, R> `[`RightProjection`](-right-projection/index.html)`<`[`L`](get-or-else.html#L)`, `[`R`](get-or-else.html#R)`>.getOrElse(default: () -> `[`R`](get-or-else.html#R)`): `[`R`](get-or-else.html#R)

Gets value of this [Right](-right/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.RightProjection((it.czerwinski.kotlin.util.getOrElse.L, it.czerwinski.kotlin.util.getOrElse.R)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.R)))/default) value if this is [Left](-left/index.html).

### Parameters

`default` - Default value provider.

**Return**
Value of this [Right](-right/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.RightProjection((it.czerwinski.kotlin.util.getOrElse.L, it.czerwinski.kotlin.util.getOrElse.R)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.R)))/default).

`inline fun <T> `[`Option`](-option/index.html)`<`[`T`](get-or-else.html#T)`>.getOrElse(default: () -> `[`T`](get-or-else.html#T)`): `[`T`](get-or-else.html#T)

Gets the value of a [Some](-some/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.getOrElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.T)))/default) value if this is [None](-none/index.html).

### Parameters

`default` - Default value provider.

**Return**
Value of a [Some](-some/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.getOrElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.T)))/default) value.

`inline fun <T> `[`Try`](-try/index.html)`<`[`T`](get-or-else.html#T)`>.getOrElse(default: () -> `[`T`](get-or-else.html#T)`): `[`T`](get-or-else.html#T)

Gets the value of a [Success](-success/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.getOrElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.T)))/default) value if this is a [Failure](-failure/index.html).

### Parameters

`default` - Default value provider.

**Return**
Value of a [Success](-success/index.html) or [default](get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.getOrElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.T)))/default) value.

