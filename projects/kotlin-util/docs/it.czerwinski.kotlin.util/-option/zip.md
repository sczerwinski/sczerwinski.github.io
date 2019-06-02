---
title: Option.zip - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [zip](./zip.html)

# zip

`infix fun <R> zip(other: `[`Option`](index.html)`<`[`R`](zip.html#R)`>): `[`Option`](index.html)`<`[`Pair`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)`<`[`T`](index.html#T)`, `[`R`](zip.html#R)`>>`

Returns [Some](../-some/index.html) containing a `Pair` of values of this and [other](index.html) if both [Option](index.html)s are [Some](../-some/index.html).
Otherwise returns [None](../-none/index.html).

### Parameters

`other` - Other [Option](index.html).

**Return**
[Some](../-some/index.html) containing a `Pair` of values of this and [other](index.html) if both [Option](index.html)s are [Some](../-some/index.html).
Otherwise returns [None](../-none/index.html).

**Since**
1.1

`inline fun <T1, R> zip(other: `[`Option`](index.html)`<`[`T1`](zip.html#T1)`>, transform: (`[`T`](index.html#T)`, `[`T1`](zip.html#T1)`) -> `[`R`](zip.html#R)`): `[`Option`](index.html)`<`[`R`](zip.html#R)`>`

Returns [Some](../-some/index.html) containing the result of applying [transform](zip.html#it.czerwinski.kotlin.util.Option$zip(it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.Option.zip.T1)), kotlin.Function2((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.zip.T1, it.czerwinski.kotlin.util.Option.zip.R)))/transform) to both values of this and [other](index.html)
if both [Option](index.html)s are [Some](../-some/index.html). Otherwise returns [None](../-none/index.html).

### Parameters

`other` - Other [Option](index.html).

`transform` - Function transforming values of both [Some](../-some/index.html).

**Return**
[Some](../-some/index.html) containing the result of applying [transform](zip.html#it.czerwinski.kotlin.util.Option$zip(it.czerwinski.kotlin.util.Option((it.czerwinski.kotlin.util.Option.zip.T1)), kotlin.Function2((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.zip.T1, it.czerwinski.kotlin.util.Option.zip.R)))/transform) to both values of this and [other](index.html)
if both [Option](index.html)s are [Some](../-some/index.html). Otherwise returns [None](../-none/index.html).

**Since**
1.1

