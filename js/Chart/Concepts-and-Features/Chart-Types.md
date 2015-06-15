---
layout: post
title: Chart-Types
description: chart types
platform: js
control: Chart
documentation: ug
---

# Chart Types

**Essential JavaScript Chart** control supports more than 20 types of Chart for your business requirements. Each one is highly and easily configurable with built-in support for creating stunning visual effects.

Chart types are specified on each **series** through the **type** property. All the Chart types are required to have at least one **x** and one **y** value. Certain Chart types require more than one y value.

You can combine several Chart types in one Chart using the **type** property on series to set different Chart types for each series.

{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                type: 'line',
                name: 'lineSeries',
                //.......
            },
            {
                type: 'column',
                name: 'columnSeries',
                //.......
            }
            ],
        });


{% endhighlight %}



In multiple series case, you can use **commonSeriesOptions** property to specify the properties that are common for all series in Chart. 

{% highlight js %}


        $("#container").ejChart({
            commonSeriesOptions: {
                type: 'line', enableAnimation: false,
                marker:
                   {
                       shape: 'circle',
                       size: { height: 10, width: 10 },
                       visible: true
                   },
            },
            //.......
        });


{% endhighlight %}

## Line Chart

**Line Charts** join points on a plot using straight lines showing trends in data at equal intervals. **Line Charts** treats the input as non-numeric, categorical information, equally spaced along the x-axis.

You can configure the appearance of the lines and the points with options **fill** used and **width** of line.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img1.png" Caption="Line Chart"%}

{% highlight js %}


       $("#chartcontainer").ejChart({
            //  .......
            series: [{
                points: [{ x: 2005, y: 28 }, { x: 2006, y: 35 },
                    { x: 2007, y: 42 }, { x: 2008, y: 37 },
                    { x: 2009, y: 41 }, { x: 2010, y: 35 },
                    { x: 2011, y: 37 }],
                name: 'India', type: 'line', width: 4, fill: '#FBAF4F'
            }],
            //.......
        }); 


{% endhighlight %}

## StepLine Chart

**Step Line Charts** use horizontal and vertical lines to connect data points resulting in a step like progression. You can configure the appearance of line using **fill** and **width** property in series.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img2.png" Caption="Step Line Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({

            //   .......
            series: [{
                points: [{ x: 2006, y: 430 }, { x: 2007, y: 416 }, { x: 2008, y: 404 },
                         { x: 2009, y: 390 }, { x: 2010, y: 376 }, { x: 2011, y: 362 },
                         { x: 2012, y: 351 }],
                name: 'USA', type: "stepline", fill: '#F07542', width: 3
            }],
            // .......
        });


{% endhighlight %}

## Area Chart

**Area Chart** is rendered using a collection of line segments connected to form a closed-loop area filled with a specified color.You can plot multiple series on the same Chart. You can use **Fill** in series to customize the series color and the **border** to customize the series border color and width.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img3.png" Caption="Area Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            //   .......
            series: [{
                points: [{ x: 1900, y: 2.6 }, { x: 1920, y: 2.8 },
                         { x: 1940, y: 2.6 }, { x: 1960, y: 3 },
                         { x: 1980, y: 3.6 }, { x: 2000, y: 3 }
                ],
                name: 'Product B', type: 'Area',
                border: { color: 'black', width: 1 }, fill: '#C4C24A'
            },
            {
                points: [{ x: 1900, y: 2.8 }, { x: 1920, y: 2.5 },
                         { x: 1940, y: 2.8 }, { x: 1960, y: 3.2 },
                         { x: 1980, y: 2.9 }, { x: 2000, y: 2 }
                ],
                name: 'Product C', type: 'Area',
                border: { color: 'black', width: 1 }, fill: '#6A4B82',
            }
            ],
            //.......

        });


{% endhighlight %}

## Range Area Chart

**Range Area Charts** are similar to regular area Charts except that, each area is rendered over a range.  Specify the y-axis high and low values for each point for the **Range Area Chart.** You can customize the series color and border****using **fill** and **border** properties in series.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img4.png" Caption="Range Area Chart"%}



{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                points: [{ x: 1900, low: 2, high: 4 },
                         { x: 1920, low: 2.5, high: 4.5 },
                         { x: 1940, low: 3, high: 5 },
                         { x: 1960, low: 3.3, high: 5.3 },
                         { x: 1980, low: 3, high: 5 },
                         { x: 2000, low: 2.5, high: 4.5 },
                         { x: 2020, low: 2, high: 4 }
                ],
                name: 'Product B'
            },
            {
                points: [{ x: 1900, low: 0, high: 2 },
                         { x: 1920, low: 0.5, high: 2.5 },
                         { x: 1940, low: 1, high: 3 },
                         { x: 1960, low: 1.3, high: 3.3 },
                         { x: 1980, low: 1, high: 3 },
                         { x: 2000, low: 0.5, high: 2.5 },
                         { x: 2020, low: 0, high: 2 }
                ],

                name: 'Product C',

            }
            ],
        });


