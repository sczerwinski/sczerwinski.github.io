---
title: filterOrElse -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Success](index.html)/[filterOrElse](filter-or-else.html)



# filterOrElse  
[common]  
Brief description  


Returns the same [Success](index.html) if the predicate is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html) containing the given throwable.



#### Return  


The same [Success](index.html) if the predicate is satisfied for the value. Otherwise returns a [Failure](../-failure/index.html) containing the given throwable.



#### Since  


1.2



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
| throwable| <br><br>Function providing a throwable to be used when the predicate is not satisfied.<br><br>
  
  
Content  
open override fun [filterOrElse](filter-or-else.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), throwable: ([T](index.html)) -> [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)): [Try](../-try/index.html)<[T](index.html)>  



