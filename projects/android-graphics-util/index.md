---
title: Android Graphics Utilities
layout: toc-page
abstract: Extensions for Android graphics
keywords: oss,software,programming,android,graphics,kotlin
project: android-graphics-util
---

{% include breadcrumbs-project.html %}

[![Build Status](https://travis-ci.org/sczerwinski/android-graphics-util.svg?branch=develop)](https://travis-ci.org/sczerwinski/android-graphics-util)
[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android/graphics-util.svg)](https://repo1.maven.org/maven2/it/czerwinski/android/graphics-util/)
[![Sonatype Snapshot](https://img.shields.io/nexus/s/https/oss.sonatype.org/it.czerwinski.android/graphics-util.svg)](https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/graphics-util/)
[![Source](https://img.shields.io/badge/source-GitHub-blue.svg)](https://github.com/sczerwinski/android-graphics-util)
[![API Documentation](https://img.shields.io/badge/api-docs-blue.svg)](./docs)
![License](https://img.shields.io/github/license/sczerwinski/android-graphics-util.svg)

## Project Setup

To use Android Graphics Utilities in the project, add the following dependency
to your Gradle script:
```groovy
implementation "it.czerwinski.android:graphics-util:$graphicsUtilVersion"
```

## Library Features

### Constants

The library defines several useful constants:
* `PI` – `Float` value closest to _&pi;_ (the Ludolphian number)
* `DOUBLE_PI` – `Float` value closest to 2*&pi;*
* `RIGHT_ANGLE` – `Float` value of the right angle measured in degrees (90)
* `STRAIGHT_ANGLE` – `Float` value of the straight angle measured in degrees (180)
* `FULL_ANGLE` – `Float` value of the full angle measured in degrees (360)

### Extensions for angles

There are several extension functions for `Float`, useful when working with angles.

#### Conversion between radians and degrees

To convert radians to degrees, use `Float.radToDeg()`, e.g.:
```kotlin
val degrees = PI.radToDeg() // 180.0f
```

To convert degrees to radians, use `Float.degToRad()`, e.g.:
```kotlin
val radians = STRAIGHT_ANGLE.degToRad() // PI / 2
```

#### Conversion between angle in degrees and arc length

To calculate the angle enclosing the arc with the specified length and radius,
use `arcLengthToAngle()`, e.g.:
```kotlin
val angle = DOUBLE_PI.arcLengthToAngle(radius = 2f) // 180.0f
```

To calculate the length of an arc enclosed by the specified angle and having specified radius,
use `angleToArcLength()`, e.g.:
```kotlin
val angle = 90.angleToArcLength(radius = 4f) // 2 * PI
```

### Extensions for colours

#### Mixing colours

To mix two colours in a specified proportion, use `mixColors()`, e.g.:
```kotlin
val orange = mixColors(Color.RED, Color.YELLOW, ratio = 0.5f)
```

#### HSV colour model

There are a few functions simplifying conversion between colour `Int` and HSV colour model:
```kotlin
val color = hsvColor(hue = 30f, saturation = 0.9f, value = 0.8f)
val hue = color.colorHue()
val saturation = color.colorSaturation()
val value = color.colorValue()
```

Note that `colorHue()`, `colorSaturation()` and `colorValue()` are not optimized for accessing
more than one of the HSV colour model channels.

### Extensions for rectangles

#### Setting `Rect`

An instance of `Rect` can be set with the values closest to a defined `RectF`, e.g.:
```kotlin
val rectF: RectF
val rect: Rect

rect.set(rectF)
```

It is also possible to set values in an instance of `Rect` to enclose
a circle or an oval, e.g.:
```kotlin
rect.setCircle(cx = 10, cx = 20, radius = 1) // Rect(left = 9, top = 19, right = 11, bottom = 21)
rect.setOval(cx = 10, cx = 20, rx = 3, ry = 2) // Rect(left = 7, top = 18, right = 13, bottom = 22)
```

#### Setting `RectF`

Extensions facilitating definition of a rectangle enclosing a circle or an oval
are also provided for `RectF`, e.g.:
```kotlin
rectF.setCircle(cx = 1f, cx = 2f, radius = 0.5f) // RectF(left = 0.5f, top = 1.5f, right = 1.5f, bottom = 2.5f)
rectF.setOval(cx = 1f, cx = 2f, rx = 1.5f, ry = 1f) // RectF(left = -0.5f, top = 1f, right = 2.5f, bottom = 3f)
```

### Extensions for paths

#### Defining a new path

To easily replace an existing `Path` with a new contour,
use `Path.set()` extension, e.g.:
```kotlin
path.set(close = true) {
    moveTo(1f, 1f)
    lineTo(2f, 1f)
    lineTo(2f, 2f)
    lineTo(1f, 2f)
}
```

#### Advanced paths

`AdvancedPath` provides several additional methods to Android `Path`s.

An additional version of `arcTo` allows to add arc contours in a more intuitive way, e.g.:
```kotlin
path.arcTo(
    cx = 1f,
    cy = 2f,
    radius = 0.5f,
    startAngle = 10f,
    sweepAngle = 20f,
    forceMoveTo = true
)
```

`AdvancedPath` also contains methods for defining circular sectors and annulus (ring) sectors, e.g.:
```kotlin
path.addCircleSector(
    cx = 1f,
    cy = 2f,
    radius = 10f,
    startAngle = 90f,
    sweepAngle = 90f,
    inset = 0.1f
)

path.addRingSector(
    cx = 1f,
    cy = 2f,
    radius = 10f,
    startAngle = 90f,
    sweepAngle = 90f,
    thickness = 2.5f,
    inset = 0.1f
)
```

### Extensions for canvas

#### Transformations

Android KTX defines [a few extensions](https://android.github.io/android-ktx/core-ktx/androidx.graphics/android.graphics.-canvas/index.html)
for affine transformations. For example, it is possible to perform
part of the drawing with translation:
```kotlin
canvas.withTranslation(x = 10f, y = 20f) {
    drawText(…)
}
```

Android Graphics Utilities define an additional extension for translation with radial coordinates:
```kotlin
canvas.withRadialTranslation(
    distance = 10f,
    angle = 30f
) {
    drawText(…)
}
```
