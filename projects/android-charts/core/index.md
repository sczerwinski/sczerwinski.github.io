---
title: 'Android Charts: Core'
layout: toc-page
abstract: Android charts core
keywords: oss,software,programming,android,charts,graphs,kotlin
---

{% include breadcrumbs-subproject.html project="android-charts" %}

[![Sonatype Snapshot](https://img.shields.io/nexus/s/https/oss.sonatype.org/it.czerwinski.android/charts-core.svg)](https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/charts-core/)
[![Source](https://img.shields.io/badge/source-GitHub-blue.svg)](https://github.com/sczerwinski/android-charts)
![License](https://img.shields.io/github/license/sczerwinski/android-charts.svg)

{% include warn.html
content="Library under development. Backward compatibility not guaranteed before version 1.0." %}

## Dependencies

To use charts core library in an Android project, include the following dependencies:

```groovy
dependencies {

    // Charts core library dependency:
    implementation "it.czerwinski.android:charts-core:$android_charts_version"

    // Material Design styles for charts core library: 
    implementation "it.czerwinski.android:charts-core-material:$android_charts_version"
}
```

See also [Material Design styles for core library](../core-material).

## Styling

### Available Attributes

#### Text Paint

`TextPaing` has the following attributes:

| Attribute            | Description                                       |
| -------------------- | ------------------------------------------------- |
| `android:textSize`   | Text size                                         |
| `android:textColor`  | Text color                                        |
| `android:textStyle`  | Text style: `normal`, `bold`, `italic`            |
| `android:typeface`   | Typeface: `normal`, `sans`, `serif`, `monospace`  |
| `android:fontFamily` | **Min SDK 16.** Font family name or font resource |
| `fontFamily`         | Font family name or font resource                 |
| `textAllCaps`        | If `true`, text will be converted to all caps     |

### Provided Styles

See also [Material Design styles](../core-material).

#### Dark Text

Style: `AndroidCharts.TextAppearance.Dark`

| Attribute            | Value                               |
| -------------------- | ----------------------------------- |
| `android:textSize`   | `12sp`                              |
| `android:textColor`  | `#000000` (black)                   |
| `android:fontFamily` | **Min SDK 16.** `sans-serif-medium` |
| `fontFamily`         | `sans-serif-medium`                 |

#### Light Text

Style: `AndroidCharts.TextAppearance.Light`

| Attribute            | Value                               |
| -------------------- | ----------------------------------- |
| `android:textSize`   | `12sp`                              |
| `android:textColor`  | `#FFFFFF` (white)                   |
| `android:fontFamily` | **Min SDK 16.** `sans-serif-medium` |
| `fontFamily`         | `sans-serif-medium`                 |
