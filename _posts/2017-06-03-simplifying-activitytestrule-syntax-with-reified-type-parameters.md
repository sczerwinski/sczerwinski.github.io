---
disqusid: simplifying-activitytestrule-syntax-with-reified-type-parameters
title: Simplifying ActivityTestRule syntax with reified type parameters
mobileTitle: Reified type parameters
layout: post
abstract: How to simplify ActivityTestRule syntax with reified type parameters in Kotlin
keywords: kotlin,android,testing,reified,ActivityTestRule,IntentsTestRule
tags: kotlin,android
---

## Before We Start

The code in this article uses Espresso Core and Espresso Intents dependencies:

```gradle
androidTestCompile('com.android.support.test.espresso:espresso-core:2.2.2', {
    exclude group: 'com.android.support', module: 'support-annotations'
})
androidTestCompile('com.android.support.test.espresso:espresso-intents:2.2.2', {
    exclude group: 'com.android.support', module: 'support-annotations'
})
```

## The Problem

I want to [test Android UI](https://developer.android.com/training/testing/ui-testing/espresso-testing.html)
with [Espresso Intents](https://google.github.io/android-testing-support-library/docs/espresso/intents/index.html)

```kotlin
@RunWith(AndroidJUnit4::class)
class MyTestClass {

    @Rule
    @JvmField
    val intentsRule = IntentsTestRule(MainActivity::class.java, false, false)
}
```

Two problems with that:
1. I don't like ugly `::class.java`.
2. I would like to use named parameters like `launchActivity = false`,
but that is only allowed with Kotlin functions.

## First Attempt

```kotlin
fun <T : Activity> intentsTestRule(
        activityClass: Class<T>,
        initialTouchMode: Boolean = false,
        launchActivity: Boolean = true) =
    IntentsTestRule(activityClass, initialTouchMode, launchActivity)
```

```kotlin
@RunWith(AndroidJUnit4::class)
class MyTestClass {

    @Rule
    @JvmField
    val intentsRule = intentsTestRule(SplashScreenActivity::class.java, launchActivity = false)
}
```

## Reify

We will use
[reified type parameters](https://kotlinlang.org/docs/reference/inline-functions.html#reified-type-parameters).

```kotlin
inline fun <reified T : Activity> intentsTestRule(
        initialTouchMode: Boolean = false,
        launchActivity: Boolean = true) =
    IntentsTestRule(T::class.java, initialTouchMode, launchActivity)
```

```kotlin
@RunWith(AndroidJUnit4::class)
class MyTestClass {

    @Rule
    @JvmField
    val intentsRule = intentsTestRule<MainActivity>(launchActivity = false)
}
```

I did similar with `ActivityTestRule`.
Full code on [Gist](https://gist.github.com/sczerwinski/bcd7e38a02638c249878b78b2e9e6cd0)
