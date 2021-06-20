---
title: defaultIfEmpty -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[defaultIfEmpty](default-if-empty.md)



# defaultIfEmpty  
[androidJvm]  
Content  
fun <[T](default-if-empty.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](default-if-empty.md)>.[defaultIfEmpty](default-if-empty.md)(defaultValue: [T](default-if-empty.md)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](default-if-empty.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) that emits the values emitted by this LiveData or a specified default value if this LiveData has not yet emitted any values at the time of observing.

  


[androidJvm]  
Content  
fun <[T](default-if-empty.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](default-if-empty.md)>.[defaultIfEmpty](default-if-empty.md)(defaultValueProducer: () -> [T](default-if-empty.md)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](default-if-empty.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) that emits the values emitted by this LiveData or a value returned by [defaultValueProducer](default-if-empty.md) if this LiveData has not yet emitted any values at the time of observing.



[defaultValueProducer](default-if-empty.md) will be executed on the main thread.

  



