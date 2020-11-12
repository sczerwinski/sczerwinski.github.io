---
title: Try -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Try](index.md)



# Try  
 [Kotlin utilities] Representation of an operation that might successfully return a value or throw an exception.An instance of [Try](index.md) may be either a [Success](../-success/index.md) or a [Failure](../-failure/index.md).This type is based on scala.util.Try.  
  
sealed class [Try](index.md)<[T](index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>    


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| T| Type of the value of a successful operation.
  


## Types  
  
|  Name|  Summary| 
|---|---|
| [Companion](-companion/index.md)| [Kotlin utilities]  <br>Content  <br>object [Companion](-companion/index.md)  <br><br><br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [equals](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/equals.html)| [Kotlin utilities]  <br>Content  <br>open operator override fun [equals](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/equals.html)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [filter](filter.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Success](../-success/index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [Failure](../-failure/index.md).  <br>Content  <br>abstract fun [filter](filter.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Try](index.md)<[T](index.md)>  <br><br><br>
| [filterIsInstance](filter-is-instance.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Success](../-success/index.md) casted to type [R]() if it is [R](). Otherwise returns a [Failure](../-failure/index.md).  <br>Content  <br>inline fun <[R](filter-is-instance.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [filterIsInstance](filter-is-instance.md)(): [Try](index.md)<[R](filter-is-instance.md)>  <br><br><br>
| [filterNot](filter-not.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Success](../-success/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.md).  <br>Content  <br>abstract fun [filterNot](filter-not.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Try](index.md)<[T](index.md)>  <br><br><br>
| [filterOrElse](filter-or-else.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Success](../-success/index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [Failure](../-failure/index.md) containing the given [throwable]().  <br>Content  <br>abstract fun [filterOrElse](filter-or-else.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), throwable: ([T](index.md)) -> [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)): [Try](index.md)<[T](index.md)>  <br><br><br>
| [flatMap](flat-map.md)| [Kotlin utilities]  <br>Brief description  <br>Maps value of a [Success](../-success/index.md) to a new [Try](index.md) using [transform]() or returns the same [Try](index.md) if this is a [Failure](../-failure/index.md).  <br>Content  <br>abstract fun <[R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [flatMap](flat-map.md)(transform: ([T](index.md)) -> [Try](index.md)<[R](flat-map.md)>): [Try](index.md)<[R](flat-map.md)>  <br><br><br>
| [fold](fold.md)| [Kotlin utilities]  <br>Brief description  <br>Transforms a [Success](../-success/index.md) using [successTransform]() or a [Failure](../-failure/index.md) using [failureTransform]().  <br>Content  <br>inline fun <[R](fold.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [fold](fold.md)(successTransform: ([T](index.md)) -> [R](fold.md), failureTransform: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [R](fold.md)): [R](fold.md)  <br><br><br>
| [forEach](for-each.md)| [Kotlin utilities]  <br>Brief description  <br>Runs [action]() if this is a [Success](../-success/index.md). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Failure](../-failure/index.md).  <br>Content  <br>abstract fun [forEach](for-each.md)(action: ([T](index.md)) -> [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))  <br><br><br>
| [get](get.md)| [Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Success](../-success/index.md) or throw an exception from a [Failure](../-failure/index.md).  <br>Content  <br>abstract fun [get](get.md)(): [T](index.md)  <br><br><br>
| [getOrNull](get-or-null.md)| [Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Success](../-success/index.md) or null if this is a [Failure](../-failure/index.md).  <br>Content  <br>abstract fun [getOrNull](get-or-null.md)(): [T](index.md)?  <br><br><br>
| [hashCode](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/hash-code.html)| [Kotlin utilities]  <br>Content  <br>open override fun [hashCode](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/hash-code.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| [map](map.md)| [Kotlin utilities]  <br>Brief description  <br>Maps value of a [Success](../-success/index.md) using [transform]() or returns the same [Try](index.md) if this is a [Failure](../-failure/index.md).  <br>Content  <br>abstract fun <[R](map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [map](map.md)(transform: ([T](index.md)) -> [R](map.md)): [Try](index.md)<[R](map.md)>  <br><br><br>
| [toEither](to-either.md)| [Kotlin utilities]  <br>Brief description  <br>Converts this [Try](index.md) to [Either](../-either/index.md).  <br>Content  <br>abstract fun [toEither](to-either.md)(): [Either](../-either/index.md)<[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html), [T](index.md)>  <br><br><br>
| [toOption](to-option.md)| [Kotlin utilities]  <br>Brief description  <br>Converts this [Try](index.md) to [Option](../-option/index.md).  <br>Content  <br>abstract fun [toOption](to-option.md)(): [Option](../-option/index.md)<[T](index.md)>  <br><br><br>
| [toString](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/to-string.html)| [Kotlin utilities]  <br>Content  <br>open override fun [toString](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/to-string.html)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>
| [transform](transform.md)| [Kotlin utilities]  <br>Brief description  <br>Transforms a [Success](../-success/index.md) using [successTransform]() or a [Failure](../-failure/index.md) using [failureTransform]().  <br>Content  <br>inline fun <[R](transform.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [transform](transform.md)(successTransform: ([T](index.md)) -> [Try](index.md)<[R](transform.md)>, failureTransform: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [Try](index.md)<[R](transform.md)>): [Try](index.md)<[R](transform.md)>  <br><br><br>
| [zip](zip.md)| [Kotlin utilities]  <br>Brief description  <br>Returns [Success](../-success/index.md) containing a Pair of values of this and [other](index.md) if both instances of [Try](index.md) are [Success](../-success/index.md). Otherwise returns first [Failure](../-failure/index.md).  <br>Content  <br>infix fun <[R](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](zip.md)(other: [Try](index.md)<[R](zip.md)>): [Try](index.md)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.md), [R](zip.md)>>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns [Success](../-success/index.md) containing the result of applying [transform]() to both values of this and [other](index.md) if both instances of [Try](index.md) are [Success](../-success/index.md). Otherwise returns first [Failure](../-failure/index.md).  <br>Content  <br>inline fun <[T1](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](zip.md)(other: [Try](index.md)<[T1](zip.md)>, transform: ([T](index.md), [T1](zip.md)) -> [R](zip.md)): [Try](index.md)<[R](zip.md)>  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| [failed](index.md#it.czerwinski.kotlin.util/Try/failed/#/PointingToDeclaration/)|  [Kotlin utilities] Returns a [Success](../-success/index.md) with an exception it this is a [Failure](../-failure/index.md) or a [Failure](../-failure/index.md) if this is a [Success](../-success/index.md).abstract val [failed](index.md#it.czerwinski.kotlin.util/Try/failed/#/PointingToDeclaration/): [Try](index.md)<[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)>   <br>
| [isFailure](index.md#it.czerwinski.kotlin.util/Try/isFailure/#/PointingToDeclaration/)|  [Kotlin utilities] Returns true if this is a [Failure](../-failure/index.md) or false if this is [Success](../-success/index.md).abstract val [isFailure](index.md#it.czerwinski.kotlin.util/Try/isFailure/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>
| [isSuccess](index.md#it.czerwinski.kotlin.util/Try/isSuccess/#/PointingToDeclaration/)|  [Kotlin utilities] Returns true if this is a [Success](../-success/index.md) or false if this is [Failure](../-failure/index.md).abstract val [isSuccess](index.md#it.czerwinski.kotlin.util/Try/isSuccess/#/PointingToDeclaration/): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)   <br>


## Inheritors  
  
|  Name| 
|---|
| [Success](../-success/index.md)
| [Failure](../-failure/index.md)


## Extensions  
  
|  Name|  Summary| 
|---|---|
| [evert](../evert.md)| [Kotlin utilities]  <br>Brief description  <br>Moves inner [Option](../-option/index.md) outside of the outer [Try](index.md).  <br>Content  <br>fun <[T](../evert.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](index.md)<[Option](../-option/index.md)<[T](../evert.md)>>.[evert](../evert.md)(): [Option](../-option/index.md)<[Try](index.md)<[T](../evert.md)>>  <br><br><br>
| [filterNotNull](../filter-not-null.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Success](../-success/index.md) if its value is not null. Otherwise returns a [Failure](../-failure/index.md).  <br>Content  <br>fun <[T](../filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](index.md)<[T](../filter-not-null.md)??>.[filterNotNull](../filter-not-null.md)(): [Try](index.md)<[T](../filter-not-null.md)>  <br><br><br>
| [flatten](../flatten.md)| [Kotlin utilities]  <br>Brief description  <br>Extracts an [Option](../-option/index.md) nested in the [Try](index.md) to a not nested [Option](../-option/index.md).  <br>Content  <br>fun <[T](../flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](index.md)<[Option](../-option/index.md)<[T](../flatten.md)>>.[flatten](../flatten.md)(): [Option](../-option/index.md)<[T](../flatten.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Transforms a nested [Try](index.md) to a not nested [Try](index.md).  <br>Content  <br>fun <[T](../flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](index.md)<[Try](index.md)<[T](../flatten.md)>>.[flatten](../flatten.md)(): [Try](index.md)<[T](../flatten.md)>  <br><br><br>
| [getOrElse](../get-or-else.md)| [Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Success](../-success/index.md) or [default]() value if this is a [Failure](../-failure/index.md).  <br>Content  <br>inline fun <[T](../get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](index.md)<[T](../get-or-else.md)>.[getOrElse](../get-or-else.md)(default: () -> [T](../get-or-else.md)): [T](../get-or-else.md)  <br><br><br>
| [orElse](../or-else.md)| [Kotlin utilities]  <br>Brief description  <br>Returns this [Try](index.md) if this is a [Success](../-success/index.md) or [default]() if this is a [Failure](../-failure/index.md).  <br>Content  <br>inline fun <[T](../or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](index.md)<[T](../or-else.md)>.[orElse](../or-else.md)(default: () -> [Try](index.md)<[T](../or-else.md)>): [Try](index.md)<[T](../or-else.md)>  <br><br><br>
| [recover](../recover.md)| [Kotlin utilities]  <br>Brief description  <br>Returns this [Try](index.md) if this is a [Success](../-success/index.md) or a [Try](index.md) created for the [rescue]() operation if this is a [Failure](../-failure/index.md).  <br>Content  <br>inline fun <[T](../recover.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](index.md)<[T](../recover.md)>.[recover](../recover.md)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [T](../recover.md)): [Try](index.md)<[T](../recover.md)>  <br><br><br>
| [recoverWith](../recover-with.md)| [Kotlin utilities]  <br>Brief description  <br>Returns this [Try](index.md) if this is a [Success](../-success/index.md) or a [Try](index.md) created by the [rescue]() function if this is a [Failure](../-failure/index.md).  <br>Content  <br>inline fun <[T](../recover-with.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](index.md)<[T](../recover-with.md)>.[recoverWith](../recover-with.md)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [Try](index.md)<[T](../recover-with.md)>): [Try](index.md)<[T](../recover-with.md)>  <br><br><br>

