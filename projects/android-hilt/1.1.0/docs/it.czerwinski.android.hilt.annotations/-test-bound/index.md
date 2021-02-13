---
title: TestBound -
---
//[Extensions for Dagger Hilt](../../index.html)/[it.czerwinski.android.hilt.annotations](../index.html)/[TestBound](index.html)



# TestBound  
 [jvm] @[Target](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.annotation/-target/index.html)(allowedTargets = [[AnnotationTarget.CLASS](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.annotation/-annotation-target/-c-l-a-s-s/index.html)])  
  
annotation class [TestBound](index.html)(**component**: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>)

Marks test implementation bound to the supertype of the annotated class in the given [component](component.html).



Annotated implementation must have **exactly** one direct supertype (excluding [java.lang.Object](https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html)).



Any annotations annotated with @Scope or @Qualifier will also annotate the resulting @Binds method.



#### Since  


1.1.0

   


## Constructors  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.hilt.annotations/TestBound/TestBound/#kotlin.reflect.KClass[*]/PointingToDeclaration/"></a>[TestBound](-test-bound.html)| <a name="it.czerwinski.android.hilt.annotations/TestBound/TestBound/#kotlin.reflect.KClass[*]/PointingToDeclaration/"></a> [jvm] fun [TestBound](-test-bound.html)(component: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*> = SingletonComponent::class)   <br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[equals](../-test-factory-method/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[jvm]  <br>Content  <br>open operator fun [equals](../-test-factory-method/index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[hashCode](../-test-factory-method/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[jvm]  <br>Content  <br>open fun [hashCode](../-test-factory-method/index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[toString](../-test-factory-method/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[jvm]  <br>Content  <br>open fun [toString](../-test-factory-method/index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.hilt.annotations/TestBound/component/#/PointingToDeclaration/"></a>[component](component.html)| <a name="it.czerwinski.android.hilt.annotations/TestBound/component/#/PointingToDeclaration/"></a> [jvm] val [component](component.html): [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>Hilt component in which the binding should be installed.   <br>

