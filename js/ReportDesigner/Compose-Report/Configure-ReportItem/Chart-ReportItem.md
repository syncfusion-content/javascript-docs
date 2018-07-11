---
layout: post
title: Visualize Data using chart report item with Syncfusion Web Report Designer
description: How to visualize data using chart report item with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Chart Report Item

Chart data region is used when the data needs to be presented in a visual format in the report. To present the data, choose the appropriate chart type; it will determine how well the data can be interpreted while visualizing it in chart form.

## Chart types

Web Designer supports the following chart types:

1. **Column charts** - A column chart displays a series as a set of vertical bars that are grouped by category.

   * **Stacked column** - A column chart where multiple series are stacked vertically.
   * **Percent stacked** - A column chart where multiple series are stacked vertically to fit 100% of the chart area. 

2. **Bar charts** - A bar chart displays series as sets of horizontal bars.

    * **Stacked bar** - A bar chart where multiple series are stacked vertically. 
    * **Percent stacked** - A bar chart where multiple series are stacked vertically to fit 100% of the chart area.

3. **Area charts** - An area chart displays a series as a set of points connected by a line, with all the area filled in below the line.

   * **Stacked area** -  An area chart where multiple series are stacked vertically.
   * **Smooth area** -  An area chart where the data points are connected by a smooth line instead of a regular line.
   * **Percent stacked area** - An area chart where multiple series are stacked vertically to fit the entire chart area.

4. **Line charts** -  A line chart displays a series as a set of points connected by a single line. Line charts are used to represent large amounts of data that occur over a continuous period of time.

   * **Smooth line** -  A line chart that uses a curved line instead of a regular line.
      * Smooth line with markers  
   * **Stepped line** -  A line chart that uses a curved line instead of a regular line.
   * Line with markers 

5. **Scatter charts** - A scatter chart displays a series as a set of points. Values are represented by the position of points on the chart.

   * **Bubble** - Bubble charts display the difference between two values of a data point based on the size of the bubble.

6. **Polar charts** - A polar chart displays a series as a set of points that are grouped by category on a 360-degree circle.

7. **Shape charts**
   * **Funnel** - A funnel chart displays values as progressively in decreasing proportions.
   * **Pyramid** - A pyramid chart displays proportional data so that the chart looks like a pyramid.
   * **Pie chart** - A pie chart displays data as a proportion of the whole. Pie charts are most commonly used to make comparisons between groups.

      * **Exploded pie** - A pie chart where all of the slices are moved away from the center of the pie.

   * **Doughnut** - A pie chart with an open space in the center and it displays data as a proportion of the whole.

# To add and configure a chart

* Create a report and define a dataset. For more information refer [Create Dataset](/js/ReportDesigner/create-Data/Create-New-Data).

  > Note: **AdventureWorks** database is used for demonstration.

* To add a **Chart** data region to the report, drag and drop the chart type of your choice from the item panel. The wizard offers column, line, pie, bar and area charts.

    ![](chart-images/itempanel.png)

    > Note: Here **Column** chart is used to demonstrate. 

    ![](chart-images/Column-Chart.png)

## Designing a chart

After adding a chart data region to the design surface, click the properties icon in the configuration panel to display the chart properties panel.

 ![](chart-images/Properties-Icon.png)

In the chart `Properties` pane, the visual effects of the charts can be designed using the **Properties** tab.

 ![](chart-images/Properties-Tab.png)

In the `Properties` pane, we have an icon in the right corner of each property which has expression or advanced options. We need to click the icon to load below context menu options:

  * **Expression**: To add expression for the property using various options in expression dialog.
  * **Advanced**: To load advanced options with sub level properties related to main property. 

> Note: The above context menu options will vary based on properties. If there is no sub level properties available for respective main property, then `Advanced` option will not be visible. Similarly, if there is no expression support for that property, then `Expression` option will not be visible.

 ![](chart-images/Expression.png)

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

You can see the list of properties available for the chart report item with default value.

### Properties

#### Basic settings

**Name**

 Title for the column chart report item can be set using this property.

 ![](chart-images/Basic-Properties.png)

The below properties in basic setting will be visible in the properties window, after assigning the data to the chart.

 * **Show legend**
   Legends are symbols and text used to provide additional information about the chart. This allows you to enable/disable the visibility of chart legend. By default, the chart legend visibility will be enabled.

     ![](chart-images/Legend.png)

 * **Show data label**
   This allows you to enable/disable the visibility of data labels for chart.

     ![](chart-images/Data-Label.png)

   Using the above properties in the above image, you can design the data label for better presentation of data.

     ![](chart-images/Data-Label-Chart.png)

 * **Enable smart label**
   Smart labels manage overlapping of labels even when a large number of labels are placed in close vicinity. This allows you to enable/disable smart label option for chart. 

     ![](chart-images/SmartLabel.png)

   Using the advanced option, set the label style and smart label position.

   * **Label style**
     Choose the label style based on the type of chart that are used to present the data.

      ![](chart-images/SmartLabel-Style.png)

   * **Value**
     Choose the position of data label to be displayed in the chart columns.

      ![](chart-images/Smart-Label-Value.png)

      **Inside**: 

        ![](chart-images/Inside-SmartLabel.png)

      **Outside**:

        ![](chart-images/Outside-SmartLabel.png)

  Enable/disable smart label by enabling/disabling the `Show Smart Label` check box.

