---
title: zip -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Try](index.md)/[zip](zip.md)



# zip  
[Kotlin utilities]  
Brief description  
Returns [Success](../-success/index.md) containing a Pair of values of this and [other](index.md) if both instances of [Try](index.md) are [Success](../-success/index.md). Otherwise returns first [Failure](../-failure/index.md).  
  


#### Return  
[Success](../-success/index.md) containing a Pair of values of this and [other](index.md) if both instances of [Try](index.md) are [Success](../-success/index.md). Otherwise returns first [Failure](../-failure/index.md).  
  


#### Since  
1.1  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| other| Other [Try](index.md).
  
  
Content  
infix fun <[R](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](zip.md)(other: [Try](index.md)<[R](zip.md)>): [Try](index.md)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.md), [R](zip.md)>>  


[Kotlin utilities]  
Brief description  
Returns [Success](../-success/index.md) containing the result of applying [transform]() to both values of this and [other](index.md) if both instances of [Try](index.md) are [Success](../-success/index.md). Otherwise returns first [Failure](../-failure/index.md).  
  


#### Return  
[Success](../-success/index.md) containing the result of applying [transform]() to both values of this and [other](index.md) if both instances of [Try](index.md) are [Success](../-success/index.md). Otherwise returns first [Failure](../-failure/index.md).  
  


#### Since  
1.1  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| other| Other [Try](index.md).
| transform| Function transforming values of both instances of [Success](../-success/index.md).
  
  
Content  
inline fun <[T1](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](zip.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [zip](zip.md)(other: [Try](index.md)<[T1](zip.md)>, transform: ([T](index.md), [T1](zip.md)) -> [R](zip.md)): [Try](index.md)<[R](zip.md)>  



