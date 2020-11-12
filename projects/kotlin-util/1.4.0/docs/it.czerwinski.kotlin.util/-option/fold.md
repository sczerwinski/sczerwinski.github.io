---
title: fold -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Option](index.md)/[fold](fold.md)



# fold  
[Kotlin utilities]  
Brief description  
Returns result of applying [transform]() on the value of [Some](../-some/index.md) or [default]() if this is [None](../-none/index.md).  
  


#### Return  
Result of applying [transform]() on the value of [Some](../-some/index.md) or [default]() if this is [None](../-none/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| default| Value to be returned if the option is empty.
| transform| Function transforming [Some](../-some/index.md) value.
  
  
Content  
inline fun <[R](fold.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [fold](fold.md)(default: [R](fold.md), transform: ([T](index.md)) -> [R](fold.md)): [R](fold.md)  


[Kotlin utilities]  
Brief description  
Returns result of applying [transform]() on the value of [Some](../-some/index.md) or [default]() if this is [None](../-none/index.md).  
  


#### Return  
Result of applying [transform]() on the value of [Some](../-some/index.md) or [default]() if this is [None](../-none/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| default| Function producing value to be returned if the option is empty.
| transform| Function transforming [Some](../-some/index.md) value.
  
  
Content  
inline fun <[R](fold.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [fold](fold.md)(default: () -> [R](fold.md), transform: ([T](index.md)) -> [R](fold.md)): [R](fold.md)  



