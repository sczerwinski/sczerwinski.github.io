---
title: map -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[RightProjection](index.html)/[map](map.html)



# map  
[common]  
Brief description  


Maps value of this [Right](../-right/index.html) using transform.



#### Return  


[Right](../-right/index.html) mapped using transform or this object if this is a [Left](../-left/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming a [Right](../-right/index.html).<br><br>
  
  
Content  
inline fun <[T](map.html)> [map](map.html)(transform: ([R](index.html)) -> [T](map.html)): [Either](../-either/index.html)<[L](index.html), [T](map.html)>  



