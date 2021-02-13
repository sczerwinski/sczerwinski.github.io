---
title: it.czerwinski.android.lifecycle.livedata.test -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata.test](index.html)



# Package it.czerwinski.android.lifecycle.livedata.test  
 [androidJvm] 

Common testing extensions for Jetpack Lifecycle

   


## Types  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver///PointingToDeclaration/"></a>[TestObserver](-test-observer/index.html)| <a name="it.czerwinski.android.lifecycle.livedata.test/TestObserver///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>class [TestObserver](-test-observer/index.html)<[T](-test-observer/index.html)> : [Observer](https://developer.android.com/reference/kotlin/androidx/lifecycle/Observer.html)<[T](-test-observer/index.html)>   <br>More info  <br>A callback testing values emitted by [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).  <br><br><br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test//test/androidx.lifecycle.LiveData[TypeParam(bounds=[kotlin.Any?])]#/PointingToDeclaration/"></a>[test](test.html)| <a name="it.czerwinski.android.lifecycle.livedata.test//test/androidx.lifecycle.LiveData[TypeParam(bounds=[kotlin.Any?])]#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun <[T](test.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](test.html)>.[test](test.html)(): [TestObserver](-test-observer/index.html)<[T](test.html)>  <br>More info  <br>Creates a non-forwarding [TestObserver](-test-observer/index.html) observing all values emitted by this [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).  <br><br><br>[androidJvm]  <br>Content  <br>fun <[T](test.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](test.html)>.[test](test.html)(downstream: [Observer](https://developer.android.com/reference/kotlin/androidx/lifecycle/Observer.html)<[T](test.html)>): [TestObserver](-test-observer/index.html)<[T](test.html)>  <br>More info  <br>Creates a forwarding [TestObserver](-test-observer/index.html) observing all values emitted by this [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).  <br><br><br>

