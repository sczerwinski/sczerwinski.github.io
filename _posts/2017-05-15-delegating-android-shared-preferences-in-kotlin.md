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

How can this be done in Java?

First, we need to get an instance of `SharedPreferences` object. Assuming our code is in the `Activity`,
we can do it by calling `getSharedPreferences()`:

```java
SharedPreferences sharedPreferences =
        getSharedPreferences(
            "it.czerwinski.myapp.MY_PREFERENCES",
            Context.MODE_PRIVATE);
```

Or, if multiple preferences files are not needed, we may use the default shared preferences instead:

```java
SharedPreferences sharedPreferences =
        PreferenceManager.getDefaultSharedPreferences(this);
```

We may then retrieve a `String` by calling the `getString()` method, which requires the name
of the preference, and the default value, returned if the preference does not exist:

```java
usernameEditText.setText(
        sharedPreferences.getString("USERNAME", ""));
```

Storing the value, however, is not that straightforward. `SharedPreferences` object only provides
methods to get preferences. To save any values, we need to use an `Editor`,
returned by the `edit()` method:

```java
sharedPreferences.edit()
        .putString("USERNAME", usernameEditText.getText().toString())
        .apply();
```

We shouldn’t forget to call `apply()`. Otherwise, the value would not be saved.

It looks simple and clean… as long as we only need two or three calls to `SharedPreferences`.
But typically, that is not the case, is it?

## Anko Comes To The Rescue

Kotlin language is probably the best thing that has happened to Android developers
since first Android phones hit the market. It allowed to create powerful
yet lightweight tools that simplify our lives.

One of those tools, Anko, provides an
[extension property](https://kotlinlang.org/docs/reference/extensions.html#extension-properties)
for Android `Context` class—`defaultSharedPreferences`—that eliminates the need
to explicitly initialize the `SharedPreferences` object.
Nonetheless, we still need to retrieve and store the values in the same inconvenient manner:

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

If several instructions appear in the code more than once, they should be extracted into a separate method,
or in this case, two methods—`getUsername` and `setUsername`.

But this is Kotlin, right? Why not declare a property with defined custom
[getter and setter](https://kotlinlang.org/docs/reference/properties.html#getters-and-setters)?
It can also be made an extension property that might be referenced from any `Activity` in our app:

```kotlin
var Context.username: String
    get() = defaultSharedPreferences.getString("USERNAME", "")
    set(value) = defaultSharedPreferences.edit()
            .putString("USERNAME", value)
            .apply()
```

As a result, saving and restoring the username becomes much simpler:

```kotlin
usernameEditText.setText(username)
```

```kotlin
username = usernameEditText.text.toString()
```

We can now get or set the username by referring to a single property.
I cannot imagine any way of simplifying that.

However, this approach still has its drawbacks.
Take another look at the declaration of the `username` property.
It’s a bit complicated, but at least everything is in one place, right?
Fair enough. Now, imagine that there are 10 similar properties in the app… or make it 20… or 50…

## Delegate

> _There are certain common kinds of properties, that, though we can implement them manually
> every time we need them, would be very nice to implement once and for all […]_
>
> — Delegated Properties, Kotlin Programming Language Reference

The above quotation perfectly conveys our needs. And Kotlin offers us
a solution—[delegated properties](https://kotlinlang.org/docs/reference/delegated-properties.html).

So let’s create a delegate that deals with values stored in `SharedPreferences`:

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

Now, any declaration of a property might be delegated to an instance of `StringSharedPreferenceDelegate`
in a single line of code:

```kotlin
var username: String by StringSharedPreferenceDelegate(context, "USERNAME", "")
```

## Reuse

> _[…] and put into a library._
>
> — Delegated Properties, Kotlin Programming Language Reference

Most Android applications use `SharedPreferences`. So we should probably create an external library
to make the solution reusable. And guess what. I’ve already done that. The project is available on
[GitHub](https://github.com/sczerwinski/android-delegates-shared-preferences/tree/master).

To use the library, simply include it in your Gradle dependencies (the package is linked to
[_jcenter_](https://bintray.com/sczerwinski/android/delegates-shared-preferences) repository):

```gradle
dependencies {
    compile 'it.czerwinski.android:delegates-shared-preferences:0.1'
}
```

A property can then be defined in your `Activity` class:

```kotlin
var username by stringSharedPreference("USERNAME", "")
```

Or in any other class containing a reference to the `Context`:

```kotlin
var username by context.stringSharedPreference("USERNAME", "")
```

Though, it might be a good idea to define
an [extension function](https://kotlinlang.org/docs/reference/extensions.html#extension-functions),
at least for those preferences, which are referenced from multiple different classes:

```kotlin
fun Context.usernameSharedPreference() =
        stringSharedPreference("USERNAME", "")
```

```kotlin
var username by usernameSharedPreference()
```

## What’s Next?

So far, the library only supports several basic data types:
`Int`, `Long`, `Float`, `Double`, `Boolean`, `String` and `Set<String>`.
In future releases, I plan to implement delegates for other common types,
e.g. `Array`, `List`, `Date`, as well as `data` classes.

For example, if the user selects the ‘remember password’ `CheckBox`,
both `username` and `password` should be stored in the `SharedPreferences`:

```kotlin
data class User(val username: String, val password: String)
```

What’s more, both values should be committed at the same time:

```kotlin
sharedPreferences.edit()
        .putString("USERNAME", username)
        .putString("PASSWORD", password)
        .apply()
```

But that’s another story.
