---
title: it.czerwinski.android.lifecycle.livedata.test.junit5 -
---
//[Extensions for Jetpack Lifecycle](../index.html)/[it.czerwinski.android.lifecycle.livedata.test.junit5](index.html)



# Package it.czerwinski.android.lifecycle.livedata.test.junit5  
 [androidJvm] 

JUnit5 testing extensions for Jetpack Lifecycle

   


## Types  
  
|  Name|  Summary| 
|---|---|
| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/InstantTaskExecutorExtension///PointingToDeclaration/"></a>[InstantTaskExecutorExtension](-instant-task-executor-extension/index.html)| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/InstantTaskExecutorExtension///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>class [InstantTaskExecutorExtension](-instant-task-executor-extension/index.html) : [InstantTaskExecutorRule](https://developer.android.com/reference/kotlin/androidx/arch/core/executor/testing/InstantTaskExecutorRule.html), BeforeEachCallback, AfterEachCallback  <br>More info  <br>JUnit5 extension that swaps the background executor used by the Architecture Components with a different one which executes each task synchronously.  <br><br><br>
| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/TestCoroutineDispatcherExtension///PointingToDeclaration/"></a>[TestCoroutineDispatcherExtension](-test-coroutine-dispatcher-extension/index.html)| <a name="it.czerwinski.android.lifecycle.livedata.test.junit5/TestCoroutineDispatcherExtension///PointingToDeclaration/"></a>[androidJvm]  <br>Content  <br>@ExperimentalCoroutinesApi()  <br>  <br>class [TestCoroutineDispatcherExtension](-test-coroutine-dispatcher-extension/index.html) : BeforeEachCallback, AfterEachCallback  <br>More info  <br>JUnit5 extension that swaps main coroutine dispatcher with TestCoroutineDispatcher.  <br><br><br>

