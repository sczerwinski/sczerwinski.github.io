---
title: recover -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[recover](recover.md)



# recover  
[Kotlin utilities]  
Brief description  
Returns this [Try](-try/index.md) if this is a [Success](-success/index.md) or a [Try](-try/index.md) created for the [rescue]() operation if this is a [Failure](-failure/index.md).  
  


#### Return  
This [Try](-try/index.md) if this is a [Success](-success/index.md) or a [Try](-try/index.md) created for the [rescue]() operation if this is a [Failure](-failure/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| rescue| Function creating a new value from the exception of a [Failure](-failure/index.md).
  
  
Content  
inline fun <[T](recover.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](recover.md)>.[recover](recover.md)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [T](recover.md)): [Try](-try/index.md)<[T](recover.md)>  



