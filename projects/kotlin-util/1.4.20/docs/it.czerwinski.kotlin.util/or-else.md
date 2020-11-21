---
title: orElse -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[orElse](or-else.html)



# orElse  
[common]  
Brief description  


Returns this [Option](-option/index.html) if this is a [Some](-some/index.html) or default if this is [None](-none/index.html).



#### Return  


This [Some](-some/index.html) or default.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| default| <br><br>Default [Option](-option/index.html) provider.<br><br>
  
  
Content  
inline fun <[T](or-else.html)> [Option](-option/index.html)<[T](or-else.html)>.[orElse](or-else.html)(default: () -> [Option](-option/index.html)<[T](or-else.html)>): [Option](-option/index.html)<[T](or-else.html)>  


[common]  
Brief description  


Returns this [Try](-try/index.html) if this is a [Success](-success/index.html) or default if this is a [Failure](-failure/index.html).



#### Return  


This [Success](-success/index.html) or default.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| default| <br><br>Default [Try](-try/index.html) provider.<br><br>
  
  
Content  
inline fun <[T](or-else.html)> [Try](-try/index.html)<[T](or-else.html)>.[orElse](or-else.html)(default: () -> [Try](-try/index.html)<[T](or-else.html)>): [Try](-try/index.html)<[T](or-else.html)>  



