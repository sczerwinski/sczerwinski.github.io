---
title: Either - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Either](./index.html)

# Either

`sealed class Either<out L, out R>`

Disjoint union. The instance might be either [Left](../-left/index.html) or [Right](../-right/index.html).

This type is based on `scala.Either`.

### Parameters

`L` - Type of [Left](../-left/index.html)

`R` - Type of [Right](../-right/index.html)

### Properties

| [isLeft](is-left.html) | `abstract val isLeft: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if this is a [Left](../-left/index.html) or `false` if this is [Right](../-right/index.html). |
| [isRight](is-right.html) | `abstract val isRight: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if this is a [Right](../-right/index.html) or `false` if this is [Left](../-left/index.html). |
| [left](left.html) | `val left: `[`LeftProjection`](../-left-projection/index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>`<br>Projects [Either](./index.html) as [Left](../-left/index.html). |
| [right](right.html) | `val right: `[`RightProjection`](../-right-projection/index.html)`<`[`L`](index.html#L)`, `[`R`](index.html#R)`>`<br>Projects [Either](./index.html) as [Right](../-right/index.html). |

### Functions

| [contains](contains.html) | `abstract operator fun contains(element: `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if the [element](contains.html#it.czerwinski.kotlin.util.Either$contains(kotlin.Any)/element) is equal to the value of this [Either](./index.html), or `false` otherwise. |
| [fold](fold.html) | `fun <T> fold(leftTransform: (`[`L`](index.html#L)`) -> `[`T`](fold.html#T)`, rightTransform: (`[`R`](index.html#R)`) -> `[`T`](fold.html#T)`): `[`T`](fold.html#T)<br>Transforms [Left](../-left/index.html) with [leftTransform](fold.html#it.czerwinski.kotlin.util.Either$fold(kotlin.Function1((it.czerwinski.kotlin.util.Either.L, it.czerwinski.kotlin.util.Either.fold.T)), kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.fold.T)))/leftTransform) or [Right](../-right/index.html) with [rightTransform](fold.html#it.czerwinski.kotlin.util.Either$fold(kotlin.Function1((it.czerwinski.kotlin.util.Either.L, it.czerwinski.kotlin.util.Either.fold.T)), kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.fold.T)))/rightTransform). |
| [swap](swap.html) | `abstract fun swap(): `[`Either`](./index.html)`<`[`R`](index.html#R)`, `[`L`](index.html#L)`>`<br>Swaps [Left](../-left/index.html) to [Right](../-right/index.html) and [Right](../-right/index.html) to [Left](../-left/index.html). |

### Extension Functions

| [asOption](../as-option.html) | `fun <T> `[`T`](../as-option.html#T)`?.asOption(): `[`Option`](../-option/index.html)`<`[`T`](../as-option.html#T)`>`<br>Returns [Some](../-some/index.html) if this is not `null` or [None](../-none/index.html) if this is `null`. |
| [joinLeft](../join-left.html) | `fun <L, R> `[`Either`](./index.html)`<`[`Either`](./index.html)`<`[`L`](../join-left.html#L)`, `[`R`](../join-left.html#R)`>, `[`R`](../join-left.html#R)`>.joinLeft(): `[`Either`](./index.html)`<`[`L`](../join-left.html#L)`, `[`R`](../join-left.html#R)`>`<br>Returns this if this is [Right](../-right/index.html). Otherwise returns value of [Left](../-left/index.html). |
| [joinRight](../join-right.html) | `fun <L, R> `[`Either`](./index.html)`<`[`L`](../join-right.html#L)`, `[`Either`](./index.html)`<`[`L`](../join-right.html#L)`, `[`R`](../join-right.html#R)`>>.joinRight(): `[`Either`](./index.html)`<`[`L`](../join-right.html#L)`, `[`R`](../join-right.html#R)`>`<br>Returns this if this is [Left](../-left/index.html). Otherwise returns value of [Right](../-right/index.html). |
| [merge](../merge.html) | `fun <T> `[`Either`](./index.html)`<`[`T`](../merge.html#T)`, `[`T`](../merge.html#T)`>.merge(): `[`T`](../merge.html#T)<br>Merges [Left](../-left/index.html) and [Right](../-right/index.html) of the same type to a single value. |

### Inheritors

| [Left](../-left/index.html) | `data class Left<out L> : `[`Either`](./index.html)`<`[`L`](../-left/index.html#L)`, `[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`>` |
| [Right](../-right/index.html) | `data class Right<out R> : `[`Either`](./index.html)`<`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`, `[`R`](../-right/index.html#R)`>` |

