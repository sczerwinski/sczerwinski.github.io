---
title: onFragment -
---
//[Extensions for Dagger Hilt](../../index.html)/[it.czerwinski.android.hilt.fragment.testing](../index.html)/[HiltFragmentScenario](index.html)/[onFragment](on-fragment.html)



# onFragment  
[androidJvm]  
Content  
fun [onFragment](on-fragment.html)(action: [HiltFragmentScenario.FragmentAction](-fragment-action/index.html)<[F](index.html)>): [HiltFragmentScenario](index.html)<[F](index.html), [A](index.html)>  
More info  


Runs a given action on the current Activity's main thread.



Note that you should never keep Fragment reference passed into your action because it can be recreated at anytime during state transitions.



Throwing an exception from action makes the host Activity crash. You can inspect the exception in logcat outputs.



This method cannot be called from the main thread.

  



