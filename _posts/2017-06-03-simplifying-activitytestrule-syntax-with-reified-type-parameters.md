---
disqusid: simplifying-activitytestrule-syntax-with-reified-type-parameters
title: Simplifying ActivityTestRule syntax with reified type parameters
mobileTitle: Reified type parameters
layout: post
abstract: How to simplify ActivityTestRule syntax with reified type parameters in Kotlin
keywords: kotlin,android,testing,reified,ActivityTestRule,IntentsTestRule
tags: kotlin,android
---

## Introduction

In this article, I am using JUnit&nbsp;4.12,
and [Espresso](https://google.github.io/android-testing-support-library/docs/espresso/index.html)&nbsp;2.2.2
with [Espresso Intents](https://google.github.io/android-testing-support-library/docs/espresso/intents/index.html).

Since Espresso uses old version of Android Support Annotations (i.e.&nbsp;23.1.1),
it is mandatory to exclude this module when using latest Android Support library:

```gradle
dependencies {
    // […]
    androidTestCompile('com.android.support.test.espresso:espresso-core:2.2.2', {
        exclude group: 'com.android.support', module: 'support-annotations'
    })
    androidTestCompile('com.android.support.test.espresso:espresso-intents:2.2.2', {
        exclude group: 'com.android.support', module: 'support-annotations'
    })
}
```

## The Problems

While [testing Android UI](https://developer.android.com/training/testing/ui-testing/espresso-testing.html)
with Espresso, I define an `ActivityTestRule` or an `IntentsTestRule` (in the examples, I will use the latter).
Sometimes, I need to start the `Activity` under test with a specific `Intent`, so the rule must be instantiated
by calling a constructor with three arguments:

```kotlin
@RunWith(AndroidJUnit4::class)
class MyTestClass {

    @Rule
    @JvmField
    val mainActivityRule = IntentsTestRule(
            MainActivity::class.java, false, false)
}
```

The first argument is the class of the `Activity`.
The second one regards touch mode (it is `false` by default, and I don’t need to change it).
And the last argument tells whether the `Activity` should be launched automatically before each test method
(by default it is set to `true`).

There are several problems with this snippet of code:

1. When I see the constructor call, I don’t know the meaning of each `false` argument
without looking at the definition of the constructor. In Kotlin, it is possible to use
[named arguments](https://kotlinlang.org/docs/reference/functions.html#named-arguments),
e.g. `launchActivity = false`,
but it is not allowed with non-Kotlin functions.
2. I don’t need to change the default value of `initialTouchMode`.
The second argument is only there to prevent ambiguity—constructor:
```java
// Java code:
public ActivityTestRule(Class<T> activityClass, boolean launchActivity)
```
would have the same arguments as already existing:
```java
// Java code:
public ActivityTestRule(Class<T> activityClass, boolean initialTouchMode)
```
3. The `::class.java` suffix to the `Activity` class makes the code obscure.

All these problems could be easily avoided in Kotlin, but Espresso is written in Java.

## Using Kotlin Functions

To solve the first and the second issue, I created a simple Kotlin function
that assigns default values to both arguments:

```kotlin
fun <T : Activity> intentsTestRule(
        activityClass: Class<T>,
        initialTouchMode: Boolean = false,
        launchActivity: Boolean = true) =
    IntentsTestRule(activityClass, initialTouchMode, launchActivity)
```

As a result, I can omit the second argument and name the third one:

```kotlin
@RunWith(AndroidJUnit4::class)
class MyTestClass {

    @Rule
    @JvmField
    val mainActivityRule = intentsTestRule(
            MainActivity::class.java,
            launchActivity = false)
}
```

## Using Reified Type Parameters

To solve the last problem, I needed to harness Kotlin
[reified type parameters](https://kotlinlang.org/docs/reference/inline-functions.html#reified-type-parameters).

After reifying parameter&nbsp;`T`, I can directly access its type inside the function
(note that I can only do that with `inline` functions). Thus, the first argument is no longer needed:

```kotlin
inline fun <reified T : Activity> intentsTestRule(
        initialTouchMode: Boolean = false,
        launchActivity: Boolean = true) =
    IntentsTestRule(T::class.java, initialTouchMode, launchActivity)
```

So I can define the rule as:

```kotlin
@RunWith(AndroidJUnit4::class)
class MyTestClass {

    @Rule
    @JvmField
    val mainActivityRule = intentsTestRule<MainActivity>(launchActivity = false)
}
```

## Other Resources

A similar function might be defined for `ActivityTestRule`s.
Full code with examples is available [here](https://gist.github.com/sczerwinski/bcd7e38a02638c249878b78b2e9e6cd0).
