---
title: filterIsInstanceToOption -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[LeftProjection](index.md)/[filterIsInstanceToOption](filter-is-instance-to-option.md)



# filterIsInstanceToOption  
[Kotlin utilities]  
Brief description  
Returns [Some](../-some/index.md) containing the same [Left](../-left/index.md) casted to type [T]() if it is [T](). Otherwise returns [None](../-none/index.md).  
  


#### Return  
[Some](../-some/index.md) containing the same [Left](../-left/index.md) casted to type [T]() if it is [T](). Otherwise returns [None](../-none/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| T| Required type of the optional value.
  
  
Content  
inline fun <[T](filter-is-instance-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [filterIsInstanceToOption](filter-is-instance-to-option.md)(): [Option](../-option/index.md)<[Either](../-either/index.md)<[T](filter-is-instance-to-option.md), [R](index.md)>>  



