---
title: fold -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.util](../index.html)/[Option](index.html)/[fold](fold.html)



# fold  
[common]  
Brief description  


Returns result of applying transform on the value of [Some](../-some/index.html) or default if this is [None](../-none/index.html).



#### Return  


Result of applying transform on the value of [Some](../-some/index.html) or default if this is [None](../-none/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| default| <br><br>Value to be returned if the option is empty.<br><br>
| transform| <br><br>Function transforming [Some](../-some/index.html) value.<br><br>
  
  
Content  
inline fun <[R](fold.html)> [fold](fold.html)(default: [R](fold.html), transform: ([T](index.html)) -> [R](fold.html)): [R](fold.html)  


[common]  
Brief description  


Returns result of applying transform on the value of [Some](../-some/index.html) or default if this is [None](../-none/index.html).



#### Return  


Result of applying transform on the value of [Some](../-some/index.html) or default if this is [None](../-none/index.html).



## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| default| <br><br>Function producing value to be returned if the option is empty.<br><br>
| transform| <br><br>Function transforming [Some](../-some/index.html) value.<br><br>
  
  
Content  
inline fun <[R](fold.html)> [fold](fold.html)(default: () -> [R](fold.html), transform: ([T](index.html)) -> [R](fold.html)): [R](fold.html)  