{% endhighlight %}

## StepArea Chart

**Step Area Charts** are similar to regular area Charts except that, instead of a straight line tracing the shortest path between points, the values are connected by continuous vertical and horizontal lines forming a step like progression. You can use the **fill** and **border** properties in series to customize the series color and border.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img5.png" Caption="Step Area Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            //.......
            series: [{
                points: [{ x: 2000, y: 416 }, { x: 2001, y: 490 },
                         { x: 2002, y: 470 }, { x: 2003, y: 500 },
                         { x: 2004, y: 449 }, { x: 2005, y: 470 },
                         { x: 2006, y: 437 }, { x: 2007, y: 458 },
                         { x: 2008, y: 500 }, { x: 2009, y: 473 },
                         { x: 2010, y: 520 }, { x: 2011, y: 509 }],
                name: 'Brazil', border: { color: 'black', width: 2 },
                fill: '#69D2E7', type: 'steparea'
            }
            ],
            //......

        });  


{% endhighlight %}

## SplineArea Chart

**Spline Area Chart** is similar to an **Area Chart** except the difference in the way the points of a series are connected. It connects each series of points by a smooth spline curve. You can plot multiple series on the same Chart. To customize the series color and border, use the **fill** and **border** properties in series.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img6.png" Caption="Spline Area Chart"%}

{% highlight js %}

 
        $("#chartcontainer").ejChart({
            //    .......

            series: [{
                points: [{ x: 2002, y: 2.2 }, { x: 2003, y: 3.4 },
                         { x: 2004, y: 2.8 }, { x: 2005, y: 1.6 }, { x: 2006, y: 2.3 },
                         { x: 2007, y: 2.5 }, { x: 2008, y: 2.9 }, { x: 2009, y: 3.8 },
                         { x: 2010, y: 1.4 }, { x: 2011, y: 3.1 }],
                name: 'US', border: { color: 'transparent' },
                fill: '#C4C24A', type: "splinearea"
            },
            {
                points: [{ x: 2002, y: 0.8 }, { x: 2003, y: 1.3 },
                         { x: 2004, y: 1.1 }, { x: 2005, y: 1.6 }, { x: 2006, y: 2 },
                         { x: 2007, y: 1.7 }, { x: 2008, y: 2.3 }, { x: 2009, y: 2.7 },
                         { x: 2010, y: 1.1 }, { x: 2011, y: 2.3 }],
                name: 'Germany', border: { color: 'transparent' },
                fill: '#6A4B82', type: "splinearea"
            }
            ],
            //......

        });


{% endhighlight %}

## StackingArea Chart

**Stacking Area Charts** are similar to regular area Charts except that the Y values stack on top of each other in the specified series order. This enables you to visualize the relationship of parts to the whole. You can customize the series color and border using **fill** and **border** properties in series.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img7.png" Caption="Stacking Area Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart(
        {
            //.......
            series: [{
                points: [{ x: 2002, y: 6 }, { x: 2003, y: 7.5 },
                   { x: 2004, y: 6 }, { x: 2005, y: 6.5 }, { x: 2006, y: 7.4 },
                   { x: 2007, y: 7.9 }, { x: 2008, y: 7.5 }, { x: 2009, y: 8.5 },
                   { x: 2010, y: 4.8 }, { x: 2011, y: 9.3 }],
                name: 'US', border: { color: 'black', width: 2 },
                fill: '#C4C24A', type: 'stackingarea'
            },
            {
                points: [{ x: 2002, y: 3.5 }, { x: 2003, y: 4.9 },
                 { x: 2004, y: 3.7 }, { x: 2005, y: 7.5 }, { x: 2006, y: 4.8 },
                 { x: 2007, y: 2.6 }, { x: 2008, y: 4.7 }, { x: 2009, y: 3.7 },
                 { x: 2010, y: 3.5 }, { x: 2011, y: 3.6 }],
                name: 'Indonesia', border: { color: 'black', width: 2 },
                fill: '#69D2E7', type: 'stackingarea'
            }

            ],
            //......

        });


{% endhighlight %}

## 100% Stacking area chart  

