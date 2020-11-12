---
title: transform -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Try](index.md)/[transform](transform.md)



# transform  
[Kotlin utilities]  
Brief description  
Transforms a [Success](../-success/index.md) using [successTransform]() or a [Failure](../-failure/index.md) using [failureTransform]().  
  


#### Return  
New [Try](index.md) being a result of a transformation of a [Success](../-success/index.md) with [successTransform]() or a [Failure](../-failure/index.md) with [failureTransform]().  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| failureTransform| Function transforming exception from a [Failure](../-failure/index.md) to a new [Try](index.md).
| successTransform| Function transforming value of a [Success](../-success/index.md) to a new [Try](index.md).
  
  
Content  
inline fun <[R](transform.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [transform](transform.md)(successTransform: ([T](index.md)) -> [Try](index.md)<[R](transform.md)>, failureTransform: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [Try](index.md)<[R](transform.md)>): [Try](index.md)<[R](transform.md)>  



