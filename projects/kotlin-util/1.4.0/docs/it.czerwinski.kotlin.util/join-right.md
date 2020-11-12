---
title: joinRight -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[joinRight](join-right.md)



# joinRight  
[Kotlin utilities]  
Brief description  
Returns this if this is [Left](-left/index.md). Otherwise returns value of [Right](-right/index.md).Requires [Right](-right/index.md) to be an [Either](-either/index.md).  
  


#### Return  
This if this is [Left](-left/index.md). Otherwise returns value of [Right](-right/index.md).  
  
  
Content  
fun <[L](join-right.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](join-right.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](join-right.md), [Either](-either/index.md)<[L](join-right.md), [R](join-right.md)>>.[joinRight](join-right.md)(): [Either](-either/index.md)<[L](join-right.md), [R](join-right.md)>  



