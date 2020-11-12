---
title: map -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Try](index.html)/[map](map.html)



# map  
[common]  
Brief description  


Maps value of a [Success](../-success/index.html) using transform or returns the same [Try](index.html) if this is a [Failure](../-failure/index.html).



#### Return  


[Try](index.html) with a value mapped using transform or this object if this is a [Failure](../-failure/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming value of a [Success](../-success/index.html).<br><br>
  
  
Content  
abstract fun <[R](map.html)> [map](map.html)(transform: ([T](index.html)) -> [R](map.html)): [Try](index.html)<[R](map.html)>  



