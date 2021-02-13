---
title: launch -
---
//[Extensions for Dagger Hilt](../../../index.html)/[it.czerwinski.android.hilt.fragment.testing](../../index.html)/[HiltFragmentScenario](../index.html)/[Companion](index.html)/[launch](launch.html)



# launch  
[androidJvm]  
Content  
fun <[F](launch.html) : [Fragment](https://developer.android.com/reference/kotlin/androidx/fragment/app/Fragment.html)> [launch](launch.html)(fragmentClass: [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html)<[F](launch.html)>, fragmentArgs: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)? = null, @[StyleRes](https://developer.android.com/reference/kotlin/androidx/annotation/StyleRes.html)()themeResId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = defaultTheme, factory: [FragmentFactory](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentFactory.html)? = null): [HiltFragmentScenario](../index.html)<[F](launch.html), [HiltFragmentScenario.EmptyFragmentActivity](../-empty-fragment-activity/index.html)>  
fun <[F](launch.html) : [Fragment](https://developer.android.com/reference/kotlin/androidx/fragment/app/Fragment.html), [A](launch.html) : [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html)> [launch](launch.html)(activityClass: [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html)<[A](launch.html)>, fragmentClass: [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html)<[F](launch.html)>, fragmentArgs: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)? = null, @[StyleRes](https://developer.android.com/reference/kotlin/androidx/annotation/StyleRes.html)()themeResId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = defaultTheme, factory: [FragmentFactory](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentFactory.html)? = null): [HiltFragmentScenario](../index.html)<[F](launch.html), [A](launch.html)>  
More info  


Launches a Fragment with given arguments hosted by an empty [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html) themed by themeResId, using the given [FragmentFactory](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentFactory.html) and waits for it to reach the resumed state.



This method cannot be called from the main thread.

  



