---
title: joinRight -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[joinRight](join-right.html)



# joinRight  
[common]  
Brief description  




Returns this if this is [Left](-left/index.html). Otherwise returns value of [Right](-right/index.html).



Requires [Right](-right/index.html) to be an [Either](-either/index.html).





#### Return  


This if this is [Left](-left/index.html). Otherwise returns value of [Right](-right/index.html).

  
Content  
fun <[L](join-right.html), [R](join-right.html)> [Either](-either/index.html)<[L](join-right.html), [Either](-either/index.html)<[L](join-right.html), [R](join-right.html)>>.[joinRight](join-right.html)(): [Either](-either/index.html)<[L](join-right.html), [R](join-right.html)>  



