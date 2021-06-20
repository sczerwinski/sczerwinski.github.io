---
title: reduceNotNull -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[reduceNotNull](reduce-not-null.md)



# reduceNotNull  
[androidJvm]  
Content  
fun <[T](reduce-not-null.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](reduce-not-null.md)>.[reduceNotNull](reduce-not-null.md)(operation: ([T](reduce-not-null.md), [T](reduce-not-null.md)) -> [T](reduce-not-null.md)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](reduce-not-null.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting non-null accumulated value starting with the first non-null value emitted by this LiveData and applying [operation](reduce-not-null.md) from left to right to current accumulator value and each subsequent non-null value emitted by this LiveData.



[operation](reduce-not-null.md) will be executed on the main thread.



**Example:**

val newOperationsCountLiveData: LiveData<Int> = ...  
val operationsCountLiveData: LiveData<Int> =  
    newOperationsCountLiveData.reduceNotNull { acc, next -> acc + next }  



