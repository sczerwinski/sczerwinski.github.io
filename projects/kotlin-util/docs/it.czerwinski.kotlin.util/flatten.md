---
title: flatten -
---
//[kotlin-util](../index.md)/[it.czerwinski.kotlin.util](index.md)/[flatten](flatten.md)



# flatten  
[Kotlin utilities]  
Brief description  
Extracts an [Option](-option/index.md) nested in the [Try](-try/index.md) to a not nested [Option](-option/index.md).  
  


#### Return  
[Option](-option/index.md) nested in a [Success](-success/index.md) or [None](-none/index.md) if this is a [Failure](-failure/index.md).  
  
  
Content  
fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[Option](-option/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [Option](-option/index.md)<[T](flatten.md)>  


[Kotlin utilities]  
Brief description  
Returns [Some](-some/index.md) if this [Some](-some/index.md) contains a [Success](-success/index.md). Otherwise returns [None](-none/index.md).  
  


#### Return  
[Some](-some/index.md) if this [Some](-some/index.md) contains a [Success](-success/index.md). Otherwise returns [None](-none/index.md).  
  
  
Content  
fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Try](-try/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [Option](-option/index.md)<[T](flatten.md)>  


[Kotlin utilities]  
Brief description  
Returns nested [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) if this is [Some](-some/index.md). Otherwise returns an empty [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).  
  


#### Return  
Nested [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) if this is [Some](-some/index.md). Otherwise returns an empty [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).  
  
  
Content  
fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](flatten.md)>>.[flatten](flatten.md)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](flatten.md)>  


[Kotlin utilities]  
Brief description  
Returns [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) of values of each [Some](-some/index.md) in this [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).  
  


#### Return  
[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html) of values of each [Some](-some/index.md) in this [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/index.html).  
  
  
Content  
fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[Option](-option/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](flatten.md)>  


[Kotlin utilities]  
Brief description  
Transforms a nested [Option](-option/index.md) to a not nested [Option](-option/index.md).  
  


#### Return  
[Option](-option/index.md) nested in a [Some](-some/index.md) or [None](-none/index.md) if this option is empty.  
  
  
Content  
fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Option](-option/index.md)<[Option](-option/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [Option](-option/index.md)<[T](flatten.md)>  


[Kotlin utilities]  
Brief description  
Transforms a nested [Try](-try/index.md) to a not nested [Try](-try/index.md).  
  


#### Return  
[Try](-try/index.md) nested in a [Success](-success/index.md) or this object if this is a [Failure](-failure/index.md).  
  
  
Content  
fun <[T](flatten.md) : [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?> [Try](-try/index.md)<[Try](-try/index.md)<[T](flatten.md)>>.[flatten](flatten.md)(): [Try](-try/index.md)<[T](flatten.md)>  



