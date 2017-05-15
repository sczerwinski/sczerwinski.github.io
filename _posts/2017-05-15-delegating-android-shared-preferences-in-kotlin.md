---
disqusid: delegating-android-shared-preferences-in-kotlin
title: Delegating Android SharedPreferences in Kotlin
mobileTitle: Delegating SharedPreferences
layout: post
abstract: How to solve the problem of boilerplate code related to SharedPreferences in Android applications
keywords: kotlin,delegation,android,sharedpreferences
tags: kotlin,android
---

> [_I have learned to delegate._](https://www.brainyquote.com/quotes/quotes/g/gwenstefan468230.html)
>
> — Gwen Stefani

## The Problem: Boilerplate Code

[`SharedPreferences`](https://developer.android.com/reference/android/content/SharedPreferences.html)
provide a relatively simple way to store key-value pairs on Android.
The application might not only use them to save its settings, but also to keep its persistent state.

However, when the app gets more complex, using `SharedPreferences` might become painful.
The boilerplate code required to retrieve and later store the preference takes more lines
than the actual operation performed on its value.

For example, consider a `LoginActivity` that only displays input for username and password.
As a user, I want the application to remember my username so that I don’t need to type it again
the next time I want to log in—true _story_ (pun intended).

How can we do this in Java?

First, we need to get an instance of `SharedPreferences` object. Assuming our code is in the `Activity`,
we can do it by calling `getSharedPreferences()`:

```java
SharedPreferences sharedPreferences =
        getSharedPreferences(
            "it.czerwinski.myapp.MY_PREFERENCES",
            Context.MODE_PRIVATE);
```

Or, if multiple preferences files are not needed, we may use the default shared preferences:

```java
SharedPreferences sharedPreferences =
        PreferenceManager.getDefaultSharedPreferences(this);
```

To retrieve a `String` value, we may use `getString()` method, which requires the name
of the preference, and the default value, returned if the preference does not exist:

```java
usernameEditText.setText(
        sharedPreferences.getString("USERNAME", ""));
```

Storing the value, however, is not that straightforward. `SharedPreferences` object only provides
the methods to retrieve preferences. To save the values, we need to use an `Editor`,
returned by the `edit()` method:

```java
sharedPreferences.edit()
        .putString("USERNAME", usernameEditText.getText().toString())
        .apply();
```

Don’t forget to call `apply()`. Otherwise, the value would not be saved.

It looks simple and clean… so long as we only need two or three calls to `SharedPreferences`.
But typically, that is not the case, is it?

## Anko Comes To The Rescue

Kotlin language is probably the best thing that has happened to Android developers
since first Android phones hit the market. It allowed to create powerful
yet lightweight tools that simplify our lives.

One of those tools, Anko, provides an
[extension property](https://kotlinlang.org/docs/reference/extensions.html#extension-properties)
for Android `Context` class—`defaultSharedPreferences`. By using that property,
we no longer need to explicitly initialize the `SharedPreferences` object.
Still, we need to retrieve and store the values in the same inconvenient manner:

```kotlin
usernameEditText.setText(
        defaultSharedPreferences.getString("USERNAME", ""))
```

```kotlin
defaultSharedPreferences.edit()
        .putString("USERNAME", usernameEditText.text.toString())
        .apply()
```

## Utilize Kotlin Properties

If several instructions appear in the code more than once, we should extract it into a separate method,
or in this case, two methods—`getUsername` and `setUsername`.

But this is Kotlin, right? Why not declare a property with
[a custom getter and a custom setter](https://kotlinlang.org/docs/reference/properties.html#getters-and-setters)?
We may also make it an extension property and use it from any `Activity` in our app:

```kotlin
var Context.username: String
    get() = defaultSharedPreferences.getString("USERNAME", "")
    set(value) = defaultSharedPreferences.edit()
            .putString("USERNAME", value)
            .apply()
```

As a result, saving and restoring the username is much simpler:

```kotlin
usernameEditText.setText(username)
```

```kotlin
username = usernameEditText.text.toString()
```

Wy can now get or set the username by referring to a single property.
I cannot imagine any way of simplifying that.

However, this approach still has its disadvantages.
Take another look at the declaration of the `username` property…
It doesn’t look very nice, but at least everything is in one place, right?
Okay… Now, imagine that we need 20 similar properties in our app… or 50… or 100…

## Delegate

> _There are certain common kinds of properties, that, though we can implement them manually
> every time we need them, would be very nice to implement once and for all […]_
>
> — Delegated Properties, Kotlin Programming Language Reference

The above quotation perfectly conveys our needs. And Kotlin offers a solution in the form of
[delegated properties](https://kotlinlang.org/docs/reference/delegated-properties.html).

So let’s create one:

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

Now, any declaration of a property might be delegated to `SharedPreferences` in a single line of code:

```kotlin
var username: String by StringSharedPreferenceDelegate(context, "USERNAME", "")
```

## Reuse

> _[…] and put into a library._
>
> — Delegated Properties, Kotlin Programming Language Reference

Most Android applications use `SharedPreferences`. So we should probably create an external library
to make our solution reusable. And guess what. I’ve already done that. The project is available on
[GitHub](https://github.com/sczerwinski/android-delegates-shared-preferences/tree/master).

To use the library, add it to your Gradle dependencies (the package is added to _jcenter_ repository):

```gradle
dependencies {
    compile 'it.czerwinski.android:delegates-shared-preferences:0.1'
}
```

A property can now be defined with a single line in your `Activity` class:

```kotlin
var username by stringSharedPreference("USERNAME", "")
```

Or in any other class with a reference to the `Context`:

```kotlin
var username by context.stringSharedPreference("USERNAME", "")
```

Though, it might be a good idea to define
an [extension function](https://kotlinlang.org/docs/reference/extensions.html#extension-functions),
at least for those preferences which are referenced from several different classes:

```kotlin
fun Context.usernameSharedPreference() =
        stringSharedPreference("USERNAME", "")
```

```kotlin
var username by usernameSharedPreference()
```

## What’s Next?

So far, the library only supports several data types:
`Int`, `Long`, `Float`, `Double`, `Boolean`, `String` and `Set<String>`.
In future releases, I plan to implement delegates for other common types, e.g. `Array`, `List`, `Date`,
as well as `data` classes.

For example, if the user selects the ‘remember password’ `CheckBox`,
we should store both `username` and `password` in the `SharedPreferences`:

```kotlin
data class User(val username: String, val password: String)
```

And both values should be committed at the same time:

```kotlin
sharedPreferences.edit()
        .putString("USERNAME", username)
        .putString("PASSWORD", password)
        .apply()
```

Hopefully, I’ll be able to describe my solution soon.
