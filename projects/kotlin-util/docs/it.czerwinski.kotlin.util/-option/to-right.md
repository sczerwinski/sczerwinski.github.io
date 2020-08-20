---
title: toRight -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Option](index.md)/[toRight](to-right.md)



# toRight  
[Kotlin utilities]  
Brief description  
Returns a [Left](../-left/index.md) containing the given argument [left]() if this is empty, or a [Right](../-right/index.md) containing this option's value if it is defined.  
  


#### Return  
a [Left](../-left/index.md) containing the given argument [left]() if this is empty, or a [Right](../-right/index.md) containing this option's value if it is defined.  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| L| The type of the [Left](../-left/index.md) value.
| left| Producer of the fallback [Left](../-left/index.md) value.
  
  
Content  
inline fun <[L](to-right.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [toRight](to-right.md)(left: () -> [L](to-right.md)): [Either](../-either/index.md)<[L](to-right.md), [T](index.md)>  



