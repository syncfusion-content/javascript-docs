---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Circular Gauge
documentation: ug
---

# Getting Started

This section encompasses how to configure **Circular Gauge**. You can provide data to a **Circular Gauge** and make them to display  in a required way. 

The following screen shot displays a **Circular Gauge**, which visually represents the functions of an Automobile speedometer with RPM (Rotation per Minute), KmpH (Kilometer per hour) and it denotes the speed level indicators (Safe, Caution and Danger). 

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img1.png" Caption="Speedometer Gauge"%}

1. First create an **HTML** file and add references to the required libraries.

{% highlight js %}

**[HTML]**
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta charset="utf-8" />
<link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<!--scripts-->
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.js"></script>
<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js">                                                               </script>
</head>



{% endhighlight %}



2. Add a div element that acts as a container for **ejCircularGauge** widget.

{% highlight js %}

**[HTML]**

<body>
<div id="CircularGauge1"></div>
</body>



{% endhighlight %}



3. Create the **ejCircularGauge** widget as follows,

{% highlight js %}

**[HTML]**

<script type="text/javascript">
$(function () {
$("#CircularGauge1").ejCircularGauge();
});
</script>
</html>


{% endhighlight %}



On executing the above code, sample renders a default **Circular Gauge** with default values as follows.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img2.png" Caption="Circular Gauge"%}

**Set Height and Width values**

Pointers have different height and range. You can set the height and width of the gauge.

{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
});


{% endhighlight %}



The following screenshot displays a **Gauge** in which height and width are set.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img3.png" Caption="Circular Gauge"%}

**Set Background Color**

You can draw the speedometer with dark background and to vary the speed of the pointer, set the **readOnly** option as **False** for user interaction. 

{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,
});


{% endhighlight %}



The above code example renders a **Gauge** as shown in the following screen shot.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img4.png" Caption="Circular Gauge with background color"%}

**Provide scale values**

You can customize the pointer cap using the following options- Cap radius, Cap border color, cap background color, pointer cap border width. 

Set the maximum speed limit in the **Gauge** as 200KmpH.

Major Ticks and Minor Ticks have the interval values 20 and 5 respectively. Show ranges and show indicators are used to display the ranges and indicators in their respective positions.

{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
showRanges: true,
showIndicators: true,
pointerCap: {
radius: 15,
borderWidth: 0,
backgroundColor: "#797C79",
borderColor: "#797C79"
},
maximum: 200,
majorIntervalValue: 20,
minorIntervalValue: 5,
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here
}]
});


{% endhighlight %}



On executing the above code, sample renders a **Circular Gauge** with customized labels as follows.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img5.png" Caption="Circular Gauge with scale values"%}

**Add Label Customization**

To display the values in the **Gauge,** scale labels are used. You can customize the label color.  

{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,
scales: [{
//Add the labels customization code here

labels: [{
color: "#ffffff"
}],
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here

}]
});



{% endhighlight %}



On executing the above code, sample renders a default **Circular Gauge** with customized labels as follows.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img6.png" Caption="Circular Gauge with Labels"%}

**Add pointer data**

You can use three pointers that denote kilometer value, rotation per minute value and torque value.The torque value pointer should not be similar to other two pointers. Set the torque pointer as marker pointer. You can set other attributes for pointer such as background color, border color, Length, width and distance from scale.

{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
//Add the labels customization code here
//Add the pointers customization code here

pointers: [{
value: 140,
distanceFromScale: 60,
showBackNeedle: false,
length: 20,
type: "marker",
markerType: "triangle",
width: 10,
radius: 10,
backgroundColor: "#FF940A",
border: {
color: "#FF940A"
},
},
{
value: 110,
showBackNeedle: false,
length: 150,
width: 2,
radius: 10,
needleType: "rectangle",
backgroundColor: "#05AFFF",
border: {
color: "#05AFFF"
},                }, {
value: 67,
showBackNeedle: false,
length: 100,
width: 15,
radius: 10,
backgroundColor: "#FC5D07",
border: {
color: "#FC5D07"
},

}],
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here

}]
});


{% endhighlight %}



On executing the above code, sample renders a customized **Circular Gauge** as follows.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img7.png" Caption="Circular Gauge with Pointer"%}

**Add Tick Details**

You can display the tick value with customization as given in the following code example. You can set width and height of the Major ticks greater than the Minor ticks. You can set dark background for tick Color to have a better visibility.

