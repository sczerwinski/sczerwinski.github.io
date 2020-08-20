---
title: filterNotNull -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[filterNotNull](filter-not-null.md)



# filterNotNull  
[Kotlin utilities]  
Brief description  
Returns the same [Right](-right/index.md) if its value is not null. Otherwise returns null.  
  


#### Return  
The same [Right](-right/index.md) if its value is not null. Otherwise returns null.  
  


#### Since  
1.3  
  
  
Content  
fun <[L](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Either](-either/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)??>.[filterNotNull](filter-not-null.md)(): [Either](-either/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)>?  


[Kotlin utilities]  
Brief description  
Returns the same [Left](-left/index.md) if its value is not null. Otherwise returns null.  
  


#### Return  
The same [Left](-left/index.md) if its value is not null. Otherwise returns null.  
  
  
Content  
fun <[L](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [LeftProjection](-left-projection/index.md)<[L](filter-not-null.md)??, [R](filter-not-null.md)>.[filterNotNull](filter-not-null.md)(): [Either](-either/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)>?  


[Kotlin utilities]  
Brief description  
Returns the same [Right](-right/index.md) if its value is not null. Otherwise returns null.  
  


#### Return  
The same [Right](-right/index.md) if its value is not null. Otherwise returns null.  
  
  
Content  
fun <[L](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [R](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [RightProjection](-right-projection/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)??>.[filterNotNull](filter-not-null.md)(): [Either](-either/index.md)<[L](filter-not-null.md), [R](filter-not-null.md)>?  


[Kotlin utilities]  
Brief description  
Returns the same [Success](-success/index.md) if its value is not null. Otherwise returns a [Failure](-failure/index.md).  
  


#### Return  
The same [Success](-success/index.md) if its value is not null. Otherwise returns a [Failure](-failure/index.md).  
  
  
Content  
fun <[T](filter-not-null.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[T](filter-not-null.md)??>.[filterNotNull](filter-not-null.md)(): [Try](-try/index.md)<[T](filter-not-null.md)>  