100% Stacking area is similar to the stacking area chart. But here, the series display multiple data series as stacked areas and the cumulative portion of each stacked element is summed to 100%. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                points: [{ x: 2006, y: 34 }, { x: 2007, y: 20 },
                         { x: 2008, y: 40 }, { x: 2009, y: 51 },
                         { x: 2010, y: 26 }, { x: 2011, y: 37 },
                         { x: 2012, y: 54 }, { x: 2013, y: 44 },
                         { x: 2014, y: 48 }
                ],
                type: "stackingarea100"
            },
            {
                points: [{ x: 2006, y: 51 }, { x: 2007, y: 26 },
                         { x: 2008, y: 37 }, { x: 2009, y: 51 },
                         { x: 2010, y: 26 }, { x: 2011, y: 37 },
                         { x: 2012, y: 43 }, { x: 2013, y: 23 },
                         { x: 2014, y: 55 }
                ],
                type: "stackingarea100"
            }
            ],
        });


{% endhighlight %}



The following screenshot displays the **100% Stacking area chart.**

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img8.png" Caption="100% Stacking area chart"%}

## Column Chart

**Column Charts** are among the most common Chart types that are used. It uses vertical bars (columns) to display different values of one or more items. It is similar to a bar Chart except that the bars are vertical and not horizontal as in bar Chart. Points from adjacent series are drawn as bars next to each other. You can customize the series color and border****using **fill** and **border** properties in series and each segment of series using **fill** and **border** properties in point.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img9.png" Caption="Column Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart(
        {
            //   .......
            series: [{
                points: [{ x: "USA", y: 50 }, { x: "China", y: 40 },
                         { x: "Japan", y: 70 }, { x: "Australia", y: 60 },
                         { x: "France", y: 50 }, { x: "Germany", y: 40 },
                         { x: "Italy", y: 40 }, { x: "Sweden", y: 30 }
                ],

                name: 'Gold', type: 'column',
                border: { width: 2, color: 'black' }, fill: '#BF812A'
            },
            {
                points: [{ x: "USA", y: 70 }, { x: "China", y: 60 },
                         { x: "Japan", y: 60 }, { x: "Australia", y: 56 },
                         { x: "France", y: 45 }, { x: "Germany", y: 30 },
                         { x: "Italy", y: 35 }, { x: "Sweden", y: 25 }
                ],

                name: 'Silver', type: 'column',
                border: { width: 2, color: 'black' }, fill: '#0D97D4'
            },

            ],
            //    ......

        });


{% endhighlight %}

## RangeColumn Chart

**RangeColumn Chart** is similar to the **Column Chart** except that each column is rendered over a range. Specify the y-axis Starting and Ending values for each point for the **RangeColumn Chart**. You can customize the series color and border****using **fill** and **border** properties in series and each segment of series using **fill** and **border** properties in point.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img10.png" Caption="RangeColumn Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            //          .......
            series: [{
                points: [{ x: 'Jan', low: 0.7, high: 6.1 },
                          { x: 'Feb', low: 1.3, high: 6.3 },
                          { x: 'Mar', low: 1.9, high: 8.5 },
                          { x: 'Apr', low: 3.1, high: 10.8 },
                          { x: 'May', low: 5.7, high: 14.4 }],
                name: 'India', fill: '#E94649', border: { color: 'black', width: 1 }
            },
            {
                points: [{ x: 'Jan', low: 1.7, high: 7.1 },
                         { x: 'Feb', low: 1.9, high: 7.7 },
                         { x: 'Mar', low: 1.2, high: 7.5 },
                         { x: 'Apr', low: 2.5, high: 9.8 },
                         { x: 'May', low: 4.7, high: 11.4 }],
                name: 'Germany', fill: '#F6B53F', border: { color: 'black', width: 1 }
            }],
            //  ......

        });


{% endhighlight %}

## StackingColumn Chart

**Stacking Column Charts** are similar to regular column Charts except that the Y values stack on top of each other in the specified series order. This enables you to visualize the relationship of parts to the whole.You can customize the series color and border****using **fill** and **border** properties in series and each segment of series using **fill** and **border** properties in point.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img11.png" Caption="Stacking Column Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            // .......
            series: [{
                points: [{ x: 'Jan', y: 900 }, { x: 'Feb', y: 820 },
                         { x: 'Mar', y: 880 }, { x: 'Apr', y: 725 },
                         { x: 'May', y: 765 }
                ],
                name: 'Google', fill: '#00558B', type: 'stackingcolumn',
                border: { color: 'black', width: 1 }
            },

            {
                points: [{ x: 'Jan', y: 190 }, { x: 'Feb', y: 226 },
                         { x: 'Mar', y: 194 }, { x: 'Apr', y: 250 },
                         { x: 'May', y: 222 },
                ],
                name: 'Bing', fill: '#75A010', type: 'stackingcolumn',
                border: { color: 'black', width: 1 }
            },

            {
                points: [{ x: 'Jan', y: 250 }, { x: 'Feb', y: 145 },
                         { x: 'Mar', y: 190 }, { x: 'Apr', y: 220 },
                         { x: 'May', y: 225 },
                ],
                name: 'Yahoo', fill: '#D98F31', type: 'stackingcolumn',
                border: { color: 'black', width: 1 }
            }
            ],
            //  ......

        });


