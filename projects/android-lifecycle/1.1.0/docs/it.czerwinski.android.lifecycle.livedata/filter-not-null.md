---
title: filterNotNull -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[filterNotNull](filter-not-null.html)



# filterNotNull  
[androidJvm]  
Content  
fun <[T](filter-not-null.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](filter-not-null.html)?>.[filterNotNull](filter-not-null.html)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](filter-not-null.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting only non-null values from this LiveData.



**Example:**

val userLiveData: LiveData<User?> = ...  
val nonNullUserLiveData: LiveData<User> = userLiveData.filterNotNull()  



