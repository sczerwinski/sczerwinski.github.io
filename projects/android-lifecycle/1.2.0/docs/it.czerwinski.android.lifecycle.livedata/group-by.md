---
title: groupBy -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[groupBy](group-by.md)



# groupBy  
[androidJvm]  
Content  
fun <[K](group-by.md), [V](group-by.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[V](group-by.md)>.[groupBy](group-by.md)(keySelector: ([V](group-by.md)) -> [K](group-by.md)): [GroupedLiveData](-grouped-live-data/index.md)<[K](group-by.md), [V](group-by.md)>  
More info  


Returns a [GroupedLiveData](-grouped-live-data/index.md) providing a set of [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html), each emitting a different subset of values from this LiveData, based on the result of the given [keySelector](group-by.md) function.



[keySelector](group-by.md) will be executed on the main thread.



**Example:**

val userLiveData: LiveData<User> = ...  
val userByStatusLiveData: GroupedLiveData<UserStatus, User> = errorLiveData.groupBy { user -> user.status }  
val activeUserLiveData: LiveData<User> = userByStatusLiveData[UserStatus.ACTIVE]  



