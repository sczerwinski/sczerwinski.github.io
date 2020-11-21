---
title: evert -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[evert](evert.html)



# evert  
[common]  
Brief description  


Moves inner [Option](-option/index.html) outside of the outer [Try](-try/index.html).



#### Return  


[Try](-try/index.html) nested in an [Option](-option/index.html) for an [Option](-option/index.html) nested in a [Try](-try/index.html).



#### Since  


1.4.0

  
Content  
fun <[T](evert.html)> [Try](-try/index.html)<[Option](-option/index.html)<[T](evert.html)>>.[evert](evert.html)(): [Option](-option/index.html)<[Try](-try/index.html)<[T](evert.html)>>  


[common]  
Brief description  


Moves inner [Try](-try/index.html) outside of the outer [Option](-option/index.html).



#### Return  


[Option](-option/index.html) nested in a [Try](-try/index.html) for a [Try](-try/index.html) nested in an [Option](-option/index.html).



#### Since  


1.4.0

  
Content  
fun <[T](evert.html)> [Option](-option/index.html)<[Try](-try/index.html)<[T](evert.html)>>.[evert](evert.html)(): [Try](-try/index.html)<[Option](-option/index.html)<[T](evert.html)>>  



