---
title: filterOrElse -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[filterOrElse](filter-or-else.md)



# filterOrElse  
[Kotlin utilities]  
Brief description  
Returns the same [Right](-right/index.md) if the [predicate]() is satisfied for the value, Left(zero) if the [predicate]() is not satisfied for the value, or the same [Left](-left/index.md) if this is [Left](-left/index.md).  
  


#### Return  
The same [Right](-right/index.md) if the [predicate]() is satisfied for the value, Left(zero) if the [predicate]() is not satisfied for the value, or the same [Left](-left/index.md) if this is [Left](-left/index.md).  
  


#### Since  
1.3  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
| zero| Provider of the value used if the [predicate]() is not satisfied.
  
  
Content  
inline fun <[L](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>.[filterOrElse](filter-or-else.md)(predicate: ([R](filter-or-else.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [L](filter-or-else.md)): [Either](-either/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>?  


[Kotlin utilities]  
Brief description  
Returns the same [Left](-left/index.md) if the [predicate]() is satisfied for the value, Right(zero) if the [predicate]() is not satisfied for the value, or the same [Right](-right/index.md) if this is [Right](-right/index.md).  
  


#### Return  
The same [Left](-left/index.md) if the [predicate]() is satisfied for the value, Right(zero) if the [predicate]() is not satisfied for the value, or the same [Right](-right/index.md) if this is [Right](-right/index.md).  
  


#### Since  
1.2  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
| zero| Provider of the value used if the [predicate]() is not satisfied.
  
  
Content  
inline fun <[L](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>.[filterOrElse](filter-or-else.md)(predicate: ([L](filter-or-else.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [R](filter-or-else.md)): [Either](-either/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>?  


[Kotlin utilities]  
Brief description  
Returns the same [Right](-right/index.md) if the [predicate]() is satisfied for the value, Left(zero) if the [predicate]() is not satisfied for the value, or the same [Left](-left/index.md) if this is [Left](-left/index.md).  
  


#### Return  
The same [Right](-right/index.md) if the [predicate]() is satisfied for the value, Left(zero) if the [predicate]() is not satisfied for the value, or the same [Left](-left/index.md) if this is [Left](-left/index.md).  
  


#### Since  
1.2  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
| zero| Provider of the value used if the [predicate]() is not satisfied.
  
  
Content  
inline fun <[L](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>.[filterOrElse](filter-or-else.md)(predicate: ([R](filter-or-else.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [L](filter-or-else.md)): [Either](-either/index.md)<[L](filter-or-else.md), [R](filter-or-else.md)>?  



