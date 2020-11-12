---
title: filterToOption -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[RightProjection](index.html)/[filterToOption](filter-to-option.html)



# filterToOption  
[common]  
Brief description  


Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) if the predicate is satisfied for the value. Otherwise returns [None](../-none/index.html).



#### Return  


[Some](../-some/index.html) containing the same [Right](../-right/index.html) if the predicate is satisfied for the value. Otherwise returns [None](../-none/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
  
  
Content  
inline fun [filterToOption](filter-to-option.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.html)<[Either](../-either/index.html)<[L](index.html), [R](index.html)>>  



