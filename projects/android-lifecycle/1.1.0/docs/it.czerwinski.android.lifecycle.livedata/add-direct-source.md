---
title: addDirectSource -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[addDirectSource](add-direct-source.html)



# addDirectSource  
[androidJvm]  
Content  
@[MainThread](https://developer.android.com/reference/kotlin/androidx/annotation/MainThread.html)()  
  
inline fun <[T](add-direct-source.html)> [MediatorLiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/MediatorLiveData.html)<in [T](add-direct-source.html)>.[addDirectSource](add-direct-source.html)(source: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<out [T](add-direct-source.html)>)  
More info  


Starts to listen the given source LiveData. Whenever source value is changed, it is set as a new value of this [MediatorLiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/MediatorLiveData.html).



If the given LiveData is already added as a source [IllegalArgumentException](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-illegal-argument-exception/index.html) will be thrown.



Equivalent to:

mediatorLiveData.addSource(liveData) { x -> mediatorLiveData.value = x }  



