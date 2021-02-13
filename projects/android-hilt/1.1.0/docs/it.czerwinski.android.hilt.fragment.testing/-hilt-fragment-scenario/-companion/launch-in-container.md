---
title: launchInContainer -
---
//[Extensions for Dagger Hilt](../../../index.html)/[it.czerwinski.android.hilt.fragment.testing](../../index.html)/[HiltFragmentScenario](../index.html)/[Companion](index.html)/[launchInContainer](launch-in-container.html)



# launchInContainer  
[androidJvm]  
Content  
fun <[F](launch-in-container.html) : [Fragment](https://developer.android.com/reference/kotlin/androidx/fragment/app/Fragment.html)> [launchInContainer](launch-in-container.html)(fragmentClass: [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html)<[F](launch-in-container.html)>, fragmentArgs: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)? = null, @[StyleRes](https://developer.android.com/reference/kotlin/androidx/annotation/StyleRes.html)()themeResId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = defaultTheme, factory: [FragmentFactory](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentFactory.html)? = null): [HiltFragmentScenario](../index.html)<[F](launch-in-container.html), [HiltFragmentScenario.EmptyFragmentActivity](../-empty-fragment-activity/index.html)>  
fun <[F](launch-in-container.html) : [Fragment](https://developer.android.com/reference/kotlin/androidx/fragment/app/Fragment.html), [A](launch-in-container.html) : [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html)> [launchInContainer](launch-in-container.html)(activityClass: [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html)<[A](launch-in-container.html)>, fragmentClass: [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html)<[F](launch-in-container.html)>, fragmentArgs: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)? = null, @[StyleRes](https://developer.android.com/reference/kotlin/androidx/annotation/StyleRes.html)()themeResId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = defaultTheme, factory: [FragmentFactory](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentFactory.html)? = null): [HiltFragmentScenario](../index.html)<[F](launch-in-container.html), [A](launch-in-container.html)>  
More info  


Launches a Fragment in the Activity's root view container android.R.id.content, with given arguments hosted by an empty [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html) themed by themeResId, using the given [FragmentFactory](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentFactory.html) and waits for it to reach the resumed state.



This method cannot be called from the main thread.

  



