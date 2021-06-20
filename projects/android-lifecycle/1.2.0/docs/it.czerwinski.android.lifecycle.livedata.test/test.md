---
title: test -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata.test](index.md)/[test](test.md)



# test  
[androidJvm]  
Content  
fun <[T](test.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](test.md)>.[test](test.md)(): [TestObserver](-test-observer/index.md)<[T](test.md)>  
More info  


Creates a non-forwarding [TestObserver](-test-observer/index.md) observing all values emitted by this [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).



#### Since  


1.1.0

  


[androidJvm]  
Content  
fun <[T](test.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](test.md)>.[test](test.md)(downstream: [Observer](https://developer.android.com/reference/kotlin/androidx/lifecycle/Observer.html)<[T](test.md)>): [TestObserver](-test-observer/index.md)<[T](test.md)>  
More info  


Creates a forwarding [TestObserver](-test-observer/index.md) observing all values emitted by this [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html).



#### Since  


1.1.0

  