{% endhighlight %}

## 100% Stacking column chart 

**100% Stacking column** is similar to the stacking column charts. But here, the combined contribution of Y values is the combined total of the vertical column with 100 percent.

{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                points: [{ x: 2006, y: 900 }, { x: 2007, y: 544 },
                          { x: 2008, y: 880 }, { x: 2009, y: 725 },
                          { x: 2010, y: 765 }, { x: 2011, y: 679 },
                          { x: 2012, y: 770 }
                ],
                type: "stackingcolumn100"
            },
            {
                points: [{ x: 2006, y: 190 }, { x: 2007, y: 226 },
                         { x: 2008, y: 194 }, { x: 2009, y: 545 },
                         { x: 2010, y: 222 }, { x: 2011, y: 181 },
                         { x: 2012, y: 128 }
                ],
                type: "stackingcolumn100"
            }
            ],
        });


{% endhighlight %}



The following screenshot displays the **100% Stacking column chat**.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img12.png" Caption="100% Stacking column chat."%}

## Bar Chart

**Bar Chart** is the simplest and most versatile of statistical diagrams. It displays horizontal bars for each point in the series and points from adjacent series are drawn as bars next to each other. Bar Charts are used to compare values across categories, to display variations in the value of an item over time or to display the values of several items at a single point in time.You can customize the series color and border****using **fill** and **border** properties in series and each segment of series using **fill** and **border** properties in point.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img13.png" Caption="Bar Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            //  .......
            series: [{
                points: [{ x: 2006, y: 7.8 }, { x: 2007, y: 7.2 },
                         { x: 2008, y: 6.8 }, { x: 2009, y: 10.7 },
                         { x: 2010, y: 10.8 }, { x: 2011, y: 9.8 }
                ],

                name: 'India', fill: '#C8D7A8', type: 'bar',
                border: { color: 'black', width: 1 }
            },
            {
                points: [{ x: 2006, y: 4.8 }, { x: 2007, y: 4.6 },
                         { x: 2008, y: 7.2 }, { x: 2009, y: 9.3 },
                         { x: 2010, y: 9.7 }, { x: 2011, y: 9 }
                ],

                name: 'US', fill: '#004068', type: 'bar',
                border: { color: 'black', width: 1 }
            }

            ],
            //  ......

        }); 


{% endhighlight %}

## Stackingbar Chart

**Stacking Bar Charts** are similar to regular bar Charts except that the Y values stack on top of each other in the specified series order. This enables you to visualize the relationship of parts to the whole. You can customize the series color and border****using **fill** and **border** properties in series and each segment of series using **fill** and **border** properties in point.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img14.png" Caption="Stacking Bar Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            //   .......
            series: [{
                points: [{ x: "Jan", y: 6 }, { x: "Feb", y: 8 },
                         { x: "Mar", y: 12 }, { x: "Apr", y: 15.5 },
                         { x: "May", y: 20 }, { x: "Jun", y: 24 },
                         { x: "Jul", y: 28 },
                ],

                name: 'Apple', type: 'stackingbar',
                fill: "#1ABC9C", border: { color: 'black', width: 1 }
            },

            {
                points: [{ x: "Jan", y: -1 }, { x: "Feb", y: -1.5 },
                         { x: "Mar", y: -2 }, { x: "Apr", y: -2.5 },
                       { x: "May", y: -3 }, { x: "Jun", y: -3.5 },
                       { x: "Jul", y: -4 },
                ],

                name: 'Wastage', type: 'stackingbar', fill: "#34495E",
                opacity: 0.7, border: { color: 'black', width: 1 }
            }
            ],
            // ......

        });          


{% endhighlight %}

## 100% Stacking bar chart 

**100% Stacking bar** is similar to stacking bar charts. Here, the combined contribution of Y values is the combined total of the horizontal bar with 100 percent.

{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                points: [{ x: 2007, y: 453 }, { x: 2008, y: 354 },
                         { x: 2009, y: 282 }, { x: 2010, y: 321 },
                         { x: 2011, y: 333 }, { x: 2012, y: 351 },
                         { x: 2013, y: 403 }, { x: 2014, y: 421 }
                ],
                type: "stackingbar100"
            },
            {
                points: [{ x: 2007, y: 876 }, { x: 2008, y: 564 },
                         { x: 2009, y: 242 }, { x: 2010, y: 121 },
                         { x: 2011, y: 343 }, { x: 2012, y: 451 },
                         { x: 2013, y: 203 }, { x: 2014, y: 431 },
                ],
                type: "stackingbar100"
            }
            ],
        });   


{% endhighlight %}



