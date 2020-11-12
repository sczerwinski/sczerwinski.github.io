---
title: filterNot -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Either](index.md)/[filterNot](filter-not.md)



# filterNot  
[Kotlin utilities]  
Brief description  
Returns the same [Right](../-right/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns null.  
  


#### Return  
The same [Right](../-right/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns null.  
  


#### Since  
1.3  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
inline fun [filterNot](filter-not.md)(predicate: ([R](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Either](index.md)<[L](index.md), [R](index.md)>?  



