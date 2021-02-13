---
title: delayStart -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[delayStart](delay-start.html)



# delayStart  
[androidJvm]  
Content  
fun <[T](delay-start.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](delay-start.html)>.[delayStart](delay-start.html)(timeInMillis: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), context: [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) = EmptyCoroutineContext): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](delay-start.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting values from this LiveData, after dropping values followed by newer values before timeInMillis expires since the result LiveData has been created. The values emitted after timeInMillis are not affected.



Delay will be applied on a thread determined by the given context.



**Example:**

val resultLiveData: LiveData<ResultData> = ...  
val delayedResultLiveData: LiveData<ResultData> = resultLiveData.delayStart(  
    timeInMillis = 1000L,  
    context = viewModelScope.coroutineContext  
)  



