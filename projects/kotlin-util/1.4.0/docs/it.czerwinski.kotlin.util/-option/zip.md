---
title: zip -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Option](index.md)/[zip](zip.md)



# zip  
[Kotlin utilities]  
Brief description  
Returns [Some](../-some/index.md) containing a Pair of values of this and [other](index.md) if both [Option](index.md)s are [Some](../-some/index.md). Otherwise returns [None](../-none/index.md).  
  


#### Return  
[Some](../-some/index.md) containing a Pair of values of this and [other](index.md) if both [Option](index.md)s are [Some](../-some/index.md). Otherwise returns [None](../-none/index.md).  
  


#### Since  
1.1  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| other| Other [Option](index.md).
  
  
Content  
infix fun <[R](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](zip.md)(other: [Option](index.md)<[R](zip.md)>): [Option](index.md)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.md), [R](zip.md)>>  


[Kotlin utilities]  
Brief description  
Returns [Some](../-some/index.md) containing the result of applying [transform]() to both values of this and [other](index.md) if both [Option](index.md)s are [Some](../-some/index.md). Otherwise returns [None](../-none/index.md).  
  


#### Return  
[Some](../-some/index.md) containing the result of applying [transform]() to both values of this and [other](index.md) if both [Option](index.md)s are [Some](../-some/index.md). Otherwise returns [None](../-none/index.md).  
  


#### Since  
1.1  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| other| Other [Option](index.md).
| transform| Function transforming values of both [Some](../-some/index.md).
  
  
Content  
inline fun <[T1](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](zip.md)(other: [Option](index.md)<[T1](zip.md)>, transform: ([T](index.md), [T1](zip.md)) -> [R](zip.md)): [Option](index.md)<[R](zip.md)>  



