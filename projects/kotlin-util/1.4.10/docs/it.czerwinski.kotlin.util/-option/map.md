---
title: map -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Option](index.html)/[map](map.html)



# map  
[common]  
Brief description  


Maps value of a [Some](../-some/index.html) using transform or returns the same [None](../-none/index.html).



#### Return  


[Some](../-some/index.html) with a value mapped using transform or this object if this is a [None](../-none/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming value of a [Some](../-some/index.html).<br><br>
  
  
Content  
inline fun <[R](map.html)> [map](map.html)(transform: ([T](index.html)) -> [R](map.html)): [Option](index.html)<[R](map.html)>  



