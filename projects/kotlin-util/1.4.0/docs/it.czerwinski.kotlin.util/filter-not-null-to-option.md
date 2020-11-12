---
title: filterNotNullToOption -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[filterNotNullToOption](filter-not-null-to-option.md)



# filterNotNullToOption  
[Kotlin utilities]  
Brief description  
Returns [Some](-some/index.md) containing the same [Right](-right/index.md) if its value is not null. Otherwise returns [None](-none/index.md).  
  


#### Return  
[Some](-some/index.md) containing the same [Right](-right/index.md) if its value is not null. Otherwise returns [None](-none/index.md).  
  


#### Since  
1.3  
  
  
Content  
fun <[L](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)??>.[filterNotNullToOption](filter-not-null-to-option.md)(): [Option](-option/index.md)<[Either](-either/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)>>  


[Kotlin utilities]  
Brief description  
Returns [Some](-some/index.md) containing the same [Left](-left/index.md) if its value is not null. Otherwise returns [None](-none/index.md).  
  


#### Return  
[Some](-some/index.md) containing the same [Left](-left/index.md) if its value is not null. Otherwise returns [None](-none/index.md).  
  
  
Content  
fun <[L](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](filter-not-null-to-option.md)??, [R](filter-not-null-to-option.md)>.[filterNotNullToOption](filter-not-null-to-option.md)(): [Option](-option/index.md)<[Either](-either/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)>>  


[Kotlin utilities]  
Brief description  
Returns [Some](-some/index.md) containing the same [Right](-right/index.md) if its value is not null. Otherwise returns [None](-none/index.md).  
  


#### Return  
[Some](-some/index.md) containing the same [Right](-right/index.md) if its value is not null. Otherwise returns [None](-none/index.md).  
  
  
Content  
fun <[L](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null-to-option.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)??>.[filterNotNullToOption](filter-not-null-to-option.md)(): [Option](-option/index.md)<[Either](-either/index.md)<[L](filter-not-null-to-option.md), [R](filter-not-null-to-option.md)>>  



