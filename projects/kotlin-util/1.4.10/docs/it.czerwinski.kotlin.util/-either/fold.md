---
title: fold -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Either](index.html)/[fold](fold.html)



# fold  
[common]  
Brief description  


Transforms [Left](../-left/index.html) with leftTransform or [Right](../-right/index.html) with rightTransform.



#### Return  


Result of applying leftTransform on [Left](../-left/index.html) or rightTransform on [Right](../-right/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| leftTransform| <br><br>Function transforming [Left](../-left/index.html) value.<br><br>
| rightTransform| <br><br>Function transforming [Right](../-right/index.html) value.<br><br>
  
  
Content  
inline fun <[T](fold.html)> [fold](fold.html)(leftTransform: ([L](index.html)) -> [T](fold.html), rightTransform: ([R](index.html)) -> [T](fold.html)): [T](fold.html)  



