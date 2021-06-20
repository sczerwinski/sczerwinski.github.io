---
title: reduce -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[reduce](reduce.md)



# reduce  
[androidJvm]  
Content  
fun <[T](reduce.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](reduce.md)?>.[reduce](reduce.md)(operation: ([T](reduce.md)?, [T](reduce.md)?) -> [T](reduce.md)?): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](reduce.md)?>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting accumulated value starting with the first value emitted by this LiveData and applying [operation](reduce.md) from left to right to current accumulator value and each value emitted by this.



[operation](reduce.md) will be executed on the main thread.



**Example:**

val newOperationsCountLiveData: LiveData<Int?> = ...  
val operationsCountLiveData: LiveData<Int?> =  
    newOperationsCountLiveData.reduce { acc, next -> if (next == null) null else acc + next }  



