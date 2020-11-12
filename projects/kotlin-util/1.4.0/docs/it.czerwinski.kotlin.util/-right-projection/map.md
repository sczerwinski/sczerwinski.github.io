---
title: map -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[RightProjection](index.md)/[map](map.md)



# map  
[Kotlin utilities]  
Brief description  
Maps value of this [Right](../-right/index.md) using [transform]().  
  


#### Return  
[Right](../-right/index.md) mapped using [transform]() or this object if this is a [Left](../-left/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming a [Right](../-right/index.md).
  
  
Content  
inline fun <[T](map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [map](map.md)(transform: ([R](index.md)) -> [T](map.md)): [Either](../-either/index.md)<[L](index.md), [T](map.md)>  



