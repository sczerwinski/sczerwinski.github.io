---
title: unzip - Kotlin utilities
---

[Kotlin utilities](../index.html) / [it.czerwinski.kotlin.util](index.html) / [unzip](./unzip.html)

# unzip

`fun <A, B> `[`Option`](-option/index.html)`<`[`Pair`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)`<`[`A`](unzip.html#A)`, `[`B`](unzip.html#B)`>>.unzip(): `[`Pair`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-pair/index.html)`<`[`Option`](-option/index.html)`<`[`A`](unzip.html#A)`>, `[`Option`](-option/index.html)`<`[`B`](unzip.html#B)`>>`

Transforms an [Option](-option/index.html) of a `Pair` into a `Pair` of an [Option](-option/index.html) of the first value
and an [Option](-option/index.html) of the second value.

**Return**
A `Pair` of an [Option](-option/index.html) of the first value and an [Option](-option/index.html) of the second value.

`fun <A, B, C> `[`Option`](-option/index.html)`<`[`Triple`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)`<`[`A`](unzip.html#A)`, `[`B`](unzip.html#B)`, `[`C`](unzip.html#C)`>>.unzip(): `[`Triple`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-triple/index.html)`<`[`Option`](-option/index.html)`<`[`A`](unzip.html#A)`>, `[`Option`](-option/index.html)`<`[`B`](unzip.html#B)`>, `[`Option`](-option/index.html)`<`[`C`](unzip.html#C)`>>`

Transforms an [Option](-option/index.html) of a `Triple` into a `Triple` of an [Option](-option/index.html) of the first value,
an [Option](-option/index.html) of the second value, and an [Option](-option/index.html) of the third value.

**Return**
A `Triple` of an [Option](-option/index.html) of the first value, an [Option](-option/index.html) of the second value,
and an [Option](-option/index.html) of the third value.

