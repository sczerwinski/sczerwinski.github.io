---
title: fold -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Try](index.html)/[fold](fold.html)



# fold  
[common]  
Brief description  


Transforms a [Success](../-success/index.html) using successTransform or a [Failure](../-failure/index.html) using failureTransform.



#### Return  


Result of applying successTransform on [Success](../-success/index.html) or failureTransform on [Failure](../-failure/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| failureTransform| <br><br>Function transforming exception from a [Failure](../-failure/index.html) to a new [Try](index.html).<br><br>
| successTransform| <br><br>Function transforming value of a [Success](../-success/index.html) to a new [Try](index.html).<br><br>
  
  
Content  
inline fun <[R](fold.html)> [fold](fold.html)(successTransform: ([T](index.html)) -> [R](fold.html), failureTransform: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [R](fold.html)): [R](fold.html)  



