---
title: getOrElse -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[getOrElse](get-or-else.md)



# getOrElse  
[Kotlin utilities]  
Brief description  
Gets value of this [Right](-right/index.md) or [default]() value if this is [Left](-left/index.md).  
  


#### Return  
Value of this [Right](-right/index.md) or [default]().  
  


#### Since  
1.3  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| default| Default value provider.
  
  
Content  
inline fun <[L](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](get-or-else.md), [R](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [R](get-or-else.md)): [R](get-or-else.md)  


[Kotlin utilities]  
Brief description  
Gets value of this [Left](-left/index.md) or [default]() value if this is [Right](-right/index.md).  
  


#### Return  
Value of this [Left](-left/index.md) or [default]().  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| default| Default value provider.
  
  
Content  
inline fun <[L](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](get-or-else.md), [R](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [L](get-or-else.md)): [L](get-or-else.md)  


[Kotlin utilities]  
Brief description  
Gets value of this [Right](-right/index.md) or [default]() value if this is [Left](-left/index.md).  
  


#### Return  
Value of this [Right](-right/index.md) or [default]().  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| default| Default value provider.
  
  
Content  
inline fun <[L](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](get-or-else.md), [R](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [R](get-or-else.md)): [R](get-or-else.md)  


[Kotlin utilities]  
Brief description  
Gets the value of a [Some](-some/index.md) or [default]() value if this is [None](-none/index.md).  
  


#### Return  
Value of a [Some](-some/index.md) or [default]() value.  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| default| Default value provider.
  
  
Content  
inline fun <[T](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[T](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [T](get-or-else.md)): [T](get-or-else.md)  


[Kotlin utilities]  
Brief description  
Gets the value of a [Success](-success/index.md) or [default]() value if this is a [Failure](-failure/index.md).  
  


#### Return  
Value of a [Success](-success/index.md) or [default]() value.  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| default| Default value provider.
  
  
Content  
inline fun <[T](get-or-else.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](get-or-else.md)>.[getOrElse](get-or-else.md)(default: () -> [T](get-or-else.md)): [T](get-or-else.md)  



