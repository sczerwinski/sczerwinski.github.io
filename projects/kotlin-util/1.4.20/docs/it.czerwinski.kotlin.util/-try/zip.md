---
title: zip -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Try](index.html)/[zip](zip.html)



# zip  
[common]  
Brief description  


Returns [Success](../-success/index.html) containing a Pair of values of this and [other](index.html) if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).



#### Return  


[Success](../-success/index.html) containing a Pair of values of this and [other](index.html) if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).



#### Since  


1.1



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| other| <br><br>Other [Try](index.html).<br><br>
  
  
Content  
infix fun <[R](zip.html)> [zip](zip.html)(other: [Try](index.html)<[R](zip.html)>): [Try](index.html)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.html), [R](zip.html)>>  


[common]  
Brief description  


Returns [Success](../-success/index.html) containing the result of applying transform to both values of this and [other](index.html) if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).



#### Return  


[Success](../-success/index.html) containing the result of applying transform to both values of this and [other](index.html) if both instances of [Try](index.html) are [Success](../-success/index.html). Otherwise returns first [Failure](../-failure/index.html).



#### Since  


1.1



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| other| <br><br>Other [Try](index.html).<br><br>
| transform| <br><br>Function transforming values of both instances of [Success](../-success/index.html).<br><br>
  
  
Content  
inline fun <[T1](zip.html), [R](zip.html)> [zip](zip.html)(other: [Try](index.html)<[T1](zip.html)>, transform: ([T](index.html), [T1](zip.html)) -> [R](zip.html)): [Try](index.html)<[R](zip.html)>  