The following screenshot displays the **100% Stackingbar chart.**

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img15.png" Caption="100% Stackingbar chart"%}

## Spline Chart

**Spline Chart** is similar to a **Line Chart** except that it connects the different data points using splines instead of straight lines. You can configure the appearance of the lines and the points with options **fill** used and the **width** of lines.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img16.png" Caption="Spline Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            //  .......
            series: [{
                points: [{ x: 'Jan', y: -1 }, { x: 'Feb', y: -1 },
                         { x: 'Mar', y: 2 }, { x: 'Apr', y: 8 },
                         { x: 'May', y: 6 }, { x: 'Jun', y: 18 },
                         { x: 'Jul', y: 11 }

                ],
                name: 'London', type: 'spline', fill: '#E49519', width: 3
            },
            {
                points: [{ x: 'Jan', y: 3 }, { x: 'Feb', y: 3.5 },
                         { x: 'Mar', y: 7 }, { x: 'Apr', y: 5.5 },
                         { x: 'May', y: 5 }, { x: 'Jun', y: 13.5 },
                         { x: 'Jul', y: 16 }

                ],
                name: 'Germany', type: 'spline', fill: '#986827', width: 3
            },

            ],
            // ......

        });


{% endhighlight %}

## Pie Chart

A **Pie Chart** renders y values as slices in a pie. The slices are rendered in proportion to the whole that is the sum of all the y values in the series. Consequently, **Pie Charts** are used to visualize the proportional contribution in terms of percentage or fraction of categories of data to the whole data set. The x values in the data series are treated only as nominal in categorical, qualitative data. The **Pie Chart** displays only one Data Series at a time. You can customize the series color and border****using **fill** and **border** properties in series and each slice of series using **fill** and **border** properties in point.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img17.png" Caption="Pie Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart(
        {
            //  .......
            series: [{
                points: [{ x: 'Labour', y: 28, text: 'Labour 28%', fill: '#00558B' },
                         { x: 'Legal', y: 10, text: 'Legal 10%', fill: '#00558B' },
                         {
                             x: 'Production', y: 20, text: 'Production 20%',
                             fill: '#68E1E6'
                         },
                         { x: 'License', y: 15, text: 'License 15%', fill: '#57760B' },
                         {
                             x: 'Facilities', y: 23, text: 'Facilities 23%',
                             fill: '#00558B'
                         },
                         { x: 'Taxes', y: 17, text: 'Taxes 17%', fill: '#8A4B05' },
                         {
                             x: 'Insurance', y: 12, text: 'Insurance 12%',
                             fill: '#8A4B05'
                         }
                ],
                marker: {
                    dataLabel: {
                        visible: true, connectorLine: { height: 30 },
                        font: { size: '20px' }
                    }
                },
                name: 'Newyork', type: 'pie', explode: true, labelPosition: 'outside',
                pieCoefficient: 0.7, explodeIndex: 2, border: { width: 1, color: 'black' }
            }
            ],
            // ......

        });


{% endhighlight %}

## Doughnut Chart

**Doughnut Charts** are pie Charts with a hole, whose value is specified as the doughnut coefficient. The **Doughnut Chart** is best suited for presenting data in proportions. You can customize the series color and border****using **fill** and **border** properties in series and each slice of series using **fill** and **border** properties in point.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img18.png" Caption="Doughnut Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            //.......
            series: [{
                points: [{ x: 'Labour', y: 28, text: 'Labour 28%', fill: '#00558B' },
                         { x: 'Legal', y: 10, text: 'Legal 10%', fill: '#00558B' },
                         {
                             x: 'Production', y: 20, text: 'Production 20%',
                             fill: '#57760B'
                         },
                         { x: 'License', y: 15, text: 'License 15%', fill: '#57760B' },
                         {
                             x: 'Facilities', y: 23, text: 'Facilities 23%',
                             fill: '#00558B'
                         },
                         { x: 'Taxes', y: 17, text: 'Taxes 17%', fill: '#8A4B05' },
                         {
                             x: 'Insurance', y: 12, text: 'Insurance 12%',
                             fill: '#8A4B05'
                         }
                ],
                marker: {
                    dataLabel: {
                        visible: true, connectorLine: { height: 30 },
                        font: { size: '20px' }
                    }
                },
                name: 'Newyork', type: 'doughnut', explode: true,
                labelPosition: 'outside', doughnutCoefficient: 0.4,
                border: { width: 1, color: 'black' }
            }
            ],
            //   ......

        });


{% endhighlight %}

## Semi Pie and Doughnut Chart

The semi pie and doughnut chart is a semicircular chart. Data are represented in different sectors within a semi-circle.

**EJ Chart** allows you to create semi pie and doughnut chart using **startAngle** and **endAngle** property. Default values of startAngle and endAngle are null. The specified data are represented within start angle to end angle degree.

