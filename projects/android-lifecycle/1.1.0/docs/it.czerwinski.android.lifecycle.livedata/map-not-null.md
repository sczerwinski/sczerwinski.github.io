---
title: mapNotNull -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[mapNotNull](map-not-null.html)



# mapNotNull  
[androidJvm]  
Content  
fun <[T](map-not-null.html), [R](map-not-null.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](map-not-null.html)>.[mapNotNull](map-not-null.html)(transform: ([T](map-not-null.html)) -> [R](map-not-null.html)?): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](map-not-null.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting only the non-null results of applying the given transform function to each value emitted by this LiveData.



transform will be executed on the main thread.



**Example:**

val userOptionLiveData: LiveData<Option<User>> = ...  
val userLiveData: LiveData<User> = userOptionLiveData.mapNotNull { user -> user.getOrNull() }  



