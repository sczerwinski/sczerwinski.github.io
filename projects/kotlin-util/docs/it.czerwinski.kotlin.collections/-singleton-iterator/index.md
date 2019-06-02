---
title: SingletonIterator - Kotlin utilities
---

[Kotlin utilities](../../index.html) / [it.czerwinski.kotlin.collections](../index.html) / [SingletonIterator](./index.html)

# SingletonIterator

`class SingletonIterator<T> : `[`Iterator`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-iterator/index.html)`<`[`T`](index.html#T)`>`

Iterator producing a single [element](#).

### Parameters

`element` - The element to be produced by the iterator.

`T` - Type of the [element](#).

### Constructors

| [&lt;init&gt;](-init-.html) | `SingletonIterator(element: `[`T`](index.html#T)`)`<br>Iterator producing a single [element](#). |

### Functions

| [hasNext](has-next.html) | `fun hasNext(): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [next](next.html) | `fun next(): `[`T`](index.html#T) |

### Extension Functions

| [asOption](../../it.czerwinski.kotlin.util/as-option.html) | `fun <T> `[`T`](../../it.czerwinski.kotlin.util/as-option.html#T)`?.asOption(): `[`Option`](../../it.czerwinski.kotlin.util/-option/index.html)`<`[`T`](../../it.czerwinski.kotlin.util/as-option.html#T)`>`<br>Returns [Some](../../it.czerwinski.kotlin.util/-some/index.html) if this is not `null` or [None](../../it.czerwinski.kotlin.util/-none/index.html) if this is `null`. |

