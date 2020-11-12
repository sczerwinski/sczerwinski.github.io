---
title: filterOrElse -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Success](index.md)/[filterOrElse](filter-or-else.md)



# filterOrElse  
[Kotlin utilities]  
Brief description  
Returns the same [Success](index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [Failure](../-failure/index.md) containing the given [throwable]().  
  


#### Return  
The same [Success](index.md) if the [predicate]() is satisfied for the value. Otherwise returns a [Failure](../-failure/index.md) containing the given [throwable]().  
  


#### Since  
1.2  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
| throwable| Function providing a throwable to be used when the [predicate]() is not satisfied.
  
  
Content  
open override fun [filterOrElse](filter-or-else.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), throwable: ([T](index.md)) -> [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)): [Try](../-try/index.md)<[T](index.md)>  



