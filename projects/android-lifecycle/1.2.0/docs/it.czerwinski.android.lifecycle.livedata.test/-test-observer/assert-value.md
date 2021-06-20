---
title: assertValue -
---
//[Extensions for Jetpack Lifecycle](../../../index.md)/[it.czerwinski.android.lifecycle.livedata.test](../index.md)/[TestObserver](index.md)/[assertValue](assert-value.md)



# assertValue  
[androidJvm]  
Content  
fun [assertValue](assert-value.md)(value: [T](index.md)): [TestObserver](index.md)<[T](index.md)>  
More info  


Asserts that this observer received exactly one [onChanged](on-changed.md) value, equal to the given [value](assert-value.md).

  


[androidJvm]  
Content  
fun [assertValue](assert-value.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [TestObserver](index.md)<[T](index.md)>  
More info  


Asserts that this observer received exactly one [onChanged](on-changed.md) value, for which the given [predicate](assert-value.md) returns true.

  



