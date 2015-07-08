---
layout: post
title: 3D-Chart
description: 3d chart
platform: js
control: Chart
documentation: ug
---

# 3D Chart

Now EJChart allows you to create stunning 3D Charts for Bar, Column, StackingBar, StackingColumn, 100%StackedColumn, 100%StackedBar, Pie and Doughnut series. The representation of data in 3D Chart is very clear and easy to understand when compared to 2D charts. Three dimensions of the series are seen by rotating them. The following properties enhance the perception of 3D Charts.

* `enable3D`-The property [`enable3D`](/js/api/ejchart#enable3dspan-classtype-signature-type-booleanbooleanspan "enable3D") renders 3D Charts and accepts only the `Boolean` values.
* `wallSize`-In 3D, Cartesian axes lines are represented as walls. The property [`wallSize`](/js/api/ejchart#wallsizespan-classtype-signature-type-numbernumberspan "wallSize") defines the width of the wall. The [`wallSize`](/js/api/ejchart#wallsizespan-classtype-signature-type-numbernumberspan "wallSize") property does not support for 3D Pie or Doughnut series because they do not have Cartesian axes lines.
* `depth`-The [`depth`](/js/api/ejchart#depthspan-classtype-signature-type-numbernumberspan "depth") property defines the depth of the 3D Chart from front view of the series to wall.
* `tilt`-The [`tilt`](/js/api/ejchart#titlespan-classtype-signature-type-objectobjectspan "tilt") property defines the angle of the slope of 3D Chart. The positive and negative values declare the side where the slope is present.
* `rotation`-The [`rotation`](/js/api/ejchart#rotationspan-classtype-signature-type-numbernumberspan "rotation") property is used to spin the 3D chart. The direction of the spin depends upon the positive and negative values of [`rotation`](/js/api/ejchart#rotationspan-classtype-signature-type-numbernumberspan "rotation") property.
* `enableRotation`-The [`enableRotation`](/js/api/ejchart#enablerotationspan-classtype-signature-type-booleanbooleanspan "enableRotation") property allows rotation of the 3D Chart dynamically by dragging the mouse on 3D Chart. Accepting value of this property is `Boolean`.
* `perspectiveAngle`-The [`perspectiveAngle`](/js/api/ejchart#perspectiveanglespan-classtype-signature-type-numbernumberspan "perspectiveAngle") declares the appearance of the height, width, depth and wall of the 3D Chart. When the [`perspectiveAngle`](/js/api/ejchart#perspectiveanglespan-classtype-signature-type-numbernumberspan "perspectiveAngle") is decreased, the 3D object appears closer to viewer. But when it is increased, the 3D object appears far away from the viewer.
* `sideBySideSeriesPlacement`-The [`sideBySideSeriesPlacement`](/js/api/ejchart#sidebysideseriesplacementspan-classtype-signature-type-booleanbooleanspan "sideBySideSeriesPlacement") property defines the appearance of the different sets of data on 3D Chart. When it is set to `true`, the data is displayed side by side, otherwise it is displayed one by one.

## 3D Series Types

The following are 3D series types:

### 3D Column Chart

`Column charts` represent data in a vertical rectangular shape. The size of the shape depends upon the data. Different sets of data are compared by using `column chart`. The comparison is easy when it is set in 3 Dimensional view. Now EJChart gives its support for 3D by setting the property [`enable3D`](/js/api/ejchart#enable3dspan-classtype-signature-type-booleanbooleanspan "enable3D") to `true`. For clear perception, rotate the `3D column chart` to 360 degrees by giving the value as `true` for [`enableRotation`](/js/api/ejchart#enablerotationspan-classtype-signature-type-booleanbooleanspan "enableRotation") property. The depth, wall size, tilt, and rotation of the 3D chart are customized by setting the property [`depth`](/js/api/ejchart#depthspan-classtype-signature-type-numbernumberspan "depth"), [`wallSize`](/js/api/ejchart#wallsizespan-classtype-signature-type-numbernumberspan "wallSize"), [`tilt`](/js/api/ejchart#titlespan-classtype-signature-type-objectobjectspan "tilt"), and [`rotation`](/js/api/ejchart#rotationspan-classtype-signature-type-numbernumberspan "rotation") respectively.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
            depth: 100,
            wallSize: 2,
            tilt: 0,
            rotation: 34,
            perspectiveAngle: 90,
            enableRotation: true,
            enable3D: true,
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/3D-Chart_images/3D-Chart_img1.png" %}

### 3D Bar Chart

`3D Bar charts` are similar to `3D Column charts`, but it represents the data in horizontal rectangular shape. The size of the bar depends upon the data. You can customize the depth, wall size, tilt, and rotation of the `3D Bar chart` by setting the property [`depth`](/js/api/ejchart#depthspan-classtype-signature-type-numbernumberspan "depth"), [`wallSize`](/js/api/ejchart#wallsizespan-classtype-signature-type-numbernumberspan "wallSize"), [`tilt`](/js/api/ejchart#titlespan-classtype-signature-type-objectobjectspan "tilt"), and [`rotation`](/js/api/ejchart#rotationspan-classtype-signature-type-numbernumberspan "rotation") respectively.

{% highlight js %}

        $("#chartcontainer").ejChart({
            commonSeriesOptions: { type: "bar" },
            // ...             
            depth: 100,
            wallSize: 2,
            tilt: 0,
            rotation: 34,
            perspectiveAngle: 90,
            enableRotation: true,
            enable3D: true,
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/3D-Chart_images/3D-Chart_img2.png" %}

### 3D Stacking Column Chart

`3D Stacking Column Charts` are similar to `3D Column Charts`, but here the Y values of different sets of data are represented in a single vertical bar. You can set different colors and borders for different y values in a single vertical bar by setting the [`fill`](/js/api/ejchart#seriesfillspan-classtype-signature-type-stringstringspan "fill") and [`border`](/js/api/ejchart#seriesborderspan-classtype-signature-type-objectobjectspan "border") properties. You can customize the depth, wall size, tilt, and rotation of the `3D Stacking Column Chart` by setting [`depth`](/js/api/ejchart#depthspan-classtype-signature-type-numbernumberspan "depth"), [`wallSize`](/js/api/ejchart#wallsizespan-classtype-signature-type-numbernumberspan "wallSize"), [`tilt`](/js/api/ejchart#titlespan-classtype-signature-type-objectobjectspan "tilt"), and [`rotation`](/js/api/ejchart#rotationspan-classtype-signature-type-numbernumberspan "rotation") respectively.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...   
            series: [{
                points: [{ x: 2006, y: 8 }, { x: 2007, y: 5 },
                    { x: 2008, y: 4 }, { x: 2009, y: 12 },
                    { x: 2010, y: 16 }, { x: 2011, y: 6 },
                    { x: 2012, y: 13 }],
                name: "Google", type: 'stackingcolumn'
            },
            {
                points: [{ x: 2006, y: 5 }, { x: 2007, y: 6 },
                    { x: 2008, y: 7 }, { x: 2009, y: 10 },
                    { x: 2010, y: 14 }, { x: 2011, y: 14 },
                    { x: 2012, y: 15 }],
                name: "Bing", type: 'stackingcolumn'
            }
            ],
            depth: 100,
            wallSize: 2,
            tilt: 0,
            rotation: 34,
            perspectiveAngle: 90,
            enableRotation: true,
            enable3D: true,
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/3D-Chart_images/3D-Chart_img3.png" %}

### 3D Stacking Bar Chart

`3D Stacking Bar Charts` are similar to `3D Bar Charts`, but here the Y values of different sets of data are represented in a single horizontal bar. So the comparison of different sets of data is easier than the normal bar chart. You can customize the depth, wall size, tilt, and rotation of the `3D Stacking Bar Chart` by setting the property [`depth`](/js/api/ejchart#depthspan-classtype-signature-type-numbernumberspan "depth"), [`wallSize`](/js/api/ejchart#wallsizespan-classtype-signature-type-numbernumberspan "wallSize"), [`tilt`](/js/api/ejchart#titlespan-classtype-signature-type-objectobjectspan "tilt"), and [`rotation`](/js/api/ejchart#rotationspan-classtype-signature-type-numbernumberspan "rotation") respectively.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ... 
            series: [{
                points: [{ x: 2009, y: 2.9 }, { x: 2010, y: 3.8 },
                    { x: 2011, y: 4.9 }, { x: 2012, y: 6.5 },
                    { x: 2013, y: 7.1 }, { x: 2014, y: 7.5 }],
                name: "Desktop Display", type: 'stackingbar'
            },
            {
                points: [{ x: 2009, y: 0.1 }, { x: 2010, y: 0.5 },
                    { x: 2011, y: 1.4 }, { x: 2012, y: 2.9 },
                    { x: 2013, y: 4.9 }, { x: 2014, y: 6.8 }],
                name: "Mobile", type: 'stackingbar'
            }],
            depth: 100,
            wallSize: 2,
            tilt: 0,
            rotation: 34,
            perspectiveAngle: 90,
            enableRotation: true,
            enable3D: true,
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/3D-Chart_images/3D-Chart_img4.png" %}

### 3D Pie Chart

`Pie Charts` are circular with several segments. The segments are calculated from the `y` value of the series. Normally, in 2D only the front view of the `pie chart` can be seen. In 3D, there is an option to see the whole side of the `pie chart` by enabling the [`enableRotation`](/js/api/ejchart#enablerotationspan-classtype-signature-type-booleanbooleanspan "enableRotation") property. You can explode a particular segment of pie series by setting the [`explodeIndex`](/js/api/ejchart#seriesexplodeindexspan-classtype-signature-type-numbernumberspan "explodeIndex") property. You can customize the color of each segment by setting the `fill` property, and can also customize the depth, perspective angle, rotation, tilt of the pie chart by setting the appropriate properties.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...  
            series: [{
                points: [{ x: "Housing", y: 31 }, { x: "Food", y: 16 },
                         { x: "Transportation", y: 14 }, { x: "Clothing", y: 6 },
                         { x: "Health care", y: 8 }, { x: "Education", y: 17 },
                         { x: "Miscellaneous", y: 8 }],
                explodeIndex: 1,
                border: { width: 2, color: 'white' },
                type: 'pie', startAngle: 145
            }],
            depth: 30,
            wallSize: 10,
            tilt: -30,
            rotation: -30,
            perspectiveAngle: 90,
            enableRotation: true,
            enable3D: true,
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/3D-Chart_images/3D-Chart_img5.png" %}

### 3D Doughnut Chart

`3D Doughnut charts` are similar to `3D Pie Charts*` with the difference of having a hole in the center of the `Doughnut chart`. The size of the hole is customized by using the [`doughnutCoefficient`](/js/api/ejchart#seriesdoughnutcoefficientspan-classtype-signature-type-numbernumberspan "doughnutCoefficient") property. The size of the `doughnut` is customized by using the [`doughnutSize`](/js/api/ejchart#seriesdoughnutsizespan-classtype-signature-type-numbernumberspan "doughnutSize") property. You can rotate the `3D doughnut chart` to 360 degrees by enabling the [`enableRotation`](/js/api/ejchart#enablerotationspan-classtype-signature-type-booleanbooleanspan "enableRotation") property. You can customize each segment’s color and border by setting `fill` and `border` property.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...  
            series: [{
                points: [{ x: "Watching TV", y: 56 }, { x: "Socializing", y: 26 },
                         { x: "Reading", y: 3 }, { x: "Sports", y: 7 },
                         { x: "Others", y: 8 }],
                explodeIndex: 1,
                doughnutCoefficient: 0.5, doughnutSize: 0.8,
                type: 'doughnut', startAngle: 145
            }],
            depth: 30,
            wallSize: 10,
            tilt: -30,
            rotation: -30,
            perspectiveAngle: 90,
            enableRotation: true,
            enable3D: true,
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/3D-Chart_images/3D-Chart_img6.png" %}

### 100% 3D Stacking Column

`100% 3D Stacking Column` charts are similar to `3D stacking Column` charts. But here, the combined contribution of Y values is the combined total of the vertical bar with 100 percent. You can customize the depth, wall size, tilt and rotate the `100% 3D Stacking Column` by using the [`depth`](/js/api/ejchart#depthspan-classtype-signature-type-numbernumberspan "depth"), [`wallSize`](/js/api/ejchart#wallsizespan-classtype-signature-type-numbernumberspan "wallSize"), [`tilt`](/js/api/ejchart#titlespan-classtype-signature-type-objectobjectspan "tilt"), and [`rotation`](/js/api/ejchart#rotationspan-classtype-signature-type-numbernumberspan "rotation") properties respectively.

{% highlight js %}

        $("#chartcontainer").ejChart({
            commonSeriesOptions:
            {
                type: 'stackingcolumn100'
            },
            series:
            [
               {
                   points: [{ x: 2006, y: 80000 }, { x: 2007, y: 22000 },
                            { x: 2008, y: 60000 }, { x: 2009, y: 39000 },
                            { x: 2010, y: 62000 }, { x: 2011, y: 90000 }
                   ],
                   name: "Australia"
               },
               {
                   points: [{ x: 2006, y: 50000 }, { x: 2007, y: 41000 },
                            { x: 2008, y: 52000 }, { x: 2009, y: 43000 },
                            { x: 2010, y: 47000 }, { x: 2011, y: 93000 }
                   ],
                   name: "China"
               }
            ],
            enable3D: true,
        });


{% endhighlight %}



The following screenshot displays the **100% 3D Stacking Column.**

{% include image.html url="/js/Chart/3D-Chart_images/3D-Chart_img7.png" %}

### 100% 3D Stacking Bar

`100% 3D Stacking Bar charts` are similar to 3D stacking Bar charts. But here, the combined contribution of Y values is the combined total of the horizontal bar with 100 percent. You can customize the depth, wall size, tilt and rotate the `100% 3D Stacking Bar` by using the [`depth`](/js/api/ejchart#depthspan-classtype-signature-type-numbernumberspan "depth"), [`wallSize`](/js/api/ejchart#wallsizespan-classtype-signature-type-numbernumberspan "wallSize"), [`tilt`](/js/api/ejchart#titlespan-classtype-signature-type-objectobjectspan "tilt"), and [`rotation`](/js/api/ejchart#rotationspan-classtype-signature-type-numbernumberspan "rotation") properties respectively..

{% highlight js %}

        $("#chartcontainer").ejChart({
            commonSeriesOptions:
            {
                type: 'stackingbar100'
            },
            series:
            [
               {
                   points: [{ x: 2006, y: 8000 }, { x: 2007, y: 1200 },
                            { x: 2008, y: 20000 }, { x: 2009, y: 21000 },
                            { x: 2010, y: 28000 }, { x: 2011, y: 29000 }
                   ],
                   name: "Brazil"
               },
               {
                   points: [{ x: 2006, y: 5000 }, { x: 2007, y: 15000 },
                            { x: 2008, y: 19000 }, { x: 2009, y: 25000 },
                            { x: 2010, y: 26000 }, { x: 2011, y: 30000 }
                   ],
                   name: "Nigeria"
               }
            ],
            enable3D: true,
        });


{% endhighlight %}



The following screenshot displays the `100% 3D Stacking Bar`.

{% include image.html url="/js/Chart/3D-Chart_images/3D-Chart_img8.png" %}

