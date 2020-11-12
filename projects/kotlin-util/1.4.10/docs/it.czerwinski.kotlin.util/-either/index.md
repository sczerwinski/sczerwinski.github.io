---
title: Either -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Either](index.html)



# Either  
 [common] 



Disjoint union. The instance might be either [Left](../-left/index.html) or [Right](../-right/index.html).



This type is based on scala.Either.



sealed class [Either](index.html)<out [L](index.html), out [R](index.html)>   


## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| L| <br><br>Type of [Left](../-left/index.html)<br><br>
| R| <br><br>Type of [Right](../-right/index.html)<br><br>
  


## Functions  
  
|  Name|  Summary| 
|---|---|
| [all](all.html)| [common]  <br>Brief description  <br><br><br>Returns the result of applying the predicate to the value if this is [Right](../-right/index.html) or true if this is [Left](../-left/index.html).<br><br>  <br>Content  <br>inline fun [all](all.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [any](any.html)| [common]  <br>Brief description  <br><br><br>Returns the result of applying the predicate to the value if this is [Right](../-right/index.html) or false if this is [Left](../-left/index.html).<br><br>  <br>Content  <br>inline fun [any](any.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [contains](contains.html)| [common]  <br>Brief description  <br><br><br>Returns true if the element is equal to the value of this [Either](index.html), or false otherwise.<br><br>  <br>Content  <br>abstract operator fun [contains](contains.html)(element: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [equals](../-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)| [common]  <br>Content  <br>open operator override fun [equals](../-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [filter](filter.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Right](../-right/index.html) if the predicate is satisfied for the value. Otherwise returns null.<br><br>  <br>Content  <br>inline fun [filter](filter.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Either](index.html)<[L](index.html), [R](index.html)>?  <br><br><br>
| [filterIsInstance](filter-is-instance.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Right](../-right/index.html) casted to type [T](filter-is-instance.html) if it is [T](filter-is-instance.html). Otherwise returns null.<br><br>  <br>Content  <br>inline fun <[T](filter-is-instance.html)> [filterIsInstance](filter-is-instance.html)(): [Either](index.html)<[L](index.html), [T](filter-is-instance.html)>?  <br><br><br>
| [filterIsInstanceToOption](filter-is-instance-to-option.html)| [common]  <br>Brief description  <br><br><br>Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) casted to type [T](filter-is-instance-to-option.html) if it is [T](filter-is-instance-to-option.html). Otherwise returns [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun <[T](filter-is-instance-to-option.html)> [filterIsInstanceToOption](filter-is-instance-to-option.html)(): [Option](../-option/index.html)<[Either](index.html)<[L](index.html), [T](filter-is-instance-to-option.html)>>  <br><br><br>
| [filterNot](filter-not.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Right](../-right/index.html) if the predicate is not satisfied for the value. Otherwise returns null.<br><br>  <br>Content  <br>inline fun [filterNot](filter-not.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Either](index.html)<[L](index.html), [R](index.html)>?  <br><br><br>
| [filterNotToOption](filter-not-to-option.html)| [common]  <br>Brief description  <br><br><br>Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) if the predicate is not satisfied for the value. Otherwise returns [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun [filterNotToOption](filter-not-to-option.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.html)<[Either](index.html)<[L](index.html), [R](index.html)>>  <br><br><br>
| [filterToOption](filter-to-option.html)| [common]  <br>Brief description  <br><br><br>Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) if the predicate is satisfied for the value. Otherwise returns [None](../-none/index.html).<br><br>  <br>Content  <br>inline fun [filterToOption](filter-to-option.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.html)<[Either](index.html)<[L](index.html), [R](index.html)>>  <br><br><br>
| [fold](fold.html)| [common]  <br>Brief description  <br><br><br>Transforms [Left](../-left/index.html) with leftTransform or [Right](../-right/index.html) with rightTransform.<br><br>  <br>Content  <br>inline fun <[T](fold.html)> [fold](fold.html)(leftTransform: ([L](index.html)) -> [T](fold.html), rightTransform: ([R](index.html)) -> [T](fold.html)): [T](fold.html)  <br><br><br>
| [forEach](for-each.html)| [common]  <br>Brief description  <br><br><br>Runs action if this is a [Right](../-right/index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Left](../-left/index.html).<br><br>  <br>Content  <br>inline fun [forEach](for-each.html)(action: ([R](index.html)) -> [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))  <br><br><br>
| [get](get.html)| [common]  <br>Brief description  <br><br><br>Gets value of this [Right](../-right/index.html).<br><br>  <br>Content  <br>fun [get](get.html)(): [R](index.html)  <br><br><br>
| [getOrNull](get-or-null.html)| [common]  <br>Brief description  <br><br><br>Gets value of this [Right](../-right/index.html) or null if this is [Left](../-left/index.html).<br><br>  <br>Content  <br>fun [getOrNull](get-or-null.html)(): [R](index.html)?  <br><br><br>
| [hashCode](../-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [hashCode](../-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| [map](map.html)| [common]  <br>Brief description  <br><br><br>Maps value of this [Right](../-right/index.html) using transform.<br><br>  <br>Content  <br>inline fun <[T](map.html)> [map](map.html)(transform: ([R](index.html)) -> [T](map.html)): [Either](index.html)<[L](index.html), [T](map.html)>  <br><br><br>
| [none](none.html)| [common]  <br>Brief description  <br><br><br>Returns false if the predicate is met by the value if this is [Right](../-right/index.html) or true otherwise.<br><br>  <br>Content  <br>inline fun [none](none.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [swap](swap.html)| [common]  <br>Brief description  <br><br><br>Swaps [Left](../-left/index.html) to [Right](../-right/index.html) and [Right](../-right/index.html) to [Left](../-left/index.html).<br><br>  <br>Content  <br>abstract fun [swap](swap.html)(): [Either](index.html)<[R](index.html), [L](index.html)>  <br><br><br>
| [toOption](to-option.html)| [common]  <br>Brief description  <br><br><br>Returns a [Some](../-some/index.html) containing the [Right](../-right/index.html) value if it exists, or a [None](../-none/index.html) if this is a [Left](../-left/index.html).<br><br>  <br>Content  <br>fun [toOption](to-option.html)(): [Option](../-option/index.html)<[R](index.html)>  <br><br><br>
| [toString](../-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [toString](../-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [isLeft](index.html#it.czerwinski.kotlin.util/Either/isLeft/#/PointingToDeclaration/)|  [common] <br><br>Returns true if this is a [Left](../-left/index.html) or false if this is [Right](../-right/index.html).<br><br>abstract val [isLeft](index.html#it.czerwinski.kotlin.util/Either/isLeft/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isRight](index.html#it.czerwinski.kotlin.util/Either/isRight/#/PointingToDeclaration/)|  [common] <br><br>Returns true if this is a [Right](../-right/index.html) or false if this is [Left](../-left/index.html).<br><br>abstract val [isRight](index.html#it.czerwinski.kotlin.util/Either/isRight/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [left](index.html#it.czerwinski.kotlin.util/Either/left/#/PointingToDeclaration/)|  [common] <br><br>Projects [Either](index.html) as [Left](../-left/index.html).<br><br>val [left](index.html#it.czerwinski.kotlin.util/Either/left/#/PointingToDeclaration/): [LeftProjection](../-left-projection/index.html)<[L](index.html), [R](index.html)>   <br>
| [right](index.html#it.czerwinski.kotlin.util/Either/right/#/PointingToDeclaration/)|  [common] <br><br><br><br>Projects [Either](index.html) as [Right](../-right/index.html).<br><br><br><br>Deprecated in 1.3. [Either](index.html) is right-biased. All methods from [RightProjection](../-right-projection/index.html) should be called directly on [Either](index.html).<br><br><br><br>~~val~~ [~~right~~](index.html#it.czerwinski.kotlin.util/Either/right/#/PointingToDeclaration/)~~:~~ [RightProjection](../-right-projection/index.html)<[L](index.html), [R](index.html)>   <br>


## Inheritors  
  
|  Name| 
|---|
| [Left](../-left/index.html)
| [Right](../-right/index.html)


## Extensions  
  
|  Name|  Summary| 
|---|---|
| [filterNotNull](../filter-not-null.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Right](../-right/index.html) if its value is not null. Otherwise returns null.<br><br>  <br>Content  <br>fun <[L](../filter-not-null.html), [R](../filter-not-null.html)> [Either](index.html)<[L](../filter-not-null.html), [R](../filter-not-null.html)?>.[filterNotNull](../filter-not-null.html)(): [Either](index.html)<[L](../filter-not-null.html), [R](../filter-not-null.html)>?  <br><br><br>
| [filterNotNullToOption](../filter-not-null-to-option.html)| [common]  <br>Brief description  <br><br><br>Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) if its value is not null. Otherwise returns [None](../-none/index.html).<br><br>  <br>Content  <br>fun <[L](../filter-not-null-to-option.html), [R](../filter-not-null-to-option.html)> [Either](index.html)<[L](../filter-not-null-to-option.html), [R](../filter-not-null-to-option.html)?>.[filterNotNullToOption](../filter-not-null-to-option.html)(): [Option](../-option/index.html)<[Either](index.html)<[L](../filter-not-null-to-option.html), [R](../filter-not-null-to-option.html)>>  <br><br><br>
| [filterOrElse](../filter-or-else.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Right](../-right/index.html) if the predicate is satisfied for the value, Left(zero) if the predicate is not satisfied for the value, or the same [Left](../-left/index.html) if this is [Left](../-left/index.html).<br><br>  <br>Content  <br>inline fun <[L](../filter-or-else.html), [R](../filter-or-else.html)> [Either](index.html)<[L](../filter-or-else.html), [R](../filter-or-else.html)>.[filterOrElse](../filter-or-else.html)(predicate: ([R](../filter-or-else.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [L](../filter-or-else.html)): [Either](index.html)<[L](../filter-or-else.html), [R](../filter-or-else.html)>?  <br><br><br>
| [flatMap](../flat-map.html)| [common]  <br>Brief description  <br><br><br>Maps value of this [Right](../-right/index.html) to a new [Either](index.html) using transform.<br><br>  <br>Content  <br>inline fun <[L](../flat-map.html), [R](../flat-map.html), [T](../flat-map.html)> [Either](index.html)<[L](../flat-map.html), [R](../flat-map.html)>.[flatMap](../flat-map.html)(transform: ([R](../flat-map.html)) -> [Either](index.html)<[L](../flat-map.html), [T](../flat-map.html)>): [Either](index.html)<[L](../flat-map.html), [T](../flat-map.html)>  <br><br><br>
| [getOrElse](../get-or-else.html)| [common]  <br>Brief description  <br><br><br>Gets value of this [Right](../-right/index.html) or default value if this is [Left](../-left/index.html).<br><br>  <br>Content  <br>inline fun <[L](../get-or-else.html), [R](../get-or-else.html)> [Either](index.html)<[L](../get-or-else.html), [R](../get-or-else.html)>.[getOrElse](../get-or-else.html)(default: () -> [R](../get-or-else.html)): [R](../get-or-else.html)  <br><br><br>
| [joinLeft](../join-left.html)| [common]  <br>Brief description  <br><br><br><br><br>Returns this if this is [Right](../-right/index.html). Otherwise returns value of [Left](../-left/index.html).<br><br><br><br>Requires [Left](../-left/index.html) to be an [Either](index.html).<br><br><br><br>  <br>Content  <br>fun <[L](../join-left.html), [R](../join-left.html)> [Either](index.html)<[Either](index.html)<[L](../join-left.html), [R](../join-left.html)>, [R](../join-left.html)>.[joinLeft](../join-left.html)(): [Either](index.html)<[L](../join-left.html), [R](../join-left.html)>  <br><br><br>
| [joinRight](../join-right.html)| [common]  <br>Brief description  <br><br><br><br><br>Returns this if this is [Left](../-left/index.html). Otherwise returns value of [Right](../-right/index.html).<br><br><br><br>Requires [Right](../-right/index.html) to be an [Either](index.html).<br><br><br><br>  <br>Content  <br>fun <[L](../join-right.html), [R](../join-right.html)> [Either](index.html)<[L](../join-right.html), [Either](index.html)<[L](../join-right.html), [R](../join-right.html)>>.[joinRight](../join-right.html)(): [Either](index.html)<[L](../join-right.html), [R](../join-right.html)>  <br><br><br>
| [merge](../merge.html)| [common]  <br>Brief description  <br><br><br>Merges [Left](../-left/index.html) and [Right](../-right/index.html) of the same type to a single value.<br><br>  <br>Content  <br>fun <[T](../merge.html)> [Either](index.html)<[T](../merge.html), [T](../merge.html)>.[merge](../merge.html)(): [T](../merge.html)  <br><br><br>

