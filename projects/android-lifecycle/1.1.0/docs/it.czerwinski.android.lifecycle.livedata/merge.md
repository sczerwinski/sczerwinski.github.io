---
title: merge -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[merge](merge.html)



# merge  
[androidJvm]  
Content  
infix fun <[T](merge.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.html)>.[merge](merge.html)(other: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.html)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting each value emitted by either this or other LiveData.



**Example:**

val serverError: LiveData<String> = ...  
val databaseError: LiveData<String> = ...  
val error: LiveData<String> = serverError merge databaseError  


[androidJvm]  
Content  
fun <[T](merge.html)> [merge](merge.html)(vararg sources: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.html)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](merge.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting each value emitted by any of the given LiveData.



**Example:**

val serverError: LiveData<String> = ...  
val databaseError: LiveData<String> = ...  
val fileError: LiveData<String> = ...  
val error: LiveData<String> = merge(serverError, databaseError, fileError)  



