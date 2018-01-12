---
layout: post
title: Basic-Settings
description: basic settings
platform: js
control: Linear Gauge
documentation: ug
api: /api/js/ejlineargauge
---

# Basic Settings

## Adding Dimension

* The basic customization for any control is setting the dimension. Here dimension refers the two major attributes, [`height`](../api/ejlineargauge#members:height) and [`width`](../api/ejlineargauge#members:width). The height and width assigned in the control will render the canvas element in the given size. 

* The value attribute is used to set all pointer value in the Linear Gauge control. The attributes, [`minimum`](../api/ejlineargauge#members:minimum) and [`maximum`](../api/ejlineargauge#members:maximum) value are used to set the minimum value and maximum value for all the scales exist in the Linear Gauge control.


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

   $(function () {
        // For Linear Gauge rendering
        $("#LinearGauge1").ejLinearGauge({
            // For setting linear gauge width
            width: 300,
            // For setting linear gauge height
            height: 500,
            // For setting linear gauge minimum value
            minimum: 10,
            // For setting linear gauge maximum value
            maximum: 110,
            // For setting linear gauge pointer value
            value: 78,
            // Adding scale collection
            scales: [{
                border: { color: "transparent", width: 0 },
                showMarkerPointers: false, showBarPointers: true,
                // Adding bar pointer collection
                barPointers: [{ width: 5, backgroundColor: "Grey" }],
                // Adding ticks collection
                ticks: [{
                    type: "majorinterval", width: 2,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                },
                {
                    type: "minorinterval", width: 1, height: 6,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                }]
            }]
        });
    });


{% endhighlight %}



Execute the above code to render the following output.



![](/js/LinearGauge/Basic-Settings_images/Basic-Settings_img1.png)



## Adding frame

* Frame is the element that decides the appearance of the **Linear Gauge**. You can customize it by using the object called **frame.** It contains frame inner width, frame outer width and frame background image URL properties. 

* The [`innerWidth`](../api/ejlineargauge#members:frame-innerwidth) of the [`frame`](../api/ejlineargauge#members:frame) defines the distance between the canvas element and the frame and the [`outerWidth`](../api/ejlineargauge#members:frame-outerwidth) refers to distance from the frame. [`backgroundImageUrl`](../api/ejlineargauge#members:frame-backgroundimageurl) is used to set the background image for the frame.


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
        // For Linear Gauge rendering
        $("#LinearGauge1").ejLinearGauge({
            value: 80,
            frame: {
                // For setting frame inner width
                innerWidth: 8,
                // For setting frame outer width
                outerWidth: 10,
                // For setting back ground Image URL
                backgroundImageUrl: "../images/gauge/Gauge_linear_light.png"
            },
            // Adding scale collection               
            scales: [{
                backgroundColor: "transparent",
                border: { color: "transparent", width: 0 },
                showMarkerPointers: false, showBarPointers: true,
                // Adding bar pointer collection
                barPointers: [{ width: 5, backgroundColor: "Grey" }],
                // Adding ticks collection
                ticks: [{
                    type: "majorinterval", width: 2,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                },
                {
                    type: "minorinterval", width: 1, height: 6,
                    color: "#8c8c8c", distanceFromScale: { x: 7, y: 0 }
                }]
            }]
        });
    });


{% endhighlight %}



Execute the above code to render the following output.



![](/js/LinearGauge/Basic-Settings_images/Basic-Settings_img2.png)



## Appearance

* The attribute [`orientation`](../api/ejlineargauge#members:orientation) is used to render the Linear Gauges either in horizontal position or vertical position.You can set the background color for the Linear Gauge for better appearance using the [`backgroundColor`](../api/ejlineargauge#members:backgroundcolor) property. borderColor specifies the [`borderColor`](../api/ejlineargauge#members:bordercolor) of the Linear Gauge. You can also add gradient effects to Linear Gauge with the help of pointerGradient1 and pointerGradient2 attribute.

* Theme is the basic property of any control. It is used to set the [`theme`](../api/ejlineargauge#members:theme) for Linear Gauge. There are two types of themes used for Linear Gauge such as

 * flatlight

 * flatdark


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 
     $(function () {
        // For Linear Gauge rendering
        $("#LinearGauge1").ejLinearGauge({
            enableAnimation: false,
            width: 400,
            height: 100,
            value: 80,
            // For setting theme
            theme: "flatlight",
            // For setting Orientation
            orientation: "Horizontal",
            // For setting label color
            labelColor: "Black",
            //For Adding Frame
            frame: {
                backgroundImageUrl: "../images/gauge/Gauge_linear_light1.png"
            },
            //For Adding Scales              
            scales: [{
                backgroundColor: "transparent",
                direction: ej.datavisualization.LinearGauge.Directions.Clockwise,
                border: { color: "transparent", width: 0 },
                showMarkerPointers: false, showBarPointers: true,
                //For Adding bar pointers
                barPointers: [{ width: 5, backgroundColor: "Grey" }],
                //For Adding label pointers
                labels: [{ angle: 90, distanceFromScale: { x: 5, y: -5 } }],
                //For Adding ticks
                ticks: [{
                    type: "majorinterval", width: 2,
                    color: "#8c8c8c", distanceFromScale: { x: 0, y: 0 }
                },
                {
                    type: "minorinterval", width: 1, height: 6,
                    color: "#8c8c8c", distanceFromScale: { x: 0, y: 0 }
                }]
            }]
        });
    });


{% endhighlight %}



Execute the above code to render the following output.

![](/js/LinearGauge/Basic-Settings_images/Basic-Settings_img3.png)



## Responsive 

* For any display devices, the control is to be rendered based on the space in that device. The control must be responsive. For this purpose resizing property is present in **Linear Gauge** control. 

* The **Linear Gauge** renders with the specified value. When the browser changes its size, the canvas element checks the dimension with its parent element and if there are any changes in parent dimension, gauge control also changes the dimension based on its parent changes. You can enable this feature using [`isResponsive`](../api/ejlineargauge#members:isresponsive) property**.**


{% highlight html %}

<div id="LinearGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

  $(function () {
        // For Linear Gauge rendering
        $("#LinearGauge1").ejLinearGauge({
            enableAnimation: false,
            width: 400,
            height: 100,
            value: 80,
            orientation: "Horizontal",
            labelColor: "Black",
            //For enabling responsible layout
            isResponsive: true,
            //For Adding Frame
            frame: {
                backgroundImageUrl: "../images/gauge/Gauge_linear_light1.png"
            },
            //For Adding Scale             
            scales: [{
                backgroundColor: "transparent",
                direction: ej.datavisualization.LinearGauge.Directions.Clockwise,
                border: { color: "transparent", width: 0 },
                showMarkerPointers: false, showBarPointers: true,
                //For Adding bar pointer collection             
                barPointers: [{ width: 5, backgroundColor: "Grey" }],
                //For Adding label collection             
                labels: [{ angle: 90, distanceFromScale: { x: 5, y: -5 } }],
                //For Adding tick collection             
                ticks: [{
                    type: "majorinterval", width: 2,
                    color: "#8c8c8c", distanceFromScale: { x: 0, y: 0 }
                },
               {
                   type: "minorinterval", width: 1, height: 6,
                   color: "#8c8c8c", distanceFromScale: { x: 0, y: 0 }
               }]
            }]
        });
    });


{% endhighlight %}



Execute the above code to render the following output.


![](/js/LinearGauge/Basic-Settings_images/Basic-Settings_img4.png)


Responsiveness of the linear gauge is controlled by using [`enableResize`](../api/ejlineargauge#members:enableresize) property.

{% highlight javascript %}

<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ enableResize: true });   
</script>

{% endhighlight %}

## Localization

**LinearGauge** supports localization for its axis labels and tooltip. To render the gauge with specific culture you have to refer the corresponding globalize culture script and need to specify the culture name in [`locale`](../api/ejlineargauge#members:locale) property of gauge.

**Enable Group Separator** is used to Convert the date object to string while using the locale settings, you can set [`enableGroupSeparator`](../api/ejlineargauge#members:enablegroupseparator) property as **true**.

{% highlight javascript %}

<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ 
            locale : "en-US" ,
            enableGroupSeparator: true
            }); 
</script>

{% endhighlight %}



