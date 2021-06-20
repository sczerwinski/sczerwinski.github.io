---
title: throttleWithTimeout -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[throttleWithTimeout](throttle-with-timeout.md)



# throttleWithTimeout  
[androidJvm]  
Content  
fun <[T](throttle-with-timeout.md)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](throttle-with-timeout.md)>.[throttleWithTimeout](throttle-with-timeout.md)(timeInMillis: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), context: [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) = EmptyCoroutineContext): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](throttle-with-timeout.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting values from this LiveData, after dropping values followed by newer values before [timeInMillis](throttle-with-timeout.md) expires.



Delay will be applied on a thread determined by the given [context](throttle-with-timeout.md).



**Example:**

val isLoadingLiveData: LiveData<Boolean> = ...  
val isLoadingThrottledLiveData: LiveData<Boolean> = isLoadingLiveData.throttleWithTimeout(  
    timeInMillis = 1000L,  
    context = viewModelScope.coroutineContext  
)  



