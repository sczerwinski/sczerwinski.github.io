---
title: combineLatest -
---
//[Extensions for Jetpack Lifecycle](../../index.md)/[it.czerwinski.android.lifecycle.livedata](index.md)/[combineLatest](combine-latest.md)



# combineLatest  
[androidJvm]  
Content  
fun <[A](combine-latest.md), [B](combine-latest.md)> [combineLatest](combine-latest.md)(first: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[A](combine-latest.md)>, second: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[B](combine-latest.md)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[A](combine-latest.md)?, [B](combine-latest.md)?>>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting pairs of latest values emitted by the [first](combine-latest.md) and the [second](combine-latest.md) LiveData.



**Example:**

val userLiveData: LiveData<User> = ...  
val avatarUrlLiveData: LiveData<String> = ...  
val userWithAvatar: LiveData<Pair<User?, String?>> = combineLatest(userLiveData, avatarUrlLiveData)  


[androidJvm]  
Content  
fun <[A](combine-latest.md), [B](combine-latest.md), [C](combine-latest.md)> [combineLatest](combine-latest.md)(first: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[A](combine-latest.md)>, second: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[B](combine-latest.md)>, third: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[C](combine-latest.md)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[Triple](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)<[A](combine-latest.md)?, [B](combine-latest.md)?, [C](combine-latest.md)?>>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting triples of latest values emitted by the [first](combine-latest.md), the [second](combine-latest.md) and the [third](combine-latest.md) LiveData.

  


[androidJvm]  
Content  
fun <[T](combine-latest.md)> [combineLatest](combine-latest.md)(vararg sources: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](combine-latest.md)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](combine-latest.md)?>>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting lists of latest values emitted by the given source LiveData.

  


[androidJvm]  
Content  
fun <[A](combine-latest.md), [B](combine-latest.md), [R](combine-latest.md)> [combineLatest](combine-latest.md)(first: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[A](combine-latest.md)>, second: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[B](combine-latest.md)>, combineFunction: ([A](combine-latest.md)?, [B](combine-latest.md)?) -> [R](combine-latest.md)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](combine-latest.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting results of applying the given [combineFunction](combine-latest.md) to the latest values emitted by the [first](combine-latest.md) and the [second](combine-latest.md) LiveData.



[combineFunction](combine-latest.md) will be executed on the main thread.



**Example:**

val userLiveData: LiveData<User> = ...  
val avatarUrlLiveData: LiveData<String> = ...  
val userWithAvatar: LiveData<UserWithAvatar> =  
    combineLatest(userLiveData, avatarUrlLiveData) { user, avatarUrl ->  
        UserWithAvatar(user, avatarUrl)  
    }  


[androidJvm]  
Content  
fun <[A](combine-latest.md), [B](combine-latest.md), [C](combine-latest.md), [R](combine-latest.md)> [combineLatest](combine-latest.md)(first: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[A](combine-latest.md)>, second: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[B](combine-latest.md)>, third: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[C](combine-latest.md)>, combineFunction: ([A](combine-latest.md)?, [B](combine-latest.md)?, [C](combine-latest.md)?) -> [R](combine-latest.md)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](combine-latest.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting results of applying the given [combineFunction](combine-latest.md) to the latest values emitted by the [first](combine-latest.md), the [second](combine-latest.md) and the [third](combine-latest.md) LiveData.



[combineFunction](combine-latest.md) will be executed on the main thread.

  


[androidJvm]  
Content  
fun <[T](combine-latest.md), [R](combine-latest.md)> [combineLatest](combine-latest.md)(vararg sources: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](combine-latest.md)>, combineFunction: ([List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](combine-latest.md)?>) -> [R](combine-latest.md)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](combine-latest.md)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting results of applying the given [combineFunction](combine-latest.md) to the latest values emitted by the given source LiveData.



[combineFunction](combine-latest.md) will be executed on the main thread.

  



