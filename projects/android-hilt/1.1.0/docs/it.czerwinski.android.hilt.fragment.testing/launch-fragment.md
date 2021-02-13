---
title: launchFragment -
---
//[Extensions for Dagger Hilt](../index.html)/[it.czerwinski.android.hilt.fragment.testing](index.html)/[launchFragment](launch-fragment.html)



# launchFragment  
[androidJvm]  
Content  
inline fun <[F](launch-fragment.html) : [Fragment](https://developer.android.com/reference/kotlin/androidx/fragment/app/Fragment.html)> [launchFragment](launch-fragment.html)(fragmentArgs: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)? = null, @[StyleRes](https://developer.android.com/reference/kotlin/androidx/annotation/StyleRes.html)()themeResId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = HiltFragmentScenario.defaultTheme, factory: [FragmentFactory](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentFactory.html)? = null): [HiltFragmentScenario](-hilt-fragment-scenario/index.html)<[F](launch-fragment.html), [HiltFragmentScenario.EmptyFragmentActivity](-hilt-fragment-scenario/-empty-fragment-activity/index.html)>  
More info  


Launches a Fragment with given arguments hosted by an empty [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html) using given [FragmentFactory](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentFactory.html) and waits for it to reach a resumed state.



This method cannot be called from the main thread.



## Parameters  
  
androidJvm  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#androidx.fragment.app.FragmentFactory?/PointingToDeclaration/"></a>fragmentArgs| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#androidx.fragment.app.FragmentFactory?/PointingToDeclaration/"></a><br><br>a bundle to passed into fragment<br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#androidx.fragment.app.FragmentFactory?/PointingToDeclaration/"></a>themeResId| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#androidx.fragment.app.FragmentFactory?/PointingToDeclaration/"></a><br><br>a style resource id to be set to the host activity's theme<br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#androidx.fragment.app.FragmentFactory?/PointingToDeclaration/"></a>factory| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#androidx.fragment.app.FragmentFactory?/PointingToDeclaration/"></a><br><br>a fragment factory to use or null to use default factory<br><br>
  
  


[androidJvm]  
Content  
inline fun <[F](launch-fragment.html) : [Fragment](https://developer.android.com/reference/kotlin/androidx/fragment/app/Fragment.html)> [launchFragment](launch-fragment.html)(fragmentArgs: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html)? = null, @[StyleRes](https://developer.android.com/reference/kotlin/androidx/annotation/StyleRes.html)()themeResId: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) = HiltFragmentScenario.defaultTheme, crossinline instantiate: () -> [F](launch-fragment.html)): [HiltFragmentScenario](-hilt-fragment-scenario/index.html)<[F](launch-fragment.html), [HiltFragmentScenario.EmptyFragmentActivity](-hilt-fragment-scenario/-empty-fragment-activity/index.html)>  
More info  


Launches a Fragment with given arguments hosted by an empty [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html) using instantiate to create the Fragment and waits for it to reach a resumed state.



This method cannot be called from the main thread.



## Parameters  
  
androidJvm  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#kotlin.Function0[TypeParam(bounds=[androidx.fragment.app.Fragment])]/PointingToDeclaration/"></a>fragmentArgs| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#kotlin.Function0[TypeParam(bounds=[androidx.fragment.app.Fragment])]/PointingToDeclaration/"></a><br><br>a bundle to passed into fragment<br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#kotlin.Function0[TypeParam(bounds=[androidx.fragment.app.Fragment])]/PointingToDeclaration/"></a>themeResId| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#kotlin.Function0[TypeParam(bounds=[androidx.fragment.app.Fragment])]/PointingToDeclaration/"></a><br><br>a style resource id to be set to the host activity's theme<br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#kotlin.Function0[TypeParam(bounds=[androidx.fragment.app.Fragment])]/PointingToDeclaration/"></a>instantiate| <a name="it.czerwinski.android.hilt.fragment.testing//launchFragment/#android.os.Bundle?#kotlin.Int#kotlin.Function0[TypeParam(bounds=[androidx.fragment.app.Fragment])]/PointingToDeclaration/"></a><br><br>method which will be used to instantiate the Fragment.<br><br>
  
  



