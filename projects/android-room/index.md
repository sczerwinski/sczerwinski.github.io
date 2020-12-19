---
title: Android Room Extensions
layout: toc-page
abstract: Extensions for Jetpack Room
keywords: oss,software,programming,android,room,database
project: android-room
---

{% include breadcrumbs-project.html %}

[![Build](https://github.com/sczerwinski/android-room/workflows/Build/badge.svg)][ci-build]
[![Source](https://img.shields.io/badge/source-GitHub-blue.svg)](https://github.com/sczerwinski/android-room)
![License](https://img.shields.io/badge/license-Apache%202-blue)

## Room Database Extensions

[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android.room/room-database)][room-database-release]
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/it.czerwinski.android.room/room-database?server=https%3A%2F%2Foss.sonatype.org)][room-database-snapshot]

### Build Configuration

#### Kotlin
```kotlin
dependencies {
    implementation("androidx.room:room-runtime:2.2.6")
    implementation("it.czerwinski.android.room:room-database:[VERSION]")
}
```

#### Groovy
```groovy
dependencies {
    implementation 'androidx.room:room-runtime:2.2.6'
    implementation 'it.czerwinski.android.room:room-database:[VERSION]'
}
```

### Room Database Builders

#### `roomDatabaseBuilder`
Creates a `RoomDatabase.Builder` for a persistent database with type `T` and the given `name`.

```kotlin
val database = context.roomDatabaseBuilder<MyDatabase>().build()
```
or:
```kotlin
val database = context.roomDatabaseBuilder<MyDatabase>(name = "database").build()
```

#### `roomInMemoryDatabaseBuilder`
Creates a `RoomDatabase.Builder` for an in memory database with type `T`.

```kotlin
val database = context.roomInMemoryDatabaseBuilder<MyDatabase>().build()
```


[ci-build]: https://github.com/sczerwinski/android-room/actions?query=workflow%3ABuild
[room-database-release]: https://repo1.maven.org/maven2/it/czerwinski/android/room/room-database/
[room-database-snapshot]: https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/room/room-database/
