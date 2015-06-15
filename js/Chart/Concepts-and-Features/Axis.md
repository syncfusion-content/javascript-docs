---
layout: post
title: Axis
description: axis
platform: js
control: Chart
documentation: ug
---

# Axis

**Charts** typically have two axes that are used to measure and categorize data: a vertical (y) axis, and a horizontal (x) axis. To make a Chart easier to understand, you can add axis titles, tick marks, and labels. You can also change the alignment of axis title and format the labels that are displayed on axes. By default horizontal (x) axis and vertical (y) axis gets added to the Chart with axis labels, gridlines, and tick lines. You can also customize these axis explicitly by adding axis title or removing gridlines, tick lines that are added to the axis by default.

Chart Axis supports the following types:

* Double

* DateTime

* Category

* Logarithmic

You can choose any of the Chart axis type using the” **valueType**” property in axis. Axis calculates the range and interval automatically based on the series data points.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
            primaryXAxis:
            {
                majorTickLines: { visible: false },
                title: { text: 'Country' }
            },

            primaryYAxis:
            {

                title: { text: 'Production' },
            },
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img1.png" Caption="Chart with Axis"%}

## Double 

By default the valueType of the axis is double and it represents the numerical data.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
            primaryXAxis:
            {
                title: { text: 'Year' },
                valueType: 'double'
            },
            series: [{
                points: [
                    { x: 200, y: 10 }, { x: 210, y: 13 },
                    { x: 220, y: 18 }, { x: 230, y: 13 },
                    { x: 240, y: 15 }, { x: 250, y: 13 },
                    { x: 260, y: 16 }, { x: 270, y: 10 },
                    { x: 280, y: 18 }
                ],
                name: 'product A'
            }
            ],
            // ...             
        });


{% endhighlight %}



With the default auto range calculation, the range padding properties allows you to customize the automatic range calculation.

### Range Padding

#### None

By default, the **rangePadding** for Numerical Axis is none.

The following screenshot displays a Chart’s x-axis with **rangePadding** set to **none**.

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img2.png" Caption="Chart with double axis"%}

#### Additional

If **rangePadding** for Numerical Axis is set to **additional**, the interval of the axis is added as padding.

The following screenshot illustrates a Chart’s x-axis with **rangePadding** set to **additional**.

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img3.png" Caption="Chart’s x-axis with RangePadding set to Additional"%}

#### Normal

Normal **rangePadding** for a Numerical Axis is used mostly for the y-axis to have padding based on the Range calculation.

The following screenshot illustrates a Chart’s y-axis with **rangePadding** set to **normal**.

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img4.png" Caption="Chart’s y-axis with RangePadding set to Normal"%}

#### Round

Round **rangePadding** for a Numerical Axis rounds the range of the Chart axis to the nearest possible value divisible by the interval.

The following screenshot illustrates a Chart’s x-axis with **rangePadding** set to **Round**.

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img5.png" Caption="Chart’s x-axis with RangePadding set to Round"%}

## DateTime Axis

The **DateTime** Axis has a property **IntervalType** that sets the **DateTime** interval to one of the following:

* Days

* Hours

* Milliseconds

* Minutes 

* Months

* Seconds

* Years

The **Interval** property of **DateTime** Axis can be any double value based on the **IntervalType**.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
            primaryXAxis:
            {

                title: { text: 'Year' },
                valueType: 'datetime',
                range: {
                    min: new Date(2000, 6, 1),
                    max: new Date(2010, 6, 1),
                    interval: 1
                },
                intervalType: 'Years'
            },
            series: [{
                points: [
                     { x: new Date(2000, 06, 11), y: 10 },
                     { x: new Date(2002, 03, 07), y: 30 },
                     { x: new Date(2004, 03, 06), y: 15 },
                     { x: new Date(2006, 03, 30), y: 65 },
                     { x: new Date(2008, 03, 08), y: 90 },
                     { x: new Date(2010, 03, 08), y: 85 }
                ],
                name: 'Sales', type: 'line'
            }
            ],
            // ...  
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img6.png" Caption="Chart with DateTime Axis"%}

With the default auto range calculation, the **rangePadding** properties for date-time axis allow you to customize the automatic range calculation.

### Range Padding

#### None

By default, the **rangePadding** for a **DateTime** Axis is none.

