---
title: filterNotNull -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[filterNotNull](filter-not-null.html)



# filterNotNull  
[common]  
Brief description  


Returns the same [Right](-right/index.html) if its value is not null. Otherwise returns null.



#### Return  


The same [Right](-right/index.html) if its value is not null. Otherwise returns null.



#### Since  


1.3

  
Content  
fun <[L](filter-not-null.html), [R](filter-not-null.html)> [Either](-either/index.html)<[L](filter-not-null.html), [R](filter-not-null.html)?>.[filterNotNull](filter-not-null.html)(): [Either](-either/index.html)<[L](filter-not-null.html), [R](filter-not-null.html)>?  


[common]  
Brief description  


Returns the same [Left](-left/index.html) if its value is not null. Otherwise returns null.



#### Return  


The same [Left](-left/index.html) if its value is not null. Otherwise returns null.

  
Content  
fun <[L](filter-not-null.html), [R](filter-not-null.html)> [LeftProjection](-left-projection/index.html)<[L](filter-not-null.html)?, [R](filter-not-null.html)>.[filterNotNull](filter-not-null.html)(): [Either](-either/index.html)<[L](filter-not-null.html), [R](filter-not-null.html)>?  


[common]  
Brief description  


Returns the same [Right](-right/index.html) if its value is not null. Otherwise returns null.



#### Return  


The same [Right](-right/index.html) if its value is not null. Otherwise returns null.

  
Content  
fun <[L](filter-not-null.html), [R](filter-not-null.html)> [RightProjection](-right-projection/index.html)<[L](filter-not-null.html), [R](filter-not-null.html)?>.[filterNotNull](filter-not-null.html)(): [Either](-either/index.html)<[L](filter-not-null.html), [R](filter-not-null.html)>?  


[common]  
Brief description  


Returns the same [Success](-success/index.html) if its value is not null. Otherwise returns a [Failure](-failure/index.html).



#### Return  


The same [Success](-success/index.html) if its value is not null. Otherwise returns a [Failure](-failure/index.html).

  
Content  
fun <[T](filter-not-null.html)> [Try](-try/index.html)<[T](filter-not-null.html)?>.[filterNotNull](filter-not-null.html)(): [Try](-try/index.html)<[T](filter-not-null.html)>  



