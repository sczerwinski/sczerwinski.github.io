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

## Room Extensions – Aggregate

[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android.room/room-extensions)][room-extensions-release]
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/it.czerwinski.android.room/room-extensions?server=https%3A%2F%2Foss.sonatype.org)][room-extensions-snapshot]

Artifact `it.czerwinski.android.room:room-extensions` aggregates artifacts:
- `room-database`,
- `room-database-sql`,
- `room-converters`.

You can either use `room-extensions` or any combination of the other artifacts, whichever suites your project.

### Build Configuration

#### Kotlin
```kotlin
dependencies {
    implementation("androidx.room:room-runtime:2.2.6")
    implementation("it.czerwinski.android.room:room-extensions:[VERSION]")
}
```

#### Groovy
```groovy
dependencies {
    implementation 'androidx.room:room-runtime:2.2.6'
    implementation 'it.czerwinski.android.room:room-extensions:[VERSION]'
}
```

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

## Room Database SQL Extensions

[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android.room/room-database-sql)][room-database-sql-release]
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/it.czerwinski.android.room/room-database-sql?server=https%3A%2F%2Foss.sonatype.org)][room-database-sql-snapshot]

### Build Configuration

#### Kotlin
```kotlin
dependencies {
    implementation("androidx.room:room-runtime:2.2.6")
    implementation("it.czerwinski.android.room:room-database-sql:[VERSION]")
}
```

#### Groovy
```groovy
dependencies {
    implementation 'androidx.room:room-runtime:2.2.6'
    implementation 'it.czerwinski.android.room:room-database-sql:[VERSION]'
}
```

### SQL Script Executor

```kotlin
val database: SupportSQLiteDatabase
val sqlScriptExecutor = SQLScriptExecutor {
    +"""
        insert into users(id, username, password) values (1, 'root', 'qwerty');
        insert into user_roles(user_id, role_id) values (1, 1);
    """
}
sqlScriptExecutor.executeOn(database)
```

### Room Database Builder Extensions

#### Populate From SQL
Configures Room to populate a newly created database with an SQL script.

```kotlin
val database = context.roomDatabaseBuilder<MyDatabase>()
    .populateFromSql {
        +"""
            insert into users(id, username, password) values (1, 'root', 'qwerty');
            insert into user_roles(user_id, role_id) values (1, 1);
        """
    }
    .build()
```

#### Populate From SQL Asset
Configures Room to populate a newly created database with an SQL script located in the application `assets/` folder.

```kotlin
val database = context.roomDatabaseBuilder<MyDatabase>()
    .populateFromSqlAsset(context, "sql/populate.sql")
    .build()
```

#### Add Migration From SQL
Adds an SQL script migration to the builder.

```kotlin
val database = context.roomDatabaseBuilder<MyDatabase>()
    .addMigrationFromSql(startVersion = 1, endVersion = 2) {
        +"""
            create table if not exists users (
                id integer primary key asc,
                username text not null,
                password text not null
            );
        """
    }
    .build()
```

#### Add Migration From SQL Asset
Adds a migration to the builder, executing an SQL script located in the application `assets/` folder.

```kotlin
val database = context.roomDatabaseBuilder<MyDatabase>()
    .addMigrationFromSqlAsset(startVersion = 1, endVersion = 2, context, "sql/migrate_1_2.sql")
    .build()
```

#### Add Migrations From SQL Assets
Adds migrations to the builder, executing an SQL scripts located in the application `assets/` folder,
matching the given format.

```kotlin
val database = context.roomDatabaseBuilder<MyDatabase>()
    .addMigrationsFromSqlAssets(context, sqlFilePathFormat = "sql/migrate_{}_{}.sql")
    .build()
```

## Room `TypeConverter`s Generator

[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android.room/room-converters)][room-converters-release]
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/it.czerwinski.android.room/room-converters?server=https%3A%2F%2Foss.sonatype.org)][room-converters-snapshot]

### Build Configuration

#### Kotlin
```kotlin
dependencies {
    implementation("androidx.room:room-runtime:2.2.6")
    implementation("it.czerwinski.android.room:room-converters:[VERSION]")
    kapt("it.czerwinski.android.room:room-converters-processor:[VERSION]")
}
```

#### Groovy
```groovy
dependencies {
    implementation 'androidx.room:room-runtime:2.2.6'
    implementation 'it.czerwinski.android.room:room-converters:[VERSION]'
    kapt 'it.czerwinski.android.room:room-converters-processor:[VERSION]'
}
```

### Generating Room `TypeConverter`s

#### `@GenerateEnumTypeConverter`
Marks an enum class to have automatically generated `@TypeConverter`s to and from the given type.

Enum can be stored in the database as name (`String` – default) or as ordinal (`Int`).

To store enum in a text field (as name):
```kotlin
@GenerateEnumTypeConverter(type = EnumType.STRING)
enum class MyEnum {
    FOO,
    BAR
}
```

To store enum in an integer field (as ordinal):
```kotlin
@GenerateEnumTypeConverter(type = EnumType.ORDINAL)
enum class MyEnum {
    FOO,
    BAR
}
```


[ci-build]: https://github.com/sczerwinski/android-room/actions?query=workflow%3ABuild
[room-extensions-release]: https://repo1.maven.org/maven2/it/czerwinski/android/room/room-extensions/
[room-extensions-snapshot]: https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/room/room-extensions/
[room-database-release]: https://repo1.maven.org/maven2/it/czerwinski/android/room/room-database/
[room-database-snapshot]: https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/room/room-database/
[room-database-sql-release]: https://repo1.maven.org/maven2/it/czerwinski/android/room/room-database-sql/
[room-database-sql-snapshot]: https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/room/room-database-sql/
[room-converters-release]: https://repo1.maven.org/maven2/it/czerwinski/android/room/room-converters/
[room-converters-snapshot]: https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/room/room-converters/