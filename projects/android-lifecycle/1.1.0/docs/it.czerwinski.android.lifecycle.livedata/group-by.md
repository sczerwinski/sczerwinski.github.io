---
title: groupBy -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[groupBy](group-by.html)



# groupBy  
[androidJvm]  
Content  
fun <[K](group-by.html), [V](group-by.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[V](group-by.html)>.[groupBy](group-by.html)(keySelector: ([V](group-by.html)) -> [K](group-by.html)): [GroupedLiveData](-grouped-live-data/index.html)<[K](group-by.html), [V](group-by.html)>  
More info  


Returns a [GroupedLiveData](-grouped-live-data/index.html) providing a set of [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html), each emitting a different subset of values from this LiveData, based on the result of the given keySelector function.



keySelector will be executed on the main thread.



**Example:**

val userLiveData: LiveData<User> = ...  
val userByStatusLiveData: GroupedLiveData<UserStatus, User> = errorLiveData.groupBy { user -> user.status }  
val activeUserLiveData: LiveData<User> = userByStatusLiveData[UserStatus.ACTIVE]  



