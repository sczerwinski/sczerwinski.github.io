---
title: mapNotNull -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[mapNotNull](map-not-null.md)



# mapNotNull  
[androidJvm]  
Content  
fun <[T](map-not-null.md), [R](map-not-null.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](map-not-null.md)>.[mapNotNull](map-not-null.md)(transform: ([T](map-not-null.md)) -> [R](map-not-null.md)?): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](map-not-null.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting only the non-null results of applying the given [transform](map-not-null.md) function to each value emitted by this LiveData.



[transform](map-not-null.md) will be executed on the main thread.



**Example:**

val userOptionLiveData: LiveData<Option<User>> = ...  
val userLiveData: LiveData<User> = userOptionLiveData.mapNotNull { user -> user.getOrNull() }  



