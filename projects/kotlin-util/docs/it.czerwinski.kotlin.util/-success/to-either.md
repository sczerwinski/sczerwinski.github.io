---
title: toEither -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Success](index.md)/[toEither](to-either.md)



# toEither  
[Kotlin utilities]  
Brief description  
Converts this [Try](../-try/index.md) to [Either](../-either/index.md).  
  


#### Return  
[Left](../-left/index.md) if this is [Failure](../-failure/index.md) or [Right](../-right/index.md) if this is [Success](index.md).  
  
  
Content  
open override fun [toEither](to-either.md)(): [Either](../-either/index.md)<[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html), [T](index.md)>  



