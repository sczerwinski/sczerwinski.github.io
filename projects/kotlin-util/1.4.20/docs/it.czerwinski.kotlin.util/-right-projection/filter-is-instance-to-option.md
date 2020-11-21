---
title: filterIsInstanceToOption -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[RightProjection](index.html)/[filterIsInstanceToOption](filter-is-instance-to-option.html)



# filterIsInstanceToOption  
[common]  
Brief description  


Returns [Some](../-some/index.html) containing the same [Right](../-right/index.html) casted to type [T](filter-is-instance-to-option.html) if it is [T](filter-is-instance-to-option.html). Otherwise returns [None](../-none/index.html).



#### Return  


[Some](../-some/index.html) containing the same [Right](../-right/index.html) casted to type [T](filter-is-instance-to-option.html) if it is [T](filter-is-instance-to-option.html). Otherwise returns [None](../-none/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| T| <br><br>Required type of the optional value.<br><br>
  
  
Content  
inline fun <[T](filter-is-instance-to-option.html)> [filterIsInstanceToOption](filter-is-instance-to-option.html)(): [Option](../-option/index.html)<[Either](../-either/index.html)<[L](index.html), [T](filter-is-instance-to-option.html)>>  



