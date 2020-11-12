---
title: zip -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Option](index.html)/[zip](zip.html)



# zip  
[common]  
Brief description  


Returns [Some](../-some/index.html) containing a Pair of values of this and [other](index.html) if both [Option](index.html)s are [Some](../-some/index.html). Otherwise returns [None](../-none/index.html).



#### Return  


[Some](../-some/index.html) containing a Pair of values of this and [other](index.html) if both [Option](index.html)s are [Some](../-some/index.html). Otherwise returns [None](../-none/index.html).



#### Since  


1.1



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| other| <br><br>Other [Option](index.html).<br><br>
  
  
Content  
infix fun <[R](zip.html)> [zip](zip.html)(other: [Option](index.html)<[R](zip.html)>): [Option](index.html)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[T](index.html), [R](zip.html)>>  


[common]  
Brief description  


Returns [Some](../-some/index.html) containing the result of applying transform to both values of this and [other](index.html) if both [Option](index.html)s are [Some](../-some/index.html). Otherwise returns [None](../-none/index.html).



#### Return  


[Some](../-some/index.html) containing the result of applying transform to both values of this and [other](index.html) if both [Option](index.html)s are [Some](../-some/index.html). Otherwise returns [None](../-none/index.html).



#### Since  


1.1



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| other| <br><br>Other [Option](index.html).<br><br>
| transform| <br><br>Function transforming values of both [Some](../-some/index.html).<br><br>
  
  
Content  
inline fun <[T1](zip.html), [R](zip.html)> [zip](zip.html)(other: [Option](index.html)<[T1](zip.html)>, transform: ([T](index.html), [T1](zip.html)) -> [R](zip.html)): [Option](index.html)<[R](zip.html)>  



