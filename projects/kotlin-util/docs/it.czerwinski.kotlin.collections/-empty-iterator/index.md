---
title: EmptyIterator - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.collections](../index.html) / [EmptyIterator](./index.html)

# EmptyIterator

`object EmptyIterator : `[`Iterator`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)`<`[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html)`>`

Iterator producing no values.

### Functions

| [hasNext](has-next.html) | `fun hasNext(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [next](next.html) | `fun next(): `[`Nothing`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-nothing/index.html) |

### Extension Functions

| [asOption](../../it.czerwinski.kotlin.util/as-option.html) | `fun <T> `[`T`](../../it.czerwinski.kotlin.util/as-option.html#T)`?.asOption(): `[`Option`](../../it.czerwinski.kotlin.util/-option/index.html)`<`[`T`](../../it.czerwinski.kotlin.util/as-option.html#T)`>`<br>Returns [Some](../../it.czerwinski.kotlin.util/-some/index.html) if this is not `null` or [None](../../it.czerwinski.kotlin.util/-none/index.html) if this is `null`. |

