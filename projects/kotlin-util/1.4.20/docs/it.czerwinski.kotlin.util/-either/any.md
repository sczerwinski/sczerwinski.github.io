---
title: any -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Either](index.html)/[any](any.html)



# any  
[common]  
Brief description  


Returns the result of applying the predicate to the value if this is [Right](../-right/index.html) or false if this is [Left](../-left/index.html).



#### Return  


The result of applying the predicate to the value if this is [Right](../-right/index.html) or false if this is [Left](../-left/index.html).



#### Since  


1.3



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
  
  
Content  
inline fun [any](any.html)(predicate: ([R](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  