{% highlight js %}



        $("#chartcontainer").ejChart({
            // ...     
            series: [{
                points: [{ x: 'Australia', y: 53.3, text: 'Australia 53.3' },
                         { x: 'China', y: 55.7, text: 'China 55.7' },
                         { x: 'India', y: 60.5, text: 'India 60.5' },
                         { x: 'Japan', y: 12.5, text: 'Japan 12.5' },
                         { x: 'South Africa', y: 79.4, text: 'South Africa 79.4' },
                         { x: 'United Kingdom', y: 70.9, text: 'United Kingdom 70.9' },
                         { x: 'United States', y: 45.0, text: 'United States 45.0' }
                ],
                border: { width: 1, color: 'white' },
                name: 'Agricultural Land', type: 'doughnut', labelPosition: 'outside',
                startAngle: -90, endAngle: 90
            },
            ],
            // ...             
        });



{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img19.jpeg" Caption="Semi Doughnut Chart"%}

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img20.jpeg" Caption="Semi Pie Chart"%}

## Pyramid Chart

The **Pyramid Chart** type displays the data that when totalled renders 100%. This type of Chart is a single series Chart representing the data as portions of 100%, and this Chart does not use any axes. You can customize the series color and border****using **fill** and **border** properties in series and each slice of series using **fill** and **border** properties in point.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img21.png" Caption="Pyramid Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart( {
            //.......
            series: [{
                points: [{ x: 'India', y: 24, text: 'India 24%' },
                        { x: 'Japan', y: 25, text: 'Japan 25%' },
                        { x: 'Australia', y: 20, text: 'Australia 20%' },
                        { x: 'USA', y: 35, text: ' USA 35%' },
                        { x: 'China', y: 23, text: ' China 23%' },
                        { x: 'Germany', y: 27, text: ' Germany 27%' },
                        { x: 'France', y: 22, text: ' France 22%' }
                ],
                marker: {
                    dataLabel: {
                        visible: true, shape: 'rectangle',
                        font: { color: 'white', size: '15px’ }
                        }
                    },
                    name: 'Newyork', type: 'pyramid', labelPosition: 'outside',

                }
            }
            ],
            //......

        }); 


{% endhighlight %}

## Funnel Chart

The **Funnel** chart is a single series chart representing the data as portions of 100%, and this chart does not use any axes. Funnel charts are often used to represent stages in a sales process and expresses the amount of potential revenue for each stage. This type of chart can also be useful in identifying potential problem area in an organization’s sales process. You can customize the funnel width and height using **funnelWidth** and **funnelHeight** properties.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img22.png" Caption="Funnel Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            //.......
            series: [{
                points: [{ x: 'Renewed', y: 18.20, text: 'Renewed : 18.20%' },
                        { x: 'Subscribe', y: 27.3, text: 'Subscribed : 27.3%' },
                        { x: 'Support', y: 55.9, text: 'Contact to Support : 55.9%' },
                        { x: 'Downloaded', y: 76.8, text: ' Downloaded a Trail : 76.8%' },
                        { x: 'Visited', y: 100, text: ' Visited Web Site : 100%' },
                ],	
                marker: {
                    dataLabel: {
                        visible: true, shape: 'rectangle',
                        font: { color: 'white', size: '15px' }
                    }
                },
                name: 'Website', type: 'funnel', funnelWidth: '32.7%',
                funnelHeight: '11.2%', labelPosition: 'outside',

            }
            ],
            //......

        });


{% endhighlight %}

## Bubble Chart

**Bubble Chart** is an extension of the **Scatter Chart** (or XY-Chart) where each data marker is represented by a circle whose dimension forms a third variable. Consequently, bubble Charts allow three-variable comparisons allowing for easy visualization of complex interdependencies that are not apparent in two-variable Charts. Bubble Charts are frequently used in market and product comparison studies.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img23.png" Caption="Bubble Chart"%}

{% highlight js %}


        $("#chartcontainer").ejChart({
            //.......      
            series: [{
                points: [
                        { x: 92.2, y: 7.8, size: 1.347, fill: '#E94649' },
                        { x: 74, y: 6.5, size: 1.241, fill: '#F6B53F' },
                        { x: 90.4, y: 6.0, size: 0.238, fill: '#6FAAB0' },
                        { x: 99.4, y: 2.2, size: 0.312, fill: '#C4C24A' },
                        { x: 88.6, y: 1.3, size: 0.197, fill: '#FB954F' },
                        { x: 54.9, y: 3.7, size: 0.177, fill: '#D9CEB2' },
                        { x: 99, y: 0.7, size: 0.0818, fill: '#FF8D8D' },
                        { x: 72, y: 2.0, size: 0.0826, fill: '#69D2E7' },
                        { x: 99.6, y: 3.4, size: 0.143, fill: '#E27F2D' },
                        { x: 99, y: 0.2, size: 0.128, fill: '#6A4B82' },
                        { x: 86.1, y: 4.0, size: 0.115, fill: '#F6B53F' },
                        { x: 92.6, y: 6.6, size: 0.096, fill: '#C4C24A' },
                        { x: 61.3, y: 14.5, size: 0.162, fill: '#FF8D8D' },
                        { x: 56.8, y: 6.1, size: 0.151, fill: '#69D2E7' }
                ],
                enableAnimation: true,
                name: 'pound',
                type: 'bubble',
            },
            ],
            //.......
        });


