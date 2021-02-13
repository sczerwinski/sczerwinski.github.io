---
title: test -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata.test](index.html)/[test](test.html)



# test  
[androidJvm]  
Content  
fun <[T](test.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](test.html)>.[test](test.html)(): [TestObserver](-test-observer/index.html)<[T](test.html)>  
More info  


Creates a non-forwarding [TestObserver](-test-observer/index.html) observing all values emitted by this [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).



#### Since  


1.1.0

  


[androidJvm]  
Content  
fun <[T](test.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](test.html)>.[test](test.html)(downstream: [Observer](https://developer.android.com/reference/kotlin/androidx/lifecycle/Observer.html)<[T](test.html)>): [TestObserver](-test-observer/index.html)<[T](test.html)>  
More info  


Creates a forwarding [TestObserver](-test-observer/index.html) observing all values emitted by this [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).



#### Since  


1.1.0

  



