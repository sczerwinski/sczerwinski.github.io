---
title: invoke -
---
//[Kotlin utilities](../../../index.html)/[it.czerwinski.kotlin.util](../../index.html)/[Try](../index.html)/[Companion](index.html)/[invoke](invoke.html)



# invoke  
[common]  
Brief description  


Creates a new [Try](../index.html) based on the result of the callable.



#### Return  


An instance of [Success](../../-success/index.html) or [Failure](../../-failure/index.html), depending on whether the operation.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| callable| <br><br>A callable operation.<br><br>
  
  
Content  
inline operator fun <[T](invoke.html)> [invoke](invoke.html)(callable: () -> [T](invoke.html)): [Try](../index.html)<[T](invoke.html)>  



