---
title: forEach -
---
//[kotlin-util](../../index.md)/[it.czerwinski.kotlin.util](../index.md)/[Success](index.md)/[forEach](for-each.md)



# forEach  
[Kotlin utilities]  
Brief description  
Runs [action]() if this is a [Success](index.md). Returns [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) without any action if this is a [Failure](../-failure/index.md).  
  


## Parameters  
  
Kotlin utilities  
  
|  Name|  Summary| 
|---|---|
| action| Action to be run on a value of a [Success](index.md).
  
  
Content  
open override fun [forEach](for-each.md)(action: ([T](index.md)) -> [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html))  



