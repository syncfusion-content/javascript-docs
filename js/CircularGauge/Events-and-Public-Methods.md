---
layout: post
title: Events-and-Public-Methods
description: events and public methods
platform: js
control: Circular Gauge
documentation: ug
api: /api/js/ejcirculargauge
---

# Methods and Events

## Public Methods

### Destroying the Circular Gauge

The [`destroy`](../api/ejcirculargauge#methods:destroy) method is used to destroy the **CircularGauge** widget. All events bound using this._on will be unbind automatically and bring the control to pre-init state.

{% highlight html %}

<div id="CoreCircularGauge"></div> 

<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.destroy();
</script>

{% endhighlight %}

### Getting Back Needle Length

The [`getBackNeedleLength`](../api/ejcirculargauge#methods:getbackneedlelength) method is used to get the needle length of **CircularGauge**.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true }] }] });
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getBackNeedleLength(0, 0);
</script>

{% endhighlight %}

### Getting Custom Label Angle

The [`getCustomLabelAngle`](../api/ejcirculargauge#methods:getcustomlabelangle) method is used to get the angle of custom label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
 
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{textAngle:30,value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getCustomLabelAngle(0, 0);
</script>

{% endhighlight %}

### Getting Custom Label value

The [`getCustomLabelValue`](../api/ejcirculargauge#methods:getcustomlabelvalue) method is used to get the value of custom label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{textAngle:30,value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getCustomLabelValue(0, 0);
</script>

{% endhighlight %}

### Getting Label Angle

The [`getLabelAngle`](../api/ejcirculargauge#methods:getlabelangle) method is used to get angle of label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getLabelAngle(0, 0);
</script>

{% endhighlight %}

### Getting Label Distance From Scale

The [`getLabelDistanceFromScale`](../api/ejcirculargauge#methods:getlabeldistancefromscale) method is used to get the distance value from scale for label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getLabelDistanceFromScale(0, 0);
</script>

{% endhighlight %}

### Getting Label Placement

The [`getLabelPlacement`](../api/ejcirculargauge#methods:getlabelplacement) method is used to get placement of label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getLabelPlacement(0, 0);
</script>

{% endhighlight %}

### Getting Label Style

The [`getLabelStyle`](../api/ejcirculargauge#methods:getlabelstyle) method is used to get style of label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getLabelStyle(0, 0);
</script>

{% endhighlight %}

### Getting Major Interval Value

The [`getMajorIntervalValue`](../api/ejcirculargauge#methods:getmajorintervalvalue) method is used to get major interval value of CircularGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getMajorIntervalValue(0);
</script>

{% endhighlight %}

### Getting Maker Distance From Scale

The [`getMarkerDistanceFromScale`](../api/ejcirculargauge#methods:getmarkerdistancefromscale) method is used to get distance from scale value of marker.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getMarkerDistanceFromScale(0);
</script>

{% endhighlight %}

### Getting Maker Style

The [`getMarkerStyle`](../api/ejcirculargauge#methods:getmarkerstyle) method is used to get distance from scale value of marker.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getMarkerStyle(0, 0);
</script>

{% endhighlight %}

### Getting Maximum Value

The [`getMaximumValue`](../api/ejcirculargauge#methods:getmaximumvalue) method is used to get maximum value of CircularGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getMaximumValue(0);
</script>

{% endhighlight %}

### Getting Minimum Value

The [`getMinimumValue`](../api/ejcirculargauge#methods:getminimumvalue) method is used to get minimum value of CircularGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getMinimumValue(0);
</script>

{% endhighlight %}

### Getting Minor Interval Value

The [`getMinorIntervalValue`](../api/ejcirculargauge#methods:getminorintervalvalue) method is used to get minor interval value of CircularGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getMinorIntervalValue(0);
</script>

{% endhighlight %}

### Getting Needle Style

The [`getNeedleStyle`](../api/ejcirculargauge#methods:getneedlestyle) method is used to get style of needle.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getNeedleStyle(0, 0);
</script>

{% endhighlight %}

### Getting Pointer Cap Border Width

The [`getPointerCapBorderWidth`](../api/ejcirculargauge#methods:getpointercapborderwidth) method is used to get border width of pointer cap.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getPointerCapBorderWidth(0);
</script>

{% endhighlight %}

### Getting Pointer Cap Radius

The [`getPointerCapRadius`](../api/ejcirculargauge#methods:getpointercapradius) method is used to get radius of pointer cap.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getPointerCapRadius(0);
</script>

{% endhighlight %}

### Getting Pointer Length

The [`getPointerLength`](../api/ejcirculargauge#methods:getpointerlength) method is used to get pointer length.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getPointerLength(0, 0);
</script>

{% endhighlight %}

### Getting Pointer Needle Type

The [`getPointerNeedleType`](../api/ejcirculargauge#methods:getpointerneedletype) method is used to get needle type of pointer.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getPointerNeedleType(0, 0);
</script>

{% endhighlight %}

### Getting Pointer Placement

The [`getPointerPlacement`](../api/ejcirculargauge#methods:getpointerplacement) method is used to get placement of pointer.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getPointerPlacement(0, 0);
</script>

{% endhighlight %}

### Getting Pointer Value

The [`getPointerValue`](../api/ejcirculargauge#methods:getpointervalue) method is used to get pointer value.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getPointerValue(0, 0);
</script>

{% endhighlight %}

### Getting Pointer Value

The [`getPointerWidth`](../api/ejcirculargauge#methods:getpointerwidth) method is used to get pointer width.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getPointerWidth(0, 0);
</script>

{% endhighlight %}

### Getting Range Border Width

The [`getRangeBorderWidth`](../api/ejcirculargauge#methods:getrangeborderwidth) method is used to get border width of range.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getRangeBorderWidth(0, 0);
</script>

{% endhighlight %}

### Getting Range Distance From Scale

The [`getRangeDistanceFromScale`](../api/ejcirculargauge#methods:getrangedistancefromscale) method is used to get range distance from scale.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getRangeDistanceFromScale(0, 0);
</script>

{% endhighlight %}

### Getting Range End Value

The [`getRangeEndValue`](../api/ejcirculargauge#methods:getrangeendvalue) method is used to get end value of range.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getRangeEndValue(0, 0);
</script>

{% endhighlight %}

### Getting Range Position

The [`getRangePosition`](../api/ejcirculargauge#methods:getrangeposition) method is used to get range position.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getRangePosition(0, 0);
</script>

{% endhighlight %}

### Getting Range Size

The [`getRangeSize`](../api/ejcirculargauge#methods:getrangesize) method is used to get range size.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getRangeSize(0, 0);
</script>

{% endhighlight %}

### Getting Range Start Value

The [`getRangeStartValue`](../api/ejcirculargauge#methods:getrangestartvalue) method is used to get range start value.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getRangeStartValue(0, 0);
</script>

{% endhighlight %}

### Getting Scale Bar Size

The [`getScaleBarSize`](../api/ejcirculargauge#methods:getscalebarsize) method is used to get scale bar size.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getScaleBarSize(0);
</script>

{% endhighlight %}

### Getting Scale Border Width

The [`getScaleBorderWidth`](../api/ejcirculargauge#methods:getscaleborderwidth) method is used to get border width of scale.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{Width: 1.5} }] });
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getScaleBorderWidth(0);
</script>

{% endhighlight %}

### Getting Scale Direction

The [`getScaleDirection`](../api/ejcirculargauge#methods:getscaledirection) method is used to get scale direction.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getScaleDirection(0);
</script>

{% endhighlight %}

### Getting Scale Radius

The [`getScaleRadius`](../api/ejcirculargauge#methods:getscaleradius) method is used to get scale radius.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getScaleRadius(0);
</script>

{% endhighlight %}

### Getting Start Angle

The [`getStartAngle`](../api/ejcirculargauge#methods:getstartangle) method is used to get start angle.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getStartAngle(0);
</script>

{% endhighlight %}

### Getting Sub Gauge Location

The [`getSubGaugeLocation`](../api/ejcirculargauge#methods:getsubgaugelocation) method is used to get location of subGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<div id="subGauge1"></div> 
 
<script>
    $("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
    $("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 150 }}]}]});
    circulargaugeObj.getSubGaugeLocation(0, 0);
</script>

{% endhighlight %}

### Getting Sweep Angle

The [`getSweepAngle`](../api/ejcirculargauge#methods:getsweepangle) method is used to get sweep angle.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getSweepAngle(0);
</script>

{% endhighlight %}

### Getting Tick Angle

The [`getTickAngle`](../api/ejcirculargauge#methods:gettickangle) method is used to get tick angle.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getTickAngle(0, 0);
</script>

{% endhighlight %}

### Getting Tick Distance From Scale

The [`getTickDistanceFromScale`](../api/ejcirculargauge#methods:gettickdistancefromscale) method is used to get tick distance from scale value.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getTickDistanceFromScale(0, 0);
</script>

{% endhighlight %}

### Getting Tick Height

The [`getTickHeight`](../api/ejcirculargauge#methods:gettickheight) method is used to get tick height.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getTickHeight(0, 0);
</script>

{% endhighlight %}

### Getting Tick Placement

The [`getTickPlacement`](../api/ejcirculargauge#methods:gettickplacement) method is used to get tick placement.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getTickPlacement(0, 0);
</script>

{% endhighlight %}

### Getting Tick Style

The [`getTickStyle`](../api/ejcirculargauge#methods:gettickstyle) method is used to get tick style.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getTickStyle(0, 0);
</script>

{% endhighlight %}

### Getting Tick Width

The [`getTickWidth`](../api/ejcirculargauge#methods:gettickwidth) method is used to get tick width.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.getTickWidth(0, 0);
</script>

{% endhighlight %}

### Setting IncludeFirstValue

The [`includeFirstValue`](../api/ejcirculargauge#methods:includefirstvalue) method is used to set includeFirstValue.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.includeFirstValue(0, 0, false);
</script>

{% endhighlight %}

### Redrawing Circular Gauge

The [`redraw`](../api/ejcirculargauge#methods:redraw) method is used to redraw the Circular Gauge widget.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.redraw("scale");
</script>

{% endhighlight %}

### Setting Back Needle Length

The [`setBackNeedleLength`](../api/ejcirculargauge#methods:setbackneedlelength) method is used to set the needle length of **CircularGauge**.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true }] }] });
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setBackNeedleLength(0, 0, 10);
</script>

{% endhighlight %}

### Setting Custom Label Angle

The [`setCustomLabelAngle`](../api/ejcirculargauge#methods:setcustomlabelangle) method is used to set the angle of custom label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
 
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font: { size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setCustomLabelAngle(0, 0, 10);
</script>

{% endhighlight %}

### Setting Custom Label value

The [`setCustomLabelValue`](../api/ejcirculargauge#methods:setcustomlabelvalue) method is used to set the value of custom label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{value:"MyLabel",position:{x:180,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setCustomLabelValue(0, 0, "CircularGauge");
</script>

{% endhighlight %}

### Setting Label Angle

The [`setLabelAngle`](../api/ejcirculargauge#methods:setlabelangle) method is used to set angle of label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setLabelAngle(0, 0, 10);
</script>

{% endhighlight %}

### Setting Label Distance From Scale

The [`setLabelDistanceFromScale`](../api/ejcirculargauge#methods:setlabeldistancefromscale) method is used to set the distance value from scale for label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setLabelDistanceFromScale(0, 0, 10);
</script>

{% endhighlight %}

### Setting Label Placement

The [`setLabelPlacement`](../api/ejcirculargauge#methods:setlabelplacement) method is used to set placement of label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setLabelPlacement(0, 0, 'far');
</script>

{% endhighlight %}

### Setting Label Style

The [`setLabelStyle`](../api/ejcirculargauge#methods:setlabelstyle) method is used to set style of label.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setLabelStyle(0, 0, 'major');
</script>

{% endhighlight %}

### Setting Major Interval Value

The [`setMajorIntervalValue`](../api/ejcirculargauge#methods:setmajorintervalvalue) method is used to set major interval value of CircularGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setMajorIntervalValue(0, 10);
</script>

{% endhighlight %}

### Setting Maker Distance From Scale

The [`setMarkerDistanceFromScale`](../api/ejcirculargauge#methods:setmarkerdistancefromscale) method is used to set distance from scale value of marker.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setMarkerDistanceFromScale(0, 10);
</script>

{% endhighlight %}

### Setting Maker Style

The [`setMarkerStyle`](../api/ejcirculargauge#methods:setmarkerstyle) method is used to set distance from scale value of marker.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setMarkerStyle(0, 0, 'rectangle');
</script>

{% endhighlight %}

### Setting Maximum Value

The [`setMaximumValue`](../api/ejcirculargauge#methods:setmaximumvalue) method is used to set maximum value of CircularGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setMaximumValue(0, 130);
</script>

{% endhighlight %}

### Setting Minimum Value

The [`setMinimumValue`](../api/ejcirculargauge#methods:setminimumvalue) method is used to set minimum value of CircularGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setMinimumValue(0, 10);
</script>

{% endhighlight %}

### Setting Minor Interval Value

The [`setMinorIntervalValue`](../api/ejcirculargauge#methods:setminorintervalvalue) method is used to set minor interval value of CircularGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setMinorIntervalValue(0, 2);
</script>

{% endhighlight %}

### Setting Needle Style

The [`setNeedleStyle`](../api/ejcirculargauge#methods:setneedlestyle) method is used to set style of needle.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setNeedleStyle(0, 0, 'arrow');
</script>

{% endhighlight %}

### Setting Pointer Cap Border Width

The [`setPointerCapBorderWidth`](../api/ejcirculargauge#methods:setpointercapborderwidth) method is used to set border width of pointer cap.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setPointerCapBorderWidth(0, 5);
</script>

{% endhighlight %}

### Setting Pointer Cap Radius

The [`setPointerCapRadius`](../api/ejcirculargauge#methods:setpointercapradius) method is used to set radius of pointer cap.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setPointerCapRadius(0, 10);
</script>

{% endhighlight %}

### Setting Pointer Length

The [`setPointerLength`](../api/ejcirculargauge#methods:setpointerlength) method is used to set pointer length.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setPointerLength(0, 0, 90);
</script>

{% endhighlight %}

### Setting Pointer Needle Type

The [`setPointerNeedleType`](../api/ejcirculargauge#methods:setpointerneedletype) method is used to set needle type of pointer.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setPointerNeedleType(0, 0, 'triangle');
</script>

{% endhighlight %}

### Setting Pointer Placement

The [`setPointerPlacement`](../api/ejcirculargauge#methods:setpointerplacement) method is used to set placement of pointer.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setPointerPlacement(0, 0,'near');
</script>

{% endhighlight %}

### Setting Pointer Value

The [`setPointerValue`](../api/ejcirculargauge#methods:setpointervalue) method is used to set pointer value.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setPointerValue(0, 0, 10);
</script>

{% endhighlight %}

### Setting Pointer Value

The [`setPointerWidth`](../api/ejcirculargauge#methods:setpointerwidth) method is used to set pointer width.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setPointerWidth(0, 0, 10);
</script>

{% endhighlight %}

### Setting Range Border Width

The [`setRangeBorderWidth`](../api/ejcirculargauge#methods:setrangeborderwidth) method is used to set border width of range.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setRangeBorderWidth(0, 0, 5);
</script>

{% endhighlight %}

### Setting Range Distance From Scale

The [`setRangeDistanceFromScale`](../api/ejcirculargauge#methods:setrangedistancefromscale) method is used to set range distance from scale.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setRangeDistanceFromScale(0, 0, 10);
</script>

{% endhighlight %}

### Setting Range End Value

The [`setRangeEndValue`](../api/ejcirculargauge#methods:setrangeendvalue) method is used to set end value of range.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setRangeEndValue(0, 0, 70);
</script>

{% endhighlight %}

### Setting Range Position

The [`setRangePosition`](../api/ejcirculargauge#methods:setrangeposition) method is used to set range position.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setRangePosition(0, 0, 'far');
</script>

{% endhighlight %}

### Setting Range Size

The [`setRangeSize`](../api/ejcirculargauge#methods:setrangesize) method is used to set range size.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setRangeSize(0, 0, 10);
</script>

{% endhighlight %}

### Setting Range Start Value

The [`setRangeStartValue`](../api/ejcirculargauge#methods:setrangestartvalue) method is used to set range start value.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setRangeStartValue(0, 0, 10);
</script>

{% endhighlight %}

### Setting Scale Bar Size

The [`setScaleBarSize`](../api/ejcirculargauge#methods:setscalebarsize) method is used to set scale bar size.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setScaleBarSize(0, 160);
</script>

{% endhighlight %}

### Setting Scale Border Width

The [`setScaleBorderWidth`](../api/ejcirculargauge#methods:setscaleborderwidth) method is used to set border width of scale.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{Width: 1.5} }] });
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setScaleBorderWidth(0, 3);
</script>

{% endhighlight %}

### Setting Scale Direction

The [`setScaleDirection`](../api/ejcirculargauge#methods:setscaledirection) method is used to set scale direction.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setScaleDirection(0, 'clockwise');
</script>

{% endhighlight %}

### Setting Scale Radius

The [`setScaleRadius`](../api/ejcirculargauge#methods:setscaleradius) method is used to set scale radius.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setScaleRadius(0, 140);
</script>

{% endhighlight %}

### Setting Start Angle

The [`setStartAngle`](../api/ejcirculargauge#methods:setstartangle) method is used to set start angle.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setStartAngle(0, 10);
</script>

{% endhighlight %}

### Setting Sub Gauge Location

The [`setSubGaugeLocation`](../api/ejcirculargauge#methods:setsubgaugelocation) method is used to set location of subGauge.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<div id="subGauge1"></div> 
 
<script>
    $("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
    $("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 150 }}]}]});
    circulargaugeObj.setSubGaugeLocation(0, 0, {x:50,y:100});
</script>

{% endhighlight %}

### Setting Sweep Angle

The [`setSweepAngle`](../api/ejcirculargauge#methods:setsweepangle) method is used to set sweep angle.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setSweepAngle(0, 220);
</script>

{% endhighlight %}

### Setting Tick Angle

The [`setTickAngle`](../api/ejcirculargauge#methods:settickangle) method is used to set tick angle.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setTickAngle(0, 0, 10);
</script>

{% endhighlight %}

### Setting Tick Distance From Scale

The [`setTickDistanceFromScale`](../api/ejcirculargauge#methods:settickdistancefromscale) method is used to set tick distance from scale value.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setTickDistanceFromScale(0, 0, 15);
</script>

{% endhighlight %}

### Setting Tick Height

The [`setTickHeight`](../api/ejcirculargauge#methods:settickheight) method is used to set tick height.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setTickHeight(0, 0, 10);
</script>

{% endhighlight %}

### Setting Tick Placement

The [`setTickPlacement`](../api/ejcirculargauge#methods:settickplacement) method is used to set tick placement.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setTickPlacement(0, 0, 'near');
</script>

{% endhighlight %}

### Setting Tick Style

The [`setTickStyle`](../api/ejcirculargauge#methods:settickstyle) method is used to set tick style.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setTickStyle(0, 0, 'minor');
</script>

{% endhighlight %}

### Setting Tick Width

The [`setTickWidth`](../api/ejcirculargauge#methods:settickwidth) method is used to set tick width.

{% highlight html %}

<div id="CoreCircularGauge"></div> 
  
<script>
    $("#CoreCircularGauge").ejCircularGauge();
    var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
    circulargaugeObj.setTickWidth(0, 0, 5);
</script>

{% endhighlight %}


## Events

### Draw Custom Label

The [`drawCustomLabel`](../api/ejcirculargauge#events:drawcustomlabel) event is triggered while custom labels are drawn on the gauge. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //draw custom label event
            drawCustomLabel: function(args){

            },

            //...
        });

{% endhighlight %}

### Draw Indicators

The [`drawIndicators`](../api/ejcirculargauge#events:drawindicators) event is triggered while indicators are being drawn on the gauge. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //draw indicators event
            drawIndicators: function(args){

            },

            //...
        });

{% endhighlight %}

### Draw Labels

The [`drawLabels`](../api/ejcirculargauge#events:drawlabels) event is triggered while labels are being drawn on the gauge. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //draw labels event
            drawLabels: function(args){

            },

            //...
        });

{% endhighlight %}

### Draw Pointer Cap

The [`drawPointerCap`](../api/ejcirculargauge#events:drawpointercap) event is triggered while pointer cap is being drawn on the gauge. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //draw pointer cap event
            drawPointerCap: function(args){

            },

            //...
        });

{% endhighlight %}

### Draw Pointers

The [`drawPointers`](../api/ejcirculargauge#events:drawpointers) event is triggered while pointer cap is being drawn on the gauge. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //draw pointer event
            drawPointers: function(args){

            },

            //...
        });

{% endhighlight %}

### Draw Range

The [`drawRange`](../api/ejcirculargauge#events:drawrange) event is triggered when ranges starts to be drawn on the gauge. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //draw range event
            drawRange: function(args){

            },

            //...
        });

{% endhighlight %}

### Draw Ticks

The [`drawTicks`](../api/ejcirculargauge#events:drawticks) event is triggered when ticks are being drawn on the gauge. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //draw ticks event
            drawTicks: function(args){

            },

            //...
        });

{% endhighlight %}

### Load

The [`load`](../api/ejcirculargauge#events:load) event is triggered when gauge starts to load. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //load event
            load: function(args){

            },

            //...
        });

{% endhighlight %}

### Mouse Click

The [`mouseClick`](../api/ejcirculargauge#events:mouseclick) event is triggered when left mouse button is clicked. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //mouse click event
            mouseClick: function(args){

            },

            //...
        });

{% endhighlight %}

### Mouse Click Move

The [`mouseClickMove`](../api/ejcirculargauge#events:mouseclickmove) event is triggered when clicking and dragging the mouse pointer over the gauge pointer. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //mouse click move event
            mouseClickMove: function(args){

            },

            //...
        });

{% endhighlight %}

### Mouse Click Up

The [`mouseClickUp`](../api/ejcirculargauge#events:mouseclickup) event is triggered when clicking and dragging the mouse pointer over the gauge pointer. 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //mouse click up event
            mouseClickUp: function(args){

            },

            //...
        });

{% endhighlight %}

### Render Complete

The [`renderComplete`](../api/ejcirculargauge#events:rendercomplete) event is triggered when rendering of the gauge is completed.

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //render complete event
            renderComplete: function(args){

            },

            //...
        });

{% endhighlight %}

### Range Mouse Move

The [`rangeMouseMove`](../api/ejcirculargauge#events:rangemousemove) event is triggered when moving mouse on ranges.

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //range mouse move event
            rangeMouseMove: function(args){

            },

            //...
        });

{% endhighlight %}


### doubleClick

The [`doubleClick`](../api/ejcirculargauge#events:doubleclick) event is triggered when double clicking the gauges.

{% highlight js %}
 
//DoubleClick event for circular gauge

$("#CoreCircularGauge").ejCircularGauge({

    doubleClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### rightClick

The [`rightClick`](../api/ejcirculargauge#events:rightclick) event is triggered when right clicking the gauges.

{% highlight js %}
 
//RightClick event for circular gauge

$("#CoreCircularGauge").ejCircularGauge({
    rightClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}