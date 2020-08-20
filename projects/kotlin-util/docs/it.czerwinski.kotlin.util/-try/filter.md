---
title: filter -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Try](index.md)/[filter](filter.md)



# filter  
[Kotlin utilities]  
Brief description  
Returns the same [Success](../-success/index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [Failure](../-failure/index.md).  
  


#### Return  
The same [Success](../-success/index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [Failure](../-failure/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
abstract fun [filter](filter.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Try](index.md)<[T](index.md)>  



