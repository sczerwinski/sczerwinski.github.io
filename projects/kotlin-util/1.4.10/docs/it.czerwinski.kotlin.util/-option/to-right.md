---
title: toRight -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Option](index.html)/[toRight](to-right.html)



# toRight  
[common]  
Brief description  


Returns a [Left](../-left/index.html) containing the given argument left if this is empty, or a [Right](../-right/index.html) containing this option's value if it is defined.



#### Return  


a [Left](../-left/index.html) containing the given argument left if this is empty, or a [Right](../-right/index.html) containing this option's value if it is defined.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| L| <br><br>The type of the [Left](../-left/index.html) value.<br><br>
| left| <br><br>Producer of the fallback [Left](../-left/index.html) value.<br><br>
  
  
Content  
inline fun <[L](to-right.html)> [toRight](to-right.html)(left: () -> [L](to-right.html)): [Either](../-either/index.html)<[L](to-right.html), [T](index.html)>  



