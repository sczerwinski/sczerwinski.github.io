---
title: moveToState -
---
//[Extensions for Dagger Hilt](../../index.html)/[it.czerwinski.android.hilt.fragment.testing](../index.html)/[HiltFragmentScenario](index.html)/[moveToState](move-to-state.html)



# moveToState  
[androidJvm]  
Content  
fun [moveToState](move-to-state.html)(newState: [Lifecycle.State](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.State.html)): [HiltFragmentScenario](index.html)<[F](index.html), [A](index.html)>  
More info  


Moves Fragment state to a new state.



If a new state and current state are the same, this method does nothing.



It accepts [CREATED](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.State.CREATED.html), [STARTED](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.State.STARTED.html), [RESUMED](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.State.RESUMED.html), and [DESTROYED](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.State.DESTROYED.html).



[DESTROYED](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.State.DESTROYED.html) is a terminal state. You cannot move to any other state after the Fragment reaches that state.



This method cannot be called from the main thread.



*Note: Moving state to* [*STARTED*](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.State.STARTED.html) *is not supported on Android API level 23 and lower.* [*UnsupportedOperationException*](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unsupported-operation-exception/index.html) *will be thrown.*

  



