---
title: throttleWithTimeout -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[throttleWithTimeout](throttle-with-timeout.html)



# throttleWithTimeout  
[androidJvm]  
Content  
fun <[T](throttle-with-timeout.html)> [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](throttle-with-timeout.html)>.[throttleWithTimeout](throttle-with-timeout.html)(timeInMillis: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), context: [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) = EmptyCoroutineContext): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](throttle-with-timeout.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting values from this LiveData, after dropping values followed by newer values before timeInMillis expires.



Delay will be applied on a thread determined by the given context.



**Example:**

val isLoadingLiveData: LiveData<Boolean> = ...  
val isLoadingThrottledLiveData: LiveData<Boolean> = isLoadingLiveData.throttleWithTimeout(  
    timeInMillis = 1000L,  
    context = viewModelScope.coroutineContext  
)  



