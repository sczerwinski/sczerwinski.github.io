---
title: Try - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Try](./index.html)

# Try

`sealed class Try<out T>`

Representation of an operation that might successfully return a value or throw an exception.

An instance of [Try](./index.html) may be either a [Success](../-success/index.html) or a [Failure](../-failure/index.html).

This type is based on `scala.util.Try`.

### Parameters

`T` - Type of the value of a successful operation.

### Properties

| [failed](failed.html) | `abstract val failed: `[`Try`](./index.html)`<`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`>`<br>Returns a [Success](../-success/index.html) with an exception it this is a [Failure](../-failure/index.html) or a [Failure](../-failure/index.html) if this is a [Success](../-success/index.html). |
| [isFailure](is-failure.html) | `abstract val isFailure: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if this is a [Failure](../-failure/index.html) or `false` if this is [Success](../-success/index.html). |
| [isSuccess](is-success.html) | `abstract val isSuccess: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if this is a [Success](../-success/index.html) or `false` if this is [Failure](../-failure/index.html). |

### Functions

| [filter](filter.html) | `abstract fun filter(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](./index.html)`<`[`T`](index.html#T)`>`<br>Returns the same [Success](../-success/index.html) if the [predicate](filter.html#it.czerwinski.kotlin.util.Try$filter(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html). |
| [filterIsInstance](filter-is-instance.html) | `fun <R> filterIsInstance(): `[`Try`](./index.html)`<`[`R`](filter-is-instance.html#R)`>`<br>Returns the same [Success](../-success/index.html) casted to type [R](filter-is-instance.html#R) if it is [R](filter-is-instance.html#R). Otherwise returns a [Failure](../-failure/index.html). |
| [filterNot](filter-not.html) | `abstract fun filterNot(predicate: (`[`T`](index.html#T)`) -> `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Try`](./index.html)`<`[`T`](index.html#T)`>`<br>Returns the same [Success](../-success/index.html) if the [predicate](filter-not.html#it.czerwinski.kotlin.util.Try$filterNot(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Boolean)))/predicate) is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.html). |
| [flatMap](flat-map.html) | `abstract fun <R> flatMap(transform: (`[`T`](index.html#T)`) -> `[`Try`](./index.html)`<`[`R`](flat-map.html#R)`>): `[`Try`](./index.html)`<`[`R`](flat-map.html#R)`>`<br>Maps value of a [Success](../-success/index.html) to a new [Try](./index.html) using [transform](flat-map.html#it.czerwinski.kotlin.util.Try$flatMap(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.flatMap.R)))))/transform) or returns the same [Try](./index.html) if this is a [Failure](../-failure/index.html). |
| [fold](fold.html) | `fun <R> fold(successTransform: (`[`T`](index.html#T)`) -> `[`R`](fold.html#R)`, failureTransform: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`R`](fold.html#R)`): `[`R`](fold.html#R)<br>Transforms a [Success](../-success/index.html) using [successTransform](fold.html#it.czerwinski.kotlin.util.Try$fold(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.fold.R)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try.fold.R)))/successTransform) or a [Failure](../-failure/index.html) using [failureTransform](fold.html#it.czerwinski.kotlin.util.Try$fold(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.fold.R)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try.fold.R)))/failureTransform). |
| [forEach](for-each.html) | `abstract fun forEach(action: (`[`T`](index.html#T)`) -> `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Runs [action](for-each.html#it.czerwinski.kotlin.util.Try$forEach(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, kotlin.Unit)))/action) if this is a [Success](../-success/index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Failure](../-failure/index.html). |
| [get](get.html) | `abstract fun get(): `[`T`](index.html#T)<br>Gets the value of a [Success](../-success/index.html) or throw an exception from a [Failure](../-failure/index.html). |
| [getOrNull](get-or-null.html) | `abstract fun getOrNull(): `[`T`](index.html#T)`?`<br>Gets the value of a [Success](../-success/index.html) or `null` if this is a [Failure](../-failure/index.html). |
| [map](map.html) | `abstract fun <R> map(transform: (`[`T`](index.html#T)`) -> `[`R`](map.html#R)`): `[`Try`](./index.html)`<`[`R`](map.html#R)`>`<br>Maps value of a [Success](../-success/index.html) using [transform](map.html#it.czerwinski.kotlin.util.Try$map(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try.map.R)))/transform) or returns the same [Try](./index.html) if this is a [Failure](../-failure/index.html). |
| [toEither](to-either.html) | `abstract fun toEither(): `[`Either`](../-either/index.html)`<`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`, `[`T`](index.html#T)`>`<br>Converts this [Try](./index.html) to [Either](../-either/index.html). |
| [toOption](to-option.html) | `abstract fun toOption(): `[`Option`](../-option/index.html)`<`[`T`](index.html#T)`>`<br>Converts this [Try](./index.html) to [Option](../-option/index.html). |
| [transform](transform.html) | `fun <R> transform(successTransform: (`[`T`](index.html#T)`) -> `[`Try`](./index.html)`<`[`R`](transform.html#R)`>, failureTransform: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`Try`](./index.html)`<`[`R`](transform.html#R)`>): `[`Try`](./index.html)`<`[`R`](transform.html#R)`>`<br>Transforms a [Success](../-success/index.html) using [successTransform](transform.html#it.czerwinski.kotlin.util.Try$transform(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))))/successTransform) or a [Failure](../-failure/index.html) using [failureTransform](transform.html#it.czerwinski.kotlin.util.Try$transform(kotlin.Function1((it.czerwinski.kotlin.util.Try.T, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.Try.transform.R)))))/failureTransform). |

### Companion Object Functions

| [invoke](invoke.html) | `operator fun <T> invoke(callable: () -> `[`T`](invoke.html#T)`): `[`Try`](./index.html)`<`[`T`](invoke.html#T)`>`<br>Creates a new [Try](./index.html) based on the result of the [callable](invoke.html#it.czerwinski.kotlin.util.Try.Companion$invoke(kotlin.Function0((it.czerwinski.kotlin.util.Try.Companion.invoke.T)))/callable). |

### Extension Functions

| [filterNotNull](../filter-not-null.html) | `fun <T> `[`Try`](./index.html)`<`[`T`](../filter-not-null.html#T)`?>.filterNotNull(): `[`Try`](./index.html)`<`[`T`](../filter-not-null.html#T)`>`<br>Returns the same [Success](../-success/index.html) if its value is not `null`. Otherwise returns a [Failure](../-failure/index.html). |
| [flatten](../flatten.html) | `fun <T> `[`Try`](./index.html)`<`[`Option`](../-option/index.html)`<`[`T`](../flatten.html#T)`>>.flatten(): `[`Option`](../-option/index.html)`<`[`T`](../flatten.html#T)`>`<br>Extracts an [Option](../-option/index.html) nested in the [Try](./index.html) to a not nested [Option](../-option/index.html).`fun <T> `[`Try`](./index.html)`<`[`Try`](./index.html)`<`[`T`](../flatten.html#T)`>>.flatten(): `[`Try`](./index.html)`<`[`T`](../flatten.html#T)`>`<br>Transforms a nested [Try](./index.html) to a not nested [Try](./index.html). |
| [getOrElse](../get-or-else.html) | `fun <T> `[`Try`](./index.html)`<`[`T`](../get-or-else.html#T)`>.getOrElse(default: () -> `[`T`](../get-or-else.html#T)`): `[`T`](../get-or-else.html#T)<br>Gets the value of a [Success](../-success/index.html) or [default](../get-or-else.html#it.czerwinski.kotlin.util$getOrElse(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.getOrElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.getOrElse.T)))/default) value if this is a [Failure](../-failure/index.html). |
| [orElse](../or-else.html) | `fun <T> `[`Try`](./index.html)`<`[`T`](../or-else.html#T)`>.orElse(default: () -> `[`Try`](./index.html)`<`[`T`](../or-else.html#T)`>): `[`Try`](./index.html)`<`[`T`](../or-else.html#T)`>`<br>Returns this [Try](./index.html) if this is a [Success](../-success/index.html) or [default](../or-else.html#it.czerwinski.kotlin.util$orElse(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.orElse.T)), kotlin.Function0((it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.orElse.T)))))/default) if this is a [Failure](../-failure/index.html). |
| [recover](../recover.html) | `fun <T> `[`Try`](./index.html)`<`[`T`](../recover.html#T)`>.recover(rescue: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`T`](../recover.html#T)`): `[`Try`](./index.html)`<`[`T`](../recover.html#T)`>`<br>Returns this [Try](./index.html) if this is a [Success](../-success/index.html) or a [Try](./index.html) created for the [rescue](../recover.html#it.czerwinski.kotlin.util$recover(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recover.T)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.recover.T)))/rescue) operation if this is a [Failure](../-failure/index.html). |
| [recoverWith](../recover-with.html) | `fun <T> `[`Try`](./index.html)`<`[`T`](../recover-with.html#T)`>.recoverWith(rescue: (`[`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`) -> `[`Try`](./index.html)`<`[`T`](../recover-with.html#T)`>): `[`Try`](./index.html)`<`[`T`](../recover-with.html#T)`>`<br>Returns this [Try](./index.html) if this is a [Success](../-success/index.html) or a [Try](./index.html) created by the [rescue](../recover-with.html#it.czerwinski.kotlin.util$recoverWith(it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recoverWith.T)), kotlin.Function1((kotlin.Throwable, it.czerwinski.kotlin.util.Try((it.czerwinski.kotlin.util.recoverWith.T)))))/rescue) function if this is a [Failure](../-failure/index.html). |

### Inheritors

| [Failure](../-failure/index.html) | `data class Failure : `[`Try`](./index.html)`<`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`>` |
| [Success](../-success/index.html) | `data class Success<out T> : `[`Try`](./index.html)`<`[`T`](../-success/index.html#T)`>` |