The following screenshot illustrates a Chart’s x-axis with **rangePadding** set to **none**. 

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img7.png" Caption="Chart’s x-axis with RangePadding set to None"%}

#### Additional

If **rangePadding** for **DateTime** Axis is set to **additional**, the **DateTime** interval of the axis is added as padding.

The following screenshot illustrates a Chart’s x-axis with **rangePadding** set to **Additional**.

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img8.png" Caption="Chart’s x-axis with RangePadding set to Additional"%}

#### Round

Round **rangePadding** for a **DateTime** Axis rounds the range of the Chart axis to the nearest possible Date Time value.

The following screenshot illustrates a Chart’s x-axis with **rangePadding** set to **Round**.

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img9.png" Caption="Chart’s x-axis with RangePadding set to Round"%}

## Category Axis

Category (x) axis displays text labels instead of numerical intervals. By default, the interval is 1 for which all the labels are displayed. To display every nth label, you can set that in interval property. For example, to display every 2nd label, you can set interval as 2. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
            primaryYAxis:
            {
                range: { min: 0, max: 80, interval: 20 },
                title: { text: 'Medals' }
            },
            series: [{
                points: [{ x: "USA", y: 50 }, { x: "China", y: 40 },
                     { x: "Japan", y: 70 }, { x: "Australia", y: 60 },
                     { x: "France", y: 50 }, { x: "Germany", y: 40 },
                     { x: "Italy", y: 40 }, { x: "Sweden", y: 30 }
                ],

                name: 'Gold'
            }
            ],
            // ...  
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img10.png" Caption="Chart with Category Axis"%}

## Logarithmic Axis

An axis displaying a logarithmic scale is very useful when your data values span orders of magnitude. Log axis is enabled using **valueType** property.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
            primaryYAxis: {
                valueType: "logarithmic",
            },
            series: [{
                points: [
                     { x: 1990, y: 80 }, { x: 1991, y: 200 },
                     { x: 1992, y: 400 }, { x: 1993, y: 600 },
                     { x: 1994, y: 900 }, { x: 1995, y: 1400 },
                     { x: 1996, y: 2000 }, { x: 1997, y: 4000 },
                     { x: 1998, y: 6000 }, { x: 1999, y: 8000 },
                     { x: 2000, y: 9000 }],
                type: 'line'
            }],
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img11.png" Caption="Chart with Logarthimic Axis"%}

## Chart Axis Properties

_Chart Axis Properties Table_

<table>
<tr>
<td>
<b>Chart Axis Properties</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
desiredIntervals</td><td>
An integer property used to indicate the preferred total number of intervals to be displayed for auto range calculation.</td></tr>
<tr>
<td>
maximumLabels</td><td>
An Integer property used to indicate number of labels per 100 pixels. By default, 3 labels renders for 100 pixels of length.</td></tr>
</table>
## Multiple Axis

In cases of multiple series, a **Chart** can have multiple x and y axes to represent each series. The axes can be arranged in stacking or side-by-side mode. By default, the axes are arranged in side-by-side mode. In order to arrange the axis in a stacking mode, you can split the Chart into number of rows or columns using **rowDefinitions** and **columnDefinitions** and then you can place the required axis in the desired row and column. Heights of the vertical axes are customized using the **rowHeight** property in **rowDefinitions** and the widths of the horizontal axes are customized using **columnWidth** property in **columnDefinitions.**

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
            rowDefinitions:
            [{
                rowHeight: 50,
                unit: 'percentage'
            },
            {
                rowHeight: 50,
                unit: 'percentage'
            }],
            primaryXAxis:
            {
                title: { text: "Month" }
            },

            primaryYAxis:
            {
                title: { text: "Temperature(Fahrenheit)" },
                range: { min: 0, max: 60, interval: 10 },
            },
            axes: [{
                orientation: 'Vertical',
                rowIndex: "1",
                name: 'yAxis',
                title: { text: "Temperature(Celsius)" },
                plotOffset: 20
            }],

            series: [{
                points: [{ x: "Jan", y: 15 }, { x: "Feb", y: 20 },
                         { x: "Mar", y: 35 }, { x: "Apr", y: 40 },
                         { x: "May", y: 30 }, { x: "Jun", y: 40 },
                         { x: "Jul", y: 43 }, { x: "Aug", y: 35 },
                ],
                name: 'Germany',
            },

            {
                points: [{ x: "Jan", y: 33 }, { x: "Feb", y: 31 },
                         { x: "Mar", y: 30 }, { x: "Apr", y: 28 },
                         { x: "May", y: 29 }, { x: "Jun", y: 30 },
                         { x: "Jul", y: 33 }, { x: "Aug", y: 32 },
                ],
                name: 'India', yAxisName: 'yAxis',

            },
            ],
            // ...             

        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img12.png" Caption="Chart with Multiple Axis"%}

