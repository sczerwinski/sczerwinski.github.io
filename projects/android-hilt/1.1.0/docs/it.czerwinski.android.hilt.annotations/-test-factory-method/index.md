---
title: TestFactoryMethod -
---
//[Extensions for Dagger Hilt](../../index.html)/[it.czerwinski.android.hilt.annotations](../index.html)/[TestFactoryMethod](index.html)



# TestFactoryMethod  
 [jvm] @[Target](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.annotation/-target/index.html)(allowedTargets = [[AnnotationTarget.FUNCTION](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.annotation/-annotation-target/-f-u-n-c-t-i-o-n/index.html)])  
  
annotation class [TestFactoryMethod](index.html)(**component**: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>)

Marks test factory method for the class returned by the annotated function.



The implementation will be provided in the given [component](component.html).



Any annotations annotated with @Scope or @Qualifier will also annotate the resulting @Provides method.



If the annotated function is neither static nor a member of an object, the enclosing class will become the first parameter of the generated provide function.



#### Since  


1.1.0

   


## Constructors  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.hilt.annotations/TestFactoryMethod/TestFactoryMethod/#kotlin.reflect.KClass[*]/PointingToDeclaration/"></a>[TestFactoryMethod](-test-factory-method.html)| <a name="it.czerwinski.android.hilt.annotations/TestFactoryMethod/TestFactoryMethod/#kotlin.reflect.KClass[*]/PointingToDeclaration/"></a> [jvm] fun [TestFactoryMethod](-test-factory-method.html)(component: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*> = SingletonComponent::class)   <br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[equals](index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)| <a name="kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/"></a>[jvm]  <br>Content  <br>open operator fun [equals](index.html#%5Bkotlin%2FAny%2Fequals%2F%23kotlin.Any%3F%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[hashCode](index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)| <a name="kotlin/Any/hashCode/#/PointingToDeclaration/"></a>[jvm]  <br>Content  <br>open fun [hashCode](index.html#%5Bkotlin%2FAny%2FhashCode%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[toString](index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)| <a name="kotlin/Any/toString/#/PointingToDeclaration/"></a>[jvm]  <br>Content  <br>open fun [toString](index.html#%5Bkotlin%2FAny%2FtoString%2F%23%2FPointingToDeclaration%2F%5D%2FFunctions%2F499647441)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>


## Properties  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.hilt.annotations/TestFactoryMethod/component/#/PointingToDeclaration/"></a>[component](component.html)| <a name="it.czerwinski.android.hilt.annotations/TestFactoryMethod/component/#/PointingToDeclaration/"></a> [jvm] val [component](component.html): [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>Hilt component in which the provider should be installed.   <br>

