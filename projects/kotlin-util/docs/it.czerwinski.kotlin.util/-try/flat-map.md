---
title: flatMap -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Try](index.md)/[flatMap](flat-map.md)



# flatMap  
[Kotlin utilities]  
Brief description  
Maps value of a [Success](../-success/index.md) to a new [Try](index.md) using [transform]() or returns the same [Try](index.md) if this is a [Failure](../-failure/index.md).  
  


#### Return  
[Try](index.md) returned by [transform]() or this object if this is a [Failure](../-failure/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming value of a [Success](../-success/index.md) to a [Try](index.md).
  
  
Content  
abstract fun <[R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [flatMap](flat-map.md)(transform: ([T](index.md)) -> [Try](index.md)<[R](flat-map.md)>): [Try](index.md)<[R](flat-map.md)>  



