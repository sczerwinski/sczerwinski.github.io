---
title: map -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Failure](index.md)/[map](map.md)



# map  
[Kotlin utilities]  
Brief description  
Maps value of a [Success](../-success/index.md) using [transform]() or returns the same [Try](../-try/index.md) if this is a [Failure](index.md).  
  


#### Return  
[Try](../-try/index.md) with a value mapped using [transform]() or this object if this is a [Failure](index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming value of a [Success](../-success/index.md).
  
  
Content  
open override fun <[R](map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [map](map.md)(transform: ([Nothing](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)) -> [R](map.md)): [Try](../-try/index.md)<[R](map.md)>  



