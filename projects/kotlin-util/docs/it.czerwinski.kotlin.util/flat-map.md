---
title: flatMap -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[flatMap](flat-map.md)



# flatMap  
[Kotlin utilities]  
Brief description  
Maps value of this [Right](-right/index.md) to a new [Either](-either/index.md) using [transform]().  
  


#### Return  
[Either](-either/index.md) mapped using [transform]() or this object if this is a [Left](-left/index.md).  
  


#### Since  
1.3  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming a [Right](-right/index.md) to an [Either](-either/index.md).
  
  
Content  
inline fun <[L](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [T](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](flat-map.md), [R](flat-map.md)>.[flatMap](flat-map.md)(transform: ([R](flat-map.md)) -> [Either](-either/index.md)<[L](flat-map.md), [T](flat-map.md)>): [Either](-either/index.md)<[L](flat-map.md), [T](flat-map.md)>  


[Kotlin utilities]  
Brief description  
Maps value of this [Left](-left/index.md) to a new [Either](-either/index.md) using [transform]().  
  


#### Return  
[Either](-either/index.md) mapped using [transform]() or this object if this is a [Right](-right/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming a [Left](-left/index.md) to an [Either](-either/index.md).
  
  
Content  
inline fun <[L](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [T](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](flat-map.md), [R](flat-map.md)>.[flatMap](flat-map.md)(transform: ([L](flat-map.md)) -> [Either](-either/index.md)<[T](flat-map.md), [R](flat-map.md)>): [Either](-either/index.md)<[T](flat-map.md), [R](flat-map.md)>  


[Kotlin utilities]  
Brief description  
Maps value of this [Right](-right/index.md) to a new [Either](-either/index.md) using [transform]().  
  


#### Return  
[Either](-either/index.md) mapped using [transform]() or this object if this is a [Left](-left/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| transform| Function transforming a [Right](-right/index.md) to an [Either](-either/index.md).
  
  
Content  
inline fun <[L](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [T](flat-map.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](flat-map.md), [R](flat-map.md)>.[flatMap](flat-map.md)(transform: ([R](flat-map.md)) -> [Either](-either/index.md)<[L](flat-map.md), [T](flat-map.md)>): [Either](-either/index.md)<[L](flat-map.md), [T](flat-map.md)>  



