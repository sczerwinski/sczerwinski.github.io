---
disqusid: delegating-android-shared-preferences-in-kotlin
title: Delegating Android SharedPreferences in Kotlin
mobileTitle: Delegating SharedPreferences
layout: post
abstract: How I solved the problem of <code>SharedPreferences</code> boilerplate code in Android applications
keywords: kotlin,delegation,android,sharedpreferences
tags: kotlin,android
---

> [_I have learned to delegate._](https://www.brainyquote.com/quotes/quotes/g/gwenstefan468230.html)
>
> — Gwen Stefani

[`SharedPreferences`](https://developer.android.com/reference/android/content/SharedPreferences.html)
provide a relatively simple way to store key-value pairs on Android.
The application might not only use them to save its settings, but also to keep its persistent state.

## The Problem: Boilerplate Code

However, when the app gets more complex, using `SharedPreferences` might become really painful.
The boilerplate code required to retrieve and later store the preference takes more lines
than the actual operation performed on its value.

As an example, consider a `LoginActivity` that only displays input for username and password.
As a user, I want the application to remember my username so that I do not need to type it again
the next time I want to log in. True _story_ (pun intended).



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
        sharedPreferences.getString("USERNAME", ""));
```

```java
sharedPreferences.edit()
        .putString("USERNAME", usernameEditText.getText().toString())
        .apply();
```

## Anko Comes To The Rescue

```kotlin
import org.jetbrains.anko.defaultSharedPreferences
```

```kotlin
usernameEditText.setText(
        defaultSharedPreferences.getString("USERNAME", ""))
```

```kotlin
defaultSharedPreferences.edit()
        .putString("USERNAME", usernameEditText.text.toString())
        .apply()
```

## Utilizing Kotlin Properties

[getters and setters](https://kotlinlang.org/docs/reference/properties.html#getters-and-setters)

```kotlin
var username: String
    get() = defaultSharedPreferences.getString("USERNAME", "")
    set(value) = defaultSharedPreferences.edit()
            .putString("USERNAME", value)
            .apply()
```

```kotlin
usernameEditText.setText(username)
```

```kotlin
username = usernameEditText.text.toString()
```

## Delegate It

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
var username: String by StringSharedPreferenceDelegate(this, "USERNAME", "")
```

## The Solution: External Library

[library](https://github.com/sczerwinski/android-delegates-shared-preferences/tree/master)

```gradle
dependencies {
    compile 'it.czerwinski.android:delegates-shared-preferences:0.1'
}
```

```kotlin
var username by stringSharedPreference("USERNAME", "")
```

```kotlin
var username by context.stringSharedPreference("USERNAME", "")
```

```kotlin
fun Context.usernameSharedPreference() =
        stringSharedPreference("USERNAME", "")
```

```kotlin
var username by usernameSharedPreference()
```

## Next Step

Complex objects
