---
title: assertValueAt -
---
//[Extensions for Jetpack Lifecycle](../../index.html)/[it.czerwinski.android.lifecycle.livedata.test](../index.html)/[TestObserver](index.html)/[assertValueAt](assert-value-at.html)



# assertValueAt  
[androidJvm]  
Content  
fun [assertValueAt](assert-value-at.html)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), value: [T](index.html)): [TestObserver](index.html)<[T](index.html)>  
More info  


Asserts that this observer received an [onChanged](on-changed.html) value at the given index, equal to the given value.

  


[androidJvm]  
Content  
fun [assertValueAt](assert-value-at.html)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [TestObserver](index.html)<[T](index.html)>  
More info  


Asserts that this observer received an [onChanged](on-changed.html) value at the given index, for which the given predicate returns true.

  



