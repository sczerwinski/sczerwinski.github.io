---
title: assertValue -
---
//[Extensions for Jetpack Lifecycle](../../index.html)/[it.czerwinski.android.lifecycle.livedata.test](../index.html)/[TestObserver](index.html)/[assertValue](assert-value.html)



# assertValue  
[androidJvm]  
Content  
fun [assertValue](assert-value.html)(value: [T](index.html)): [TestObserver](index.html)<[T](index.html)>  
More info  


Asserts that this observer received exactly one [onChanged](on-changed.html) value, equal to the given value.

  


[androidJvm]  
Content  
fun [assertValue](assert-value.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [TestObserver](index.html)<[T](index.html)>  
More info  


Asserts that this observer received exactly one [onChanged](on-changed.html) value, for which the given predicate returns true.

  



