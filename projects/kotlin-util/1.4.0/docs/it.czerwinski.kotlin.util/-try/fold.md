---
title: fold -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Try](index.md)/[fold](fold.md)



# fold  
[Kotlin utilities]  
Brief description  
Transforms a [Success](../-success/index.md) using [successTransform]() or a [Failure](../-failure/index.md) using [failureTransform]().  
  


#### Return  
Result of applying [successTransform]() on [Success](../-success/index.md) or [failureTransform]() on [Failure](../-failure/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| failureTransform| Function transforming exception from a [Failure](../-failure/index.md) to a new [Try](index.md).
| successTransform| Function transforming value of a [Success](../-success/index.md) to a new [Try](index.md).
  
  
Content  
inline fun <[R](fold.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [fold](fold.md)(successTransform: ([T](index.md)) -> [R](fold.md), failureTransform: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [R](fold.md)): [R](fold.md)  



