---
title: addDirectSource -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[addDirectSource](add-direct-source.md)



# addDirectSource  
[androidJvm]  
Content  
@[MainThread](https://developer.android.com/reference/kotlin/androidx/annotation/MainThread.html)()  
  
inline fun <[T](add-direct-source.md)> [MediatorLiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/MediatorLiveData.html)<in [T](add-direct-source.md)>.[addDirectSource](add-direct-source.md)(source: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<out [T](add-direct-source.md)>)  
More info  


Starts to listen the given [source](add-direct-source.md) LiveData. Whenever [source](add-direct-source.md) value is changed, it is set as a new value of this [MediatorLiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/MediatorLiveData.html).



If the given LiveData is already added as a source [IllegalArgumentException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-illegal-argument-exception/index.html) will be thrown.



Equivalent to:

mediatorLiveData.addSource(liveData) { x -> mediatorLiveData.value = x }  



