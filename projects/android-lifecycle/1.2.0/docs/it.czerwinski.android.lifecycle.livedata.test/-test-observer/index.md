---
title: TestObserver -
---
//[Extensions for Jetpack Lifecycle](../../../index.md)/[it.czerwinski.android.lifecycle.livedata.test](../index.md)/[TestObserver](index.md)



# TestObserver  
 [androidJvm] class [TestObserver](index.md)<[T](index.md)> : [Observer](https://developer.android.com/reference/kotlin/androidx/lifecycle/Observer.html)<[T](index.md)> 

A callback testing values emitted by [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).



#### Since  


1.1.0

   


## Types  
  
|  Name |  Summary | 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver.Companion///PointingToDeclaration/"></a>[Companion](-companion/index.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver.Companion///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>object [Companion](-companion/index.md)  <br><br><br>|


## Functions  
  
|  Name |  Summary | 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertNoValues/#/PointingToDeclaration/"></a>[assertNoValues](assert-no-values.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertNoValues/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertNoValues](assert-no-values.md)(): [TestObserver](index.md)<[T](index.md)>  <br>More info  <br>Assert that this observer received no [onChanged](on-changed.md) events.  <br><br><br>|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValue/#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[assertValue](assert-value.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValue/#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValue](assert-value.md)(value: [T](index.md)): [TestObserver](index.md)<[T](index.md)>  <br>More info  <br>Asserts that this observer received exactly one [onChanged](on-changed.md) value, equal to the given [value](assert-value.md).  <br><br><br>[androidJvm]  <br>Content  <br>fun [assertValue](assert-value.md)(predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [TestObserver](index.md)<[T](index.md)>  <br>More info  <br>Asserts that this observer received exactly one [onChanged](on-changed.md) value, for which the given [predicate](assert-value.md) returns true.  <br><br><br>|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueAt/#kotlin.Int#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[assertValueAt](assert-value-at.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueAt/#kotlin.Int#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValueAt](assert-value-at.md)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), value: [T](index.md)): [TestObserver](index.md)<[T](index.md)>  <br>More info  <br>Asserts that this observer received an [onChanged](on-changed.md) value at the given [index](assert-value-at.md), equal to the given [value](assert-value-at.md).  <br><br><br>[androidJvm]  <br>Content  <br>fun [assertValueAt](assert-value-at.md)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), predicate: ([T](index.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [TestObserver](index.md)<[T](index.md)>  <br>More info  <br>Asserts that this observer received an [onChanged](on-changed.md) value at the given [index](assert-value-at.md), for which the given [predicate](assert-value-at.md) returns true.  <br><br><br>|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueCount/#kotlin.Int/PointingToDeclaration/"></a>[assertValueCount](assert-value-count.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueCount/#kotlin.Int/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValueCount](assert-value-count.md)(count: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)): [TestObserver](index.md)<[T](index.md)>  <br>More info  <br>Assert that this observer received the specified number [onChanged](on-changed.md) events.  <br><br><br>|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValues/#kotlin.Array[TypeParam(bounds=[kotlin.Any?])]/PointingToDeclaration/"></a>[assertValues](assert-values.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValues/#kotlin.Array[TypeParam(bounds=[kotlin.Any?])]/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValues](assert-values.md)(vararg values: [T](index.md)): [TestObserver](index.md)<[T](index.md)>  <br>fun [assertValues](assert-values.md)(values: [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](index.md)>): [TestObserver](index.md)<[T](index.md)>  <br>More info  <br>Asserts that this observer received only the specified [values](assert-values.md) in the exact specified order.  <br><br><br>|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueSet/#kotlin.collections.Collection[TypeParam(bounds=[kotlin.Any?])]/PointingToDeclaration/"></a>[assertValueSet](assert-value-set.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueSet/#kotlin.collections.Collection[TypeParam(bounds=[kotlin.Any?])]/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValueSet](assert-value-set.md)(values: [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<[T](index.md)>): [TestObserver](index.md)<[T](index.md)>  <br>More info  <br>Asserts that this observer received only the specified [values](assert-value-set.md), irrespective of the order.  <br><br><br>|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/onChanged/#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[onChanged](on-changed.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/onChanged/#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open override fun [onChanged](on-changed.md)(t: [T](index.md))  <br>More info  <br>Called when the observed [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emits a new value.  <br><br><br>|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/valueCount/#/PointingToDeclaration/"></a>[valueCount](value-count.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/valueCount/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [valueCount](value-count.md)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br>More info  <br>Returns the number of received [onChanged](on-changed.md) values.  <br><br><br>|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/values/#/PointingToDeclaration/"></a>[values](values.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/values/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [values](values.md)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](index.md)>  <br>More info  <br>Returns a list of received [onChanged](on-changed.md) values.  <br><br><br>|

