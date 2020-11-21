---
title: map -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Failure](index.html)/[map](map.html)



# map  
[common]  
Brief description  


Maps value of a [Success](../-success/index.html) using transform or returns the same [Try](../-try/index.html) if this is a [Failure](index.html).



#### Return  


[Try](../-try/index.html) with a value mapped using transform or this object if this is a [Failure](index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming value of a [Success](../-success/index.html).<br><br>
  
  
Content  
open override fun <[R](map.html)> [map](map.html)(transform: ([Nothing](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)) -> [R](map.html)): [Try](../-try/index.html)<[R](map.html)>  



