---
title: invoke -
---
//[kotlin-util](../../../index.md)/[it.czerwinski.kotlin.util](../../index.md)/[Try](../index.md)/[Companion](index.md)/[invoke](invoke.md)



# invoke  
[Kotlin utilities]  
Brief description  
Creates a new [Try](../index.md) based on the result of the [callable]().  
  


#### Return  
An instance of [Success](../../-success/index.md) or [Failure](../../-failure/index.md), depending on whether the operation.  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| callable| A callable operation.
  
  
Content  
inline operator fun <[T](invoke.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [invoke](invoke.md)(callable: () -> [T](invoke.md)): [Try](../index.md)<[T](invoke.md)>  



