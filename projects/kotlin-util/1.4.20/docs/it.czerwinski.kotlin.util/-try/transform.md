---
title: transform -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Try](index.html)/[transform](transform.html)



# transform  
[common]  
Brief description  


Transforms a [Success](../-success/index.html) using successTransform or a [Failure](../-failure/index.html) using failureTransform.



#### Return  


New [Try](index.html) being a result of a transformation of a [Success](../-success/index.html) with successTransform or a [Failure](../-failure/index.html) with failureTransform.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| failureTransform| <br><br>Function transforming exception from a [Failure](../-failure/index.html) to a new [Try](index.html).<br><br>
| successTransform| <br><br>Function transforming value of a [Success](../-success/index.html) to a new [Try](index.html).<br><br>
  
  
Content  
inline fun <[R](transform.html)> [transform](transform.html)(successTransform: ([T](index.html)) -> [Try](index.html)<[R](transform.html)>, failureTransform: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [Try](index.html)<[R](transform.html)>): [Try](index.html)<[R](transform.html)>  