**Appearance**

In the appearance category, set the border style, border width, border color, and background color of the chart to enhance the chart effects.

![](chart-images/Chart-Appearance.png)

The border style, border width, border color for top, left, bottom, and right side can be set using the advanced option in the appearance category.

![](chart-images/Appearance-Properties.png)

**Chart area**

In the chart area category, set the border style, border width, border color, and background color of the chart area.

Hide the border styles of chart area by clearing the **Show border** check box.

**Title**

The chart title can be customized by editing the **Title Text** property of the chart.

To enable the chart title, check the **Show Chart Title** checkbox.

![](chart-images/Title-Properties.png)

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

The chart title can be positioned, using **Title Position** in the below positions.

* Center
* Right
* Left

**Axis properties**

#### Types of axes

The chart has two primary axes: the `value` axis and the `category` axis.

**Enable axis**: To enable the axis title, check the **Enable Axis** checkbox.

**Axis title**: Set the title related to the data.

**Line style** : This allows to set the line style, width, and color of the axis line.

**Label overflow mode**: The label overflow mode can be set as `Trim` or `Hide` to adjust the data label in the axis.

**Label text**: To add effects to the label text, use below properties:

  * **Label rotation** - This allows to define the rotation angle for the value labels to display.
  * **Label font**
     * Font color
     * Font size

**Tick** - To set the style, width, color, and length of the axis tick, and to set the visibility of the major and minor tick marks.

![](chart-images/Axis-Properties.png)

**Grid line** - The `Grid line` properties can be set to category and value axis.
 
* To show the grid line for category axis, enable the **Category Axis** checkbox.

* To show the grid line for value axis, enable the **Value Axis** checkbox.

    Open the `Advanced` option to set the grid line style and color.

  ![](chart-images/Grid-Properties.png)

  ![](chart-images/Grid-Line.png)


**Page break** - Add a page break to control the amount of information on each page.

 Under page break options, select one of the following options:

   * Start 
   * End 
   * Start and End
   * Between

To remove the page break select **None**.

**Position and size** - The position and size of the chart can be changed using position and size property.

![](chart-images/Position-Size.png)

**Visibility** - Select an option to indicate how the report item is initially displayed in the report.

* Enable  the checkbox to show the report item.
* Disable the checkbox to hide the report item.
* Show or hide based on an expression.

Select this option to vary the initial visibility using an expression.

Type an expression that evaluates to a boolean value of true to hide the item or false to show the item.

Click on the icon in the right corner and select **Expression** to edit the expression.

![](chart-images/Visibility.png)


# Adding Data to the Chart

Create a report and define a dataset. 

Drag and drop the doughnut chart report item into the design area.

![](chart-images/Assign-Drag.png)

> Note: **Doughnut** chart is used for demonstration.

![](chart-images/Doughnut-Chart.png)

In the chart `Properties` pane, click the `Data`.

The data pane will be opened with available measures and dimensions in the connected data source.

![](chart-images/Assign-Data-Pane.png)

# Assign value(s)

Drag and drop the `Measure` into `Value`.

![](chart-images/Measures-Drag.png)

Now, the chart will be rendered like this.

![](chart-images/first-View-Measures.png)

You can change the aggregate type of the value by clicking the `Settings` icon.

![](chart-images/Settings-Icon.png)

Select the required aggregate type from the list.

![](chart-images/Aggregation-Type.png)

You can set `Expression` by clicking the `Settings` icon.

![](chart-images/Expression.png)

You can add more number of values by drag and drop the `Measures` into `Value` field. 

![](chart-images/Measures-Drag2.png)

You can also add `Dimensions` and `Columns` to `Value(s)`.

**Assigning column** 

You can add the `Dimension` to `Column` field by drag and drop.

![](chart-images/Dimension-Drag1.png)

You can add `Measures` to `Column(s)` field.

**Filters**: You can limit the data to be displayed by choosing the filters option.

![](chart-images/Filters-Column.png)

To filter data refer [Filters](/js/ReportDesigner/Compose-Report/Filter-Data).

**Sorting**: You can control the order in which the data appears in a data region by representing sort expressions.

![](chart-images/Sort-Menu.png)

To sort data refer [Sorting](/js/ReportDesigner/Compose-Report/Sort-Data).

**Assigning row(s)**

You can add a dimension level or hierarchy to `Row` section for series rendering of the chart.

![](chart-images/Assign-Row-Drag.png)

The chart will be rendered in series as shown in the image below.
 
![](chart-images/Row-Chart.png)

You have settings options similar to column(s).

![](chart-images/Row-Filter-Menu.png)

You can add more number of values by drag and drop the `Dimension` into `Row` field.

Now, the chart **Preview** will look like below.

![](chart-images/Preview-Chart.png)
