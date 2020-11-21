---
title: filterNot -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Success](index.html)/[filterNot](filter-not.html)



# filterNot  
[common]  
Brief description  


Returns the same [Success](index.html) if the predicate is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).



#### Return  


The same [Success](index.html) if the predicate is not satisfied for the value. Otherwise returns a [Failure](../-failure/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
  
  
Content  
open override fun [filterNot](filter-not.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Try](../-try/index.html)<[T](index.html)>  



