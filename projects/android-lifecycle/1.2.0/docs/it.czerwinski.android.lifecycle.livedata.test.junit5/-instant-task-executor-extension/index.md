---
title: InstantTaskExecutorExtension -
---
//[Extensions for Jetpack Lifecycle](../../../index.md)/[it.czerwinski.android.lifecycle.livedata.test.junit5](../index.md)/[InstantTaskExecutorExtension](index.md)



# InstantTaskExecutorExtension  
 [androidJvm] class [InstantTaskExecutorExtension](index.md) : [InstantTaskExecutorRule](https://developer.android.com/reference/kotlin/androidx/arch/core/executor/testing/InstantTaskExecutorRule.html), BeforeEachCallback, AfterEachCallback

JUnit5 extension that swaps the background executor used by the Architecture Components with a different one which executes each task synchronously.



This extension is analogous to [InstantTaskExecutorRule](https://developer.android.com/reference/kotlin/androidx/arch/core/executor/testing/InstantTaskExecutorRule.html) for JUnit4.

   


## Constructors  
  
| | |
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/InstantTaskExecutorExtension/InstantTaskExecutorExtension/#/PointingToDeclaration/"></a>[InstantTaskExecutorExtension](-instant-task-executor-extension.md)| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/InstantTaskExecutorExtension/InstantTaskExecutorExtension/#/PointingToDeclaration/"></a> [androidJvm] fun [InstantTaskExecutorExtension](-instant-task-executor-extension.md)()   <br>|


## Functions  
  
|  Name |  Summary | 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/InstantTaskExecutorExtension/afterEach/#org.junit.jupiter.api.extension.ExtensionContext?/PointingToDeclaration/"></a>[afterEach](after-each.md)| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/InstantTaskExecutorExtension/afterEach/#org.junit.jupiter.api.extension.ExtensionContext?/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open override fun [afterEach](after-each.md)(context: ExtensionContext?)  <br><br><br>|
| <a name="org.junit.rules/TestWatcher/apply/#org.junit.runners.model.Statement#org.junit.runner.Description/PointingToDeclaration/"></a>[apply](index.md#-1929544992%2FFunctions%2F-800062997)| <a name="org.junit.rules/TestWatcher/apply/#org.junit.runners.model.Statement#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open override fun [apply](index.md#-1929544992%2FFunctions%2F-800062997)(p0: Statement, p1: Description): Statement  <br><br><br>|
| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/InstantTaskExecutorExtension/beforeEach/#org.junit.jupiter.api.extension.ExtensionContext?/PointingToDeclaration/"></a>[beforeEach](before-each.md)| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/InstantTaskExecutorExtension/beforeEach/#org.junit.jupiter.api.extension.ExtensionContext?/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open override fun [beforeEach](before-each.md)(context: ExtensionContext?)  <br><br><br>|
| <a name="org.junit.rules/TestWatcher/failed/#kotlin.Throwable#org.junit.runner.Description/PointingToDeclaration/"></a>[failed](index.md#2019667857%2FFunctions%2F-800062997)| <a name="org.junit.rules/TestWatcher/failed/#kotlin.Throwable#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [failed](index.md#2019667857%2FFunctions%2F-800062997)(p0: [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html), p1: Description)  <br><br><br>|
| <a name="androidx.arch.core.executor.testing/InstantTaskExecutorRule/finished/#org.junit.runner.Description/PointingToDeclaration/"></a>[finished](index.md#-452297493%2FFunctions%2F-800062997)| <a name="androidx.arch.core.executor.testing/InstantTaskExecutorRule/finished/#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open override fun [finished](index.md#-452297493%2FFunctions%2F-800062997)(p0: Description)  <br><br><br>|
| <a name="org.junit.rules/TestWatcher/skipped/#org.junit.AssumptionViolatedException#org.junit.runner.Description/PointingToDeclaration/"></a>[skipped](index.md#-1682087327%2FFunctions%2F-800062997)| <a name="org.junit.rules/TestWatcher/skipped/#org.junit.AssumptionViolatedException#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [skipped](index.md#-1682087327%2FFunctions%2F-800062997)(p0: AssumptionViolatedException, p1: Description)  <br>~~open~~ ~~fun~~ [~~skipped~~](index.md#-1688344674%2FFunctions%2F-800062997)~~(~~~~p0~~~~:~~ AssumptionViolatedException~~,~~ ~~p1~~~~:~~ Description~~)~~  <br><br><br>|
| <a name="androidx.arch.core.executor.testing/InstantTaskExecutorRule/starting/#org.junit.runner.Description/PointingToDeclaration/"></a>[starting](index.md#-1554275875%2FFunctions%2F-800062997)| <a name="androidx.arch.core.executor.testing/InstantTaskExecutorRule/starting/#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open override fun [starting](index.md#-1554275875%2FFunctions%2F-800062997)(p0: Description)  <br><br><br>|
| <a name="org.junit.rules/TestWatcher/succeeded/#org.junit.runner.Description/PointingToDeclaration/"></a>[succeeded](index.md#1776812923%2FFunctions%2F-800062997)| <a name="org.junit.rules/TestWatcher/succeeded/#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [succeeded](index.md#1776812923%2FFunctions%2F-800062997)(p0: Description)  <br><br><br>|

