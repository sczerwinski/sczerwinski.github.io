---
title: joinLeft -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[joinLeft](join-left.md)



# joinLeft  
[Kotlin utilities]  
Brief description  
Returns this if this is [Right](-right/index.md). Otherwise returns value of [Left](-left/index.md).Requires [Left](-left/index.md) to be an [Either](-either/index.md).  
  


#### Return  
This if this is [Right](-right/index.md). Otherwise returns value of [Left](-left/index.md).  
  
  
Content  
fun <[L](join-left.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](join-left.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[Either](-either/index.md)<[L](join-left.md), [R](join-left.md)>, [R](join-left.md)>.[joinLeft](join-left.md)(): [Either](-either/index.md)<[L](join-left.md), [R](join-left.md)>  



