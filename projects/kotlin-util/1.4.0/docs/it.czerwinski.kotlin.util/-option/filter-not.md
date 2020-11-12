---
title: filterNot -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Option](index.md)/[filterNot](filter-not.md)



# filterNot  
[Kotlin utilities]  
Brief description  
Returns the same [Some](../-some/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns a [None](../-none/index.md).  
  


#### Return  
The same [Some](../-some/index.md) if the [predicate]() is not satisfied for the value. Otherwise returns a [None](../-none/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
inline fun [filterNot](filter-not.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](index.md)<[T](index.md)>  



