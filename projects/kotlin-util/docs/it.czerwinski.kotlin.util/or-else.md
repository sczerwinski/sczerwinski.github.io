---
title: orElse -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[orElse](or-else.md)



# orElse  
[Kotlin utilities]  
Brief description  
Returns this [Option](-option/index.md) if this is a [Some](-some/index.md) or [default]() if this is [None](-none/index.md).  
  


#### Return  
This [Some](-some/index.md) or [default]().  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| default| Default [Option](-option/index.md) provider.
  
  
Content  
inline fun <[T](or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[T](or-else.md)>.[orElse](or-else.md)(default: () -> [Option](-option/index.md)<[T](or-else.md)>): [Option](-option/index.md)<[T](or-else.md)>  


[Kotlin utilities]  
Brief description  
Returns this [Try](-try/index.md) if this is a [Success](-success/index.md) or [default]() if this is a [Failure](-failure/index.md).  
  


#### Return  
This [Success](-success/index.md) or [default]().  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| default| Default [Try](-try/index.md) provider.
  
  
Content  
inline fun <[T](or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](or-else.md)>.[orElse](or-else.md)(default: () -> [Try](-try/index.md)<[T](or-else.md)>): [Try](-try/index.md)<[T](or-else.md)>  



