---
title: intervalLiveData -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[intervalLiveData](interval-live-data.md)



# intervalLiveData  
[androidJvm]  
Content  
fun [intervalLiveData](interval-live-data.md)(timeInMillis: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), context: [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) = EmptyCoroutineContext): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting a sequence of integer values, spaced by a given [timeInMillis](interval-live-data.md).



Delay between subsequent emissions will be applied on a thread determined by the given [context](interval-live-data.md).



**Example:**

val intervalLiveData: LiveData<Int> = intervalLiveData(timeInMillis = 1000L)

#### Since  


1.2.0

  


[androidJvm]  
Content  
fun [intervalLiveData](interval-live-data.md)(context: [CoroutineContext](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.coroutines/-coroutine-context/index.html) = EmptyCoroutineContext, timeInMillis: ([Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)) -> [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting a sequence of integer values, spaced by a result of a given [timeInMillis](interval-live-data.md) function invoked on the next value.



Delay between subsequent emissions will be applied on a thread determined by the given [context](interval-live-data.md).



**Example:**

val intervalLiveData: LiveData<Int> = intervalLiveData { index -> (index + 1) * 1000L }

#### Since  


1.2.0

  



