---
title: Some -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Some](index.md)



# Some  
 [Kotlin utilities] Representation of a value of type [T]().  
  
data class [Some](index.md)<[T](index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> (**value**: [T](index.md)) : [Option](../-option/index.md)   


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| T| Type of the value.
  


## Constructors  
  
|  Name|  Summary| 
|---|---|
| [<init>](-init-.md)|  [Kotlin utilities] Type of the value.fun <[T](index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [<init>](-init-.md)(value: [T](index.md))   <br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [all](../-option/all.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the result of applying the [predicate]() to the value if this is [Some](index.md) or true if this is [None](../-none/index.md).  <br>Content  <br>inline override fun [all](../-option/all.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [any](../-option/any.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the result of applying the [predicate]() to the value if this is [Some](index.md) or false if this is [None](../-none/index.md).  <br>Content  <br>inline override fun [any](../-option/any.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [asIterable](as-iterable.md)| [Kotlin utilities]  <br>Brief description  <br>Returns an iterable that wraps this [Option](../-option/index.md) returning its value if it is defined, or an empty iterable if the option is empty.  <br>Content  <br>open override fun [asIterable](as-iterable.md)(): [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](index.md)>  <br><br><br>
| [asSequence](as-sequence.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a sequence that wraps this [Option](../-option/index.md) returning its value if it is defined, or an empty sequence if the option is empty.  <br>Content  <br>open override fun [asSequence](as-sequence.md)(): [Sequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)<[T](index.md)>  <br><br><br>
| [component1](component1.md)| [Kotlin utilities]  <br>Content  <br>operator fun [component1](component1.md)(): [T](index.md)  <br><br><br>
| [copy](copy.md)| [Kotlin utilities]  <br>Content  <br>fun [copy](copy.md)(value: [T](index.md)): [Some](index.md)<[T](index.md)>  <br><br><br>
| [equals](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/equals.html)| [Kotlin utilities]  <br>Content  <br>open operator override fun [equals](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/equals.html)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [filter](../-option/filter.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Some](index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [None](../-none/index.md).  <br>Content  <br>inline override fun [filter](../-option/filter.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.md)<[T](index.md)>  <br><br><br>
| [filterIsInstance](../-option/filter-is-instance.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Some](index.md) casted to type [R]() if it is [R](). Otherwise returns a [None](../-none/index.md).  <br>Content  <br>inline override fun <[R]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [filterIsInstance](../-option/filter-is-instance.md)(): [Option](../-option/index.md)<[R]()>  <br><br><br>
| [filterNot](../-option/filter-not.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Some](index.md) if the [predicate]() is not satisfied for the value. Otherwise returns a [None](../-none/index.md).  <br>Content  <br>inline override fun [filterNot](../-option/filter-not.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.md)<[T](index.md)>  <br><br><br>
| [flatMap](../-option/flat-map.md)| [Kotlin utilities]  <br>Brief description  <br>Maps value of a [Some](index.md) to a new [Option](../-option/index.md) using [transform]() or returns the same [None](../-none/index.md).  <br>Content  <br>inline override fun <[R]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [flatMap](../-option/flat-map.md)(transform: ([T](index.md)) -> [Option](../-option/index.md)<[R]()>): [Option](../-option/index.md)<[R]()>  <br><br><br>
| [fold](../-option/fold.md)| [Kotlin utilities]  <br>Brief description  <br>Returns result of applying [transform]() on the value of [Some](index.md) or [default]() if this is [None](../-none/index.md).  <br>Content  <br>inline override fun <[R]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [fold](../-option/fold.md)(default: [R](), transform: ([T](index.md)) -> [R]()): [R]()  <br>inline override fun <[R]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [fold](../-option/fold.md)(default: () -> [R](), transform: ([T](index.md)) -> [R]()): [R]()  <br><br><br>
| [forEach](../-option/for-each.md)| [Kotlin utilities]  <br>Brief description  <br>Runs [action]() if this is a [Some](index.md). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is [None](../-none/index.md).  <br>Content  <br>inline override fun [forEach](../-option/for-each.md)(action: ([T](index.md)) -> [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))  <br><br><br>
| [get](get.md)| [Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Some](index.md) or throws an exception.  <br>Content  <br>open override fun [get](get.md)(): [T](index.md)  <br><br><br>
| [getOrNull](get-or-null.md)| [Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Some](index.md) or null if this is a [None](../-none/index.md).  <br>Content  <br>open override fun [getOrNull](get-or-null.md)(): [T](index.md)?  <br><br><br>
| [hashCode](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/hash-code.html)| [Kotlin utilities]  <br>Content  <br>open override fun [hashCode](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/hash-code.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| [iterator](iterator.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a singleton iterator returning the option's value if it is defined, or an empty iterator if the option is empty.  <br>Content  <br>open override fun [iterator](iterator.md)(): [Iterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)<[T](index.md)>  <br><br><br>
| [map](../-option/map.md)| [Kotlin utilities]  <br>Brief description  <br>Maps value of a [Some](index.md) using [transform]() or returns the same [None](../-none/index.md).  <br>Content  <br>inline override fun <[R]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [map](../-option/map.md)(transform: ([T](index.md)) -> [R]()): [Option](../-option/index.md)<[R]()>  <br><br><br>
| [none](../-option/none.md)| [Kotlin utilities]  <br>Brief description  <br>Returns false if the [predicate]() is met by the value if this is [Some](index.md) or true otherwise.  <br>Content  <br>inline override fun [none](../-option/none.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [toLeft](../-option/to-left.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a [Right](../-right/index.md) containing the given argument [right]() if this is empty, or a [Left](../-left/index.md) containing this option's value if it is defined.  <br>Content  <br>inline override fun <[R]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [toLeft](../-option/to-left.md)(right: () -> [R]()): [Either](../-either/index.md)<[T](index.md), [R]()>  <br><br><br>
| [toList](to-list.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a singleton list containing the option's value if it is defined, or an empty list if the option is empty.  <br>Content  <br>open override fun [toList](to-list.md)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](index.md)>  <br><br><br>
| [toRight](../-option/to-right.md)| [Kotlin utilities]  <br>Brief description  <br>Returns a [Left](../-left/index.md) containing the given argument [left]() if this is empty, or a [Right](../-right/index.md) containing this option's value if it is defined.  <br>Content  <br>inline override fun <[L]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [toRight](../-option/to-right.md)(left: () -> [L]()): [Either](../-either/index.md)<[L](), [T](index.md)>  <br><br><br>
| [toString](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/to-string.html)| [Kotlin utilities]  <br>Content  <br>open override fun [toString](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/to-string.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>
| [zip](../-option/zip.md)| [Kotlin utilities]  <br>Brief description  <br>Returns [Some](index.md) containing a Pair of values of this and [other](../-option/index.md) if both [Option](../-option/index.md)s are [Some](index.md). Otherwise returns [None](../-none/index.md).  <br>Content  <br>infix override fun <[R]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](../-option/zip.md)(other: [Option](../-option/index.md)<[R]()>): [Option](../-option/index.md)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.md), [R]()>>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns [Some](index.md) containing the result of applying [transform]() to both values of this and [other](../-option/index.md) if both [Option](../-option/index.md)s are [Some](index.md). Otherwise returns [None](../-none/index.md).  <br>Content  <br>inline override fun <[T1]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R]() : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](../-option/zip.md)(other: [Option](../-option/index.md)<[T1]()>, transform: ([T](index.md), [T1]()) -> [R]()): [Option](../-option/index.md)<[R]()>  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [isDefined](index.md#it.czerwinski.kotlin.util/Some/isDefined/#/PointingToDeclaration/)|  [Kotlin utilities] Returns true if the option is [Some](index.md). Otherwise returns false.override val [isDefined](index.md#it.czerwinski.kotlin.util/Some/isDefined/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isEmpty](index.md#it.czerwinski.kotlin.util/Some/isEmpty/#/PointingToDeclaration/)|  [Kotlin utilities] Returns true if the option is [None](../-none/index.md). Otherwise returns false.open override val [isEmpty](index.md#it.czerwinski.kotlin.util/Some/isEmpty/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isNotEmpty](index.md#it.czerwinski.kotlin.util/Some/isNotEmpty/#/PointingToDeclaration/)|  [Kotlin utilities] Returns true if the option is [Some](index.md). Otherwise returns false.override val [isNotEmpty](index.md#it.czerwinski.kotlin.util/Some/isNotEmpty/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [value](index.md#it.czerwinski.kotlin.util/Some/value/#/PointingToDeclaration/)|  [Kotlin utilities] val [value](index.md#it.czerwinski.kotlin.util/Some/value/#/PointingToDeclaration/): [T](index.md)   <br>

