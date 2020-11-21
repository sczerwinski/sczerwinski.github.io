---
title: filter -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Option](index.html)/[filter](filter.html)



# filter  
[common]  
Brief description  


Returns the same [Some](../-some/index.html) if the predicate is satisfied for the value. Otherwise returns a [None](../-none/index.html).



#### Return  


The same [Some](../-some/index.html) if the predicate is satisfied for the value. Otherwise returns a [None](../-none/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
  
  
Content  
inline fun [filter](filter.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Option](index.html)<[T](index.html)>  



