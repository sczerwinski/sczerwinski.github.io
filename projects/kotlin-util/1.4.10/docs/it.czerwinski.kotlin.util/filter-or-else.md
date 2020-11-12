---
title: filterOrElse -
---
//[Kotlin utilities](../index.html)/[it.czerwinski.kotlin.util](index.html)/[filterOrElse](filter-or-else.html)



# filterOrElse  
[common]  
Brief description  


Returns the same [Right](-right/index.html) if the predicate is satisfied for the value, Left(zero) if the predicate is not satisfied for the value, or the same [Left](-left/index.html) if this is [Left](-left/index.html).



#### Return  


The same [Right](-right/index.html) if the predicate is satisfied for the value, Left(zero) if the predicate is not satisfied for the value, or the same [Left](-left/index.html) if this is [Left](-left/index.html).



#### Since  


1.3



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
| zero| <br><br>Provider of the value used if the predicate is not satisfied.<br><br>
  
  
Content  
inline fun <[L](filter-or-else.html), [R](filter-or-else.html)> [Either](-either/index.html)<[L](filter-or-else.html), [R](filter-or-else.html)>.[filterOrElse](filter-or-else.html)(predicate: ([R](filter-or-else.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [L](filter-or-else.html)): [Either](-either/index.html)<[L](filter-or-else.html), [R](filter-or-else.html)>?  


[common]  
Brief description  


Returns the same [Left](-left/index.html) if the predicate is satisfied for the value, Right(zero) if the predicate is not satisfied for the value, or the same [Right](-right/index.html) if this is [Right](-right/index.html).



#### Return  


The same [Left](-left/index.html) if the predicate is satisfied for the value, Right(zero) if the predicate is not satisfied for the value, or the same [Right](-right/index.html) if this is [Right](-right/index.html).



#### Since  


1.2



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
| zero| <br><br>Provider of the value used if the predicate is not satisfied.<br><br>
  
  
Content  
inline fun <[L](filter-or-else.html), [R](filter-or-else.html)> [LeftProjection](-left-projection/index.html)<[L](filter-or-else.html), [R](filter-or-else.html)>.[filterOrElse](filter-or-else.html)(predicate: ([L](filter-or-else.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [R](filter-or-else.html)): [Either](-either/index.html)<[L](filter-or-else.html), [R](filter-or-else.html)>?  


[common]  
Brief description  


Returns the same [Right](-right/index.html) if the predicate is satisfied for the value, Left(zero) if the predicate is not satisfied for the value, or the same [Left](-left/index.html) if this is [Left](-left/index.html).



#### Return  


The same [Right](-right/index.html) if the predicate is satisfied for the value, Left(zero) if the predicate is not satisfied for the value, or the same [Left](-left/index.html) if this is [Left](-left/index.html).



#### Since  


1.2



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| predicate| <br><br>Predicate function.<br><br>
| zero| <br><br>Provider of the value used if the predicate is not satisfied.<br><br>
  
  
Content  
inline fun <[L](filter-or-else.html), [R](filter-or-else.html)> [RightProjection](-right-projection/index.html)<[L](filter-or-else.html), [R](filter-or-else.html)>.[filterOrElse](filter-or-else.html)(predicate: ([R](filter-or-else.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html), zero: () -> [L](filter-or-else.html)): [Either](-either/index.html)<[L](filter-or-else.html), [R](filter-or-else.html)>?  