In the above code, you can remove the **rowDefinition** and **rowIndex** from axis to arrange the axes in the side-by- side mode.

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img13.png" Caption="Chart with Multiple Axis"%}

### Spanning Axis

**Charts** having multiple series have multiple x and y axis to represent each series. By default, the axes are arranged in the corresponding row/column position. **Spanning** feature allows you to span the axis across multiple panes/rows.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...  

            // split the chart area into 3 rows with different height       
            rowDefinitions: [{
                rowHeight: 25,
                unit: "percentage"
            },
            {
                rowHeight: 25,
                unit: "percentage"
            },
            {
                rowHeight: 50,
                unit: "percentage"
            }],
            primaryXAxis:
            {
                title: { text: "Date" },
            },
            primaryYAxis:
            {
                rowIndex: 0,   // renders in 1st row                
                range: { min: 0, max: 100, interval: 25 },
                font: { size: '14px' },
                title: { text: "Quater 1" }
            },
            axes: [{
                name: 'y1SecondQuater',
                rowIndex: 1,
                rowSpan: 2, // renders in 2nd row and spans to 2 rows
                range: { min: 0, max: 100, interval: 20 },
                plotOffset: 30,
                title: { text: "Quater 2" }
            },
            {
                name: 'y2SecondQuater',
                rowSpan: 3, // renders in 1st row and spans to 3 rows
                range: { min: 0, max: 100, interval: 10 },
                title: { text: "Quater 3" }
            }
            ],
            series: [{
                points: [{ x: "USA", y: 50 }, { x: "China", y: 40 },
                         { x: "Japan", y: 70 }, { x: "Australia", y: 60 },
                         { x: "France", y: 50 }, { x: "Germany", y: 40 },
                         { x: "Italy", y: 40 }, { x: "Sweden", y: 30 }
                ],

                name: 'Gold', type: 'column'
            },
            {
                points: [{ x: "USA", y: 70 }, { x: "China", y: 60 },
                        { x: "Japan", y: 40 }, { x: "Australia", y: 36 },
                        { x: "France", y: 25 }, { x: "Germany", y: 30 },
                        { x: "Italy", y: 35 }, { x: "Sweden", y: 25 }
                ],

                name: 'Silver', yAxisName: "y1SecondQuater",
            },
            {
                points: [{ x: "USA", y: 10 }, { x: "China", y: 19 },
                         { x: "Japan", y: 40 }, { x: "Australia", y: 70 },
                         { x: "France", y: 35 }, { x: "Germany", y: 82 },
                         { x: "Italy", y: 57 }, { x: "Sweden", y: 97 }
                ],
                name: 'Bronze', yAxisName: "y2SecondQuater", type: 'spline'
            }
            ],
            // ...             

        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img14.png" Caption="Chart with Spanning Axis"%}

## Axis Title

You can customize the ejChart Axis title text, font styles and color using “**title**” property of axis.

