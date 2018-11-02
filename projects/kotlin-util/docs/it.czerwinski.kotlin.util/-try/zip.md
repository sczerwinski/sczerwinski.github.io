---
title: Try.zip - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](index.html) / [zip](./zip.html)

# zip

`infix fun <R> zip(other: `[`Try`](index.html)`<`[`R`](zip.html#R)`>): `[`Try`](index.html)`<`[`Pair`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)`<`[`T`](index.html#T)`, `[`R`](zip.html#R)`>>`

Returns [Success](../-success/index.html) containing a `Pair` of values of this and [other](index.html)
if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).

### Parameters

`other` - Other [Try](index.html).

**Return**
[Success](../-success/index.html) containing a `Pair` of values of this and [other](index.html)
if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).

**Since**
1.1

`inline fun <T1, R> zip(other: `[`Try`](index.html)`<`[`T1`](zip.html#T1)`>, transform: (`[`T`](index.html#T)`, `[`T1`](zip.html#T1)`) -> `[`R`](zip.html#R)`): `[`Try`](index.html)`<`[`R`](zip.html#R)`>`

Returns [Success](../-success/index.html) containing the result of applying [transform](zip.html#it.czerwinski.kotlin.util.Try$zip(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.zip.T1)), kotlin.Function2((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.zip.T1, it.czerwinski.kotlin.util.Try.zip.R)))/transform) to both values of this and [other](index.html)
if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).

### Parameters

`other` - Other [Try](index.html).

`transform` - Function transforming values of both instances of [Success](../-success/index.html).

**Return**
[Success](../-success/index.html) containing the result of applying [transform](zip.html#it.czerwinski.kotlin.util.Try$zip(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.zip.T1)), kotlin.Function2((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.zip.T1, it.czerwinski.kotlin.util.Try.zip.R)))/transform) to both values of this and [other](index.html)
if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).

**Since**
1.1

