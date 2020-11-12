---
title: flatMap -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Success](index.html)/[flatMap](flat-map.html)



# flatMap  
[common]  
Brief description  


Maps value of a [Success](index.html) to a new [Try](../-try/index.html) using transform or returns the same [Try](../-try/index.html) if this is a [Failure](../-failure/index.html).



#### Return  


[Try](../-try/index.html) returned by transform or this object if this is a [Failure](../-failure/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming value of a [Success](index.html) to a [Try](../-try/index.html).<br><br>
  
  
Content  
open override fun <[R](flat-map.html)> [flatMap](flat-map.html)(transform: ([T](index.html)) -> [Try](../-try/index.html)<[R](flat-map.html)>): [Try](../-try/index.html)<[R](flat-map.html)>  



