---
title: Android Lifecycle Extensions
layout: toc-page
abstract: Extensions for Jetpack Lifecycle
keywords: oss,software,programming,android,lifecycle,livedata
project: android-lifecycle
---

{% include breadcrumbs-project.html %}

[![Build](https://github.com/sczerwinski/android-lifecycle/workflows/Build/badge.svg)][ci-build]
[![Source](https://img.shields.io/badge/source-GitHub-blue.svg)](https://github.com/sczerwinski/android-lifecycle)
[![API Documentation](https://img.shields.io/badge/api-docs-blue.svg)](1.2.0/docs)
![License](https://img.shields.io/badge/license-Apache%202-blue)

## LiveData Extensions

[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android.lifecycle/lifecycle-livedata)][lifecycle-livedata-release]
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/it.czerwinski.android.lifecycle/lifecycle-livedata?server=https%3A%2F%2Foss.sonatype.org)][lifecycle-livedata-snapshot]

### Build Configuration

#### Kotlin
```kotlin
dependencies {
    implementation("it.czerwinski.android.lifecycle:lifecycle-livedata:[VERSION]")
}
```

#### Groovy
```groovy
dependencies {
    implementation 'it.czerwinski.android.lifecycle:lifecycle-livedata:[VERSION]'
}
```

### Types

#### `ConstantLiveData`
[LiveData] that always emits a single constant value.

#### `GroupedLiveData`
[MediatorLiveData] subclass which provides a separate [LiveData] per each result returned by `keySelector` function
executed on subsequent values emitted by the source LiveData.

### LiveData Factory Methods

#### `intervalLiveData`

Returns a [LiveData] emitting a sequence of integer values, spaced by a given `timeInMillis`.

```kotlin
val fixedIntervalLiveData: LiveData<Int> = intervalLiveData(timeInMillis = 1000L)
val varyingIntervalLiveData: LiveData<Int> = intervalLiveData { index -> (index + 1) * 1000L }
```

### LiveData Transformations

#### `mapNotNull`
Returns a [LiveData] emitting only the non-null results of applying the given `transform` function to each value
emitted by this LiveData.

```kotlin
val userOptionLiveData: LiveData<Option<User>> = // ...
val userLiveData: LiveData<User> = userOptionLiveData.mapNotNull { user -> user.getOrNull() }
```

#### `filter`
Returns a [LiveData] emitting only values from this LiveData matching the given `predicate`.

```kotlin
val resultLiveData: LiveData<Try<User>> = // ...
val successLiveData: LiveData<Try<User>> = resultLiveData.filter { it.isSuccess }
```

#### `filterNotNull`
Returns a [LiveData] emitting only non-null values from this LiveData.

```kotlin
val userLiveData: LiveData<User?> = // ...
val nonNullUserLiveData: LiveData<User> = userLiveData.filterNotNull()
```

#### `filterIsInstance`
Returns a [LiveData] emitting only values of the given type from this LiveData.

```kotlin
val resultLiveData: LiveData<Try<User>> = // ...
val failureLiveData: LiveData<Failure> = resultLiveData.filterIsInstance<Failure>()
```

#### `reduce`
Returns a [LiveData] emitting accumulated value starting with the first value emitted by this LiveData and applying
`operation` from left to right to current accumulator value and each value emitted by this.

```kotlin
val newOperationsCountLiveData: LiveData<Int?> = // ...
val operationsCountLiveData: LiveData<Int?> =
    newOperationsCountLiveData.reduce { acc, next -> if (next == null) null else acc + next }
```

#### `reduceNotNull`
Returns a [LiveData] emitting non-null accumulated value starting with the first non-null value emitted by this
LiveData and applying `operation` from left to right to current accumulator value and each subsequent non-null value
emitted by this LiveData.

```kotlin
val newOperationsCountLiveData: LiveData<Int> = // ...
val operationsCountLiveData: LiveData<Int> =
    newOperationsCountLiveData.reduceNotNull { acc, next -> acc + next }
```

#### `throttleWithTimeout`
Returns a [LiveData] emitting values from this LiveData, after dropping values followed by newer values before
`timeInMillis` expires.

```kotlin
val isLoadingLiveData: LiveData<Boolean> = // ...
val isLoadingThrottledLiveData: LiveData<Boolean> = isLoadingLiveData.throttleWithTimeout(
    timeInMillis = 1000L,
    context = viewModelScope.coroutineContext
)
```

#### `delayStart`
Returns a [LiveData] emitting values from this LiveData, after dropping values followed by newer values before
`timeInMillis` expires since the result LiveData has been created.

```kotlin
val resultLiveData: LiveData<ResultData> = // ...
val delayedResultLiveData: LiveData<ResultData> = resultLiveData.delayStart(
    timeInMillis = 1000L,
    context = viewModelScope.coroutineContext
)
```

#### `merge`
Returns a [LiveData] emitting each value emitted by any of the given LiveData.

```kotlin
val serverError: LiveData<String> = // ...
val databaseError: LiveData<String> = // ...
val error: LiveData<String> = serverError merge databaseError
```

```kotlin
val serverError: LiveData<String> = // ...
val databaseError: LiveData<String> = // ...
val fileError: LiveData<String> = // ...
val error: LiveData<String> = merge(serverError, databaseError, fileError)
```

#### `combineLatest`
Returns a [LiveData] emitting pairs, triples or lists of latest values emitted by the given LiveData.

```kotlin
val userLiveData: LiveData<User> = // ...
val avatarUrlLiveData: LiveData<String> = // ...
val userWithAvatar: LiveData<Pair<User?, String?>> = combineLatest(userLiveData, avatarUrlLiveData)
```

```kotlin
val userLiveData: LiveData<User> = // ...
val avatarUrlLiveData: LiveData<String> = // ...
val userWithAvatar: LiveData<UserWithAvatar> =
    combineLatest(userLiveData, avatarUrlLiveData) { user, avatarUrl ->
        UserWithAvatar(user, avatarUrl)
    }
```

#### `switch`
Converts [LiveData] that emits other LiveData into a single LiveData that emits the items emitted by the most
recently emitted LiveData.

```kotlin
val sourcesLiveData: LiveData<LiveData<String>> = // ...
val resultLiveData: LiveData<String?> = sourcesLiveData.switch()
```

#### `groupBy`
Returns a `GroupedLiveData` providing a set of [LiveData], each emitting a different subset of values from this
LiveData, based on the result of the given `keySelector` function.

```kotlin
val userLiveData: LiveData<User> = // ...
val userByStatusLiveData: GroupedLiveData<UserStatus, User> = errorLiveData.groupBy { user -> user.status }
val activeUserLiveData: LiveData<User> = userByStatusLiveData[UserStatus.ACTIVE]
```

#### `defaultIfEmpty`
Returns a [LiveData] that emits the values emitted by this LiveData or a specified default value if this LiveData has
not yet emitted any values at the time of observing.

```kotlin
val errorLiveData: LiveData<String> = // ...
val statusLiveData: LiveData<String?> = errorLiveData.defaultIfEmpty("No errors")
```

### MediatorLiveData Extensions

#### `addDirectSource`
Starts to listen the given source LiveData.
Whenever source value is changed, it is set as a new value of this [MediatorLiveData].

```kotlin
mediatorLiveData.addDirectSource(liveData)
```
is equivalent to:
```kotlin
mediatorLiveData.addSource(liveData) { x -> mediatorLiveData.value = x }
```

## Common LivaData Testing Utilities

[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android.lifecycle/lifecycle-livedata-test-common)][lifecycle-livedata-test-common-release]
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/it.czerwinski.android.lifecycle/lifecycle-livedata-test-common?server=https%3A%2F%2Foss.sonatype.org)][lifecycle-livedata-test-common-snapshot]

Available since v1.1.0.

### Build Configuration

This package is included in both `lifecycle-livedata-test-junit4` and `lifecycle-livedata-test-junit5`.

#### Kotlin
```kotlin
dependencies {
    testImplementation("junit:junit:4.13.1")
    testImplementation("it.czerwinski.android.lifecycle:lifecycle-livedata-test-common:[VERSION]")
}
```

#### Groovy
```groovy
dependencies {
    testImplementation 'junit:junit:4.13.1'
    testImplementation 'it.czerwinski.android.lifecycle:lifecycle-livedata-test-common:[VERSION]'
}
```

### Testing Observed Values

#### `TestObserver`

A callback testing values emitted by [LiveData].

```kotlin
class MyTestClass {

    @Test
    fun testMethod1() {
        MutableLiveData<Int>()
            .test()
            .assertNoValues()
    }

    @Test
    fun testMethod2() {
        val liveData = MutableLiveData<Int>()

        val observer = liveData.test()

        liveData.postValue(1)
        liveData.postValue(2)
        liveData.postValue(3)

        observer.assertValues(1, 2, 3)
    }
}
```

## LivaData Testing Utilities For JUnit4

[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android.lifecycle/lifecycle-livedata-test-junit4)][lifecycle-livedata-test-junit4-release]
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/it.czerwinski.android.lifecycle/lifecycle-livedata-test-junit4?server=https%3A%2F%2Foss.sonatype.org)][lifecycle-livedata-test-junit4-snapshot]

