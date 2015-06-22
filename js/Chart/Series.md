---
layout: post
title: Series
description: series
platform: js
control: Chart
documentation: ug
---

# Series

The **Series** property provides access to a collection of all series that are defined explicitly within a Chart control. Each series is assigned with series type and name. It contains collection of data point and each point contains x value and y value(s).

## Multiple Series

You can plot **multiple****series** on the same Chart. Series are defined by adding them to the **"series"** array and rendering order of each series can be controlled using the **zOrder** properties of the series. Series with 0 as **zOrder** renders first.

{% highlight js %}


        $("#chartcontainer").ejChart({
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
                         { x: "Japan", y: 60 }, { x: "Australia", y: 56 },
                         { x: "France", y: 45 }, { x: "Germany", y: 30 },
                         { x: "Italy", y: 35 }, { x: "Sweden", y: 25 }
                ],
                name: 'Silver', type: 'column'
            }
            ],
            // ...                       
        });


{% endhighlight %}


{% include image.html url="/js/Chart/Series_images/Series_img1.png" Caption="Chart with Multiple Series"%}

### CommonSeriesOptions

You can specify the properties common to all series of the Chart in **commonSeriesOptions.**

{% highlight js %}


        $("#chartcontainer").ejChart({
            commonSeriesOptions: {
                type: 'column',
                border: { width: 2, color: 'black' }
            },
            series: [{
                points: [{ x: "USA", y: 50 }, { x: "China", y: 40 },
                         { x: "Japan", y: 70 }, { x: "Australia", y: 60 },
                         { x: "France", y: 50 }, { x: "Germany", y: 40 },
                         { x: "Italy", y: 40 }, { x: "Sweden", y: 30 }
                ],

                name: 'Gold'
            },
            {
                points: [{ x: "USA", y: 70 }, { x: "China", y: 60 },
                         { x: "Japan", y: 60 }, { x: "Australia", y: 56 },
                         { x: "France", y: 45 }, { x: "Germany", y: 30 },
                         { x: "Italy", y: 35 }, { x: "Sweden", y: 25 }
                ],

                name: 'Silver'
            }
            ],
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Series_images/Series_img2.png" Caption="Chart with CommonSeriesOptions"%}

## Combination Series

A combination Chart combines two or more Charts types in single Charts. For example, column series with line/spline series. There are some limitations in the combination series.

1. You cannot combine Column and Bar series.
2. Pie, Doughnut Series cannot be used with other series types.

{% highlight js %}


        $("#chartcontainer").ejChart({
            primaryYAxis:
            {
                title: { text: "Unit Sold" }
            },
            axes: [{
                majorGridLines:
                {
                    visible: false
                },
                orientation: 'Vertical',
                opposedPosition: true,
                axisLine: { visible: false },
                rangePadding: 'normal',
                name: 'yAxis',
                labelFormat: '${value}',
                title: { text: "Total Transactions" }
            }
            ],

            series: [{
                points: [{ x: "Jan", y: 45 }, { x: "Feb", y: 100 },
                        { x: "March", y: 25 }, { x: "April", y: 100 },
                        { x: "May", y: 85 }, { x: "June", y: 140 }
                ],
                fill: "#69D2E7",
                name: 'Unit Sold', type: 'column',

            },
            {
                points: [{ x: "Jan", y: 1000 }, { x: "Feb", y: 3000 },
                     { x: "March", y: 1000 }, { x: "April", y: 7000 },
                     { x: "May", y: 5000 }, { x: "June", y: 7000 }
                ],
                name: 'Total Transaction', type: 'line',
                enableAnimation: true, yAxisName: 'yAxis', width: 4

            }
            ],
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Series_images/Series_img3.png" Caption="Combination Chart"%}

## Customize Series

You can customize the Chart series using fill, border width and border color. You can customize the series color using **‘fill’** property of series, the stroke-width of the line, spline series using ‘**width**’ property of series, the border color and width of the column/bar using ‘**border**’ property of series and rect in the column/bar Chart using the **‘fill’** and **‘border’** property of each point.

{% highlight js %}


       $("#chartcontainer").ejChart({
            series: [{
                points: [
                    { x: "Jan", y: 45 },
                    { x: "Feb", y: 100, fill: '#F07542', border: { color: "red", width: 2 } },
                    { x: "March", y: 25 }, { x: "April", y: 100 }, { x: "May", y: 85 },
                    { x: "June", y: 140 }
                ],
                fill: "#69D2E7", name: 'Unit Sold', type: 'column',
                border: { width: 1, color: 'black' }
            },
            ],
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Series_images/Series_img4.png" Caption="Customized Chart"%}

## Data Labels

Data labels refer to the y values of data points that appear on each point. You can also display category names or custom text in data label by applying template for the dataLabel. horizontalTextAlignment and verticalTextAlignment in dataLabel is used to align the label. 

{% highlight html %}

   <div id="template">
        <div id="point">#point.x#:#point.y#%</div>
    </div>
    
{% endhighlight %}

{% highlight js %}

        $("#chartcontainer").ejChart({
            series: [{
                points: [{ x: 2006, y: 29.2 }, { x: 2007, y: 33.9 },
                         { x: 2008, y: 36 }, { x: 2009, y: 32.4 },
                         { x: 2010, y: 32 }],
                name: 'India',
                marker: {
                    dataLabel: { visible: true, template: 'template' }
                },
                fill: '#8CC640'
            },
            {
                points: [{ x: 2006, y: 21.8 }, { x: 2007, y: 24.9 },
                         { x: 2008, y: 28.5 }, { x: 2009, y: 27.2 },
                         { x: 2010, y: 23.4 }],
                name: 'Singapore',
                marker: {
                    dataLabel: { visible: true, shape: 'Rectangle' }
                },
                fill: '#CBA4C7'
            },
            ],
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Series_images/Series_img5.png" Caption="Chart with Data Labels"%}

### ConnectorLine

**ConnectorLine** in data Label is used to customize the line that connects the outside labels of the pie series in terms of color, height, width and type of line. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                points: [{ x: 'Other Personnal', y: 94658, text: 'Other Personal, 88.47%' },
                         { x: 'Medical care', y: 9090, text: 'Medical care, 8.49%' },
                         { x: 'Housing', y: 2577, text: 'Housing, 2.40%' },
                         { x: 'Transportation', y: 473, text: 'Transportation, 0.44%' },
                         { x: 'Education', y: 120, text: 'Education, 0.11%' },
                         { x: 'Electronics', y: 70, text: 'Electronics, 0.06%' }
                ],
                marker: {
                    dataLabel: {
                        visible: true,
                        shape: 'none',
                        connectorLine: { type: 'bezier', color: 'black', width: 1 },
                        font: { size: '14px' }
                    }
                },
            }
            ],
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Series_images/Series_img6.png" Caption="Chart with ConnectorLine"%}

### Data labels Rotation

Data labels refer to the y values of data points, which appear on each point. You can rotate data labels with positive and negative angles using angle property.

{% include image.html url="/js/Chart/Series_images/Series_img7.png" Caption="Rotated Data Labels"%}

{% highlight js %}


        $("#container").ejChart({
            //......
            commonSeriesOptions: {
                type: 'column', enableAnimation: false,
                tooltip: { visible: true },
                marker: {
                    dataLabel: {
                        font: { color: 'white', size: '16px' },
                        angle: 90,
                        textPosition: 'middle',
                        visible: true
                    },
                }
            },
            series: [{
                points: [{ x: "Print Ads", y: 110 }, { x: "Online Ads", y: 125 },
                   { x: "Content Marketing", y: 95 }, { x: "Tradeshows", y: 60 }],
                name: 'Marketing', tooltip: { visible: true, template: 'Tooltip' }
            }],

            //......
        }); 


{% endhighlight %}



