---
title: recoverWith -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[recoverWith](recover-with.html)



# recoverWith  
[common]  
Brief description  


Returns this [Try](-try/index.html) if this is a [Success](-success/index.html) or a [Try](-try/index.html) created by the rescue function if this is a [Failure](-failure/index.html).



#### Return  


This [Try](-try/index.html) if this is a [Success](-success/index.html) or a [Try](-try/index.html) created by the rescue function if this is a [Failure](-failure/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| rescue| <br><br>Function creating a new [Try](-try/index.html) from the exception of a [Failure](-failure/index.html).<br><br>
  
  
Content  
inline fun <[T](recover-with.html)> [Try](-try/index.html)<[T](recover-with.html)>.[recoverWith](recover-with.html)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [Try](-try/index.html)<[T](recover-with.html)>): [Try](-try/index.html)<[T](recover-with.html)>  



