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

See also [Material Design styles for pie charts](../piechart-material).

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

## Styling

### Available Attributes

#### Pie Chart

`PieChart` view has the following attributes:

| Attribute                             | Description                                                      |
| ------------------------------------- | ---------------------------------------------------------------- |
| `android:padding`                     | View padding                                                     |
| `android:gravity`                     | Gravity of the pie chart inside the view                         |
| `pieChart_rotationAngle`              | Rotation angle of the pie chart (start angle of the first slice) |
| `pieChart_dataSetInterpolator`        | Interpolator for data set changes animation                      |
| `pieChart_dataSetAnimationDuration`   | Duration of data set changes animation (in milliseconds)         |
| `pieChart_selectionInterpolator`      | Interpolator for slice selection animation                       |
| `pieChart_selectionAnimationDuration` | Duration of slice selection animation (in milliseconds)          |
| `pieChart_ui`                         | Name of a class implementing `PieChart.UI`                       |
| `pieChart_uiAppearance`               | Style for the `PieChart.UI`                                      |
| `pieChart_labelsPaddingHorizontal`    | Additional horizontal padding for labels                         |
| `pieChart_labelsPaddingVertical`      | Additional vertical padding for labels                           |
| `pieChart_labelsPaddingFromText`      | Text to be measured to determine as padding for labels           |
| `pieChart_labelsUI`                   | Name of a class implementing `PieChart.LabelsUI`                 |
| `pieChart_labelsAppearance`           | Style for the `PieChart.LabelsUI`                                |

#### Simple Pie Chart UI

Set `pieChart_ui` to `it.czerwinski.android.charts.piechart.SimplePieChartUI`.

`SimplePieChartUI` has the following attributes:

| Attribute                             | Description                                                             |
| ------------------------------------- | ----------------------------------------------------------------------- |
| `simplePieChartUI_colors`             | A single color or an array of colors for pie chart slices               |
| `simplePieChartUI_shadowColor`        | Pie chart slice shadow color                                            |
| `simplePieChartUI_sliceSpacing`       | Pie chart slice spacing                                                 |
| `simplePieChartUI_selectionColors`    | A single color or an array of colors for pie chart slices when selected |
| `simplePieChartUI_selectionShift`     | Outwards shift distance of a selected slice                             |
| `simplePieChartUI_selectionElevation` | Elevation of a selected slice                                           |

#### Donut Pie Chart UI

Set `pieChart_ui` to `it.czerwinski.android.charts.piechart.DonutPieChartUI`.

`DonutPieChartUI` has the following attributes:

| Attribute                            | Description                                                               |
| ------------------------------------ | ------------------------------------------------------------------------- |
| `donutPieChartUI_colors`             | A single color or an array of colors for donut chart slices               |
| `donutPieChartUI_shadowColor`        | Donut chart slice shadow color                                            |
| `donutPieChartUI_donutWidth`         | Donut width                                                               |
| `donutPieChartUI_donutSpacing`       | Pie chart slice spacing                                                   |
| `donutPieChartUI_selectionColors`    | A single color or an array of colors for donut chart slices when selected |
| `donutPieChartUI_selectionWidth`     | Width of a selected donut slice                                           |
| `donutPieChartUI_selectionShift`     | Outwards shift distance of a selected slice                               |
| `donutPieChartUI_selectionElevation` | Elevation of a selected slice                                             |

#### Simple Pie Chart Labels UI

Set `pieChart_` to `it.czerwinski.android.charts.piechart.SimplePieChartLabelsUI`.

`SimplePieChartLabelsUI` has the following attributes:

| Attribute                                | Description                                            |
| ---------------------------------------- | ------------------------------------------------------ |
| `simplePieChartLabelsUI_textAppearance`  | Text appearance as defined in [`charts-core`](../core) |
| `simplePieChartLabelsUI_labelPosition`   | Labels position, `inside` or `outside` the chart       |
| `simplePieChartLabelsUI_labelSpacing`    | Labels spacing from the edge of the pie chart          |
| `simplePieChartLabelsUI_labelMinPercent` | Minimum slice value in percent to display a label      |

### Provided Styles

See also [Material Design styles](../piechart-material).

#### Pie Chart – Light Theme

Style: `AndroidCharts.PieChart.Simple.LightTheme`

{% include image.html src="/assets/img/project/android-charts/piechart/piechart_simple_light.png" %}

#### Pie Chart – Dark Theme

Style: `AndroidCharts.PieChart.Simple.DarkTheme`

{% include image.html src="/assets/img/project/android-charts/piechart/piechart_simple_dark.png" %}

#### Donut Chart – Light Theme

Style: `AndroidCharts.PieChart.Donut.LightTheme`

{% include image.html src="/assets/img/project/android-charts/piechart/piechart_donut_light.png" %}

#### Donut Chart – Dark Theme

Style: `AndroidCharts.PieChart.Donut.DarkTheme`

{% include image.html src="/assets/img/project/android-charts/piechart/piechart_donut_dark.png" %}

### Custom UI

To define a custom style for `PieChart`, you can create your own implementation
of `PieChart.UI` and/or `PieChart.LabelsUI`.

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
