---
title: defaultIfEmpty -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[defaultIfEmpty](default-if-empty.html)



# defaultIfEmpty  
[androidJvm]  
Content  
fun <[T](default-if-empty.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](default-if-empty.html)>.[defaultIfEmpty](default-if-empty.html)(defaultValue: [T](default-if-empty.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](default-if-empty.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) that emits the values emitted by this LiveData or a specified default value if this LiveData has not yet emitted any values at the time of observing.

  


[androidJvm]  
Content  
fun <[T](default-if-empty.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](default-if-empty.html)>.[defaultIfEmpty](default-if-empty.html)(defaultValueProducer: () -> [T](default-if-empty.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](default-if-empty.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) that emits the values emitted by this LiveData or a value returned by defaultValueProducer if this LiveData has not yet emitted any values at the time of observing.



defaultValueProducer will be executed on the main thread.

  



