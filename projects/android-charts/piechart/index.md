---
title: 'Android Charts: Pie Charts'
layout: toc-page
abstract: Android pie charts
keywords: oss,software,programming,android,charts,pie,donut,graphs,kotlin
---

{% include breadcrumbs-subproject.html project="android-charts" %}

[![Sonatype Snapshot](https://img.shields.io/nexus/s/https/oss.sonatype.org/it.czerwinski.android/charts-piechart.svg)](https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/charts-piechart/)
[![Source](https://img.shields.io/badge/source-GitHub-blue.svg)](https://github.com/sczerwinski/android-charts)
![License](https://img.shields.io/github/license/sczerwinski/android-charts.svg)

{% include warn.html
content="Library under development. Backward compatibility not guaranteed before version 1.0." %}

## Dependencies

To use pie charts in an Android project, include the following dependencies:

```groovy
dependencies {

    // Pie Charts dependency:
    implementation "it.czerwinski.android:charts-piechart:$android_charts_version"

    // Material Design styles for Pie Charts: 
    implementation "it.czerwinski.android:charts-piechart-material:$android_charts_version"
}
```

## Layout

To add a pie chart to a layout, use a `PieChart` view:

```xml
<it.czerwinski.android.charts.piechart.PieChart
    android:id="@+id/pieChart"
    android:layout_width="match_parent"
    android:layout_height="match_parent" />
```

Never use `wrap_content` to determine the size of a `PieChart`. This value will set the size to `0dp`.
Instead, you may use `layout_constraintHeight_percent` attribute of a `ConstraintLayout`.

## Data Set Adapters

### Provided Adapters

```kotlin
val adapter = FloatListPieChartAdapter(requireContext())
pieChart.adapter = adapter

adapter.data = listOf(0.1f, 0.2f, 0.3f)
```

### Custom Adapters

```kotlin
class CustomPieChartAdapter : PieChart.DataSetAdapter() {

    private val values = listOf(0.1f, 0.2f, 0.3f)
    private val labels = listOf("A", "B", "C")

    override val size: Int get() = values.size
    override val sum: Float get() = values.sum()
    override fun get(index: Int): Float = values[index]
    override fun getLabel(index: Int): String = labels[index]
}
```

## UI Styles

### Simple Pie Chart

```xml
<style name="AppTheme">
    <item name="pieChartStyle">@style/AndroidCharts.PieChart.Simple.LightTheme</item>
</style>
```

```xml
<it.czerwinski.android.charts.piechart.PieChart
    android:id="@+id/pieChart"
    android:gravity="center"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    style="@style/AndroidCharts.PieChart.Simple.LightTheme" />
```

### Donut Chart

```xml
<style name="AppTheme">
    <item name="pieChartStyle">@style/AndroidCharts.PieChart.Donut.LightTheme</item>
</style>
```

```xml
<it.czerwinski.android.charts.piechart.PieChart
    android:id="@+id/pieChart"
    android:gravity="center"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    style="@style/AndroidCharts.PieChart.Donut.LightTheme" />
```

### Custom UI
