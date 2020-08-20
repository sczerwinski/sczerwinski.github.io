---
title: filterIsInstance -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Option](index.md)/[filterIsInstance](filter-is-instance.md)



# filterIsInstance  
[Kotlin utilities]  
Brief description  
Returns the same [Some](../-some/index.md) casted to type [R]() if it is [R](). Otherwise returns a [None](../-none/index.md).  
  


#### Return  
The same [Some](../-some/index.md) casted to type [R]() if it is [R](). Otherwise returns a [None](../-none/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| R| Required type of the optional value.
  
  
Content  
inline fun <[R](filter-is-instance.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [filterIsInstance](filter-is-instance.md)(): [Option](index.md)<[R](filter-is-instance.md)>  



