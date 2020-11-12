---
title: filterIsInstance -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Either](index.html)/[filterIsInstance](filter-is-instance.html)



# filterIsInstance  
[common]  
Brief description  


Returns the same [Right](../-right/index.html) casted to type [T](filter-is-instance.html) if it is [T](filter-is-instance.html). Otherwise returns null.



#### Return  


The same [Right](../-right/index.html) casted to type [T](filter-is-instance.html) if it is [T](filter-is-instance.html). Otherwise returns null.



#### Since  


1.3



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| T| <br><br>Required type of the optional value.<br><br>
  
  
Content  
inline fun <[T](filter-is-instance.html)> [filterIsInstance](filter-is-instance.html)(): [Either](index.html)<[L](index.html), [T](filter-is-instance.html)>?  



