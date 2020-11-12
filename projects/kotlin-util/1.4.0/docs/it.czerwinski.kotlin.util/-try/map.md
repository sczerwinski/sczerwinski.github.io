---
title: map -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Try](index.md)/[map](map.md)



# map  
[Kotlin utilities]  
Brief description  
Maps value of a [Success](../-success/index.md) using [transform]() or returns the same [Try](index.md) if this is a [Failure](../-failure/index.md).  
  


#### Return  
[Try](index.md) with a value mapped using [transform]() or this object if this is a [Failure](../-failure/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming value of a [Success](../-success/index.md).
  
  
Content  
abstract fun <[R](map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [map](map.md)(transform: ([T](index.md)) -> [R](map.md)): [Try](index.md)<[R](map.md)>  



