---
title: combineLatest -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata](index.html)/[combineLatest](combine-latest.html)



# combineLatest  
[androidJvm]  
Content  
fun <[A](combine-latest.html), [B](combine-latest.html)> [combineLatest](combine-latest.html)(first: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[A](combine-latest.html)>, second: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[B](combine-latest.html)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[Pair](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)<[A](combine-latest.html)?, [B](combine-latest.html)?>>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting pairs of latest values emitted by the first and the second LiveData.



**Example:**

val userLiveData: LiveData<User> = ...  
val avatarUrlLiveData: LiveData<String> = ...  
val userWithAvatar: LiveData<Pair<User?, String?>> = combineLatest(userLiveData, avatarUrlLiveData)  


[androidJvm]  
Content  
fun <[A](combine-latest.html), [B](combine-latest.html), [C](combine-latest.html)> [combineLatest](combine-latest.html)(first: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[A](combine-latest.html)>, second: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[B](combine-latest.html)>, third: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[C](combine-latest.html)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[Triple](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)<[A](combine-latest.html)?, [B](combine-latest.html)?, [C](combine-latest.html)?>>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting triples of latest values emitted by the first, the second and the third LiveData.

  


[androidJvm]  
Content  
fun <[T](combine-latest.html)> [combineLatest](combine-latest.html)(vararg sources: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](combine-latest.html)>): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](combine-latest.html)?>>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting lists of latest values emitted by the given source LiveData.

  


[androidJvm]  
Content  
fun <[A](combine-latest.html), [B](combine-latest.html), [R](combine-latest.html)> [combineLatest](combine-latest.html)(first: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[A](combine-latest.html)>, second: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[B](combine-latest.html)>, combineFunction: ([A](combine-latest.html)?, [B](combine-latest.html)?) -> [R](combine-latest.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](combine-latest.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting results of applying the given combineFunction to the latest values emitted by the first and the second LiveData.



combineFunction will be executed on the main thread.



**Example:**

val userLiveData: LiveData<User> = ...  
val avatarUrlLiveData: LiveData<String> = ...  
val userWithAvatar: LiveData<UserWithAvatar> =  
    combineLatest(userLiveData, avatarUrlLiveData) { user, avatarUrl ->  
        UserWithAvatar(user, avatarUrl)  
    }  


[androidJvm]  
Content  
fun <[A](combine-latest.html), [B](combine-latest.html), [C](combine-latest.html), [R](combine-latest.html)> [combineLatest](combine-latest.html)(first: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[A](combine-latest.html)>, second: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[B](combine-latest.html)>, third: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[C](combine-latest.html)>, combineFunction: ([A](combine-latest.html)?, [B](combine-latest.html)?, [C](combine-latest.html)?) -> [R](combine-latest.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](combine-latest.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting results of applying the given combineFunction to the latest values emitted by the first, the second and the third LiveData.



combineFunction will be executed on the main thread.

  


[androidJvm]  
Content  
fun <[T](combine-latest.html), [R](combine-latest.html)> [combineLatest](combine-latest.html)(vararg sources: [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[T](combine-latest.html)>, combineFunction: ([List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)<[T](combine-latest.html)?>) -> [R](combine-latest.html)): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)<[R](combine-latest.html)>  
More info  


Returns a [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html) emitting results of applying the given combineFunction to the latest values emitted by the given source LiveData.



combineFunction will be executed on the main thread.

  



