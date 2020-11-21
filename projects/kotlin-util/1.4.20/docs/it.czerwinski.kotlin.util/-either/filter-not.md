---
title: filterNot -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Either](index.html)/[filterNot](filter-not.html)



# filterNot  
[common]  
Brief description  


Returns the same [Right](../-right/index.html) if the predicate is not satisfied for the value. Otherwise returns null.



#### Return  


The same [Right](../-right/index.html) if the predicate is not satisfied for the value. Otherwise returns null.



#### Since  


1.3



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
  
  
Content  
inline fun [filterNot](filter-not.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Either](index.html)<[L](index.html), [R](index.html)>?  



