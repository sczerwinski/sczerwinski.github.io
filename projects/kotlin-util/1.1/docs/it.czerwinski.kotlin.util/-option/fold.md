---
title: Option.fold - Kotlin utility classes based on Scala
---

[Kotlin utility classes based on Scala](../../index.html) / [it.czerwinski.kotlin.util](../index.html) / [Option](index.html) / [fold](./fold.html)

# fold

`inline fun <R> fold(default: `[`R`](fold.html#R)`, transform: (`[`T`](index.html#T)`) -> `[`R`](fold.html#R)`): `[`R`](fold.html#R)

Returns result of applying [transform](fold.html#it.czerwinski.kotlin.util.Option$fold(it.czerwinski.kotlin.util.Option.fold.R, kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.fold.R)))/transform) on the value of [Some](../-some/index.html) or [default](fold.html#it.czerwinski.kotlin.util.Option$fold(it.czerwinski.kotlin.util.Option.fold.R, kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.fold.R)))/default) if this is [None](../-none/index.html).

### Parameters

`default` - Value to be returned if the option is empty.

`transform` - Function transforming [Some](../-some/index.html) value.

**Return**
Result of applying [transform](fold.html#it.czerwinski.kotlin.util.Option$fold(it.czerwinski.kotlin.util.Option.fold.R, kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.fold.R)))/transform) on the value of [Some](../-some/index.html) or [default](fold.html#it.czerwinski.kotlin.util.Option$fold(it.czerwinski.kotlin.util.Option.fold.R, kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.fold.R)))/default) if this is [None](../-none/index.html).

`inline fun <R> fold(default: () -> `[`R`](fold.html#R)`, transform: (`[`T`](index.html#T)`) -> `[`R`](fold.html#R)`): `[`R`](fold.html#R)

Returns result of applying [transform](fold.html#it.czerwinski.kotlin.util.Option$fold(kotlin.Function0((it.czerwinski.kotlin.util.Option.fold.R)), kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.fold.R)))/transform) on the value of [Some](../-some/index.html) or [default](fold.html#it.czerwinski.kotlin.util.Option$fold(kotlin.Function0((it.czerwinski.kotlin.util.Option.fold.R)), kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.fold.R)))/default) if this is [None](../-none/index.html).

### Parameters

`default` - Function producing value to be returned if the option is empty.

`transform` - Function transforming [Some](../-some/index.html) value.

**Return**
Result of applying [transform](fold.html#it.czerwinski.kotlin.util.Option$fold(kotlin.Function0((it.czerwinski.kotlin.util.Option.fold.R)), kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.fold.R)))/transform) on the value of [Some](../-some/index.html) or [default](fold.html#it.czerwinski.kotlin.util.Option$fold(kotlin.Function0((it.czerwinski.kotlin.util.Option.fold.R)), kotlin.Function1((it.czerwinski.kotlin.util.Option.T, it.czerwinski.kotlin.util.Option.fold.R)))/default) if this is [None](../-none/index.html).