### Build Configuration

#### Kotlin
```kotlin
dependencies {
    testImplementation("junit:junit:4.13.1")
    testImplementation("it.czerwinski.android.lifecycle:lifecycle-livedata-test-junit4:[VERSION]")
}
```

#### Groovy
```groovy
dependencies {
    testImplementation 'junit:junit:4.13.1'
    testImplementation 'it.czerwinski.android.lifecycle:lifecycle-livedata-test-junit4:[VERSION]'
}
```

### JUnit4 Rules

#### `TestCoroutineDispatcherRule`

JUnit4 test rule that swaps main coroutine dispatcher with [UnconfinedTestDispatcher].
_Note that [TestCoroutineDispatcher] is now deprecated._

```kotlin
class MyTestClass {

    @Rule
    @JvmField
    val testCoroutineDispatcherRule = TestCoroutineDispatcherRule()

    val testCoroutineScheduler get() = testCoroutineDispatcherRule.scheduler

    // ...
}
```

## LivaData Testing Utilities For JUnit5

[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android.lifecycle/lifecycle-livedata-test-junit5)][lifecycle-livedata-test-junit5-release]
[![Sonatype Nexus (Snapshots)](https://img.shields.io/nexus/s/it.czerwinski.android.lifecycle/lifecycle-livedata-test-junit5?server=https%3A%2F%2Foss.sonatype.org)][lifecycle-livedata-test-junit5-snapshot]

### Build Configuration

#### Kotlin
```kotlin
dependencies {
    testImplementation("org.junit.jupiter:junit-jupiter-api:5.7.0")
    testRuntimeOnly("org.junit.jupiter:junit-jupiter-engine:5.7.0")
    testImplementation("it.czerwinski.android.lifecycle:lifecycle-livedata-test-junit5:[VERSION]")
}
```

#### Groovy
```groovy
dependencies {
    testImplementation 'org.junit.jupiter:junit-jupiter-api:5.7.0'
    testRuntimeOnly 'org.junit.jupiter:junit-jupiter-engine:5.7.0'
    testImplementation 'it.czerwinski.android.lifecycle:lifecycle-livedata-test-junit5:[VERSION]'
}
```

### JUnit5 Extensions

#### `InstantTaskExecutorExtension`

JUnit5 extension that swaps the background executor used by the Architecture Components with a different one which
executes each task synchronously.

This extension is analogous to [InstantTaskExecutorRule] for JUnit4.

```kotlin
@ExtendWith(InstantTaskExecutorExtension::class)
class MyTestClass {
    // ...
}
```

#### `TestCoroutineDispatcherExtension`

JUnit5 extension that swaps main coroutine dispatcher with [UnconfinedTestDispatcher].
_Note that [TestCoroutineDispatcher] is now deprecated._

Any test method parameter of type [TestCoroutineScheduler] will be resolved as the scheduler of the [TestCoroutineDispatcher]:

```kotlin
@ExtendWith(TestCoroutineDispatcherExtension::class)
class MyTestClass {

    @Test
    fun someTest(scheduler: TestCoroutineScheduler) {
        // ...
        scheduler.advanceTimeBy(delayTimeMillis = 1000L)
        scheduler.runCurrent()
        // ...
    }
}
```

In case of parameterized tests, the scheduler can be passed as a parameter of a before method:

```kotlin
@ExtendWith(TestCoroutineDispatcherExtension::class)
class MyTestClass {

    private lateinit var testCoroutineScheduler: TestCoroutineScheduler

    @BeforeEach
    fun setScheduler(scheduler: TestCoroutineScheduler) {
        testCoroutineScheduler = scheduler
    }

    @ParameterizedTest
    @MethodSource("testData")
    fun someParameterizedTest(input: Int) {
        // ...
    }
}
```


[ci-build]: https://github.com/sczerwinski/android-lifecycle/actions?query=workflow%3ABuild
[lifecycle-livedata-release]: https://repo1.maven.org/maven2/it/czerwinski/android/lifecycle/lifecycle-livedata/
[lifecycle-livedata-test-common-release]: https://repo1.maven.org/maven2/it/czerwinski/android/lifecycle/lifecycle-livedata-test-common/
[lifecycle-livedata-test-junit4-release]: https://repo1.maven.org/maven2/it/czerwinski/android/lifecycle/lifecycle-livedata-test-junit4/
[lifecycle-livedata-test-junit5-release]: https://repo1.maven.org/maven2/it/czerwinski/android/lifecycle/lifecycle-livedata-test-junit5/
[lifecycle-livedata-snapshot]: https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/lifecycle/lifecycle-livedata/
[lifecycle-livedata-test-common-snapshot]: https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/lifecycle/lifecycle-livedata-test-common/
[lifecycle-livedata-test-junit4-snapshot]: https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/lifecycle/lifecycle-livedata-test-junit4/
[lifecycle-livedata-test-junit5-snapshot]: https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/lifecycle/lifecycle-livedata-test-junit5/

[LiveData]: https://developer.android.com/reference/androidx/lifecycle/LiveData
[MediatorLiveData]: https://developer.android.com/reference/androidx/lifecycle/MediatorLiveData
[InstantTaskExecutorRule]: https://developer.android.com/reference/androidx/arch/core/executor/testing/InstantTaskExecutorRule
[TestCoroutineDispatcher]: https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-test/kotlinx.coroutines.test/-test-coroutine-dispatcher/
[UnconfinedTestDispatcher]: https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-test/kotlinx.coroutines.test/-unconfined-test-dispatcher.html
[TestCoroutineScheduler]: https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-test/kotlinx.coroutines.test/-test-coroutine-scheduler/index.html
