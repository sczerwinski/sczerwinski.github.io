---
title: flatMap -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Failure](index.md)/[flatMap](flat-map.md)



# flatMap  
[Kotlin utilities]  
Brief description  
Maps value of a [Success](../-success/index.md) to a new [Try](../-try/index.md) using [transform]() or returns the same [Try](../-try/index.md) if this is a [Failure](index.md).  
  


#### Return  
[Try](../-try/index.md) returned by [transform]() or this object if this is a [Failure](index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming value of a [Success](../-success/index.md) to a [Try](../-try/index.md).
  
  
Content  
open override fun <[R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [flatMap](flat-map.md)(transform: ([Nothing](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)) -> [Try](../-try/index.md)<[R](flat-map.md)>): [Try](../-try/index.md)<[R](flat-map.md)>  



