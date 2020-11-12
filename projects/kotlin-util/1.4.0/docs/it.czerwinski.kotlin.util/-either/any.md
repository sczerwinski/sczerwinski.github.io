---
title: any -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Either](index.md)/[any](any.md)



# any  
[Kotlin utilities]  
Brief description  
Returns the result of applying the [predicate]() to the value if this is [Right](../-right/index.md) or false if this is [Left](../-left/index.md).  
  


#### Return  
The result of applying the [predicate]() to the value if this is [Right](../-right/index.md) or false if this is [Left](../-left/index.md).  
  


#### Since  
1.3  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| predicate| Predicate function.
  
  
Content  
inline fun [any](any.md)(predicate: ([R](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  



