---
title: flatMap -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Option](index.html)/[flatMap](flat-map.html)



# flatMap  
[common]  
Brief description  


Maps value of a [Some](../-some/index.html) to a new [Option](index.html) using transform or returns the same [None](../-none/index.html).



#### Return  


[Option](index.html) returned by transform or this object if this is a [None](../-none/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming value of a [Some](../-some/index.html) to an [Option](index.html).<br><br>
  
  
Content  
inline fun <[R](flat-map.html)> [flatMap](flat-map.html)(transform: ([T](index.html)) -> [Option](index.html)<[R](flat-map.html)>): [Option](index.html)<[R](flat-map.html)>  



