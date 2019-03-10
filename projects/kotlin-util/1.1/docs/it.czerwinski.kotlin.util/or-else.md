---
title: orElse - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../index.html) / [it.czerwinski.kotlin.util](index.html) / [orElse](./or-else.html)

# orElse

`inline fun <T> `[`Option`](-option/index.html)`<`[`T`](or-else.html#T)`>.orElse(default: () -> `[`Option`](-option/index.html)`<`[`T`](or-else.html#T)`>): `[`Option`](-option/index.html)`<`[`T`](or-else.html#T)`>`

Returns this [Option](-option/index.html) if this is a [Some](-some/index.html) or [default](or-else.html#it.czerwinski.kotlin.util$orElse(it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.orElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.orElse.T)))))/default) if this is [None](-none/index.html).

### Parameters

`default` - Default [Option](-option/index.html) provider.

**Return**
This [Some](-some/index.html) or [default](or-else.html#it.czerwinski.kotlin.util$orElse(it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.orElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.orElse.T)))))/default).

`inline fun <T> `[`Try`](-try/index.html)`<`[`T`](or-else.html#T)`>.orElse(default: () -> `[`Try`](-try/index.html)`<`[`T`](or-else.html#T)`>): `[`Try`](-try/index.html)`<`[`T`](or-else.html#T)`>`

Returns this [Try](-try/index.html) if this is a [Success](-success/index.html) or [default](or-else.html#it.czerwinski.kotlin.util$orElse(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.orElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.orElse.T)))))/default) if this is a [Failure](-failure/index.html).

### Parameters

`default` - Default [Try](-try/index.html) provider.

**Return**
This [Success](-success/index.html) or [default](or-else.html#it.czerwinski.kotlin.util$orElse(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.orElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.orElse.T)))))/default).

