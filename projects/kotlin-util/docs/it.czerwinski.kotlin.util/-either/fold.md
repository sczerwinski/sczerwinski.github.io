---
title: fold -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Either](index.md)/[fold](fold.md)



# fold  
[Kotlin utilities]  
Brief description  
Transforms [Left](../-left/index.md) with [leftTransform]() or [Right](../-right/index.md) with [rightTransform]().  
  


#### Return  
Result of applying [leftTransform]() on [Left](../-left/index.md) or [rightTransform]() on [Right](../-right/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| leftTransform| Function transforming [Left](../-left/index.md) value.
| rightTransform| Function transforming [Right](../-right/index.md) value.
  
  
Content  
inline fun <[T](fold.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [fold](fold.md)(leftTransform: ([L](index.md)) -> [T](fold.md), rightTransform: ([R](index.md)) -> [T](fold.md)): [T](fold.md)  



