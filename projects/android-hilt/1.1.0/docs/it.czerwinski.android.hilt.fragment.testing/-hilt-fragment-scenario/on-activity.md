---
title: onActivity -
---
//[Extensions for Dagger Hilt](../../index.html)/[it.czerwinski.android.hilt.fragment.testing](../index.html)/[HiltFragmentScenario](index.html)/[onActivity](on-activity.html)



# onActivity  
[androidJvm]  
Content  
fun [onActivity](on-activity.html)(action: ActivityScenario.ActivityAction<[A](index.html)>): [HiltFragmentScenario](index.html)<[F](index.html), [A](index.html)>  
More info  


Runs a given action on the current Activity's main thread.



Note that you should never keep Activity reference passed into your action because it can be recreated at anytime during state transitions.

  



