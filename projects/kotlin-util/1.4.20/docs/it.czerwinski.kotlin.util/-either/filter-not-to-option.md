---
title: filterNotToOption -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Either](index.html)/[filterNotToOption](filter-not-to-option.html)



# filterNotToOption  
[common]  
Brief description  


Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) if the predicate is not satisfied for the value. Otherwise returns [None](../-none/index.html).



#### Return  


[Some](../-some/index.html) containing the same [Right](../-right/index.html) if the predicate is not satisfied for the value. Otherwise returns [None](../-none/index.html).



#### Since  


1.3



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
  
  
Content  
inline fun [filterNotToOption](filter-not-to-option.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](../-option/index.html)<[Either](index.html)<[L](index.html), [R](index.html)>>  



