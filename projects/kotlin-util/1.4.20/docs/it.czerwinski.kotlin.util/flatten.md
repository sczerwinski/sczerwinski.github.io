---
title: flatten -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[flatten](flatten.html)



# flatten  
[common]  
Brief description  


Extracts an [Option](-option/index.html) nested in the [Try](-try/index.html) to a not nested [Option](-option/index.html).



#### Return  


[Option](-option/index.html) nested in a [Success](-success/index.html) or [None](-none/index.html) if this is a [Failure](-failure/index.html).

  
Content  
fun <[T](flatten.html)> [Try](-try/index.html)<[Option](-option/index.html)<[T](flatten.html)>>.[flatten](flatten.html)(): [Option](-option/index.html)<[T](flatten.html)>  


[common]  
Brief description  


Returns [Some](-some/index.html) if this [Some](-some/index.html) contains a [Success](-success/index.html). Otherwise returns [None](-none/index.html).



#### Return  


[Some](-some/index.html) if this [Some](-some/index.html) contains a [Success](-success/index.html). Otherwise returns [None](-none/index.html).

  
Content  
fun <[T](flatten.html)> [Option](-option/index.html)<[Try](-try/index.html)<[T](flatten.html)>>.[flatten](flatten.html)(): [Option](-option/index.html)<[T](flatten.html)>  


[common]  
Brief description  


Returns nested [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) if this is [Some](-some/index.html). Otherwise returns an empty [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).



#### Return  


Nested [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) if this is [Some](-some/index.html). Otherwise returns an empty [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).

  
Content  
fun <[T](flatten.html)> [Option](-option/index.html)<[Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](flatten.html)>>.[flatten](flatten.html)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](flatten.html)>  


[common]  
Brief description  


Returns [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) of values of each [Some](-some/index.html) in this [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).



#### Return  


[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) of values of each [Some](-some/index.html) in this [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).

  
Content  
fun <[T](flatten.html)> [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[Option](-option/index.html)<[T](flatten.html)>>.[flatten](flatten.html)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](flatten.html)>  


[common]  
Brief description  


Transforms a nested [Option](-option/index.html) to a not nested [Option](-option/index.html).



#### Return  


[Option](-option/index.html) nested in a [Some](-some/index.html) or [None](-none/index.html) if this option is empty.

  
Content  
fun <[T](flatten.html)> [Option](-option/index.html)<[Option](-option/index.html)<[T](flatten.html)>>.[flatten](flatten.html)(): [Option](-option/index.html)<[T](flatten.html)>  


[common]  
Brief description  


Transforms a nested [Try](-try/index.html) to a not nested [Try](-try/index.html).



#### Return  


[Try](-try/index.html) nested in a [Success](-success/index.html) or this object if this is a [Failure](-failure/index.html).

  
Content  
fun <[T](flatten.html)> [Try](-try/index.html)<[Try](-try/index.html)<[T](flatten.html)>>.[flatten](flatten.html)(): [Try](-try/index.html)<[T](flatten.html)>  



