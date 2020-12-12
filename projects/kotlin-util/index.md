---
title: Kotlin utilities
layout: toc-page
abstract: Kotlin utility classes based on Scala
keywords: oss,software,programming,kotlin,utility
project: kotlin-util
---

{% include breadcrumbs-project.html %}

[![Build](https://github.com/sczerwinski/kotlin-util/workflows/Build/badge.svg)](https://github.com/sczerwinski/kotlin-util/actions)
![Kotlin Multiplatform](https://img.shields.io/badge/Kotlin-Multiplatform-blueviolet)  
[![Release](https://github.com/sczerwinski/kotlin-util/workflows/Release/badge.svg)](https://github.com/sczerwinski/kotlin-util/actions)
[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski/kotlin-util.svg)](https://repo1.maven.org/maven2/it/czerwinski/kotlin-util/)  
[![Snapshot Release](https://github.com/sczerwinski/kotlin-util/workflows/Snapshot%20Release/badge.svg)](https://github.com/sczerwinski/kotlin-util/actions)
[![Sonatype Snapshot](https://img.shields.io/nexus/s/https/oss.sonatype.org/it.czerwinski/kotlin-util.svg)](https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/kotlin-util/)  
[![Source](https://img.shields.io/badge/source-GitHub-blue.svg)](https://github.com/sczerwinski/kotlin-util)
[![API Documentation](https://img.shields.io/badge/api-docs-blue.svg)](1.4.20/docs)
![License](https://img.shields.io/badge/license-Apache%202-blue)

## Project Setup

### Gradle

#### Kotlin

```kotlin
implementation("it.czerwinski:kotlin-util:1.4.21")
```

#### Groovy

```groovy
implementation 'it.czerwinski:kotlin-util:1.4.21'
```

### Maven

```xml
<dependency>
  <groupId>it.czerwinski</groupId>
  <artifactId>kotlin-util</artifactId>
  <version>1.4.21</version>
</dependency>
```

### Kotlin Multiplatform Projects

In multiplatform projects, the library can be used as `commonMain` dependency.

See also [Kotlin Multiplatform Mobile Example](#kotlin-multiplatform-mobile-example).

## Supported Types

### Utilities

#### `Option`

[![Scala documentation](https://img.shields.io/badge/scala-docs-blue.svg)](http://www.scala-lang.org/api/2.13.0/scala/Option.html)
[![Scala sources](https://img.shields.io/badge/scala-sources-blue.svg)](https://github.com/scala/scala/blob/v2.13.0/src/library/scala/Option.scala)

Implementation differences:

* `exists` has been replaced with `any` – Kotlin convention
* `forall` has been replaced with `all` – Kotlin convention
* `foreach` has been replaced with `forEach` – Kotlin convention
* `orNull` has been replaced with `getOrNull` – Kotlin convention
* `unzip3` has been replaced with `unzip` – there is no ambiguity in Kotlin
* implemented additional functions: `filterNotNull`, `filterIsInstance` – Kotlin convention

Kotlin introduces its own null-safety mechanisms.
Most of the times, `Option`s can be replaced by nullable types in Kotlin, e.g.:

```kotlin
var number: Option<Int> = // …

number.map { it.toString() }.getOrElse { "" }
```

gives the same result as:

```kotlin
var number: Int? = // …

number?.let { it.toString() }.orEmpty()
```

However, `Option`s might be useful whenever `null` values are not allowed,
e.g. RxJava 2.x `Observable`.

#### `Either`

[![Scala documentation](https://img.shields.io/badge/scala-docs-blue.svg)](http://www.scala-lang.org/api/2.13.0/scala/util/Either.html)
[![Scala sources](https://img.shields.io/badge/scala-sources-blue.svg)](https://github.com/scala/scala/blob/v2.13.0/src/library/scala/util/Either.scala)

Implementation differences:

* `exists` has been replaced with `any` – Kotlin convention
* `forall` has been replaced with `all` – Kotlin convention
* `foreach` has been replaced with `forEach` – Kotlin convention
* implemented additional functions: `filterNot`, `filterNotNull`, `filterIsInstance` – Kotlin convention
* implemented additional functions: `filterToOption`, `filterNotToOption`, `filterNotNullToOption`, `filterIsInstanceToOption`
* implemented additional function `getOrNull` in addition to `toOption` – Kotlin uses its own null-safety mechanisms

Since version 1.3, this implementation is right-biased, therefore it is possible
to use methods directly on `Either` instead of `RightProjection`,
e.g. it is possible to use `Either.map {}` instead of `Either.right.map {}`.
Use of `RightProjection` has been deprecated.

Scala convention that “dictates that `Left` is used for failure and `Right` is used for success”
(Scala Standard Library Documentation) is still a preferred way of using this class.

#### `Try`

[![Scala documentation](https://img.shields.io/badge/scala-docs-blue.svg)](http://www.scala-lang.org/api/2.13.0/scala/util/Try.html)
[![Scala sources](https://img.shields.io/badge/scala-sources-blue.svg)](https://github.com/scala/scala/blob/v2.13.0/src/library/scala/util/Try.scala)

Implementation differences:

* `foreach` has been replaced with `forEach` – Kotlin convention
* implemented additional functions: `filterNot`, `filterNotNull`, `filterIsInstance` – Kotlin convention
* implemented additional function `getOrNull` in addition to `toOption` – Kotlin uses its own null-safety mechanisms

### Additional Iterators

#### `EmptyIterator`

Iterator based on the result of `scala.collection.Iterator.empty`, producing no values.

Kotlin defines an internal `EmptyIterator`, which can only be obtained indirectly
from empty collections, e.g.:

```kotlin
emptyList<Nothing>().iterator()
```

#### `SingletonIterator`

Iterator based on the result of `scala.collection.Iterator.single[A](elem: A)`, producing a single value.

An iterator for a singleton list is defined in Java, in a package-private static method
`java.util.Collections.singletonIterator(E e)`. It can only be obtained indirectly
from a new instance of a singleton list, e.g.:
```kotlin
java.util.Collections.singletonList(element).iterator()
```

## Kotlin Multiplatform Mobile Example

1. Create a new [Kotlin Multiplatform Mobile](https://kotlinlang.org/docs/mobile/home.html) project.
2. In `shared/build.gradle.kts`, add `kotlin-util` dependency to `commonMain`:
    ```kotlin
    repositories {
        // [...]
    
        mavenCentral()
    }
    kotlin {
        // [...]
    
        sourceSets {
            // [...]
    
            val commonMain by getting {
                dependencies {
                    implementation("it.czerwinski:kotlin-util:1.4.21")
                }
            }
        }
    }
    ```
3. Edit `Platform` class to return `Option<String>`:
    `commonMain`:
    ```kotlin
    expect class Platform() {
        val platform: Option<String>
    }
    ```
    `androidMain`:
    ```kotlin
    actual class Platform actual constructor() {
        actual val platform: Option<String> = Some("Android ${android.os.Build.VERSION.SDK_INT}")
    }
    ```
    `iosMain`:
    ```kotlin
    actual class Platform actual constructor() {
        actual val platform: Option<String> = Some(
            UIDevice.currentDevice.systemName() + " " + UIDevice.currentDevice.systemVersion
        )
    }
    ```
4. Edit `Greetings` class to get value from `Option`:
    ```kotlin
    class Greeting {
        fun greeting(): String {
            return "Hello, kotlin-util on ${Platform().platform.getOrElse { "unknown platform" }}!"
        }
    }    
    ```
5. Run both mobile apps.
<div class="row">
    <div class="col-xs-12 col-md-6">
        {% include thumbnail.html image="/assets/img/project/kotlin-util/kmm/screenshot-android.png" thumb="/assets/img/project/kotlin-util/kmm/screenshot-android-thumb.png" title="Android screenshot" %}
    </div>
    <div class="col-xs-12 col-md-6">
        {% include thumbnail.html image="/assets/img/project/kotlin-util/kmm/screenshot-ios.png" thumb="/assets/img/project/kotlin-util/kmm/screenshot-ios-thumb.png" title="iOS screenshot" %}
    </div>
</div>
