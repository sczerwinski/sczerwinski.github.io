---
title: filter -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[RightProjection](index.html)/[filter](filter.html)



# filter  
[common]  
Brief description  


Returns the same [Right](../-right/index.html) if the predicate is satisfied for the value. Otherwise returns null.



#### Return  


The same [Right](../-right/index.html) if the predicate is satisfied for the value. Otherwise returns null.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
  
  
Content  
inline fun [filter](filter.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Either](../-either/index.html)<[L](index.html), [R](index.html)>?  



