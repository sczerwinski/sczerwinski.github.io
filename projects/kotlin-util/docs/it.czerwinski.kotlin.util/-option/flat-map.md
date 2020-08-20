---
title: flatMap -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Option](index.md)/[flatMap](flat-map.md)



# flatMap  
[Kotlin utilities]  
Brief description  
Maps value of a [Some](../-some/index.md) to a new [Option](index.md) using [transform]() or returns the same [None](../-none/index.md).  
  


#### Return  
[Option](index.md) returned by [transform]() or this object if this is a [None](../-none/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming value of a [Some](../-some/index.md) to an [Option](index.md).
  
  
Content  
inline fun <[R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [flatMap](flat-map.md)(transform: ([T](index.md)) -> [Option](index.md)<[R](flat-map.md)>): [Option](index.md)<[R](flat-map.md)>  



