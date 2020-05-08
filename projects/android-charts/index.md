---
title: Android Charts
layout: toc-page
abstract: Android charts
keywords: oss,software,programming,android,charts,graphs,kotlin
---

[![Build Status](https://travis-ci.org/sczerwinski/android-charts.svg?branch=develop)](https://travis-ci.org/sczerwinski/android-charts)

{% include warn.html
content="Library under development. Backward compatibility not guaranteed before version 1.0." %}

## Roadmap

| Version | Features      |
| ------- | ------------- |
| 0.1     | Pie charts    |
| 0.2     | Series charts |
| 0.3     | XY charts     |
| 0.4     | Radar charts  |
| 1.0     | Stabilization |

---

[![Sonatype Snapshot](https://img.shields.io/nexus/s/https/oss.sonatype.org/it.czerwinski.android/charts-core.svg)](https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/charts-core/)

## Core

```groovy
dependencies {
    implementation "it.czerwinski.android:charts-core:$android_charts_version"
}
```

---

[![Sonatype Snapshot](https://img.shields.io/nexus/s/https/oss.sonatype.org/it.czerwinski.android/charts-piechart.svg)](https://oss.sonatype.org/content/repositories/snapshots/it/czerwinski/android/charts-piechart/)

## Pie Charts

{% include warn.html content="Under development" %}

```groovy
dependencies {
    implementation "it.czerwinski.android:charts-piechart:$android_charts_version"
}
```

### Layout

```xml
<it.czerwinski.android.charts.piechart.PieChart
    android:id="@+id/pieChart"
    android:gravity="center"
    android:layout_width="match_parent"
    android:layout_height="match_parent" />
```

### Data Set Adapters

#### Provided Adapters

```kotlin
val adapter = FloatListPieChartAdapter(requireContext())
pieChart.adapter = adapter

adapter.data = listOf(0.1f, 0.2f, 0.3f)
```

#### Custom Adapters

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

### UI Styles

#### Simple Pie Chart

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

#### Donut Chart

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

#### Custom UI

---

## Series Charts

{% include warn.html content="Planned" %}

### Point Chart

### Line Chart

### Area Chart

### Bar Chart

### Floating Bar Chart

### Gantt Chart

### Candlestick Chart

---

## XY Charts

{% include warn.html content="Planned" %}

### Point Chart

### Line Chart

### Bubble Chart

### Measurement Chart

---

## Radar Charts

{% include warn.html content="Planned" %}

### Line Chart

### Area Chart

### Bar Chart

---

## Sunburst Charts

{% include warn.html content="Planned" %}

---

## Venn Diagrams

{% include warn.html content="Planned" %}
