---
title: flatMap -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[flatMap](flat-map.html)



# flatMap  
[common]  
Brief description  


Maps value of this [Right](-right/index.html) to a new [Either](-either/index.html) using transform.



#### Return  


[Either](-either/index.html) mapped using transform or this object if this is a [Left](-left/index.html).



#### Since  


1.3



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming a [Right](-right/index.html) to an [Either](-either/index.html).<br><br>
  
  
Content  
inline fun <[L](flat-map.html), [R](flat-map.html), [T](flat-map.html)> [Either](-either/index.html)<[L](flat-map.html), [R](flat-map.html)>.[flatMap](flat-map.html)(transform: ([R](flat-map.html)) -> [Either](-either/index.html)<[L](flat-map.html), [T](flat-map.html)>): [Either](-either/index.html)<[L](flat-map.html), [T](flat-map.html)>  


[common]  
Brief description  


Maps value of this [Left](-left/index.html) to a new [Either](-either/index.html) using transform.



#### Return  


[Either](-either/index.html) mapped using transform or this object if this is a [Right](-right/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming a [Left](-left/index.html) to an [Either](-either/index.html).<br><br>
  
  
Content  
inline fun <[L](flat-map.html), [R](flat-map.html), [T](flat-map.html)> [LeftProjection](-left-projection/index.html)<[L](flat-map.html), [R](flat-map.html)>.[flatMap](flat-map.html)(transform: ([L](flat-map.html)) -> [Either](-either/index.html)<[T](flat-map.html), [R](flat-map.html)>): [Either](-either/index.html)<[T](flat-map.html), [R](flat-map.html)>  


[common]  
Brief description  


Maps value of this [Right](-right/index.html) to a new [Either](-either/index.html) using transform.



#### Return  


[Either](-either/index.html) mapped using transform or this object if this is a [Left](-left/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| transform| <br><br>Function transforming a [Right](-right/index.html) to an [Either](-either/index.html).<br><br>
  
  
Content  
inline fun <[L](flat-map.html), [R](flat-map.html), [T](flat-map.html)> [RightProjection](-right-projection/index.html)<[L](flat-map.html), [R](flat-map.html)>.[flatMap](flat-map.html)(transform: ([R](flat-map.html)) -> [Either](-either/index.html)<[L](flat-map.html), [T](flat-map.html)>): [Either](-either/index.html)<[L](flat-map.html), [T](flat-map.html)>  



