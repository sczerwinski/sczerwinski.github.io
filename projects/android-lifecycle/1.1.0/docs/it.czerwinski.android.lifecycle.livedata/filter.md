---
title: filter -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[filter](filter.html)



# filter  
[androidJvm]  
Content  
fun <[T](filter.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](filter.html)>.[filter](filter.html)(predicate: ([T](filter.html)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](filter.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting only values from this LiveData matching the given predicate.



predicate will be executed on the main thread.



**Example:**

val resultLiveData: LiveData<Try<User>> = ...  
val successLiveData: LiveData<Try<User>> = resultLiveData.filter { it.isSuccess }  



