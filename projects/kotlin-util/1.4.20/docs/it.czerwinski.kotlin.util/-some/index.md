---
title: Some -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Some](index.html)



# Some  
 [common] 

Representation of a value of type [T](index.html).

data class [Some](index.html)<[T](index.html)>(**value**: [T](index.html)) : [Option](../-option/index.html)<[T](index.html)>    


## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| T| <br><br>Type of the value.<br><br>
  


## Constructors  
  
|  Name|  Summary| 
|---|---|
| [Some](-some.html)|  [common] <br><br>Type of the value.<br><br>fun <[T](index.html)> [Some](-some.html)(value: [T](index.html))   <br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [all](../-option/all.html)| [common]  <br>Brief description  <br><br><br>Returns the result of applying the predicate to the value if this is [Some](index.html) or true if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun [all](../-option/all.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [any](../-option/any.html)| [common]  <br>Brief description  <br><br><br>Returns the result of applying the predicate to the value if this is [Some](index.html) or false if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun [any](../-option/any.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [asIterable](as-iterable.html)| [common]  <br>Brief description  <br><br><br>Returns an iterable that wraps this [Option](../-option/index.html) returning its value if it is defined, or an empty iterable if the option is empty.<br><br>  <br>Content  <br>open override fun [asIterable](as-iterable.html)(): [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](index.html)>  <br><br><br>
| [asSequence](as-sequence.html)| [common]  <br>Brief description  <br><br><br>Returns a sequence that wraps this [Option](../-option/index.html) returning its value if it is defined, or an empty sequence if the option is empty.<br><br>  <br>Content  <br>open override fun [asSequence](as-sequence.html)(): [Sequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)<[T](index.html)>  <br><br><br>
| [component1](component1.html)| [common]  <br>Content  <br>operator fun [component1](component1.html)(): [T](index.html)  <br><br><br>
| [copy](copy.html)| [common]  <br>Content  <br>fun [copy](copy.html)(value: [T](index.html)): [Some](index.html)<[T](index.html)>  <br><br><br>
| [equals](../-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)| [common]  <br>Content  <br>open operator override fun [equals](../-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [filter](../-option/filter.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Some](index.html) if the predicate is satisfied for the value. Otherwise returns a [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun [filter](../-option/filter.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.html)<[T](index.html)>  <br><br><br>
| [filterIsInstance](../-option/filter-is-instance.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Some](index.html) casted to type R if it is R. Otherwise returns a [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun <R> [filterIsInstance](../-option/filter-is-instance.html)(): [Option](../-option/index.html)<R>  <br><br><br>
| [filterNot](../-option/filter-not.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Some](index.html) if the predicate is not satisfied for the value. Otherwise returns a [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun [filterNot](../-option/filter-not.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.html)<[T](index.html)>  <br><br><br>
| [flatMap](../-option/flat-map.html)| [common]  <br>Brief description  <br><br><br>Maps value of a [Some](index.html) to a new [Option](../-option/index.html) using transform or returns the same [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun <R> [flatMap](../-option/flat-map.html)(transform: ([T](index.html)) -> [Option](../-option/index.html)<R>): [Option](../-option/index.html)<R>  <br><br><br>
| [fold](../-option/fold.html)| [common]  <br>Brief description  <br><br><br>Returns result of applying transform on the value of [Some](index.html) or default if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun <R> [fold](../-option/fold.html)(default: R, transform: ([T](index.html)) -> R): R  <br>inline override fun <R> [fold](../-option/fold.html)(default: () -> R, transform: ([T](index.html)) -> R): R  <br><br><br>
| [forEach](../-option/for-each.html)| [common]  <br>Brief description  <br><br><br>Runs action if this is a [Some](index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun [forEach](../-option/for-each.html)(action: ([T](index.html)) -> [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))  <br><br><br>
| [get](get.html)| [common]  <br>Brief description  <br><br><br>Gets the value of a [Some](index.html) or throws an exception.<br><br>  <br>Content  <br>open override fun [get](get.html)(): [T](index.html)  <br><br><br>
| [getOrNull](get-or-null.html)| [common]  <br>Brief description  <br><br><br>Gets the value of a [Some](index.html) or null if this is a [None](../-none/index.html).<br><br>  <br>Content  <br>open override fun [getOrNull](get-or-null.html)(): [T](index.html)?  <br><br><br>
| [hashCode](../-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [hashCode](../-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| [iterator](iterator.html)| [common]  <br>Brief description  <br><br><br>Returns a singleton iterator returning the option's value if it is defined, or an empty iterator if the option is empty.<br><br>  <br>Content  <br>open override fun [iterator](iterator.html)(): [Iterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)<[T](index.html)>  <br><br><br>
| [map](../-option/map.html)| [common]  <br>Brief description  <br><br><br>Maps value of a [Some](index.html) using transform or returns the same [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun <R> [map](../-option/map.html)(transform: ([T](index.html)) -> R): [Option](../-option/index.html)<R>  <br><br><br>
| [none](../-option/none.html)| [common]  <br>Brief description  <br><br><br>Returns false if the predicate is met by the value if this is [Some](index.html) or true otherwise.<br><br>  <br>Content  <br>inline override fun [none](../-option/none.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [toLeft](../-option/to-left.html)| [common]  <br>Brief description  <br><br><br>Returns a [Right](../-right/index.html) containing the given argument right if this is empty, or a [Left](../-left/index.html) containing this option's value if it is defined.<br><br>  <br>Content  <br>inline override fun <R> [toLeft](../-option/to-left.html)(right: () -> R): [Either](../-either/index.html)<[T](index.html), R>  <br><br><br>
| [toList](to-list.html)| [common]  <br>Brief description  <br><br><br>Returns a singleton list containing the option's value if it is defined, or an empty list if the option is empty.<br><br>  <br>Content  <br>open override fun [toList](to-list.html)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](index.html)>  <br><br><br>
| [toRight](../-option/to-right.html)| [common]  <br>Brief description  <br><br><br>Returns a [Left](../-left/index.html) containing the given argument left if this is empty, or a [Right](../-right/index.html) containing this option's value if it is defined.<br><br>  <br>Content  <br>inline override fun <L> [toRight](../-option/to-right.html)(left: () -> L): [Either](../-either/index.html)<L, [T](index.html)>  <br><br><br>
| [toString](../-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [toString](../-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>
| [zip](../-option/zip.html)| [common]  <br>Brief description  <br><br><br>Returns [Some](index.html) containing a Pair of values of this and [other](../-option/index.html) if both [Option](../-option/index.html)s are [Some](index.html). Otherwise returns [None](../-none/index.html).<br><br>  <br>Content  <br>infix override fun <R> [zip](../-option/zip.html)(other: [Option](../-option/index.html)<R>): [Option](../-option/index.html)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.html), R>>  <br><br><br>[common]  <br>Brief description  <br><br><br>Returns [Some](index.html) containing the result of applying transform to both values of this and [other](../-option/index.html) if both [Option](../-option/index.html)s are [Some](index.html). Otherwise returns [None](../-none/index.html).<br><br>  <br>Content  <br>inline override fun <T1, R> [zip](../-option/zip.html)(other: [Option](../-option/index.html)<T1>, transform: ([T](index.html), T1) -> R): [Option](../-option/index.html)<R>  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [isDefined](index.html#it.czerwinski.kotlin.util/Some/isDefined/#/PointingToDeclaration/)|  [common] <br><br>Returns true if the option is [Some](index.html). Otherwise returns false.<br><br>override val [isDefined](index.html#it.czerwinski.kotlin.util/Some/isDefined/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isEmpty](index.html#it.czerwinski.kotlin.util/Some/isEmpty/#/PointingToDeclaration/)|  [common] <br><br>Returns true if the option is [None](../-none/index.html). Otherwise returns false.<br><br>open override val [isEmpty](index.html#it.czerwinski.kotlin.util/Some/isEmpty/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isNotEmpty](index.html#it.czerwinski.kotlin.util/Some/isNotEmpty/#/PointingToDeclaration/)|  [common] <br><br>Returns true if the option is [Some](index.html). Otherwise returns false.<br><br>override val [isNotEmpty](index.html#it.czerwinski.kotlin.util/Some/isNotEmpty/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [value](index.html#it.czerwinski.kotlin.util/Some/value/#/PointingToDeclaration/)|  [common] val [value](index.html#it.czerwinski.kotlin.util/Some/value/#/PointingToDeclaration/): [T](index.html)   <br>

