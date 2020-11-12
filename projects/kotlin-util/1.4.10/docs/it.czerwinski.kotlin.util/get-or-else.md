---
title: getOrElse -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[getOrElse](get-or-else.html)



# getOrElse  
[common]  
Brief description  


Gets value of this [Right](-right/index.html) or default value if this is [Left](-left/index.html).



#### Return  


Value of this [Right](-right/index.html) or default.



#### Since  


1.3



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| default| <br><br>Default value provider.<br><br>
  
  
Content  
inline fun <[L](get-or-else.html), [R](get-or-else.html)> [Either](-either/index.html)<[L](get-or-else.html), [R](get-or-else.html)>.[getOrElse](get-or-else.html)(default: () -> [R](get-or-else.html)): [R](get-or-else.html)  


[common]  
Brief description  


Gets value of this [Left](-left/index.html) or default value if this is [Right](-right/index.html).



#### Return  


Value of this [Left](-left/index.html) or default.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| default| <br><br>Default value provider.<br><br>
  
  
Content  
inline fun <[L](get-or-else.html), [R](get-or-else.html)> [LeftProjection](-left-projection/index.html)<[L](get-or-else.html), [R](get-or-else.html)>.[getOrElse](get-or-else.html)(default: () -> [L](get-or-else.html)): [L](get-or-else.html)  


[common]  
Brief description  


Gets value of this [Right](-right/index.html) or default value if this is [Left](-left/index.html).



#### Return  


Value of this [Right](-right/index.html) or default.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| default| <br><br>Default value provider.<br><br>
  
  
Content  
inline fun <[L](get-or-else.html), [R](get-or-else.html)> [RightProjection](-right-projection/index.html)<[L](get-or-else.html), [R](get-or-else.html)>.[getOrElse](get-or-else.html)(default: () -> [R](get-or-else.html)): [R](get-or-else.html)  


[common]  
Brief description  


Gets the value of a [Some](-some/index.html) or default value if this is [None](-none/index.html).



#### Return  


Value of a [Some](-some/index.html) or default value.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| default| <br><br>Default value provider.<br><br>
  
  
Content  
inline fun <[T](get-or-else.html)> [Option](-option/index.html)<[T](get-or-else.html)>.[getOrElse](get-or-else.html)(default: () -> [T](get-or-else.html)): [T](get-or-else.html)  


[common]  
Brief description  


Gets the value of a [Success](-success/index.html) or default value if this is a [Failure](-failure/index.html).



#### Return  


Value of a [Success](-success/index.html) or default value.



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| default| <br><br>Default value provider.<br><br>
  
  
Content  
inline fun <[T](get-or-else.html)> [Try](-try/index.html)<[T](get-or-else.html)>.[getOrElse](get-or-else.html)(default: () -> [T](get-or-else.html)): [T](get-or-else.html)  



