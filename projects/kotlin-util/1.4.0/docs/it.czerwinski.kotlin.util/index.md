---
title: it.czerwinski.kotlin.util -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)



# Package it.czerwinski.kotlin.util  
 [Kotlin utilities] Contains utility types based on Scala.  
  
   


## Types  
  
|  Name|  Summary| 
|---|---|
| [Either](-either/index.md)| [Kotlin utilities]  <br>Brief description  <br>Disjoint union. The instance might be either [Left](-left/index.md) or [Right](-right/index.md).This type is based on scala.Either.  <br>Content  <br>sealed class [Either](-either/index.md)<[L](-either/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](-either/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>   <br><br><br>
| [Failure](-failure/index.md)| [Kotlin utilities]  <br>Content  <br>data class [Failure](-failure/index.md)(**exception**: [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) : [Try](-try/index.md)  <br><br><br>
| [Left](-left/index.md)| [Kotlin utilities]  <br>Content  <br>data class [Left](-left/index.md)<[L](-left/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> (**value**: [L](-left/index.md)) : [Either](-either/index.md)  <br><br><br>
| [LeftProjection](-left-projection/index.md)| [Kotlin utilities]  <br>Content  <br>data class [LeftProjection](-left-projection/index.md)<[L](-left-projection/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](-left-projection/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> (**either**: [Either](-either/index.md)<[L](-left-projection/index.md), [R](-left-projection/index.md)>)  <br><br><br>
| [None](-none/index.md)| [Kotlin utilities]  <br>Brief description  <br>Representation of a non-existent value.  <br>Content  <br>object [None](-none/index.md) : [Option](-option/index.md)  <br><br><br>
| [Option](-option/index.md)| [Kotlin utilities]  <br>Brief description  <br>Representation of an optional value. The instance might be either [Some](-some/index.md) value or [None](-none/index.md).  <br>Content  <br>sealed class [Option](-option/index.md)<[T](-option/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>   <br><br><br>
| [Right](-right/index.md)| [Kotlin utilities]  <br>Content  <br>data class [Right](-right/index.md)<[R](-right/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> (**value**: [R](-right/index.md)) : [Either](-either/index.md)  <br><br><br>
| [RightProjection](-right-projection/index.md)| [Kotlin utilities]  <br>Content  <br>~~data~~ ~~class~~ [~~RightProjection~~](-right-projection/index.md)~~<~~[L](-right-projection/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?~~,~~ [R](-right-projection/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?~~>~~ ~~(~~~~**either**~~~~:~~ [Either](-either/index.md)<[L](-right-projection/index.md), [R](-right-projection/index.md)>~~)~~  <br><br><br>
| [Some](-some/index.md)| [Kotlin utilities]  <br>Brief description  <br>Representation of a value of type [T]().  <br>Content  <br>data class [Some](-some/index.md)<[T](-some/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> (**value**: [T](-some/index.md)) : [Option](-option/index.md)  <br><br><br>
| [Success](-success/index.md)| [Kotlin utilities]  <br>Content  <br>data class [Success](-success/index.md)<[T](-success/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> (**value**: [T](-success/index.md)) : [Try](-try/index.md)  <br><br><br>
| [Try](-try/index.md)| [Kotlin utilities]  <br>Brief description  <br>Representation of an operation that might successfully return a value or throw an exception.An instance of [Try](-try/index.md) may be either a [Success](-success/index.md) or a [Failure](-failure/index.md).This type is based on scala.util.Try.  <br>Content  <br>sealed class [Try](-try/index.md)<[T](-try/index.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>   <br><br><br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [asOption](as-option.md)| [Kotlin utilities]  <br>Brief description  <br>Returns [Some](-some/index.md) if this is not null or [None](-none/index.md) if this is null.  <br>Content  <br>fun <[T](as-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [T](as-option.md)?.[asOption](as-option.md)(): [Option](-option/index.md)<[T](as-option.md)>  <br><br><br>
| [contains](contains.md)| [Kotlin utilities]  <br>Brief description  <br>Tests whether the [Option](-option/index.md) contains the given [element]().  <br>Content  <br>operator fun <[T](contains.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[T](contains.md)>.[contains](contains.md)(element: [T](contains.md)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [evert](evert.md)| [Kotlin utilities]  <br>Brief description  <br>Moves inner [Option](-option/index.md) outside of the outer [Try](-try/index.md).  <br>Content  <br>fun <[T](evert.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[Option](-option/index.md)<[T](evert.md)>>.[evert](evert.md)(): [Option](-option/index.md)<[Try](-try/index.md)<[T](evert.md)>>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Moves inner [Try](-try/index.md) outside of the outer [Option](-option/index.md).  <br>Content  <br>fun <[T](evert.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Try](-try/index.md)<[T](evert.md)>>.[evert](evert.md)(): [Try](-try/index.md)<[Option](-option/index.md)<[T](evert.md)>>  <br><br><br>
| [filterNotNull](filter-not-null.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Right](-right/index.md) if its value is not null. Otherwise returns null.  <br>Content  <br>fun <[L](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)??>.[filterNotNull](filter-not-null.md)(): [Either](-either/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)>?  <br>fun <[L](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)??>.[filterNotNull](filter-not-null.md)(): [Either](-either/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)>?  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns the same [Left](-left/index.md) if its value is not null. Otherwise returns null.  <br>Content  <br>fun <[L](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](filter-not-null.md)??, [R](filter-not-null.md)>.[filterNotNull](filter-not-null.md)(): [Either](-either/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)>?  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns the same [Success](-success/index.md) if its value is not null. Otherwise returns a [Failure](-failure/index.md).  <br>Content  <br>fun <[T](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](filter-not-null.md)??>.[filterNotNull](filter-not-null.md)(): [Try](-try/index.md)<[T](filter-not-null.md)>  <br><br><br>
| [filterNotNullToOption](filter-not-null-to-option.md)| [Kotlin utilities]  <br>Brief description  <br>Returns [Some](-some/index.md) containing the same [Right](-right/index.md) if its value is not null. Otherwise returns [None](-none/index.md).  <br>Content  <br>fun <[L](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)??>.[filterNotNullToOption](filter-not-null-to-option.md)(): [Option](-option/index.md)<[Either](-either/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)>>  <br>fun <[L](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)??>.[filterNotNullToOption](filter-not-null-to-option.md)(): [Option](-option/index.md)<[Either](-either/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)>>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns [Some](-some/index.md) containing the same [Left](-left/index.md) if its value is not null. Otherwise returns [None](-none/index.md).  <br>Content  <br>fun <[L](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](filter-not-null-to-option.md)??, [R](filter-not-null-to-option.md)>.[filterNotNullToOption](filter-not-null-to-option.md)(): [Option](-option/index.md)<[Either](-either/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)>>  <br><br><br>
| [filterOrElse](filter-or-else.md)| [Kotlin utilities]  <br>Brief description  <br>Returns the same [Right](-right/index.md) if the [predicate]() is satisfied for the value, Left(zero) if the [predicate]() is not satisfied for the value, or the same [Left](-left/index.md) if this is [Left](-left/index.md).  <br>Content  <br>inline fun <[L](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>.[filterOrElse](filter-or-else.md)(predicate: ([R](filter-or-else.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [L](filter-or-else.md)): [Either](-either/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>?  <br>inline fun <[L](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>.[filterOrElse](filter-or-else.md)(predicate: ([R](filter-or-else.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [L](filter-or-else.md)): [Either](-either/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>?  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns the same [Left](-left/index.md) if the [predicate]() is satisfied for the value, Right(zero) if the [predicate]() is not satisfied for the value, or the same [Right](-right/index.md) if this is [Right](-right/index.md).  <br>Content  <br>inline fun <[L](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>.[filterOrElse](filter-or-else.md)(predicate: ([L](filter-or-else.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [R](filter-or-else.md)): [Either](-either/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>?  <br><br><br>
| [flatMap](flat-map.md)| [Kotlin utilities]  <br>Brief description  <br>Maps value of this [Right](-right/index.md) to a new [Either](-either/index.md) using [transform]().  <br>Content  <br>inline fun <[L](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [T](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](flat-map.md), [R](flat-map.md)>.[flatMap](flat-map.md)(transform: ([R](flat-map.md)) -> [Either](-either/index.md)<[L](flat-map.md), [T](flat-map.md)>): [Either](-either/index.md)<[L](flat-map.md), [T](flat-map.md)>  <br>inline fun <[L](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [T](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](flat-map.md), [R](flat-map.md)>.[flatMap](flat-map.md)(transform: ([R](flat-map.md)) -> [Either](-either/index.md)<[L](flat-map.md), [T](flat-map.md)>): [Either](-either/index.md)<[L](flat-map.md), [T](flat-map.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Maps value of this [Left](-left/index.md) to a new [Either](-either/index.md) using [transform]().  <br>Content  <br>inline fun <[L](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [T](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](flat-map.md), [R](flat-map.md)>.[flatMap](flat-map.md)(transform: ([L](flat-map.md)) -> [Either](-either/index.md)<[T](flat-map.md), [R](flat-map.md)>): [Either](-either/index.md)<[T](flat-map.md), [R](flat-map.md)>  <br><br><br>
| [flatten](flatten.md)| [Kotlin utilities]  <br>Brief description  <br>Extracts an [Option](-option/index.md) nested in the [Try](-try/index.md) to a not nested [Option](-option/index.md).  <br>Content  <br>fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[Option](-option/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [Option](-option/index.md)<[T](flatten.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns [Some](-some/index.md) if this [Some](-some/index.md) contains a [Success](-success/index.md). Otherwise returns [None](-none/index.md).  <br>Content  <br>fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Try](-try/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [Option](-option/index.md)<[T](flatten.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns nested [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) if this is [Some](-some/index.md). Otherwise returns an empty [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).  <br>Content  <br>fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](flatten.md)>>.[flatten](flatten.md)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](flatten.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) of values of each [Some](-some/index.md) in this [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).  <br>Content  <br>fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[Option](-option/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](flatten.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Transforms a nested [Option](-option/index.md) to a not nested [Option](-option/index.md).  <br>Content  <br>fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Option](-option/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [Option](-option/index.md)<[T](flatten.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Transforms a nested [Try](-try/index.md) to a not nested [Try](-try/index.md).  <br>Content  <br>fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[Try](-try/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [Try](-try/index.md)<[T](flatten.md)>  <br><br><br>
| [getOrElse](get-or-else.md)| [Kotlin utilities]  <br>Brief description  <br>Gets value of this [Right](-right/index.md) or [default]() value if this is [Left](-left/index.md).  <br>Content  <br>inline fun <[L](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](get-or-else.md), [R](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [R](get-or-else.md)): [R](get-or-else.md)  <br>inline fun <[L](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](get-or-else.md), [R](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [R](get-or-else.md)): [R](get-or-else.md)  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Gets value of this [Left](-left/index.md) or [default]() value if this is [Right](-right/index.md).  <br>Content  <br>inline fun <[L](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](get-or-else.md), [R](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [L](get-or-else.md)): [L](get-or-else.md)  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Some](-some/index.md) or [default]() value if this is [None](-none/index.md).  <br>Content  <br>inline fun <[T](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[T](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [T](get-or-else.md)): [T](get-or-else.md)  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Gets the value of a [Success](-success/index.md) or [default]() value if this is a [Failure](-failure/index.md).  <br>Content  <br>inline fun <[T](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [T](get-or-else.md)): [T](get-or-else.md)  <br><br><br>
| [joinLeft](join-left.md)| [Kotlin utilities]  <br>Brief description  <br>Returns this if this is [Right](-right/index.md). Otherwise returns value of [Left](-left/index.md).Requires [Left](-left/index.md) to be an [Either](-either/index.md).  <br>Content  <br>fun <[L](join-left.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](join-left.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[Either](-either/index.md)<[L](join-left.md), [R](join-left.md)>, [R](join-left.md)>.[joinLeft](join-left.md)(): [Either](-either/index.md)<[L](join-left.md), [R](join-left.md)>  <br><br><br>
| [joinRight](join-right.md)| [Kotlin utilities]  <br>Brief description  <br>Returns this if this is [Left](-left/index.md). Otherwise returns value of [Right](-right/index.md).Requires [Right](-right/index.md) to be an [Either](-either/index.md).  <br>Content  <br>fun <[L](join-right.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](join-right.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](join-right.md), [Either](-either/index.md)<[L](join-right.md), [R](join-right.md)>>.[joinRight](join-right.md)(): [Either](-either/index.md)<[L](join-right.md), [R](join-right.md)>  <br><br><br>
| [merge](merge.md)| [Kotlin utilities]  <br>Brief description  <br>Merges [Left](-left/index.md) and [Right](-right/index.md) of the same type to a single value.  <br>Content  <br>fun <[T](merge.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[T](merge.md), [T](merge.md)>.[merge](merge.md)(): [T](merge.md)  <br><br><br>
| [orElse](or-else.md)| [Kotlin utilities]  <br>Brief description  <br>Returns this [Option](-option/index.md) if this is a [Some](-some/index.md) or [default]() if this is [None](-none/index.md).  <br>Content  <br>inline fun <[T](or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[T](or-else.md)>.[orElse](or-else.md)(default: () -> [Option](-option/index.md)<[T](or-else.md)>): [Option](-option/index.md)<[T](or-else.md)>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Returns this [Try](-try/index.md) if this is a [Success](-success/index.md) or [default]() if this is a [Failure](-failure/index.md).  <br>Content  <br>inline fun <[T](or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](or-else.md)>.[orElse](or-else.md)(default: () -> [Try](-try/index.md)<[T](or-else.md)>): [Try](-try/index.md)<[T](or-else.md)>  <br><br><br>
| [recover](recover.md)| [Kotlin utilities]  <br>Brief description  <br>Returns this [Try](-try/index.md) if this is a [Success](-success/index.md) or a [Try](-try/index.md) created for the [rescue]() operation if this is a [Failure](-failure/index.md).  <br>Content  <br>inline fun <[T](recover.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](recover.md)>.[recover](recover.md)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [T](recover.md)): [Try](-try/index.md)<[T](recover.md)>  <br><br><br>
| [recoverWith](recover-with.md)| [Kotlin utilities]  <br>Brief description  <br>Returns this [Try](-try/index.md) if this is a [Success](-success/index.md) or a [Try](-try/index.md) created by the [rescue]() function if this is a [Failure](-failure/index.md).  <br>Content  <br>inline fun <[T](recover-with.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](recover-with.md)>.[recoverWith](recover-with.md)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [Try](-try/index.md)<[T](recover-with.md)>): [Try](-try/index.md)<[T](recover-with.md)>  <br><br><br>
| [unzip](unzip.md)| [Kotlin utilities]  <br>Brief description  <br>Transforms an [Option](-option/index.md) of a Pair into a Pair of an [Option](-option/index.md) of the first value and an [Option](-option/index.md) of the second value.  <br>Content  <br>fun <[A](unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [B](unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[A](unzip.md), [B](unzip.md)>>.[unzip](unzip.md)(): [Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[Option](-option/index.md)<[A](unzip.md)>, [Option](-option/index.md)<[B](unzip.md)>>  <br><br><br>[Kotlin utilities]  <br>Brief description  <br>Transforms an [Option](-option/index.md) of a Triple into a Triple of an [Option](-option/index.md) of the first value, an [Option](-option/index.md) of the second value, and an [Option](-option/index.md) of the third value.  <br>Content  <br>fun <[A](unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [B](unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [C](unzip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Triple](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)<[A](unzip.md), [B](unzip.md), [C](unzip.md)>>.[unzip](unzip.md)(): [Triple](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)<[Option](-option/index.md)<[A](unzip.md)>, [Option](-option/index.md)<[B](unzip.md)>, [Option](-option/index.md)<[C](unzip.md)>>  <br><br><br>
