---
title: Success - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Success](./index.html)

# Success

`data class Success<out T> : `[`Try`](../-try/index.html)`<`[`T`](index.html#T)`>`

### Constructors

| [&lt;init&gt;](-init-.html) | `Success(value: `[`T`](index.html#T)`)` |

### Properties

| [failed](failed.html) | `val failed: `[`Try`](../-try/index.html)`<`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`>`<br>Returns a [Success](./index.html) with an exception it this is a [Failure](../-failure/index.html) or a [Failure](../-failure/index.html) if this is a [Success](./index.html). |
| [isFailure](is-failure.html) | `val isFailure: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if this is a [Failure](../-failure/index.html) or `false` if this is [Success](./index.html). |
| [isSuccess](is-success.html) | `val isSuccess: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if this is a [Success](./index.html) or `false` if this is [Failure](../-failure/index.html). |
| [value](value.html) | `val value: `[`T`](index.html#T) |

### Functions

| [filter](filter.html) | `fun filter(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](../-try/index.html)`<`[`T`](index.html#T)`>`<br>Returns the same [Success](./index.html) if the [predicate](../-try/filter.html#it.czerwinski.kotlin.util.Try$filter(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html). |
| [filterNot](filter-not.html) | `fun filterNot(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](../-try/index.html)`<`[`T`](index.html#T)`>`<br>Returns the same [Success](./index.html) if the [predicate](../-try/filter-not.html#it.czerwinski.kotlin.util.Try$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.html). |
| [flatMap](flat-map.html) | `fun <R> flatMap(transform: (`[`T`](index.html#T)`) -> `[`Try`](../-try/index.html)`<`[`R`](flat-map.html#R)`>): `[`Try`](../-try/index.html)`<`[`R`](flat-map.html#R)`>`<br>Maps value of a [Success](./index.html) to a new [Try](../-try/index.html) using [transform](../-try/flat-map.html#it.czerwinski.kotlin.util.Try$flatMap(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.flatMap.R)))))/transform) or returns the same [Try](../-try/index.html) if this is a [Failure](../-failure/index.html). |
| [forEach](for-each.html) | `fun forEach(action: (`[`T`](index.html#T)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Runs [action](../-try/for-each.html#it.czerwinski.kotlin.util.Try$forEach(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Unit)))/action) if this is a [Success](./index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Failure](../-failure/index.html). |
| [get](get.html) | `fun get(): `[`T`](index.html#T)<br>Gets the value of a [Success](./index.html) or throw an exception from a [Failure](../-failure/index.html). |
| [getOrNull](get-or-null.html) | `fun getOrNull(): `[`T`](index.html#T)`?`<br>Gets the value of a [Success](./index.html) or `null` if this is a [Failure](../-failure/index.html). |
| [map](map.html) | `fun <R> map(transform: (`[`T`](index.html#T)`) -> `[`R`](map.html#R)`): `[`Try`](../-try/index.html)`<`[`R`](map.html#R)`>`<br>Maps value of a [Success](./index.html) using [transform](../-try/map.html#it.czerwinski.kotlin.util.Try$map(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.map.R)))/transform) or returns the same [Try](../-try/index.html) if this is a [Failure](../-failure/index.html). |
| [toEither](to-either.html) | `fun toEither(): `[`Either`](../-either/index.html)`<`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`, `[`T`](index.html#T)`>`<br>Converts this [Try](../-try/index.html) to [Either](../-either/index.html). |
| [toOption](to-option.html) | `fun toOption(): `[`Option`](../-option/index.html)`<`[`T`](index.html#T)`>`<br>Converts this [Try](../-try/index.html) to [Option](../-option/index.html). |

### Inherited Functions

| [filterIsInstance](../-try/filter-is-instance.html) | `fun <R> filterIsInstance(): `[`Try`](../-try/index.html)`<`[`R`](../-try/filter-is-instance.html#R)`>`<br>Returns the same [Success](./index.html) casted to type [R](../-try/filter-is-instance.html#R) if it is [R](../-try/filter-is-instance.html#R). Otherwise returns a [Failure](../-failure/index.html). |
| [fold](../-try/fold.html) | `fun <R> fold(successTransform: (`[`T`](../-try/index.html#T)`) -> `[`R`](../-try/fold.html#R)`, failureTransform: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`R`](../-try/fold.html#R)`): `[`R`](../-try/fold.html#R)<br>Transforms a [Success](./index.html) using [successTransform](../-try/fold.html#it.czerwinski.kotlin.util.Try$fold(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.fold.R)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try.fold.R)))/successTransform) or a [Failure](../-failure/index.html) using [failureTransform](../-try/fold.html#it.czerwinski.kotlin.util.Try$fold(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.fold.R)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try.fold.R)))/failureTransform). |
| [transform](../-try/transform.html) | `fun <R> transform(successTransform: (`[`T`](../-try/index.html#T)`) -> `[`Try`](../-try/index.html)`<`[`R`](../-try/transform.html#R)`>, failureTransform: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`Try`](../-try/index.html)`<`[`R`](../-try/transform.html#R)`>): `[`Try`](../-try/index.html)`<`[`R`](../-try/transform.html#R)`>`<br>Transforms a [Success](./index.html) using [successTransform](../-try/transform.html#it.czerwinski.kotlin.util.Try$transform(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))))/successTransform) or a [Failure](../-failure/index.html) using [failureTransform](../-try/transform.html#it.czerwinski.kotlin.util.Try$transform(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))))/failureTransform). |
| [zip](../-try/zip.html) | `infix fun <R> zip(other: `[`Try`](../-try/index.html)`<`[`R`](../-try/zip.html#R)`>): `[`Try`](../-try/index.html)`<`[`Pair`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)`<`[`T`](../-try/index.html#T)`, `[`R`](../-try/zip.html#R)`>>`<br>Returns [Success](./index.html) containing a `Pair` of values of this and [other](../-try/index.html) if both instances of [Try](../-try/index.html) are [Success](./index.html). Otherwise returns first [Failure](../-failure/index.html).`fun <T1, R> zip(other: `[`Try`](../-try/index.html)`<`[`T1`](../-try/zip.html#T1)`>, transform: (`[`T`](../-try/index.html#T)`, `[`T1`](../-try/zip.html#T1)`) -> `[`R`](../-try/zip.html#R)`): `[`Try`](../-try/index.html)`<`[`R`](../-try/zip.html#R)`>`<br>Returns [Success](./index.html) containing the result of applying [transform](../-try/zip.html#it.czerwinski.kotlin.util.Try$zip(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.zip.T1)), kotlin.Function2((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.zip.T1, it.czerwinski.kotlin.util.Try.zip.R)))/transform) to both values of this and [other](../-try/index.html) if both instances of [Try](../-try/index.html) are [Success](./index.html). Otherwise returns first [Failure](../-failure/index.html). |

### Extension Functions

| [filterNotNull](../filter-not-null.html) | `fun <T> `[`Try`](../-try/index.html)`<`[`T`](../filter-not-null.html#T)`?>.filterNotNull(): `[`Try`](../-try/index.html)`<`[`T`](../filter-not-null.html#T)`>`<br>Returns the same [Success](./index.html) if its value is not `null`. Otherwise returns a [Failure](../-failure/index.html). |
| [getOrElse](../get-or-else.html) | `fun <T> `[`Try`](../-try/index.html)`<`[`T`](../get-or-else.html#T)`>.getOrElse(default: () -> `[`T`](../get-or-else.html#T)`): `[`T`](../get-or-else.html#T)<br>Gets the value of a [Success](./index.html) or [default](../get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.getOrElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.T)))/default) value if this is a [Failure](../-failure/index.html). |
| [orElse](../or-else.html) | `fun <T> `[`Try`](../-try/index.html)`<`[`T`](../or-else.html#T)`>.orElse(default: () -> `[`Try`](../-try/index.html)`<`[`T`](../or-else.html#T)`>): `[`Try`](../-try/index.html)`<`[`T`](../or-else.html#T)`>`<br>Returns this [Try](../-try/index.html) if this is a [Success](./index.html) or [default](../or-else.html#it.czerwinski.kotlin.util$orElse(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.orElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.orElse.T)))))/default) if this is a [Failure](../-failure/index.html). |
| [recover](../recover.html) | `fun <T> `[`Try`](../-try/index.html)`<`[`T`](../recover.html#T)`>.recover(rescue: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`T`](../recover.html#T)`): `[`Try`](../-try/index.html)`<`[`T`](../recover.html#T)`>`<br>Returns this [Try](../-try/index.html) if this is a [Success](./index.html) or a [Try](../-try/index.html) created for the [rescue](../recover.html#it.czerwinski.kotlin.util$recover(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recover.T)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.recover.T)))/rescue) operation if this is a [Failure](../-failure/index.html). |
| [recoverWith](../recover-with.html) | `fun <T> `[`Try`](../-try/index.html)`<`[`T`](../recover-with.html#T)`>.recoverWith(rescue: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`Try`](../-try/index.html)`<`[`T`](../recover-with.html#T)`>): `[`Try`](../-try/index.html)`<`[`T`](../recover-with.html#T)`>`<br>Returns this [Try](../-try/index.html) if this is a [Success](./index.html) or a [Try](../-try/index.html) created by the [rescue](../recover-with.html#it.czerwinski.kotlin.util$recoverWith(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recoverWith.T)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recoverWith.T)))))/rescue) function if this is a [Failure](../-failure/index.html). |
