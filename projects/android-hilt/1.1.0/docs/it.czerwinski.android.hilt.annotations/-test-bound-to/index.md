---
title: TestBoundTo -
---
//[Extensions for Dagger Hilt](../../index.html)/[it.czerwinski.android.hilt.annotations](../index.html)/[TestBoundTo](index.html)



# TestBoundTo  
 [jvm] @[Target](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.annotation/-target/index.html)(allowedTargets = [[AnnotationTarget.CLASS](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.annotation/-annotation-target/-c-l-a-s-s/index.html)])  
  
annotation class [TestBoundTo](index.html)(**supertype**: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>, **component**: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>)

Marks test implementation bound to the given [supertype](supertype.html) in the given [component](component.html).



Any annotations annotated with @Scope or @Qualifier will also annotate the resulting @Binds method.



#### Since  


1.1.0

   


## Constructors  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.hilt.annotations/TestBoundTo/TestBoundTo/#kotlin.reflect.KClass[*]#kotlin.reflect.KClass[*]/PointingToDeclaration/"></a>[TestBoundTo](-test-bound-to.html)| <a name="it.czerwinski.android.hilt.annotations/TestBoundTo/TestBoundTo/#kotlin.reflect.KClass[*]#kotlin.reflect.KClass[*]/PointingToDeclaration/"></a> [jvm] fun [TestBoundTo](-test-bound-to.html)(supertype: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>, component: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*> = SingletonComponent::class)   <br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[equals](../-test-factory-method/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[jvm]  <br>Content  <br>open operator fun [equals](../-test-factory-method/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[hashCode](../-test-factory-method/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[jvm]  <br>Content  <br>open fun [hashCode](../-test-factory-method/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[toString](../-test-factory-method/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[jvm]  <br>Content  <br>open fun [toString](../-test-factory-method/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.hilt.annotations/TestBoundTo/component/#/PointingToDeclaration/"></a>[component](component.html)| <a name="it.czerwinski.android.hilt.annotations/TestBoundTo/component/#/PointingToDeclaration/"></a> [jvm] val [component](component.html): [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>Hilt component in which the binding should be installed.   <br>
| <a name="it.czerwinski.android.hilt.annotations/TestBoundTo/supertype/#/PointingToDeclaration/"></a>[supertype](supertype.html)| <a name="it.czerwinski.android.hilt.annotations/TestBoundTo/supertype/#/PointingToDeclaration/"></a> [jvm] val [supertype](supertype.html): [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>Supertype to which the implementation should be bound.   <br>

