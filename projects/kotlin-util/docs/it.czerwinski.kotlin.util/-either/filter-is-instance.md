---
title: filterIsInstance -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Either](index.md)/[filterIsInstance](filter-is-instance.md)



# filterIsInstance  
[Kotlin utilities]  
Brief description  
Returns the same [Right](../-right/index.md) casted to type [T]() if it is [T](). Otherwise returns null.  
  


#### Return  
The same [Right](../-right/index.md) casted to type [T]() if it is [T](). Otherwise returns null.  
  


#### Since  
1.3  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| T| Required type of the optional value.
  
  
Content  
inline fun <[T](filter-is-instance.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [filterIsInstance](filter-is-instance.md)(): [Either](index.md)<[L](index.md), [T](filter-is-instance.md)>?  



