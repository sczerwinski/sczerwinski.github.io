---
title: it.czerwinski.android.lifecycle.livedata.test -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata.test](index.md)



# Package it.czerwinski.android.lifecycle.livedata.test  
 [androidJvm] 

Common testing extensions for Jetpack Lifecycle

   


## Types  
  
|  Name |  Summary | 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver///PointingToDeclaration/"></a>[TestObserver](-test-observer/index.md)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>class [TestObserver](-test-observer/index.md)<[T](-test-observer/index.md)> : [Observer](https://developer.android.com/reference/kotlin/androidx/lifecycle/Observer.html)<[T](-test-observer/index.md)>   <br>More info  <br>A callback testing values emitted by [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).  <br><br><br>|


## Functions  
  
|  Name |  Summary | 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test//test/androidx.lifecycle.LiveData[TypeParam(bounds=[kotlin.Any?])]#/PointingToDeclaration/"></a>[test](test.md)| <a name="it.czerwinski.android.lifecycle.livedata.test//test/androidx.lifecycle.LiveData[TypeParam(bounds=[kotlin.Any?])]#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun <[T](test.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](test.md)>.[test](test.md)(): [TestObserver](-test-observer/index.md)<[T](test.md)>  <br>More info  <br>Creates a non-forwarding [TestObserver](-test-observer/index.md) observing all values emitted by this [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).  <br><br><br>[androidJvm]  <br>Content  <br>fun <[T](test.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](test.md)>.[test](test.md)(downstream: [Observer](https://developer.android.com/reference/kotlin/androidx/lifecycle/Observer.html)<[T](test.md)>): [TestObserver](-test-observer/index.md)<[T](test.md)>  <br>More info  <br>Creates a forwarding [TestObserver](-test-observer/index.md) observing all values emitted by this [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).  <br><br><br>|

