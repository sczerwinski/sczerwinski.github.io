---
title: filter -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[RightProjection](index.md)/[filter](filter.md)



# filter  
[Kotlin utilities]  
Brief description  
Returns the same [Right](../-right/index.md) if the [predicate]() is satisfied for the value. Otherwise returns null.  
  


#### Return  
The same [Right](../-right/index.md) if the [predicate]() is satisfied for the value. Otherwise returns null.  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
inline fun [filter](filter.md)(predicate: ([R](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Either](../-either/index.md)<[L](index.md), [R](index.md)>?  



