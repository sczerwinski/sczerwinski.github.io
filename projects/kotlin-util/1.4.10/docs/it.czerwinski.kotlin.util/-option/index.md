---
title: Option -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Option](index.html)



# Option  
 [common] 

Representation of an optional value. The instance might be either [Some](../-some/index.html) value or [None](../-none/index.html).

sealed class [Option](index.html)<out [T](index.html)>   


## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| T| <br><br>Type of the optional value.<br><br>
  


## Types  
  
|  Name|  Summary| 
|---|---|
| [Companion](-companion/index.html)| [common]  <br>Content  <br>object [Companion](-companion/index.html)  <br><br><br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [all](all.html)| [common]  <br>Brief description  <br><br><br>Returns the result of applying the predicate to the value if this is [Some](../-some/index.html) or true if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun [all](all.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [any](any.html)| [common]  <br>Brief description  <br><br><br>Returns the result of applying the predicate to the value if this is [Some](../-some/index.html) or false if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun [any](any.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [asIterable](as-iterable.html)| [common]  <br>Brief description  <br><br><br>Returns an iterable that wraps this [Option](index.html) returning its value if it is defined, or an empty iterable if the option is empty.<br><br>  <br>Content  <br>abstract fun [asIterable](as-iterable.html)(): [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](index.html)>  <br><br><br>
| [asSequence](as-sequence.html)| [common]  <br>Brief description  <br><br><br>Returns a sequence that wraps this [Option](index.html) returning its value if it is defined, or an empty sequence if the option is empty.<br><br>  <br>Content  <br>abstract fun [asSequence](as-sequence.html)(): [Sequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)<[T](index.html)>  <br><br><br>
| [equals](../-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)| [common]  <br>Content  <br>open operator override fun [equals](../-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [filter](filter.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Some](../-some/index.html) if the predicate is satisfied for the value. Otherwise returns a [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun [filter](filter.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](index.html)<[T](index.html)>  <br><br><br>
| [filterIsInstance](filter-is-instance.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Some](../-some/index.html) casted to type [R](filter-is-instance.html) if it is [R](filter-is-instance.html). Otherwise returns a [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun <[R](filter-is-instance.html)> [filterIsInstance](filter-is-instance.html)(): [Option](index.html)<[R](filter-is-instance.html)>  <br><br><br>
| [filterNot](filter-not.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Some](../-some/index.html) if the predicate is not satisfied for the value. Otherwise returns a [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun [filterNot](filter-not.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](index.html)<[T](index.html)>  <br><br><br>
| [flatMap](flat-map.html)| [common]  <br>Brief description  <br><br><br>Maps value of a [Some](../-some/index.html) to a new [Option](index.html) using transform or returns the same [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun <[R](flat-map.html)> [flatMap](flat-map.html)(transform: ([T](index.html)) -> [Option](index.html)<[R](flat-map.html)>): [Option](index.html)<[R](flat-map.html)>  <br><br><br>
| [fold](fold.html)| [common]  <br>Brief description  <br><br><br>Returns result of applying transform on the value of [Some](../-some/index.html) or default if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun <[R](fold.html)> [fold](fold.html)(default: [R](fold.html), transform: ([T](index.html)) -> [R](fold.html)): [R](fold.html)  <br>inline fun <[R](fold.html)> [fold](fold.html)(default: () -> [R](fold.html), transform: ([T](index.html)) -> [R](fold.html)): [R](fold.html)  <br><br><br>
| [forEach](for-each.html)| [common]  <br>Brief description  <br><br><br>Runs action if this is a [Some](../-some/index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun [forEach](for-each.html)(action: ([T](index.html)) -> [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))  <br><br><br>
| [get](get.html)| [common]  <br>Brief description  <br><br><br>Gets the value of a [Some](../-some/index.html) or throws an exception.<br><br>  <br>Content  <br>abstract fun [get](get.html)(): [T](index.html)  <br><br><br>
| [getOrNull](get-or-null.html)| [common]  <br>Brief description  <br><br><br>Gets the value of a [Some](../-some/index.html) or null if this is a [None](../-none/index.html).<br><br>  <br>Content  <br>abstract fun [getOrNull](get-or-null.html)(): [T](index.html)?  <br><br><br>
| [hashCode](../-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [hashCode](../-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| [iterator](iterator.html)| [common]  <br>Brief description  <br><br><br>Returns a singleton iterator returning the option's value if it is defined, or an empty iterator if the option is empty.<br><br>  <br>Content  <br>abstract fun [iterator](iterator.html)(): [Iterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)<[T](index.html)>  <br><br><br>
| [map](map.html)| [common]  <br>Brief description  <br><br><br>Maps value of a [Some](../-some/index.html) using transform or returns the same [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun <[R](map.html)> [map](map.html)(transform: ([T](index.html)) -> [R](map.html)): [Option](index.html)<[R](map.html)>  <br><br><br>
| [none](none.html)| [common]  <br>Brief description  <br><br><br>Returns false if the predicate is met by the value if this is [Some](../-some/index.html) or true otherwise.<br><br>  <br>Content  <br>inline fun [none](none.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [toLeft](to-left.html)| [common]  <br>Brief description  <br><br><br>Returns a [Right](../-right/index.html) containing the given argument right if this is empty, or a [Left](../-left/index.html) containing this option's value if it is defined.<br><br>  <br>Content  <br>inline fun <[R](to-left.html)> [toLeft](to-left.html)(right: () -> [R](to-left.html)): [Either](../-either/index.html)<[T](index.html), [R](to-left.html)>  <br><br><br>
| [toList](to-list.html)| [common]  <br>Brief description  <br><br><br>Returns a singleton list containing the option's value if it is defined, or an empty list if the option is empty.<br><br>  <br>Content  <br>abstract fun [toList](to-list.html)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](index.html)>  <br><br><br>
| [toRight](to-right.html)| [common]  <br>Brief description  <br><br><br>Returns a [Left](../-left/index.html) containing the given argument left if this is empty, or a [Right](../-right/index.html) containing this option's value if it is defined.<br><br>  <br>Content  <br>inline fun <[L](to-right.html)> [toRight](to-right.html)(left: () -> [L](to-right.html)): [Either](../-either/index.html)<[L](to-right.html), [T](index.html)>  <br><br><br>
| [toString](../-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [toString](../-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>
| [zip](zip.html)| [common]  <br>Brief description  <br><br><br>Returns [Some](../-some/index.html) containing a Pair of values of this and [other](index.html) if both [Option](index.html)s are [Some](../-some/index.html). Otherwise returns [None](../-none/index.html).<br><br>  <br>Content  <br>infix fun <[R](zip.html)> [zip](zip.html)(other: [Option](index.html)<[R](zip.html)>): [Option](index.html)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.html), [R](zip.html)>>  <br><br><br>[common]  <br>Brief description  <br><br><br>Returns [Some](../-some/index.html) containing the result of applying transform to both values of this and [other](index.html) if both [Option](index.html)s are [Some](../-some/index.html). Otherwise returns [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun <[T1](zip.html), [R](zip.html)> [zip](zip.html)(other: [Option](index.html)<[T1](zip.html)>, transform: ([T](index.html), [T1](zip.html)) -> [R](zip.html)): [Option](index.html)<[R](zip.html)>  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [isDefined](index.html#it.czerwinski.kotlin.util/Option/isDefined/#/PointingToDeclaration/)|  [common] <br><br>Returns true if the option is [Some](../-some/index.html). Otherwise returns false.<br><br>val [isDefined](index.html#it.czerwinski.kotlin.util/Option/isDefined/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isEmpty](index.html#it.czerwinski.kotlin.util/Option/isEmpty/#/PointingToDeclaration/)|  [common] <br><br>Returns true if the option is [None](../-none/index.html). Otherwise returns false.<br><br>abstract val [isEmpty](index.html#it.czerwinski.kotlin.util/Option/isEmpty/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isNotEmpty](index.html#it.czerwinski.kotlin.util/Option/isNotEmpty/#/PointingToDeclaration/)|  [common] <br><br>Returns true if the option is [Some](../-some/index.html). Otherwise returns false.<br><br>val [isNotEmpty](index.html#it.czerwinski.kotlin.util/Option/isNotEmpty/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>


## Inheritors  
  
|  Name| 
|---|
| [Some](../-some/index.html)
| [None](../-none/index.html)


## Extensions  
  
|  Name|  Summary| 
|---|---|
| [contains](../contains.html)| [common]  <br>Brief description  <br><br><br>Tests whether the [Option](index.html) contains the given element.<br><br>  <br>Content  <br>operator fun <[T](../contains.html)> [Option](index.html)<[T](../contains.html)>.[contains](../contains.html)(element: [T](../contains.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [evert](../evert.html)| [common]  <br>Brief description  <br><br><br>Moves inner [Try](../-try/index.html) outside of the outer [Option](index.html).<br><br>  <br>Content  <br>fun <[T](../evert.html)> [Option](index.html)<[Try](../-try/index.html)<[T](../evert.html)>>.[evert](../evert.html)(): [Try](../-try/index.html)<[Option](index.html)<[T](../evert.html)>>  <br><br><br>
| [flatten](../flatten.html)| [common]  <br>Brief description  <br><br><br>Returns [Some](../-some/index.html) if this [Some](../-some/index.html) contains a [Success](../-success/index.html). Otherwise returns [None](../-none/index.html).<br><br>  <br>Content  <br>fun <[T](../flatten.html)> [Option](index.html)<[Try](../-try/index.html)<[T](../flatten.html)>>.[flatten](../flatten.html)(): [Option](index.html)<[T](../flatten.html)>  <br><br><br>[common]  <br>Brief description  <br><br><br>Returns nested [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) if this is [Some](../-some/index.html). Otherwise returns an empty [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).<br><br>  <br>Content  <br>fun <[T](../flatten.html)> [Option](index.html)<[Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](../flatten.html)>>.[flatten](../flatten.html)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](../flatten.html)>  <br><br><br>[common]  <br>Brief description  <br><br><br>Transforms a nested [Option](index.html) to a not nested [Option](index.html).<br><br>  <br>Content  <br>fun <[T](../flatten.html)> [Option](index.html)<[Option](index.html)<[T](../flatten.html)>>.[flatten](../flatten.html)(): [Option](index.html)<[T](../flatten.html)>  <br><br><br>
| [getOrElse](../get-or-else.html)| [common]  <br>Brief description  <br><br><br>Gets the value of a [Some](../-some/index.html) or default value if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun <[T](../get-or-else.html)> [Option](index.html)<[T](../get-or-else.html)>.[getOrElse](../get-or-else.html)(default: () -> [T](../get-or-else.html)): [T](../get-or-else.html)  <br><br><br>
| [orElse](../or-else.html)| [common]  <br>Brief description  <br><br><br>Returns this [Option](index.html) if this is a [Some](../-some/index.html) or default if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun <[T](../or-else.html)> [Option](index.html)<[T](../or-else.html)>.[orElse](../or-else.html)(default: () -> [Option](index.html)<[T](../or-else.html)>): [Option](index.html)<[T](../or-else.html)>  <br><br><br>
| [unzip](../unzip.html)| [common]  <br>Brief description  <br><br><br>Transforms an [Option](index.html) of a Pair into a Pair of an [Option](index.html) of the first value and an [Option](index.html) of the second value.<br><br>  <br>Content  <br>fun <[A](../unzip.html), [B](../unzip.html)> [Option](index.html)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[A](../unzip.html), [B](../unzip.html)>>.[unzip](../unzip.html)(): [Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[Option](index.html)<[A](../unzip.html)>, [Option](index.html)<[B](../unzip.html)>>  <br><br><br>[common]  <br>Brief description  <br><br><br>Transforms an [Option](index.html) of a Triple into a Triple of an [Option](index.html) of the first value, an [Option](index.html) of the second value, and an [Option](index.html) of the third value.<br><br>  <br>Content  <br>fun <[A](../unzip.html), [B](../unzip.html), [C](../unzip.html)> [Option](index.html)<[Triple](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)<[A](../unzip.html), [B](../unzip.html), [C](../unzip.html)>>.[unzip](../unzip.html)(): [Triple](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)<[Option](index.html)<[A](../unzip.html)>, [Option](index.html)<[B](../unzip.html)>, [Option](index.html)<[C](../unzip.html)>>  <br><br><br>

