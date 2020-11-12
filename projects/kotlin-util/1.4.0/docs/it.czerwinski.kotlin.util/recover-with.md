---
title: recoverWith -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[recoverWith](recover-with.md)



# recoverWith  
[Kotlin utilities]  
Brief description  
Returns this [Try](-try/index.md) if this is a [Success](-success/index.md) or a [Try](-try/index.md) created by the [rescue]() function if this is a [Failure](-failure/index.md).  
  


#### Return  
This [Try](-try/index.md) if this is a [Success](-success/index.md) or a [Try](-try/index.md) created by the [rescue]() function if this is a [Failure](-failure/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| rescue| Function creating a new [Try](-try/index.md) from the exception of a [Failure](-failure/index.md).
  
  
Content  
inline fun <[T](recover-with.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](recover-with.md)>.[recoverWith](recover-with.md)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [Try](-try/index.md)<[T](recover-with.md)>): [Try](-try/index.md)<[T](recover-with.md)>  



