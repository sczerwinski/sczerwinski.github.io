---
title: evert -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[evert](evert.md)



# evert  
[Kotlin utilities]  
Brief description  
Moves inner [Option](-option/index.md) outside of the outer [Try](-try/index.md).  
  


#### Return  
[Try](-try/index.md) nested in an [Option](-option/index.md) for an [Option](-option/index.md) nested in a [Try](-try/index.md).  
  


#### Since  
1.4.0  
  
  
Content  
fun <[T](evert.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[Option](-option/index.md)<[T](evert.md)>>.[evert](evert.md)(): [Option](-option/index.md)<[Try](-try/index.md)<[T](evert.md)>>  


[Kotlin utilities]  
Brief description  
Moves inner [Try](-try/index.md) outside of the outer [Option](-option/index.md).  
  


#### Return  
[Option](-option/index.md) nested in a [Try](-try/index.md) for a [Try](-try/index.md) nested in an [Option](-option/index.md).  
  


#### Since  
1.4.0  
  
  
Content  
fun <[T](evert.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Try](-try/index.md)<[T](evert.md)>>.[evert](evert.md)(): [Try](-try/index.md)<[Option](-option/index.md)<[T](evert.md)>>  



