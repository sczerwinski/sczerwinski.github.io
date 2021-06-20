---
title: filter -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[filter](filter.md)



# filter  
[androidJvm]  
Content  
fun <[T](filter.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](filter.md)>.[filter](filter.md)(predicate: ([T](filter.md)) -> [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](filter.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting only values from this LiveData matching the given [predicate](filter.md).



[predicate](filter.md) will be executed on the main thread.



**Example:**

val resultLiveData: LiveData<Try<User>> = ...  
val successLiveData: LiveData<Try<User>> = resultLiveData.filter { it.isSuccess }  



