---
title: map -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[LeftProjection](index.html)/[map](map.html)



# map  
[common]  
Brief description  


Maps value of this [Left](../-left/index.html) using transform.



#### Return  


[Left](../-left/index.html) mapped using transform or this object if this is a [Right](../-right/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming a [Left](../-left/index.html).<br><br>
  
  
Content  
inline fun <[T](map.html)> [map](map.html)(transform: ([L](index.html)) -> [T](map.html)): [Either](../-either/index.html)<[T](map.html), [R](index.html)>  



