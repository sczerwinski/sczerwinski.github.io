---
title: merge -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[merge](merge.md)



# merge  
[androidJvm]  
Content  
infix fun <[T](merge.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.md)>.[merge](merge.md)(other: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.md)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting each value emitted by either this or [other](merge.md) LiveData.



**Example:**

val serverError: LiveData<String> = ...  
val databaseError: LiveData<String> = ...  
val error: LiveData<String> = serverError merge databaseError  


[androidJvm]  
Content  
fun <[T](merge.md)> [merge](merge.md)(vararg sources: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.md)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting each value emitted by any of the given LiveData.



**Example:**

val serverError: LiveData<String> = ...  
val databaseError: LiveData<String> = ...  
val fileError: LiveData<String> = ...  
val error: LiveData<String> = merge(serverError, databaseError, fileError)  



