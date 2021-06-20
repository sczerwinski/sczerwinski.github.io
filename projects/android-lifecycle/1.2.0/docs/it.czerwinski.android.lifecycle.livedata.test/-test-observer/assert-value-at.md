---
title: assertValueAt -
---
//[Extensions for Jetpack Lifecycle](../../../index.md)/[it.czerwinski.android.lifecycle.livedata.test](../index.md)/[TestObserver](index.md)/[assertValueAt](assert-value-at.md)



# assertValueAt  
[androidJvm]  
Content  
fun [assertValueAt](assert-value-at.md)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), value: [T](index.md)): [TestObserver](index.md)<[T](index.md)>  
More info  


Asserts that this observer received an [onChanged](on-changed.md) value at the given [index](assert-value-at.md), equal to the given [value](assert-value-at.md).

  


[androidJvm]  
Content  
fun [assertValueAt](assert-value-at.md)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [TestObserver](index.md)<[T](index.md)>  
More info  


Asserts that this observer received an [onChanged](on-changed.md) value at the given [index](assert-value-at.md), for which the given [predicate](assert-value-at.md) returns true.

  



