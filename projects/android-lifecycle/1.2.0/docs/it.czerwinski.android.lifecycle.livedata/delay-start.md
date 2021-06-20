---
title: delayStart -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[delayStart](delay-start.md)



# delayStart  
[androidJvm]  
Content  
fun <[T](delay-start.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](delay-start.md)>.[delayStart](delay-start.md)(timeInMillis: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), context: [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) = EmptyCoroutineContext): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](delay-start.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting values from this LiveData, after dropping values followed by newer values before [timeInMillis](delay-start.md) expires since the result LiveData has been created. The values emitted after [timeInMillis](delay-start.md) are not affected.



Delay will be applied on a thread determined by the given [context](delay-start.md).



**Example:**

val resultLiveData: LiveData<ResultData> = ...  
val delayedResultLiveData: LiveData<ResultData> = resultLiveData.delayStart(  
    timeInMillis = 1000L,  
    context = viewModelScope.coroutineContext  
)  



