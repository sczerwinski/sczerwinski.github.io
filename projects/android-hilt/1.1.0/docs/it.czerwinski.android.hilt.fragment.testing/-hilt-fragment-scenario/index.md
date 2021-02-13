---
title: HiltFragmentScenario -
---
//[Extensions for Dagger Hilt](../../index.html)/[it.czerwinski.android.hilt.fragment.testing](../index.html)/[HiltFragmentScenario](index.html)



# HiltFragmentScenario  
 [androidJvm] class [HiltFragmentScenario](index.html)<[F](index.html) : [Fragment](https://developer.android.com/reference/kotlin/androidx/fragment/app/Fragment.html), [A](index.html) : [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html)>

HiltFragmentScenario provides API to start and drive a Fragment's lifecycle state for testing.



Unlike the FragmentScenario from AndroidX Fragment Testing library, HiltFragmentScenario supports fragments annotated with dagger.hilt.android.AndroidEntryPoint.



It also supports testing fragment in a custom [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html).

   


## Types  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.Companion///PointingToDeclaration/"></a>[Companion](-companion/index.html)| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.Companion///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>object [Companion](-companion/index.html)  <br><br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.EmptyFragmentActivity///PointingToDeclaration/"></a>[EmptyFragmentActivity](-empty-fragment-activity/index.html)| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.EmptyFragmentActivity///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>class [EmptyFragmentActivity](-empty-fragment-activity/index.html) : [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html)  <br>More info  <br>An empty activity inheriting [FragmentActivity](https://developer.android.com/reference/kotlin/androidx/fragment/app/FragmentActivity.html), annotated with AndroidEntryPoint.  <br><br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.FragmentAction///PointingToDeclaration/"></a>[FragmentAction](-fragment-action/index.html)| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.FragmentAction///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun fun interface [FragmentAction](-fragment-action/index.html)<[F](-fragment-action/index.html) : [Fragment](https://developer.android.com/reference/kotlin/androidx/fragment/app/Fragment.html)>  <br>More info  <br>FragmentAction interface should be implemented by any class whose instances are intended to be executed by the main thread.  <br><br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.FragmentFactoryViewModel///PointingToDeclaration/"></a>[FragmentFactoryViewModel](-fragment-factory-view-model/index.html)| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.FragmentFactoryViewModel///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>class [FragmentFactoryViewModel](-fragment-factory-view-model/index.html) : [ViewModel](https://developer.android.com/reference/kotlin/androidx/lifecycle/ViewModel.html)  <br>More info  <br>A ViewModel to hold a fragment factory.  <br><br><br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[equals](-companion/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open operator fun [equals](-companion/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[hashCode](-companion/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [hashCode](-companion/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario/moveToState/#androidx.lifecycle.Lifecycle.State/PointingToDeclaration/"></a>[moveToState](move-to-state.html)| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario/moveToState/#androidx.lifecycle.Lifecycle.State/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [moveToState](move-to-state.html)(newState: [Lifecycle.State](https://developer.android.com/reference/kotlin/androidx/lifecycle/Lifecycle.State.html)): [HiltFragmentScenario](index.html)<[F](index.html), [A](index.html)>  <br>More info  <br>Moves Fragment state to a new state.  <br><br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario/onActivity/#androidx.test.core.app.ActivityScenario.ActivityAction[TypeParam(bounds=[androidx.fragment.app.FragmentActivity])]/PointingToDeclaration/"></a>[onActivity](on-activity.html)| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario/onActivity/#androidx.test.core.app.ActivityScenario.ActivityAction[TypeParam(bounds=[androidx.fragment.app.FragmentActivity])]/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [onActivity](on-activity.html)(action: ActivityScenario.ActivityAction<[A](index.html)>): [HiltFragmentScenario](index.html)<[F](index.html), [A](index.html)>  <br>More info  <br>Runs a given action on the current Activity's main thread.  <br><br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario/onFragment/#it.czerwinski.android.hilt.fragment.testing.HiltFragmentScenario.FragmentAction[TypeParam(bounds=[androidx.fragment.app.Fragment])]/PointingToDeclaration/"></a>[onFragment](on-fragment.html)| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario/onFragment/#it.czerwinski.android.hilt.fragment.testing.HiltFragmentScenario.FragmentAction[TypeParam(bounds=[androidx.fragment.app.Fragment])]/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [onFragment](on-fragment.html)(action: [HiltFragmentScenario.FragmentAction](-fragment-action/index.html)<[F](index.html)>): [HiltFragmentScenario](index.html)<[F](index.html), [A](index.html)>  <br>More info  <br>Runs a given action on the current Activity's main thread.  <br><br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario/recreate/#/PointingToDeclaration/"></a>[recreate](recreate.html)| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario/recreate/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>fun [recreate](recreate.html)(): [HiltFragmentScenario](index.html)<[F](index.html), [A](index.html)>  <br>More info  <br>Recreates the host Activity.  <br><br><br>
| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[toString](-companion/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [toString](-companion/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>

