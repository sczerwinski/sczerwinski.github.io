---
disqusid: reversing-array-in-java
title: Reversing Array In Java
mobileTitle: Reversing Array In Java
layout: post
abstract: Insight into actual behaviour of some standard Java utility methods
keywords: java,array,reverse,order,risk
tags: java
---

// This post was first published in Polish, on my old blog. It has been reviewed, edited and translated to English.

## The Backstory

For the task at hand, I needed to create an array being an exact copy of the original array, but in reverse order.
It is as easy as pie, but first, I wanted to check if there is any dedicated utility method in standard Java libraries,
e.g. in `java.util.Arrays`.

After a quick search, I came across [this solution](http://answers.yahoo.com/question/index?qid=20070904201231AAIwpJv):

```java
public class ArrayHandle {
    public static Object[] reverse(Object[] arr) {
        List<Object> list = Arrays.asList(arr);
        Collections.reverse(list);
        return list.toArray();
    }
}
```

“Of course! It’s implemented for collections.”

Just in case, I decided to test this algorithm:

```java
@Test
public void testReverse() {
    Object[] objects = new Object[] {
            1, 2, 3, 4, 5, 6, 7, 8, 9, 10
    };

    Object[] reversed = ArrayHandle.reverse(objects);

    assertEquals(10, reversed[0]);
}
```

“Yes! It works!”

## It Gets Interesting…

Now, I just needed to make sure, the original array hasn’t been altered:

```java
@Test
public void testReverseNoSideEffects() {
    Object[] objects = new Object[] {
            1, 2, 3, 4, 5, 6, 7, 8, 9, 10
    };

    Object[] reversed = ArrayHandle.reverse(objects);

    assertEquals(1, objects[0]);
}
```

I ran the tests and… I saw this:

```
java.lang.AssertionError: 
Expected :1
Actual   :10
```

“But why? What happened?”

## Analysis

Let’s see how `reverse()` method works…

* First, an implementation of `java.util.List` is created, containing all elements of the original array.
Notice that the list returned by `Arrays.asList()` is _a fixed-size list backed by the specified array_,
as described in [Java SE Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html#asList(T...)).
In other words, it **does not copy the elements** of the original array.
* `Collections.reverse()` method does not create any new list, but it reverses the existing list instead.
So, actually, it **reverses the backing array**.
* Finally, `List.toArray()` **creates a new array**, which is then returned by `reverse()` method.
But it doesn’t matter. Harm has already been done.

In conclusion, `reverse()` method not only returns an array in reverse order,
but it also reverses the order of the elements in the original array.

And I have a problem with that.

When I see a function returning a result, I assume that the argument will not be altered.

## Improved Solution (1)

I decided to improve the algorithm, by creating a copy of the original array before changing the order of its elements:

```java
public static <T> T[] reverse(T[] arr) {
    T[] reversed = arr.clone();
    List<T> list = Arrays.asList(reversed);
    Collections.reverse(list);
    return reversed;
}
```

I argue that the new method is in many ways better:
* It preserves the order of the elements in the original array.
* It avoids creating two identical arrays.
* It is generic.

## Improved Solution (2)

Obviously, _in situ_ operation is still valid. But in this case, `reverse()` method should not return any value:

```java
public static <T> void reverse(T[] arr) {
    List<T> list = Arrays.asList(arr);
    Collections.reverse(list);
}
```

## Bibliography

* [_How do you reverse the order of an array in java?_, Yahoo! Answers](https://answers.yahoo.com/question/index?qid=20070904201231AAIwpJv)
* [_java.util.Arrays_, Java SE 7 Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html#asList(T...))
* [_java.util.Collections_, Java SE 7 Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/Collections.html#reverse(java.util.List))
* [_java.util.List_, Java SE 7 Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/List.html#toArray())
