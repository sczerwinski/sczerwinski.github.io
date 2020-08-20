---
title: filter -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Failure](index.md)/[filter](filter.md)



# filter  
[Kotlin utilities]  
Brief description  
Returns the same [Success](../-success/index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [Failure](index.md).  
  


#### Return  
The same [Success](../-success/index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [Failure](index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
open override fun [filter](filter.md)(predicate: ([Nothing](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Try](../-try/index.md)<[Nothing](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)>  



