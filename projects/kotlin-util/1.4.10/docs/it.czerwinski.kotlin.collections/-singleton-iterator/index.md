---
title: SingletonIterator -
---
//[Kotlin utilities](../../index.html)/[it.czerwinski.kotlin.collections](../index.html)/[SingletonIterator](index.html)



# SingletonIterator  
 [common] 

Iterator producing a single element.

class [SingletonIterator](index.html)<[T](index.html)>(**element**: [T](index.html)) : [Iterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)<[T](index.html)>    


## Parameters  
  
common  
  
|  Name|  Summary| 
|---|---|
| element| <br><br>The element to be produced by the iterator.<br><br>
| T| <br><br>Type of the element.<br><br>
  


## Constructors  
  
|  Name|  Summary| 
|---|---|
| [SingletonIterator](-singleton-iterator.html)|  [common] <br><br>The element to be produced by the iterator.<br><br>fun <[T](index.html)> [SingletonIterator](-singleton-iterator.html)(element: [T](index.html))   <br>


## Functions  
  
|  Name|  Summary| 
|---|---|
| [equals](../../it.czerwinski.kotlin.util/-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)| [common]  <br>Content  <br>open operator override fun [equals](../../it.czerwinski.kotlin.util/-failure/index.html#kotlin/Any/equals/#kotlin.Any?/PointingToDeclaration/)(other: [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [hashCode](../../it.czerwinski.kotlin.util/-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [hashCode](../../it.czerwinski.kotlin.util/-failure/index.html#kotlin/Any/hashCode/#/PointingToDeclaration/)(): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)  <br><br><br>
| [hasNext](has-next.html)| [common]  <br>Content  <br>open operator override fun [hasNext](has-next.html)(): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)  <br><br><br>
| [next](next.html)| [common]  <br>Content  <br>open operator override fun [next](next.html)(): [T](index.html)  <br><br><br>
| [toString](../../it.czerwinski.kotlin.util/-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)| [common]  <br>Content  <br>open override fun [toString](../../it.czerwinski.kotlin.util/-failure/index.html#kotlin/Any/toString/#/PointingToDeclaration/)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)  <br><br><br>

