---
title: TestObserver -
---
//[Extensions for Jetpack Lifecycle](../../index.html)/[it.czerwinski.android.lifecycle.livedata.test](../index.html)/[TestObserver](index.html)



# TestObserver  
 [androidJvm] class [TestObserver](index.html)<[T](index.html)> : [Observer](https://developer.android.com/reference/kotlin/androidx/lifecycle/Observer.html)<[T](index.html)> 

A callback testing values emitted by [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).



#### Since  


1.1.0

   


## Types  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver.Companion///PointingToDeclaration/"></a>[Companion](-companion/index.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver.Companion///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>object [Companion](-companion/index.html)  <br><br><br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertNoValues/#/PointingToDeclaration/"></a>[assertNoValues](assert-no-values.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertNoValues/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertNoValues](assert-no-values.html)(): [TestObserver](index.html)<[T](index.html)>  <br>More info  <br>Assert that this observer received no [onChanged](on-changed.html) events.  <br><br><br>
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValue/#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[assertValue](assert-value.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValue/#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValue](assert-value.html)(value: [T](index.html)): [TestObserver](index.html)<[T](index.html)>  <br>More info  <br>Asserts that this observer received exactly one [onChanged](on-changed.html) value, equal to the given value.  <br><br><br>[androidJvm]  <br>Content  <br>fun [assertValue](assert-value.html)(predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [TestObserver](index.html)<[T](index.html)>  <br>More info  <br>Asserts that this observer received exactly one [onChanged](on-changed.html) value, for which the given predicate returns true.  <br><br><br>
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueAt/#kotlin.Int#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[assertValueAt](assert-value-at.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueAt/#kotlin.Int#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValueAt](assert-value-at.html)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), value: [T](index.html)): [TestObserver](index.html)<[T](index.html)>  <br>More info  <br>Asserts that this observer received an [onChanged](on-changed.html) value at the given index, equal to the given value.  <br><br><br>[androidJvm]  <br>Content  <br>fun [assertValueAt](assert-value-at.html)(index: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html), predicate: ([T](index.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [TestObserver](index.html)<[T](index.html)>  <br>More info  <br>Asserts that this observer received an [onChanged](on-changed.html) value at the given index, for which the given predicate returns true.  <br><br><br>
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueCount/#kotlin.Int/PointingToDeclaration/"></a>[assertValueCount](assert-value-count.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueCount/#kotlin.Int/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValueCount](assert-value-count.html)(count: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)): [TestObserver](index.html)<[T](index.html)>  <br>More info  <br>Assert that this observer received the specified number [onChanged](on-changed.html) events.  <br><br><br>
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValues/#kotlin.Array[TypeParam(bounds=[kotlin.Any?])]/PointingToDeclaration/"></a>[assertValues](assert-values.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValues/#kotlin.Array[TypeParam(bounds=[kotlin.Any?])]/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValues](assert-values.html)(vararg values: [T](index.html)): [TestObserver](index.html)<[T](index.html)>  <br>fun [assertValues](assert-values.html)(values: [Iterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterable/index.html)<[T](index.html)>): [TestObserver](index.html)<[T](index.html)>  <br>More info  <br>Asserts that this observer received only the specified [values](values.html) in the exact specified order.  <br><br><br>
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueSet/#kotlin.collections.Collection[TypeParam(bounds=[kotlin.Any?])]/PointingToDeclaration/"></a>[assertValueSet](assert-value-set.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/assertValueSet/#kotlin.collections.Collection[TypeParam(bounds=[kotlin.Any?])]/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [assertValueSet](assert-value-set.html)(values: [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<[T](index.html)>): [TestObserver](index.html)<[T](index.html)>  <br>More info  <br>Asserts that this observer received only the specified [values](values.html), irrespective of the order.  <br><br><br>
| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[equals](-companion/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F-30514213)| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open operator fun [equals](-companion/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F-30514213)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[hashCode](-companion/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F-30514213)| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [hashCode](-companion/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F-30514213)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/onChanged/#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[onChanged](on-changed.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/onChanged/#TypeParam(bounds=[kotlin.Any?])/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open override fun [onChanged](on-changed.html)(t: [T](index.html))  <br>More info  <br>Called when the observed [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emits a new value.  <br><br><br>
| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[toString](-companion/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F-30514213)| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [toString](-companion/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F-30514213)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/valueCount/#/PointingToDeclaration/"></a>[valueCount](value-count.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/valueCount/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [valueCount](value-count.html)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br>More info  <br>Returns the number of received [onChanged](on-changed.html) values.  <br><br><br>
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/values/#/PointingToDeclaration/"></a>[values](values.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver/values/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [values](values.html)(): [List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](index.html)>  <br>More info  <br>Returns a list of received [onChanged](on-changed.html) values.  <br><br><br>

