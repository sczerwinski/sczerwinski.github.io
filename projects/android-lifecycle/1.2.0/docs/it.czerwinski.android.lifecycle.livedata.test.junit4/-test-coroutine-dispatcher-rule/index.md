---
title: TestCoroutineDispatcherRule -
---
//[Extensions for Jetpack Lifecycle](../../../index.md)/[it.czerwinski.android.lifecycle.livedata.test.junit4](../index.md)/[TestCoroutineDispatcherRule](index.md)



# TestCoroutineDispatcherRule  
 [androidJvm] @ExperimentalCoroutinesApi()  
  
class [TestCoroutineDispatcherRule](index.md) : TestWatcher

JUnit4 test rule that swaps main coroutine dispatcher with TestCoroutineDispatcher.

   


## Constructors  
  
| | |
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test.junit4/TestCoroutineDispatcherRule/TestCoroutineDispatcherRule/#/PointingToDeclaration/"></a>[TestCoroutineDispatcherRule](-test-coroutine-dispatcher-rule.md)| <a name="it.czerwinski.android.lifecycle.livedata.test.junit4/TestCoroutineDispatcherRule/TestCoroutineDispatcherRule/#/PointingToDeclaration/"></a> [androidJvm] fun [TestCoroutineDispatcherRule](-test-coroutine-dispatcher-rule.md)()   <br>|


## Functions  
  
|  Name |  Summary | 
|---|---|
| <a name="org.junit.rules/TestWatcher/apply/#org.junit.runners.model.Statement#org.junit.runner.Description/PointingToDeclaration/"></a>[apply](index.md#-1929544992%2FFunctions%2F-1493455702)| <a name="org.junit.rules/TestWatcher/apply/#org.junit.runners.model.Statement#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open override fun [apply](index.md#-1929544992%2FFunctions%2F-1493455702)(p0: Statement, p1: Description): Statement  <br><br><br>|
| <a name="org.junit.rules/TestWatcher/failed/#kotlin.Throwable#org.junit.runner.Description/PointingToDeclaration/"></a>[failed](index.md#2019667857%2FFunctions%2F-1493455702)| <a name="org.junit.rules/TestWatcher/failed/#kotlin.Throwable#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [failed](index.md#2019667857%2FFunctions%2F-1493455702)(p0: [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html), p1: Description)  <br><br><br>|
| <a name="org.junit.rules/TestWatcher/skipped/#org.junit.AssumptionViolatedException#org.junit.runner.Description/PointingToDeclaration/"></a>[skipped](index.md#-1682087327%2FFunctions%2F-1493455702)| <a name="org.junit.rules/TestWatcher/skipped/#org.junit.AssumptionViolatedException#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [skipped](index.md#-1682087327%2FFunctions%2F-1493455702)(p0: AssumptionViolatedException, p1: Description)  <br>~~open~~ ~~fun~~ [~~skipped~~](index.md#-1688344674%2FFunctions%2F-1493455702)~~(~~~~p0~~~~:~~ AssumptionViolatedException~~,~~ ~~p1~~~~:~~ Description~~)~~  <br><br><br>|
| <a name="org.junit.rules/TestWatcher/succeeded/#org.junit.runner.Description/PointingToDeclaration/"></a>[succeeded](index.md#1776812923%2FFunctions%2F-1493455702)| <a name="org.junit.rules/TestWatcher/succeeded/#org.junit.runner.Description/PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>open fun [succeeded](index.md#1776812923%2FFunctions%2F-1493455702)(p0: Description)  <br><br><br>|

