---
title: filterNotToOption -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Either](index.md)/[filterNotToOption](filter-not-to-option.md)



# filterNotToOption  
[Kotlin utilities]  
Brief description  
Returns [Some](../-some/index.md) containing the same [Right](../-right/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns [None](../-none/index.md).  
  


#### Return  
[Some](../-some/index.md) containing the same [Right](../-right/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns [None](../-none/index.md).  
  


#### Since  
1.3  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
inline fun [filterNotToOption](filter-not-to-option.md)(predicate: ([R](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.md)<[Either](index.md)<[L](index.md), [R](index.md)>>  



