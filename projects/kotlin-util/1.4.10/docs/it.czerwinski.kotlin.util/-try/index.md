---
title: Try -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Try](index.html)



# Try  
 [common] 



Representation of an operation that might successfully return a value or throw an exception.



An instance of [Try](index.html) may be either a [Success](../-success/index.html) or a [Failure](../-failure/index.html).



This type is based on scala.util.Try.



sealed class [Try](index.html)<out [T](index.html)>   


## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| T| <br><br>Type of the value of a successful operation.<br><br>
  


## Types  
  
|  Name|  Summary| 
|---|---|
| [Companion](-companion/index.html)| [common]  <br>Content  <br>object [Companion](-companion/index.html)  <br><br><br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [equals](../-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)| [common]  <br>Content  <br>open operator override fun [equals](../-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [filter](filter.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Success](../-success/index.html) if the predicate is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>abstract fun [filter](filter.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Try](index.html)<[T](index.html)>  <br><br><br>
| [filterIsInstance](filter-is-instance.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Success](../-success/index.html) casted to type [R](filter-is-instance.html) if it is [R](filter-is-instance.html). Otherwise returns a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>inline fun <[R](filter-is-instance.html)> [filterIsInstance](filter-is-instance.html)(): [Try](index.html)<[R](filter-is-instance.html)>  <br><br><br>
| [filterNot](filter-not.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Success](../-success/index.html) if the predicate is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>abstract fun [filterNot](filter-not.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Try](index.html)<[T](index.html)>  <br><br><br>
| [filterOrElse](filter-or-else.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Success](../-success/index.html) if the predicate is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html) containing the given throwable.<br><br>  <br>Content  <br>abstract fun [filterOrElse](filter-or-else.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), throwable: ([T](index.html)) -> [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)): [Try](index.html)<[T](index.html)>  <br><br><br>
| [flatMap](flat-map.html)| [common]  <br>Brief description  <br><br><br>Maps value of a [Success](../-success/index.html) to a new [Try](index.html) using transform or returns the same [Try](index.html) if this is a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>abstract fun <[R](flat-map.html)> [flatMap](flat-map.html)(transform: ([T](index.html)) -> [Try](index.html)<[R](flat-map.html)>): [Try](index.html)<[R](flat-map.html)>  <br><br><br>
| [fold](fold.html)| [common]  <br>Brief description  <br><br><br>Transforms a [Success](../-success/index.html) using successTransform or a [Failure](../-failure/index.html) using failureTransform.<br><br>  <br>Content  <br>inline fun <[R](fold.html)> [fold](fold.html)(successTransform: ([T](index.html)) -> [R](fold.html), failureTransform: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [R](fold.html)): [R](fold.html)  <br><br><br>
| [forEach](for-each.html)| [common]  <br>Brief description  <br><br><br>Runs action if this is a [Success](../-success/index.html). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>abstract fun [forEach](for-each.html)(action: ([T](index.html)) -> [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))  <br><br><br>
| [get](get.html)| [common]  <br>Brief description  <br><br><br>Gets the value of a [Success](../-success/index.html) or throw an exception from a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>abstract fun [get](get.html)(): [T](index.html)  <br><br><br>
| [getOrNull](get-or-null.html)| [common]  <br>Brief description  <br><br><br>Gets the value of a [Success](../-success/index.html) or null if this is a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>abstract fun [getOrNull](get-or-null.html)(): [T](index.html)?  <br><br><br>
| [hashCode](../-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [hashCode](../-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| [map](map.html)| [common]  <br>Brief description  <br><br><br>Maps value of a [Success](../-success/index.html) using transform or returns the same [Try](index.html) if this is a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>abstract fun <[R](map.html)> [map](map.html)(transform: ([T](index.html)) -> [R](map.html)): [Try](index.html)<[R](map.html)>  <br><br><br>
| [toEither](to-either.html)| [common]  <br>Brief description  <br><br><br>Converts this [Try](index.html) to [Either](../-either/index.html).<br><br>  <br>Content  <br>abstract fun [toEither](to-either.html)(): [Either](../-either/index.html)<[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html), [T](index.html)>  <br><br><br>
| [toOption](to-option.html)| [common]  <br>Brief description  <br><br><br>Converts this [Try](index.html) to [Option](../-option/index.html).<br><br>  <br>Content  <br>abstract fun [toOption](to-option.html)(): [Option](../-option/index.html)<[T](index.html)>  <br><br><br>
| [toString](../-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [toString](../-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>
| [transform](transform.html)| [common]  <br>Brief description  <br><br><br>Transforms a [Success](../-success/index.html) using successTransform or a [Failure](../-failure/index.html) using failureTransform.<br><br>  <br>Content  <br>inline fun <[R](transform.html)> [transform](transform.html)(successTransform: ([T](index.html)) -> [Try](index.html)<[R](transform.html)>, failureTransform: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [Try](index.html)<[R](transform.html)>): [Try](index.html)<[R](transform.html)>  <br><br><br>
| [zip](zip.html)| [common]  <br>Brief description  <br><br><br>Returns [Success](../-success/index.html) containing a Pair of values of this and [other](index.html) if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).<br><br>  <br>Content  <br>infix fun <[R](zip.html)> [zip](zip.html)(other: [Try](index.html)<[R](zip.html)>): [Try](index.html)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.html), [R](zip.html)>>  <br><br><br>[common]  <br>Brief description  <br><br><br>Returns [Success](../-success/index.html) containing the result of applying transform to both values of this and [other](index.html) if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).<br><br>  <br>Content  <br>inline fun <[T1](zip.html), [R](zip.html)> [zip](zip.html)(other: [Try](index.html)<[T1](zip.html)>, transform: ([T](index.html), [T1](zip.html)) -> [R](zip.html)): [Try](index.html)<[R](zip.html)>  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [failed](index.html#it.czerwinski.kotlin.util/Try/failed/#/PointingToDeclaration/)|  [common] <br><br>Returns a [Success](../-success/index.html) with an exception it this is a [Failure](../-failure/index.html) or a [Failure](../-failure/index.html) if this is a [Success](../-success/index.html).<br><br>abstract val [failed](index.html#it.czerwinski.kotlin.util/Try/failed/#/PointingToDeclaration/): [Try](index.html)<[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)>   <br>
| [isFailure](index.html#it.czerwinski.kotlin.util/Try/isFailure/#/PointingToDeclaration/)|  [common] <br><br>Returns true if this is a [Failure](../-failure/index.html) or false if this is [Success](../-success/index.html).<br><br>abstract val [isFailure](index.html#it.czerwinski.kotlin.util/Try/isFailure/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isSuccess](index.html#it.czerwinski.kotlin.util/Try/isSuccess/#/PointingToDeclaration/)|  [common] <br><br>Returns true if this is a [Success](../-success/index.html) or false if this is [Failure](../-failure/index.html).<br><br>abstract val [isSuccess](index.html#it.czerwinski.kotlin.util/Try/isSuccess/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>


## Inheritors  
  
|  Name| 
|---|
| [Success](../-success/index.html)
| [Failure](../-failure/index.html)


## Extensions  
  
|  Name|  Summary| 
|---|---|
| [evert](../evert.html)| [common]  <br>Brief description  <br><br><br>Moves inner [Option](../-option/index.html) outside of the outer [Try](index.html).<br><br>  <br>Content  <br>fun <[T](../evert.html)> [Try](index.html)<[Option](../-option/index.html)<[T](../evert.html)>>.[evert](../evert.html)(): [Option](../-option/index.html)<[Try](index.html)<[T](../evert.html)>>  <br><br><br>
| [filterNotNull](../filter-not-null.html)| [common]  <br>Brief description  <br><br><br>Returns the same [Success](../-success/index.html) if its value is not null. Otherwise returns a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>fun <[T](../filter-not-null.html)> [Try](index.html)<[T](../filter-not-null.html)?>.[filterNotNull](../filter-not-null.html)(): [Try](index.html)<[T](../filter-not-null.html)>  <br><br><br>
| [flatten](../flatten.html)| [common]  <br>Brief description  <br><br><br>Extracts an [Option](../-option/index.html) nested in the [Try](index.html) to a not nested [Option](../-option/index.html).<br><br>  <br>Content  <br>fun <[T](../flatten.html)> [Try](index.html)<[Option](../-option/index.html)<[T](../flatten.html)>>.[flatten](../flatten.html)(): [Option](../-option/index.html)<[T](../flatten.html)>  <br><br><br>[common]  <br>Brief description  <br><br><br>Transforms a nested [Try](index.html) to a not nested [Try](index.html).<br><br>  <br>Content  <br>fun <[T](../flatten.html)> [Try](index.html)<[Try](index.html)<[T](../flatten.html)>>.[flatten](../flatten.html)(): [Try](index.html)<[T](../flatten.html)>  <br><br><br>
| [getOrElse](../get-or-else.html)| [common]  <br>Brief description  <br><br><br>Gets the value of a [Success](../-success/index.html) or default value if this is a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>inline fun <[T](../get-or-else.html)> [Try](index.html)<[T](../get-or-else.html)>.[getOrElse](../get-or-else.html)(default: () -> [T](../get-or-else.html)): [T](../get-or-else.html)  <br><br><br>
| [orElse](../or-else.html)| [common]  <br>Brief description  <br><br><br>Returns this [Try](index.html) if this is a [Success](../-success/index.html) or default if this is a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>inline fun <[T](../or-else.html)> [Try](index.html)<[T](../or-else.html)>.[orElse](../or-else.html)(default: () -> [Try](index.html)<[T](../or-else.html)>): [Try](index.html)<[T](../or-else.html)>  <br><br><br>
| [recover](../recover.html)| [common]  <br>Brief description  <br><br><br>Returns this [Try](index.html) if this is a [Success](../-success/index.html) or a [Try](index.html) created for the rescue operation if this is a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>inline fun <[T](../recover.html)> [Try](index.html)<[T](../recover.html)>.[recover](../recover.html)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [T](../recover.html)): [Try](index.html)<[T](../recover.html)>  <br><br><br>
| [recoverWith](../recover-with.html)| [common]  <br>Brief description  <br><br><br>Returns this [Try](index.html) if this is a [Success](../-success/index.html) or a [Try](index.html) created by the rescue function if this is a [Failure](../-failure/index.html).<br><br>  <br>Content  <br>inline fun <[T](../recover-with.html)> [Try](index.html)<[T](../recover-with.html)>.[recoverWith](../recover-with.html)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [Try](index.html)<[T](../recover-with.html)>): [Try](index.html)<[T](../recover-with.html)>  <br><br><br>

