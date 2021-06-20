---
title: filterIsInstance -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[filterIsInstance](filter-is-instance.md)



# filterIsInstance  
[androidJvm]  
Content  
inline fun <[R](filter-is-instance.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<*>.[filterIsInstance](filter-is-instance.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](filter-is-instance.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting only values of type [R](filter-is-instance.md) from this LiveData.



**Example:**

val resultLiveData: LiveData<Try<User>> = ...  
val failureLiveData: LiveData<Failure> = resultLiveData.filterIsInstance<Failure>()  



