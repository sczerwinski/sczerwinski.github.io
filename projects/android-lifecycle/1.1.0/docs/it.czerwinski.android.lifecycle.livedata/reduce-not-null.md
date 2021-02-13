---
title: reduceNotNull -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[reduceNotNull](reduce-not-null.html)



# reduceNotNull  
[androidJvm]  
Content  
fun <[T](reduce-not-null.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](reduce-not-null.html)>.[reduceNotNull](reduce-not-null.html)(operation: ([T](reduce-not-null.html), [T](reduce-not-null.html)) -> [T](reduce-not-null.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](reduce-not-null.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting non-null accumulated value starting with the first non-null value emitted by this LiveData and applying operation from left to right to current accumulator value and each subsequent non-null value emitted by this LiveData.



operation will be executed on the main thread.



**Example:**

val newOperationsCountLiveData: LiveData<Int> = ...  
val operationsCountLiveData: LiveData<Int> =  
    newOperationsCountLiveData.reduceNotNull { acc, next -> acc + next }  



