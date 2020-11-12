---
title: recover -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[recover](recover.html)



# recover  
[common]  
Brief description  


Returns this [Try](-try/index.html) if this is a [Success](-success/index.html) or a [Try](-try/index.html) created for the rescue operation if this is a [Failure](-failure/index.html).



#### Return  


This [Try](-try/index.html) if this is a [Success](-success/index.html) or a [Try](-try/index.html) created for the rescue operation if this is a [Failure](-failure/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| rescue| <br><br>Function creating a new value from the exception of a [Failure](-failure/index.html).<br><br>
  
  
Content  
inline fun <[T](recover.html)> [Try](-try/index.html)<[T](recover.html)>.[recover](recover.html)(rescue: ([Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)) -> [T](recover.html)): [Try](-try/index.html)<[T](recover.html)>  