{% endhighlight %}

## Scatter

In **Scatter Series**, each data point is represented as an ellipse, and the width and height of each ellipse is set using the **size width** and **height** properties of marker. You can also change the color, stroke, and stroke thickness of the series using the **fill, border color**, and **width properties of marker** respectively.

The following code example is used to create a simple **scatter series**.

{% highlight js %}


        $("#chartcontainer").ejChart({
            primaryXAxis: {
                rangePadding: "additional"
            },
            series: [{
                points: [{ x: 10, y: 126.45 },
                         { x: 11, y: 150.99 },
                         { x: 12, y: 40.19 },
                         { x: 13, y: 160.23 },
                         { x: 15, y: 200.89 }],
                name: 'Scatter', type: 'scatter',
                marker: {
                    size: { height: 10, width: 10 },
                    border: { width: 2, color: "black" }
                }
            }],
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img24.png" Caption="Scatter Series"%}

## HiLoOpenCloseSeries 

A **HiLoOpenCloseSeries** displays each data point as a group of two horizontal lines and one vertical line. The height of the vertical line depends on the difference between the high value and low value of the data point. The width of the horizontal lines depends on the time span interval. The line indicating the open value is at the left side of the vertical line, and the line indicating the closed value is at its right side. You can also change the color, and stroke thickness of the series using the **fill**, **border****width** properties respectively.

The following properties are useful in mapping the value of each data point in a **HiLoOpenCloseSeries**: 

_Property Table_

<table>
<tr>
<td>
<b>API</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
x</td><td>
Represents the x-values</td></tr>
<tr>
<td>
Open</td><td>
Represents the Open values</td></tr>
<tr>
<td>
High</td><td>
Represents the high values</td></tr>
<tr>
<td>
low</td><td>
Represents the low values</td></tr>
<tr>
<td>
close</td><td>
Represents the close values</td></tr>
</table>


{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img25.png" Caption="HiLoOpenCloseSeries"%}

**bullFillColor**

**BullFillColor** is used to specify a fill color for the segments that indicates an increase in stock price in the measured time interval.

**bearFillColor**

**BearFillColor** is used to specify a fill color for the segments that indicate a decrease in stock price in the measured time interval.

**drawMode**

**drawMode** is used to specify the open and close draw mode to **hiloopenclose series**.

* Open - Points only the opening value of that period.

* Close - Points out the closing value of that period.

* Both - Points out both the opening and the closing values of that period.



To create a simple **HiLoOpenCloseSeries** use the following code example.

{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                points: [
                    { x: new Date(1950, 1, 12), high: 125.45, low: 70.23, open: 125.22, close: 90.44 },
                    { x: new Date(1953, 1, 12), high: 150.99, low: 60.23, open: 120.55, close: 70.90 },
                    { x: new Date(1956, 1, 12), high: 200.19, low: 130.37, open: 160.13, close: 190.78 },
                    { x: new Date(1959, 1, 12), high: 160.23, low: 90.16, open: 140.38, close: 110.24 },
                    { x: new Date(1962, 1, 12), high: 200.89, low: 100.23, open: 180.90, close: 120.29 }],
                name: 'Series', type: 'hiloopenclose', drawMode: 'both', border: { width: 2 }
            }],
        });


{% endhighlight %}

## Candle

A **CandleSeries** displays each data point with a combination of a vertical column and a vertical line. The height of the vertical line represents the difference between high and low value of a datapoint, whereas the height of the vertical column represents the difference between the Open and Close values of a data point. You can also change the color and stroke thickness of the series using the **fill**, **border****width** properties respectively.

The following properties are useful in mapping the value of each data point in a **Candle**.

_Property Table_

<table>
<tr>
<td>
<b>API</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
x</td><td>
Represents the x-values</td></tr>
<tr>
<td>
open</td><td>
Represents the Open values.</td></tr>
<tr>
<td>
high</td><td>
Represents the high values</td></tr>
<tr>
<td>
low</td><td>
Represents the low values</td></tr>
<tr>
<td>
close</td><td>
Represents the close values</td></tr>
</table>


