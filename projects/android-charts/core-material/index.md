---
title: 'Android Charts: Material Design Styles For Core'
layout: toc-page
abstract: Material Design styles for Android charts core
keywords: oss,software,programming,android,charts,graphs,kotlin,material
---

{% include breadcrumbs-subproject.html project="android-charts" %}

[![Maven Central](https://img.shields.io/maven-central/v/it.czerwinski.android/charts-core-material.svg)](https://repo1.maven.org/maven2/it/czerwinski/android/charts-core-material/)
[![Sonatype Snapshot](https://img.shields.io/nexus/s/https/oss.sonatype.org/it.czerwinski.android/charts-core-material.svg)](https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/charts-core-material/)
[![Source](https://img.shields.io/badge/source-GitHub-blue.svg)](https://github.com/sczerwinski/android-charts)
![License](https://img.shields.io/github/license/sczerwinski/android-charts.svg)

{% include warn.html
content="Library under development. Backward compatibility not guaranteed before version 1.0." %}

## Dependencies

To use charts core library with Material Design styles in an Android project, include the following dependency:

```groovy
dependencies {
    implementation "it.czerwinski.android:charts-core-material:$android_charts_version"
}
```

See also [core library documentation](../core).

## Styles

All styles should work equally fine with both light and dark themes. Colors are determined based on theme attributes:
`colorOnSurface`, `colorOnPrimarySurface`.

### Label Outside Chart Area (Text On Surface)

Style: `AndroidCharts.Material.TextAppearance.Label.Outside`

Base: `TextAppearance.MaterialComponents.Caption` (Sans-Serif, 12sp)

| Attribute            | Value                  |
| -------------------- | ---------------------- |
| `android:textColor`  | `?attr/colorOnSurface` |

### Label Inside Chart Area (Text On Primary Surface)

Style: `AndroidCharts.Material.TextAppearance.Label.Inside`

Base: `TextAppearance.MaterialComponents.Caption` (Sans-Serif, 12sp)

| Attribute            | Value                               |
| -------------------- | ----------------------------------- |
| `android:textColor`  | `?attr/colorOnPrimarySurface`       |
| `android:fontFamily` | **Min SDK 16.** `sans-serif-medium` |
| `fontFamily`         | `sans-serif-medium`                 |
