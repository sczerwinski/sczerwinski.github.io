---
title: flatMap -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Try](index.html)/[flatMap](flat-map.html)



# flatMap  
[common]  
Brief description  


Maps value of a [Success](../-success/index.html) to a new [Try](index.html) using transform or returns the same [Try](index.html) if this is a [Failure](../-failure/index.html).



#### Return  


[Try](index.html) returned by transform or this object if this is a [Failure](../-failure/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming value of a [Success](../-success/index.html) to a [Try](index.html).<br><br>
  
  
Content  
abstract fun <[R](flat-map.html)> [flatMap](flat-map.html)(transform: ([T](index.html)) -> [Try](index.html)<[R](flat-map.html)>): [Try](index.html)<[R](flat-map.html)>  