{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img26.png" Caption="CandleSeries"%}

**bullFillColor**

**BullFillColor** is used to specify a fill color for the segment that indicates an increase in stock price in the measured time interval.

**bearFillColor**

**BearFillColor** is used to specify a fill color for the segment that indicates a decrease in stock price in the measured time interval.

To create a simple **Candle series** use the following code example.

{% highlight js %}


        $("#chartcontainer").ejChart({

            series: [{
                points: [
                    { x: new Date(1950, 1, 12), high: 125.45, low: 70.23, open: 125.22, close: 90.44 },
                    { x: new Date(1953, 1, 12), high: 150.99, low: 60.23, open: 120.55, close: 70.90 },
                    { x: new Date(1956, 1, 12), high: 200.19, low: 130.37, open: 160.13, close: 190.78 },
                    { x: new Date(1959, 1, 12), high: 160.23, low: 90.16, open: 140.38, close: 110.24 },
                    { x: new Date(1962, 1, 12), high: 200.89, low: 100.23, open: 180.90, close: 120.29 }],
                name: 'Series', type: 'candle', border: { width: 2 }
            }],
        });


{% endhighlight %}

## Hilo

In****a **HiLoSeries,** each segment is represented by a line. The height of the line depends on the difference between the high value and low value of the data point. You can also change the color and stroke thickness of the series using the **fill**, **border****width** properties respectively.

The following properties are useful in mapping the value of each data point in a **Hilo**.

_Property Table_

<table>
<tr>
<td>
<b>API</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
x</td><td>
Represents the x-values</td></tr>
<tr>
<td>
high</td><td>
Represents the high values</td></tr>
<tr>
<td>
low</td><td>
Represents the low values</td></tr>
</table>


{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img27.png" Caption="HiLoSeries"%}

To create a simple **Hilo series** use the following code example.

{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                points: [{ x: new Date(1950, 1, 12), high: 126.45, low: 70.23 },
                         { x: new Date(1953, 1, 12), high: 150.99, low: 60.23 },
                         { x: new Date(1956, 1, 12), high: 200.19, low: 130.37 },
                         { x: new Date(1959, 1, 12), high: 160.23, low: 90.16 },
                         { x: new Date(1962, 1, 12), high: 200.89, low: 100.23 }],
                name: 'Series', type: 'hilo', border: { width: 2 }
            }],
        }); 


{% endhighlight %}

## Polar

A **Polar Chart** is a circular graph on which data is displayed in terms of values and angles. The x values define the angles at which the data points are plotted. The y value defines the distance of the data points from the center of the graph, with the center of the graph usually starting at 0. You can customize the series color and border****using **fill** and **border** properties in series. You can use **isClosed** property in series to specify whether the series drawn is in closed form. It supports three types of rendering such as **Line, Area and Column**.

**LineType**

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img28.png" Caption="Line Polar Chart"%}

**Area Type**

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img29.png" Caption="Area Polar Chart"%}

**Column Type**

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img30.png" Caption="Column Polar Chart"%}

To create a simple **Polar series** use the following code example.

{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                points: [
                         { x: '1990', y: 10 }, { x: '1991', y: 3 },
                         { x: '1992', y: 20 }, { x: '1993', y: 16 },
                         { x: '1994', y: 10 }, { x: '1995', y: 18 },
                         { x: '1996', y: 16 }, { x: '1997', y: 15 }
                ],
                name: 'India', enableAnimation: true, width: 3
            }
            ],
        }); 


{% endhighlight %}

## RadarSeries 

**RadarSeries** is a x, y Chart of three or more quantitative variables represented on multiple axis lines originating from the same point. You can customize the series color and border****using **fill** and **border** properties in series. You can use **isClosed** property in series to specify whether the series drawn is in closed form. It supports three types of rendering such as **Line, Area and Column**.

**Area Type**

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img31.png" Caption="Area RadarSeries"%}

**Line type**

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img32.png" Caption="Line RadarSeries"%}

**Column type**

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Types_images/Chart-Types_img33.png" Caption="Column RadarSeries"%}

To create simple **RadarSeries** use the following code example.

{% highlight js %}


        $("#chartcontainer").ejChart({
            series: [{
                points: [
                    { x: '1990', y: 10 }, { x: '1991', y: 3 },
                { x: '1992', y: 20 },
                { x: '1993', y: 16 }, { x: '1994', y: 10 },
                 { x: '1995', y: 18 },
                { x: '1996', y: 16 }, { x: '1997', y: 15 }
                ],
                name: 'India', enableAnimation: true, type: 'radar',
                border: { width: 2, color: 'black' }, drawType: 'area'
            }
            ],
        }); 


{% endhighlight %}



