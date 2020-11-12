---
title: toLeft -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Option](index.html)/[toLeft](to-left.html)



# toLeft  
[common]  
Brief description  


Returns a [Right](../-right/index.html) containing the given argument right if this is empty, or a [Left](../-left/index.html) containing this option's value if it is defined.



#### Return  


a [Right](../-right/index.html) containing the given argument right if this is empty, or a [Left](../-left/index.html) containing this option's value if it is defined.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| R| <br><br>The type of the [Right](../-right/index.html) value.<br><br>
| right| <br><br>Producer of the fallback [Right](../-right/index.html) value.<br><br>
  
  
Content  
inline fun <[R](to-left.html)> [toLeft](to-left.html)(right: () -> [R](to-left.html)): [Either](../-either/index.html)<[T](index.html), [R](to-left.html)>  



