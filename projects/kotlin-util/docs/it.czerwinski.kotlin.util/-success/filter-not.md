---
title: filterNot -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Success](index.md)/[filterNot](filter-not.md)



# filterNot  
[Kotlin utilities]  
Brief description  
Returns the same [Success](index.md) if the [predicate]() is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.md).  
  


#### Return  
The same [Success](index.md) if the [predicate]() is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
open override fun [filterNot](filter-not.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Try](../-try/index.md)<[T](index.md)>  



