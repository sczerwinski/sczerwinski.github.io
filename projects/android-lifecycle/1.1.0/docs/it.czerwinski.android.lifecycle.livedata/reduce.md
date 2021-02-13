---
title: reduce -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[reduce](reduce.html)



# reduce  
[androidJvm]  
Content  
fun <[T](reduce.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](reduce.html)?>.[reduce](reduce.html)(operation: ([T](reduce.html)?, [T](reduce.html)?) -> [T](reduce.html)?): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](reduce.html)?>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting accumulated value starting with the first value emitted by this LiveData and applying operation from left to right to current accumulator value and each value emitted by this.



operation will be executed on the main thread.



**Example:**

val newOperationsCountLiveData: LiveData<Int?> = ...  
val operationsCountLiveData: LiveData<Int?> =  
    newOperationsCountLiveData.reduce { acc, next -> if (next == null) null else acc + next }  



