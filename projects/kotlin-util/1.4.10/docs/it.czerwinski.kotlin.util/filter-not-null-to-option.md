---
title: filterNotNullToOption -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[filterNotNullToOption](filter-not-null-to-option.html)



# filterNotNullToOption  
[common]  
Brief description  


Returns [Some](-some/index.html) containing the same [Right](-right/index.html) if its value is not null. Otherwise returns [None](-none/index.html).



#### Return  


[Some](-some/index.html) containing the same [Right](-right/index.html) if its value is not null. Otherwise returns [None](-none/index.html).



#### Since  


1.3

  
Content  
fun <[L](filter-not-null-to-option.html), [R](filter-not-null-to-option.html)> [Either](-either/index.html)<[L](filter-not-null-to-option.html), [R](filter-not-null-to-option.html)?>.[filterNotNullToOption](filter-not-null-to-option.html)(): [Option](-option/index.html)<[Either](-either/index.html)<[L](filter-not-null-to-option.html), [R](filter-not-null-to-option.html)>>  


[common]  
Brief description  


Returns [Some](-some/index.html) containing the same [Left](-left/index.html) if its value is not null. Otherwise returns [None](-none/index.html).



#### Return  


[Some](-some/index.html) containing the same [Left](-left/index.html) if its value is not null. Otherwise returns [None](-none/index.html).

  
Content  
fun <[L](filter-not-null-to-option.html), [R](filter-not-null-to-option.html)> [LeftProjection](-left-projection/index.html)<[L](filter-not-null-to-option.html)?, [R](filter-not-null-to-option.html)>.[filterNotNullToOption](filter-not-null-to-option.html)(): [Option](-option/index.html)<[Either](-either/index.html)<[L](filter-not-null-to-option.html), [R](filter-not-null-to-option.html)>>  


[common]  
Brief description  


Returns [Some](-some/index.html) containing the same [Right](-right/index.html) if its value is not null. Otherwise returns [None](-none/index.html).



#### Return  


[Some](-some/index.html) containing the same [Right](-right/index.html) if its value is not null. Otherwise returns [None](-none/index.html).

  
Content  
fun <[L](filter-not-null-to-option.html), [R](filter-not-null-to-option.html)> [RightProjection](-right-projection/index.html)<[L](filter-not-null-to-option.html), [R](filter-not-null-to-option.html)?>.[filterNotNullToOption](filter-not-null-to-option.html)(): [Option](-option/index.html)<[Either](-either/index.html)<[L](filter-not-null-to-option.html), [R](filter-not-null-to-option.html)>>  



