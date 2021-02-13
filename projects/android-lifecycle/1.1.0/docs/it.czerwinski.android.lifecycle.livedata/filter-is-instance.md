---
title: filterIsInstance -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[filterIsInstance](filter-is-instance.html)



# filterIsInstance  
[androidJvm]  
Content  
inline fun <[R](filter-is-instance.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<*>.[filterIsInstance](filter-is-instance.html)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](filter-is-instance.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting only values of type [R](filter-is-instance.html) from this LiveData.



**Example:**

val resultLiveData: LiveData<Try<User>> = ...  
val failureLiveData: LiveData<Failure> = resultLiveData.filterIsInstance<Failure>()  



