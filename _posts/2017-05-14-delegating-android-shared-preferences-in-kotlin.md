---
disqusid: delegating-android-shared-preferences-in-kotlin
title: Delegating Android SharedPreferences in Kotlin
mobileTitle: Delegating SharedPreferences
layout: post
abstract: How to effectively delegate Android SharedPreferences using Kotlin delegated properties
keywords: kotlin,delegation,android,sharedpreferences
tags: kotlin,android
---

> [_I have learned to delegate._](https://www.brainyquote.com/quotes/quotes/g/gwenstefan468230.html)
>
> — Gwen Stefani

[SharedPreferences](https://developer.android.com/reference/android/content/SharedPreferences.html)

[Key-Value Pairs](https://developer.android.com/training/basics/data-storage/shared-preferences.html)

## The problem: Boilerplate code

```java
SharedPreferences sharedPreferences =
        getSharedPreferences(
            "it.czerwinski.myapp.MY_PREFERENCES",
            Context.MODE_PRIVATE);
```

```java
SharedPreferences sharedPreferences =
        PreferenceManager.getDefaultSharedPreferences(this);
```

```java
usernameEditText.setText(
        sharedPreferences.getString("USER_NAME", ""));
```

```java
sharedPreferences.edit()
        .putString("USER_NAME", usernameEditText.getText().toString())
        .apply();
```

## Kotlin + Anko – how it is better

```kotlin
import org.jetbrains.anko.defaultSharedPreferences
```

```kotlin
usernameEditText.setText(
        defaultSharedPreferences.getString("USER_NAME", ""))
```

```kotlin
defaultSharedPreferences.edit()
        .putString("USER_NAME", usernameEditText.text.toString())
        .apply()
```

## Kotlin properties

```kotlin
var username: String
    get() = defaultSharedPreferences.getString("USER_NAME", "")
    set(value) = defaultSharedPreferences.edit()
            .putString("USER_NAME", value)
            .apply()
```

```kotlin
usernameEditText.setText(username)
```

```kotlin
username = usernameEditText.text.toString()
```

## Delegate

[Delegated Properties](https://kotlinlang.org/docs/reference/delegated-properties.html)

```kotlin
class StringSharedPreferenceDelegate(
        context: Context,
        private val key: String,
        private val defaultValue: String) {

    private val sharedPreferences by lazy {
        PreferenceManager.getDefaultSharedPreferences(context)
    }

    operator fun getValue(ref: Any?, property: KProperty<*>): String =
            sharedPreferences.getString(key, defaultValue)

    operator fun setValue(ref: Any?, property: KProperty<*>, value: String): Unit {
        sharedPreferences.edit()
                .putString(key, value)
                .apply()
    }
}
```

```kotlin
var username: String by StringSharedPreferenceDelegate(this, "USER_NAME", "")
```

## Using my fancy [library](https://github.com/sczerwinski/android-delegates-shared-preferences/tree/master)

```gradle
dependencies {
    compile 'it.czerwinski.android:delegates-shared-preferences:0.1'
}
```

```kotlin
var username by stringSharedPreference("USER_NAME", "")
```

```kotlin
var username by context.stringSharedPreference("USER_NAME", "")
```

## What comes next?

Complex objects
