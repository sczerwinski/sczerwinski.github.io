---
title: toLeft -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Option](index.md)/[toLeft](to-left.md)



# toLeft  
[Kotlin utilities]  
Brief description  
Returns a [Right](../-right/index.md) containing the given argument [right]() if this is empty, or a [Left](../-left/index.md) containing this option's value if it is defined.  
  


#### Return  
a [Right](../-right/index.md) containing the given argument [right]() if this is empty, or a [Left](../-left/index.md) containing this option's value if it is defined.  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| R| The type of the [Right](../-right/index.md) value.
| right| Producer of the fallback [Right](../-right/index.md) value.
  
  
Content  
inline fun <[R](to-left.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [toLeft](to-left.md)(right: () -> [R](to-left.md)): [Either](../-either/index.md)<[T](index.md), [R](to-left.md)>  