{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,
scales: [{
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here

ticks: [{
type: "major",
distanceFromScale: 70,
height: 20,
width: 3,
color: "#ffffff"
}, {
type: "minor",
height: 12,
width: 1,
distanceFromScale: 70,
color: "#ffffff"
}],
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here

}]
});




{% endhighlight %}



On executing the above code, sample renders a **Circular Gauge** with customized labels as follows.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img8.png" Caption="Circular Gauge with Tick details"%}

**Add Range Values**

Ranges denote the property of scale value in the speedometer. The color values of the ranges specify the speed variation. Set **showRanges** property to **“True”** to show the ranges in the **Circular Gauge**. Select safe zone for low speed, caution zone for moderate speed and high zone for high speed.You can customize the range with the properties such as start value, end value, start width, end width,  background color , border color, etc.,

{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here

ranges: [{
distanceFromScale: 30,
startValue: 0,
endValue: 70,
backgroundColor: "#5DF243",
border: {
color: "#FFFFFF"
},
}, {
distanceFromScale: 30,
startValue: 70,
endValue: 140,
backgroundColor: "#F6FF0A",
border: {
color: "#FFFFFF"
},                },
{
distanceFromScale: 30,
startValue: 140,
endValue: 200,
backgroundColor: "#FF1807",
border: {
color: "#FFFFFF"
},
}],
//Add the indicators customization code here
//Add the Custom labels customization code here

}]
});


{% endhighlight %}



On executing the above code, sample renders a **Circular Gauge** with customized range as follows.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img9.png" Caption="Circular Gauge with range values"%}

**Add Indicator Details**

Indicators denote whether the pointer values are placed in their respective zones. You can position the indicator on the respective range value for the required changes. You can set the location of the indicator using **position** property. The **stateRanges** property defines how the indicator should behave when the pointer is in certain values. 

{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here

indicators: [
{
height: 10,
width: 10,
type: "circle",
position: { x: 210, y: 300 },
stateRanges: [{
endValue: 70,
startValue: 0,
backgroundColor: "#5DF243",
borderColor: "#5DF243",
text: "",
textColor: "#870505"
}, {
endValue: 200,
startValue: 70,
backgroundColor: "#145608",
borderColor: "#145608",
text: "",
textColor: "#870505"
}]
},
{
height: 10,
width: 10,
type: "circle",
position: { x: 255, y: 200 },
stateRanges: [{
endValue: 140,
startValue: 70,
backgroundColor: "#F6FF0A",
borderColor: "#F6FF0A",
text: "",
}, {
endValue: 70,
startValue: 0,
backgroundColor: "#969B0C",
borderColor: "#969B0C",
text: "",
}, {
endValue: 200,
startValue: 140,
backgroundColor: "#969B0C",
borderColor: "#969B0C",
text: "",
}]
}, {
height: 10,
width: 10,
type: "circle",
position: { x: 300, y: 300 },
stateRanges: [{
endValue: 140,
startValue: 0,
backgroundColor: "#890F06",
borderColor: "#890F06",
text: "",
},
{
endValue: 200,
startValue: 140,
backgroundColor: "#FF1807",
borderColor: "#FF1807",
text: "",
}]
}],
//Add the Custom labels customization code here

}]});


{% endhighlight %}



On executing the above code, sample renders a **Circular Gauge** with customized indicators as follows.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img10.png" Caption="Circular Gauge with Customized Indicators"%}

**Add Custom Label Details**

You can specify the text in the **Gauge** using **Custom labels** and you can customize it through various properties. You can use custom texts to display the three range description.

{% highlight js %}


$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here

customLabels: [{
value: "Safe",
position: { x: 200, y: 280 },
color: "#5DF243",
font:
{
size: "12px",
fontFamily: "Arial",
fontStyle: "Bold"
}
}, {
value: "Caution",
position: { x: 253, y: 212 },
color: "#F6FF0A",
font:
{
size: "12px",
fontFamily: "Arial",
fontStyle: "Bold"
}
}, {
value: "Danger",
position: { x: 290, y: 280 },
color: "#FF1807",
font:
{
size: "12px",
fontFamily: "Arial",
fontStyle: "Bold"
}
}]}]});


{% endhighlight %}



The following screenshot displays a **Circular Gauge** control with all customization properties.

{% include image.html url="/js/CircularGauge/Getting-Started_images/Getting-Started_img11.png" Caption="Circular Gauge with Custom Label details"%}

