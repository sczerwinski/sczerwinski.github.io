---
title: filterNot -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[LeftProjection](index.html)/[filterNot](filter-not.html)



# filterNot  
[common]  
Brief description  


Returns the same [Left](../-left/index.html) if the predicate is not satisfied for the value. Otherwise returns null.



#### Return  


The same [Left](../-left/index.html) if the predicate is not satisfied for the value. Otherwise returns null.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
  
  
Content  
inline fun [filterNot](filter-not.html)(predicate: ([L](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Either](../-either/index.html)<[L](index.html), [R](index.html)>?  



