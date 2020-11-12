---
title: map -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Option](index.md)/[map](map.md)



# map  
[Kotlin utilities]  
Brief description  
Maps value of a [Some](../-some/index.md) using [transform]() or returns the same [None](../-none/index.md).  
  


#### Return  
[Some](../-some/index.md) with a value mapped using [transform]() or this object if this is a [None](../-none/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming value of a [Some](../-some/index.md).
  
  
Content  
inline fun <[R](map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [map](map.md)(transform: ([T](index.md)) -> [R](map.md)): [Option](index.md)<[R](map.md)>  



