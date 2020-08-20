---
title: Option -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Option](index.md)



# Option  
 [Kotlin utilities] Representation of an optional value. The instance might be either [Some](../-some/index.md) value or [None](../-none/index.md).  
  
sealed class [Option](index.md)<[T](index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>    


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| T| Type of the optional value.
  


## Types  
  
|  Name|  Summary| 
|---|---|
| [Companion](-companion/index.md)| [Kotlin utilities]  <br>Content  <br>object [Companion](-companion/index.md)  <br><br><br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [all](all.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the result of applying the [predicate]() to the value if this is [Some](../-some/index.md) or true if this is [None](../-none/index.md).  <br>Content  <br>inline fun [all](all.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [any](any.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the result of applying the [predicate]() to the value if this is [Some](../-some/index.md) or false if this is [None](../-none/index.md).  <br>Content  <br>inline fun [any](any.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [asIterable](as-iterable.md)| [Kotlin utilities]  <br>Brief description  <br>Returns an iterable that wraps this [Option](index.md) returning its value if it is defined, or an empty iterable if the option is empty.  <br>Content  <br>abstract fun [asIterable](as-iterable.md)(): [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](index.md)>  <br><br><br>
| [asSequence](as-sequence.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a sequence that wraps this [Option](index.md) returning its value if it is defined, or an empty sequence if the option is empty.  <br>Content  <br>abstract fun [asSequence](as-sequence.md)(): [Sequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)<[T](index.md)>  <br><br><br>
| [equals](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/equals.html)| [Kotlin utilities]  <br>Content  <br>open operator override fun [equals](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/equals.html)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [filter](filter.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Some](../-some/index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [None](../-none/index.md).  <br>Content  <br>inline fun [filter](filter.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](index.md)<[T](index.md)>  <br><br><br>
| [filterIsInstance](filter-is-instance.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Some](../-some/index.md) casted to type [R]() if it is [R](). Otherwise returns a [None](../-none/index.md).  <br>Content  <br>inline fun <[R](filter-is-instance.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [filterIsInstance](filter-is-instance.md)(): [Option](index.md)<[R](filter-is-instance.md)>  <br><br><br>
| [filterNot](filter-not.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Some](../-some/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns a [None](../-none/index.md).  <br>Content  <br>inline fun [filterNot](filter-not.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](index.md)<[T](index.md)>  <br><br><br>
| [flatMap](flat-map.md)| [Kotlin utilities]  <br>Brief description  <br>Maps value of a [Some](../-some/index.md) to a new [Option](index.md) using [transform]() or returns the same [None](../-none/index.md).  <br>Content  <br>inline fun <[R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [flatMap](flat-map.md)(transform: ([T](index.md)) -> [Option](index.md)<[R](flat-map.md)>): [Option](index.md)<[R](flat-map.md)>  <br><br><br>
| [fold](fold.md)| [Kotlin utilities]  <br>Brief description  <br>Returns result of applying [transform]() on the value of [Some](../-some/index.md) or [default]() if this is [None](../-none/index.md).  <br>Content  <br>inline fun <[R](fold.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [fold](fold.md)(default: [R](fold.md), transform: ([T](index.md)) -> [R](fold.md)): [R](fold.md)  <br>inline fun <[R](fold.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [fold](fold.md)(default: () -> [R](fold.md), transform: ([T](index.md)) -> [R](fold.md)): [R](fold.md)  <br><br><br>
| [forEach](for-each.md)| [Kotlin utilities]  <br>Brief description  <br>Runs [action]() if this is a [Some](../-some/index.md). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is [None](../-none/index.md).  <br>Content  <br>inline fun [forEach](for-each.md)(action: ([T](index.md)) -> [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))  <br><br><br>
| [get](get.md)| [Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Some](../-some/index.md) or throws an exception.  <br>Content  <br>abstract fun [get](get.md)(): [T](index.md)  <br><br><br>
| [getOrNull](get-or-null.md)| [Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Some](../-some/index.md) or null if this is a [None](../-none/index.md).  <br>Content  <br>abstract fun [getOrNull](get-or-null.md)(): [T](index.md)?  <br><br><br>
| [hashCode](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/hash-code.html)| [Kotlin utilities]  <br>Content  <br>open override fun [hashCode](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/hash-code.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| [iterator](iterator.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a singleton iterator returning the option's value if it is defined, or an empty iterator if the option is empty.  <br>Content  <br>abstract fun [iterator](iterator.md)(): [Iterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)<[T](index.md)>  <br><br><br>
| [map](map.md)| [Kotlin utilities]  <br>Brief description  <br>Maps value of a [Some](../-some/index.md) using [transform]() or returns the same [None](../-none/index.md).  <br>Content  <br>inline fun <[R](map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [map](map.md)(transform: ([T](index.md)) -> [R](map.md)): [Option](index.md)<[R](map.md)>  <br><br><br>
| [none](none.md)| [Kotlin utilities]  <br>Brief description  <br>Returns false if the [predicate]() is met by the value if this is [Some](../-some/index.md) or true otherwise.  <br>Content  <br>inline fun [none](none.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [toLeft](to-left.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a [Right](../-right/index.md) containing the given argument [right]() if this is empty, or a [Left](../-left/index.md) containing this option's value if it is defined.  <br>Content  <br>inline fun <[R](to-left.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [toLeft](to-left.md)(right: () -> [R](to-left.md)): [Either](../-either/index.md)<[T](index.md), [R](to-left.md)>  <br><br><br>
| [toList](to-list.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a singleton list containing the option's value if it is defined, or an empty list if the option is empty.  <br>Content  <br>abstract fun [toList](to-list.md)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](index.md)>  <br><br><br>
| [toRight](to-right.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a [Left](../-left/index.md) containing the given argument [left]() if this is empty, or a [Right](../-right/index.md) containing this option's value if it is defined.  <br>Content  <br>inline fun <[L](to-right.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [toRight](to-right.md)(left: () -> [L](to-right.md)): [Either](../-either/index.md)<[L](to-right.md), [T](index.md)>  <br><br><br>
| [toString](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/to-string.html)| [Kotlin utilities]  <br>Content  <br>open override fun [toString](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/to-string.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>
| [zip](zip.md)| [Kotlin utilities]  <br>Brief description  <br>Returns [Some](../-some/index.md) containing a Pair of values of this and [other](index.md) if both [Option](index.md)s are [Some](../-some/index.md). Otherwise returns [None](../-none/index.md).  <br>Content  <br>infix fun <[R](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](zip.md)(other: [Option](index.md)<[R](zip.md)>): [Option](index.md)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.md), [R](zip.md)>>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns [Some](../-some/index.md) containing the result of applying [transform]() to both values of this and [other](index.md) if both [Option](index.md)s are [Some](../-some/index.md). Otherwise returns [None](../-none/index.md).  <br>Content  <br>inline fun <[T1](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](zip.md)(other: [Option](index.md)<[T1](zip.md)>, transform: ([T](index.md), [T1](zip.md)) -> [R](zip.md)): [Option](index.md)<[R](zip.md)>  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [isDefined](index.md#it.czerwinski.kotlin.util/Option/isDefined/#/PointingToDeclaration/)|  [Kotlin utilities] Returns true if the option is [Some](../-some/index.md). Otherwise returns false.val [isDefined](index.md#it.czerwinski.kotlin.util/Option/isDefined/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isEmpty](index.md#it.czerwinski.kotlin.util/Option/isEmpty/#/PointingToDeclaration/)|  [Kotlin utilities] Returns true if the option is [None](../-none/index.md). Otherwise returns false.abstract val [isEmpty](index.md#it.czerwinski.kotlin.util/Option/isEmpty/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isNotEmpty](index.md#it.czerwinski.kotlin.util/Option/isNotEmpty/#/PointingToDeclaration/)|  [Kotlin utilities] Returns true if the option is [Some](../-some/index.md). Otherwise returns false.val [isNotEmpty](index.md#it.czerwinski.kotlin.util/Option/isNotEmpty/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>


## Inheritors  
  
|  Name| 
|---|
| [Some](../-some/index.md)
| [None](../-none/index.md)


## Extensions  
  
|  Name|  Summary| 
|---|---|
| [contains](../contains.md)| [Kotlin utilities]  <br>Brief description  <br>Tests whether the [Option](index.md) contains the given [element]().  <br>Content  <br>operator fun <[T](../contains.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](index.md)<[T](../contains.md)>.[contains](../contains.md)(element: [T](../contains.md)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [evert](../evert.md)| [Kotlin utilities]  <br>Brief description  <br>Moves inner [Try](../-try/index.md) outside of the outer [Option](index.md).  <br>Content  <br>fun <[T](../evert.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](index.md)<[Try](../-try/index.md)<[T](../evert.md)>>.[evert](../evert.md)(): [Try](../-try/index.md)<[Option](index.md)<[T](../evert.md)>>  <br><br><br>
| [flatten](../flatten.md)| [Kotlin utilities]  <br>Brief description  <br>Returns [Some](../-some/index.md) if this [Some](../-some/index.md) contains a [Success](../-success/index.md). Otherwise returns [None](../-none/index.md).  <br>Content  <br>fun <[T](../flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](index.md)<[Try](../-try/index.md)<[T](../flatten.md)>>.[flatten](../flatten.md)(): [Option](index.md)<[T](../flatten.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns nested [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) if this is [Some](../-some/index.md). Otherwise returns an empty [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).  <br>Content  <br>fun <[T](../flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](index.md)<[Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](../flatten.md)>>.[flatten](../flatten.md)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](../flatten.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Transforms a nested [Option](index.md) to a not nested [Option](index.md).  <br>Content  <br>fun <[T](../flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](index.md)<[Option](index.md)<[T](../flatten.md)>>.[flatten](../flatten.md)(): [Option](index.md)<[T](../flatten.md)>  <br><br><br>
| [getOrElse](../get-or-else.md)| [Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Some](../-some/index.md) or [default]() value if this is [None](../-none/index.md).  <br>Content  <br>inline fun <[T](../get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](index.md)<[T](../get-or-else.md)>.[getOrElse](../get-or-else.md)(default: () -> [T](../get-or-else.md)): [T](../get-or-else.md)  <br><br><br>
| [orElse](../or-else.md)| [Kotlin utilities]  <br>Brief description  <br>Returns this [Option](index.md) if this is a [Some](../-some/index.md) or [default]() if this is [None](../-none/index.md).  <br>Content  <br>inline fun <[T](../or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](index.md)<[T](../or-else.md)>.[orElse](../or-else.md)(default: () -> [Option](index.md)<[T](../or-else.md)>): [Option](index.md)<[T](../or-else.md)>  <br><br><br>
| [unzip](../unzip.md)| [Kotlin utilities]  <br>Brief description  <br>Transforms an [Option](index.md) of a Pair into a Pair of an [Option](index.md) of the first value and an [Option](index.md) of the second value.  <br>Content  <br>fun <[A](../unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [B](../unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](index.md)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[A](../unzip.md), [B](../unzip.md)>>.[unzip](../unzip.md)(): [Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[Option](index.md)<[A](../unzip.md)>, [Option](index.md)<[B](../unzip.md)>>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Transforms an [Option](index.md) of a Triple into a Triple of an [Option](index.md) of the first value, an [Option](index.md) of the second value, and an [Option](index.md) of the third value.  <br>Content  <br>fun <[A](../unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [B](../unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [C](../unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](index.md)<[Triple](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)<[A](../unzip.md), [B](../unzip.md), [C](../unzip.md)>>.[unzip](../unzip.md)(): [Triple](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)<[Option](index.md)<[A](../unzip.md)>, [Option](index.md)<[B](../unzip.md)>, [Option](index.md)<[C](../unzip.md)>>  <br><br><br>