{% highlight js %}

        $("#chartcontainer").ejChart({
            primaryXAxis:
            {
                title: { text: "Expenditure", font: { color: '# AA3eeF', fontFamily: 'Segoe UI', fontStyle: 'Normal', size: '16px', opacity: 1, fontWeight: 'regular' } },
            },

            primaryYAxis:
            {
                title: { text: "Expense", font: { color: '# AA3eeF', fontFamily: 'Segoe UI', fontStyle: 'Normal', size: '16px', opacity: 1, fontWeight: 'regular' } },
            },
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img15.png" Caption="Chart with Axis Title"%}

### Trim Title

**EjChart** supports **Trimming****Axis****Titles** with the properties, **enableTrim** and **maximumTitleWidth**. These are useful for shortening the lengthy titles. On hovering with the mouse, you can see the full title in the tooltip.

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img16.png" Caption="X-Axis Title Trim         "%}

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img17.png" Caption="Y-Axis Title Trim"%}

{% highlight js %}

$("#container").ejChart({
            //......
            primaryXAxis:
            {
                title: {
                    text: 'List of countries which are using solar power in the year 2014',
                    enableTrim: true,
                    maximumTitleWidth: 60
                },
            },
            primaryYAxis:
            {
                title: {
                    text: 'Measurements of Solar power used in different countries in the year 2014( in GW)',
                    enableTrim: true,
                    maximumTitleWidth: 80
                },
                range: { min: 0, max: 40, interval: 5 },
                labelFormat: "{value}GW",
            },
            //......
        });        


{% endhighlight %}

## Labels

The axis labels are present along the axis **showing** the value of the data it corresponds to. You can further customize the **Chart** axis labels using “**font**” and “**labelFormat**” properties of the axis. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
            primaryXAxis:
            {
                title: { text: 'Countries' },
                font: { size: '11px', color: 'red' }

            },

            primaryYAxis:
            {
                labelFormat: "{value}%",
                font: { size: '11px', color: 'red' },
                title: { text: 'Efficiency' },
            },

            // ...             

        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img18.png" Caption="Figure 1: "%}

**LabelPlacement:**

The category axis includes the **labelPlacement** property that is used to set the labels of the axis between the tick lines or on the tick lines of the category axis. By default the **labelPlacement** value for the category axis is BetweenTicks.

There are two types of **LabelPlacement**:

* BetweenTicks

* OnTicks



{% highlight js %}

$("#chartcontainer").ejChart({
            // ...             
            primaryXAxis:
            {
                title: { text: 'Countries' },
                labelPlacement: 'onticks',
                font: { size: '11px', color: 'red' }

            },
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img19.png" Caption="Chart with LabelPlacement OnTicks"%}

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img20.png" Caption="Chart with LabelPlacement BetweenTicks"%}

**Label Position**

Axis labels can further be customized to render inside the chart area using the property **labelPosition**. By default, it is set as outside. This helps to display labels in a proper manner while multiple axes are used in the chart.

{% highlight js %}

        $("#Container").ejChart({
            primaryXAxis: {
                labelPosition: "inside",
                majorTickLines: { visible: false }
            },
            primaryYAxis: {
                labelPosition: "inside",
                majorTickLines: { visible: false }
            },
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img21.png" Caption="Label inside Chart"%}

**Axis label trimming** 

**Chart** provides support for trimming y axis labels and x axis labels by using the properties **enableTrim** and **maximumLabelWidth.** These are used to show the lengthy labels in a shorter form. On mouse hover, it shows the full label in the tooltip.

{% highlight js %}


        $("#chartcontainer").ejChart({
            primaryXAxis:
            {
                enableTrim: true,
                maximumLabelWidth: 34

            },
            primaryYAxis:
            {
                enableTrim: true,
                maximumLabelWidth: 34
            }
            // ...
        });


{% endhighlight %}



The following screenshot displays the **Chart Axis** with **trimming**.

{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img22.png" Caption="Axis Label Trimming"%}

## Tick Marks

Tick lines are displayed horizontally and vertically in Chart axis based on the orientation of the axis.

**Major Tick Lines**

It is rendered in Chart axis for each interval of axis range. By default, it is visible. You can collapse it by setting ‘**visible’** as **false**. You can customize the major tick lines width, opacity, and color.

**Minor Tick Lines**

It is rendered between the major tick lines of Chart axis. To display **minorTickLines** in Chart axis enable visible property of “**minorTickLines**” and set values to “**minorTicksPerInterval**” in the respective axis. By default, it is invisible. You can customize the minor tick lines width, and color.

{% highlight js %}

        $("#chartcontainer").ejChart({
            primaryXAxis:
            {
                majorTickLines:
                {
                    width: 1.5, size: 6, visible: true
                },
                minorTickLines: { width: 1, size: 4, visible: true },
                minorTicksPerInterval: 5,

            },
            primaryYAxis:
            {
                majorTickLines:
                {
                    width: 1.5, size: 6, visible: true
                },
                minorTickLines: { width: 1, size: 4, visible: true },
                minorTicksPerInterval: 5,

            },

            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img23.png" Caption="Chart with Tick lines"%}

**Tick lines placement**

You can customize tick lines and render them inside the chart area using the property **tickLinesPosition**. By default, it is set as outside. This property will be used when labels are inside.

{% highlight js %}

        $("#chartcontainer").ejChart({
            primaryXAxis: {
                tickLinesPosition: "inside",
            },
            primaryYAxis: {
                tickLinesPosition: "inside",
            },
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img24.png" Caption="Tick Lines inside chart"%}

## Grid Lines	

**Grid lines** are displayed in horizontal and vertical position in **Chart** area based on the intervals.

**Major Grid Lines**

It is rendered in Chart area for each interval of axis range. By default, it is visible. You can collapse it by setting **‘visible’** property to **false**. You can customize the **major gridlines** width, opacity, and dashArray of gridline.

**Minor Grid Lines**

It is rendered between the **major gridlines** of Chart area.To display **minor grid lines** in Chart area enable visible property of “**minorGridLines**” and set values to “**minorTicksPerInterval**” in the respective axis. By default, ‘**visibile’** property is set to “**false**”. You can customize the **minor grid lines** width, and dashArray of gridline.

{% highlight js %}

        $("#chartcontainer").ejChart({
            primaryXAxis:
            {
                majorGridLines:
                {
                    width: 2, dashArray: "", visible: true, opacity: 1
                },
                minorGridLines:
                {
                    width: 1, dashArray: "", visible: true
                },
                minorTicksPerInterval: 1,
            },
            primaryYAxis:
            {
                majorGridLines:
                {
                    width: 2, dashArray: "", visible: true, opacity: 1

                },
                minorGridLines:
                {
                    width: 1, dashArray: "", visible: true
                },
                minorTicksPerInterval: 1,
            },
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img25.png" Caption="Chart with Grid lines"%}

**Alternate Grid Band**

Grid Band is the distance between two adjacent major grid lines which are displayed in horizontal and vertical position.

**Even Grid Band**

Even Grid Band are counted from axes lines, i.e the band which is immediate adjacent for axes lines. By default, the even grid band color is transparent. You can highlight the even grid band by setting **fill** property of **even**. You can customize the **opacity** of the even grid band color.

**Odd Grid Band**

Immediate adjacent band of every even grid bands are Odd Grid Bands**.** You can discriminate the odd grid band from even by setting **fill** property of **odd**. You can customize the **opacity** of the odd grid band color.

{% highlight js %}

        $("#container").ejChart({
            primaryXAxis: {
                alternateGridBand: {
                    even: {
                        fill: "#E896E8",
                        opacity: 0.5
                    }
                }
            },
            primaryYAxis: {
                alternateGridBand: {
                    odd: {
                        fill: "#E6F0E7",
                        opacity: 0.5
                    }
                }
            }
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img26.png" Caption="Chart explaining grid band"%}

## Inversed Axis

You can display the Chart series in to inversed position using “**isInversed**” property of Chart Axis. This is illustrated in the following code.

{% highlight js %}

        $("#chartcontainer").ejChart({           
            primaryYAxis:
            {
                isInversed: true,
            },      
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img27.png" Caption="Chart with Inversed Axis"%}

## Opposed Position

By default, the x-axis is arranged horizontally at the bottom of the Chart and the y-axis is arranged vertically at the left side of the Chart. You can change the alignment of the axis by setting **opposedPosition** to true, which arranges the x-axis at the top and the y-axis at the right of the Chart. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            primaryXAxis:
            {
                opposedPosition: true,
            },

            primaryYAxis:
            {
                opposedPosition: true,
            },
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img28.png" Caption="Chart with OpposedPosition set to True"%}

## Smart Axis Labels

Sometimes the Chart dimensions could cause the labels to intersect. You can avoid overlapping labels using “**labelIntersectAction**” property of char axis. The Chart by default renders the texts one over the other. But, it also has some built-in capabilities to work around this overlap and lets you dictate the technique to follow. Refer to the following properties.

* rotate45 – Rotate the labels to 45 degree.

* rotate90 – Rotate the labels to 90 degree

* trim – Intersecting labels will be trim and mouse over the labels, it displays the trimmed text like tooltip.

* multiplerows – Split the intersecting labels in to multiple rows and display on the axis

* wrap – Wrap the intersecting text and display

* hide – It doesn’t display the intersecting label texts on the axis.



{% highlight js %}

        $("#chartcontainer").ejChart({
            primaryXAxis:
            {
                labelIntersectAction: 'rotate45'
            },
            primaryYAxis:
            {
                labelIntersectAction: 'none'
            },
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Axis_images/axis_img29.png" Caption="Chart with Smart Axis Labels"%}

