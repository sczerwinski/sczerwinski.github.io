---
title: Right - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Right](./index.html)

# Right

`data class Right<out R> : `[`Either`](../-either/index.html)`<`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`, `[`R`](index.html#R)`>`

### Constructors

| [&lt;init&gt;](-init-.html) | `Right(value: `[`R`](index.html#R)`)` |

### Properties

| [isLeft](is-left.html) | `val isLeft: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if this is a [Left](../-left/index.html) or `false` if this is [Right](./index.html). |
| [isRight](is-right.html) | `val isRight: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if this is a [Right](./index.html) or `false` if this is [Left](../-left/index.html). |
| [value](value.html) | `val value: `[`R`](index.html#R) |

### Inherited Properties

| [left](../-either/left.html) | `val left: `[`LeftProjection`](../-left-projection/index.html)`<`[`L`](../-either/index.html#L)`, `[`R`](../-either/index.html#R)`>`<br>Projects [Either](../-either/index.html) as [Left](../-left/index.html). |
| [right](../-either/right.html) | `val right: `[`RightProjection`](../-right-projection/index.html)`<`[`L`](../-either/index.html#L)`, `[`R`](../-either/index.html#R)`>`<br>Projects [Either](../-either/index.html) as [Right](./index.html). |

### Functions

| [contains](contains.html) | `fun contains(element: `[`Any`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns `true` if the [element](../-either/contains.html#it.czerwinski.kotlin.util.Either$contains(kotlin.Any)/element) is equal to the value of this [Either](../-either/index.html), or `false` otherwise. |
| [swap](swap.html) | `fun swap(): `[`Either`](../-either/index.html)`<`[`R`](index.html#R)`, `[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`>`<br>Swaps [Left](../-left/index.html) to [Right](./index.html) and [Right](./index.html) to [Left](../-left/index.html). |

### Inherited Functions

| [fold](../-either/fold.html) | `fun <T> fold(leftTransform: (`[`L`](../-either/index.html#L)`) -> `[`T`](../-either/fold.html#T)`, rightTransform: (`[`R`](../-either/index.html#R)`) -> `[`T`](../-either/fold.html#T)`): `[`T`](../-either/fold.html#T)<br>Transforms [Left](../-left/index.html) with [leftTransform](../-either/fold.html#it.czerwinski.kotlin.util.Either$fold(kotlin.Function1((it.czerwinski.kotlin.util.Either.L, it.czerwinski.kotlin.util.Either.fold.T)), kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.fold.T)))/leftTransform) or [Right](./index.html) with [rightTransform](../-either/fold.html#it.czerwinski.kotlin.util.Either$fold(kotlin.Function1((it.czerwinski.kotlin.util.Either.L, it.czerwinski.kotlin.util.Either.fold.T)), kotlin.Function1((it.czerwinski.kotlin.util.Either.R, it.czerwinski.kotlin.util.Either.fold.T)))/rightTransform). |

### Extension Functions

| [joinLeft](../join-left.html) | `fun <L, R> `[`Either`](../-either/index.html)`<`[`Either`](../-either/index.html)`<`[`L`](../join-left.html#L)`, `[`R`](../join-left.html#R)`>, `[`R`](../join-left.html#R)`>.joinLeft(): `[`Either`](../-either/index.html)`<`[`L`](../join-left.html#L)`, `[`R`](../join-left.html#R)`>`<br>Returns this if this is [Right](./index.html). Otherwise returns value of [Left](../-left/index.html). |
| [joinRight](../join-right.html) | `fun <L, R> `[`Either`](../-either/index.html)`<`[`L`](../join-right.html#L)`, `[`Either`](../-either/index.html)`<`[`L`](../join-right.html#L)`, `[`R`](../join-right.html#R)`>>.joinRight(): `[`Either`](../-either/index.html)`<`[`L`](../join-right.html#L)`, `[`R`](../join-right.html#R)`>`<br>Returns this if this is [Left](../-left/index.html). Otherwise returns value of [Right](./index.html). |
| [merge](../merge.html) | `fun <T> `[`Either`](../-either/index.html)`<`[`T`](../merge.html#T)`, `[`T`](../merge.html#T)`>.merge(): `[`T`](../merge.html#T)<br>Merges [Left](../-left/index.html) and [Right](./index.html) of the same type to a single value. |

