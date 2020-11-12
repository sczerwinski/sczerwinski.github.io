---
title: filterNot -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[LeftProjection](index.md)/[filterNot](filter-not.md)



# filterNot  
[Kotlin utilities]  
Brief description  
Returns the same [Left](../-left/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns null.  
  


#### Return  
The same [Left](../-left/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns null.  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
inline fun [filterNot](filter-not.md)(predicate: ([L](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Either](../-either/index.md)<[L](index.md), [R](index.md)>?  



