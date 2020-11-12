---
title: map -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[LeftProjection](index.md)/[map](map.md)



# map  
[Kotlin utilities]  
Brief description  
Maps value of this [Left](../-left/index.md) using [transform]().  
  


#### Return  
[Left](../-left/index.md) mapped using [transform]() or this object if this is a [Right](../-right/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming a [Left](../-left/index.md).
  
  
Content  
inline fun <[T](map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [map](map.md)(transform: ([L](index.md)) -> [T](map.md)): [Either](../-either/index.md)<[T](map.md), [R](index.md)>  



