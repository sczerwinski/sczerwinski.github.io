---
title: FragmentAction -
---
//[Extensions for Dagger Hilt](../../../index.html)/[it.czerwinski.android.hilt.fragment.testing](../../index.html)/[HiltFragmentScenario](../index.html)/[FragmentAction](index.html)



# FragmentAction  
 [androidJvm] fun fun interface [FragmentAction](index.html)<[F](index.html) : [Fragment](https://developer.android.com/reference/kotlin/androidx/fragment/app/Fragment.html)>

FragmentAction interface should be implemented by any class whose instances are intended to be executed by the main thread. A Fragment that is instrumented by the HiltFragmentScenario is passed to [FragmentAction.perform](perform.html) method.



You should never keep the Fragment reference as it will lead to unpredictable behaviour. It should only be accessed in [FragmentAction.perform](perform.html) scope.

   


## Functions  
  
|  Name|  Summary| 
|---|---|
| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[equals](../-companion/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open operator fun [equals](../-companion/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[hashCode](../-companion/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [hashCode](../-companion/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.FragmentAction/perform/#TypeParam(bounds=[androidx.fragment.app.Fragment])/PointingToDeclaration/"></a>[perform](perform.html)| <a name="it.czerwinski.android.hilt.fragment.testing/HiltFragmentScenario.FragmentAction/perform/#TypeParam(bounds=[androidx.fragment.app.Fragment])/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>@[MainThread](https://developer.android.com/reference/kotlin/androidx/annotation/MainThread.html)()  <br>  <br>abstract fun [perform](perform.html)(fragment: [F](index.html))  <br>More info  <br>This method is invoked on the main thread with the reference to the fragment.  <br><br><br>
| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[toString](../-companion/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [toString](../-companion/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F1884202767)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>

