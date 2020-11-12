---
title: filterToOption -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[LeftProjection](index.md)/[filterToOption](filter-to-option.md)



# filterToOption  
[Kotlin utilities]  
Brief description  
Returns [Some](../-some/index.md) containing the same [Left](../-left/index.md) if the [predicate]() is satisfied for the value. Otherwise returns [None](../-none/index.md).  
  


#### Return  
[Some](../-some/index.md) containing the same [Left](../-left/index.md) if the [predicate]() is satisfied for the value. Otherwise returns [None](../-none/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
inline fun [filterToOption](filter-to-option.md)(predicate: ([L](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.md)<[Either](../-either/index.md)<[L](index.md), [R](index.md)>>  



