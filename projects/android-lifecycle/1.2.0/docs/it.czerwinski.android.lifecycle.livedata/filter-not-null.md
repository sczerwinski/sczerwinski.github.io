---
title: filterNotNull -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[filterNotNull](filter-not-null.md)



# filterNotNull  
[androidJvm]  
Content  
fun <[T](filter-not-null.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](filter-not-null.md)?>.[filterNotNull](filter-not-null.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](filter-not-null.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting only non-null values from this LiveData.



**Example:**

val userLiveData: LiveData<User?> = ...  
val nonNullUserLiveData: LiveData<User> = userLiveData.filterNotNull()  



