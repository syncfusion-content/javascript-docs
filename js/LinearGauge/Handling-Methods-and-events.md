---
layout: post
title: Handling methods and events
description: methods and events
platform: js
control: Linear Gauge
documentation: ug
api: /api/js/ejlineargauge
---


##Events


### drawBarPointers

Triggers while the bar pointer are being drawn on the gauge, you can use [`drawBarPointers`](../api/js/ejlineargauge#events:drawbarpointers) event.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawBarPointers: function (args) {}
});
</script> {% endhighlight %}

### drawCustomLabel

Triggers while the customLabel are being drawn on the gauge, you can use [`drawCustomLabel`](../api/js/ejlineargauge#events:drawcustomlabel) event.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawCustomLabel: function (args) {}
});
</script> {% endhighlight %}







### drawIndicators

Triggers while the Indicator are being drawn on the gauge, you can use [`drawIndicators`](../api/js/ejlineargauge#events:drawindicators) event.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawIndicators: function (args) {}
});
</script> {% endhighlight %}







### drawLabels

Triggers while the label are being drawn on the gauge, you can use [`drawLabels`](../api/js/ejlineargauge#events:drawlabels) event.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawLabels: function (args) {}
});
</script> {% endhighlight %}




### drawMarkerPointers

Triggers while the marker are being drawn on the gauge, you can use [`drawMarkerPointers`](../api/js/ejlineargauge#events:drawmarkerpointers) event.




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawMarkerPointers: function (args) {}
});
</script> {% endhighlight %}




### drawRange

Triggers while the range are being drawn on the gauge, you can use [`drawRange`](../api/js/ejlineargauge#events:drawrange) event.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawRange: function (args) {}
});
</script> {% endhighlight %}







### drawTicks

Triggers while the ticks are being drawn on the gauge, you can use [`drawTicks`](../api/js/ejlineargauge#events:drawticks) event.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawTicks: function (args) {}
});
</script> {% endhighlight %}







### init

Triggers when the gauge is initialized, you can use [`init`](../api/js/ejlineargauge#events:init)event.




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   init: function (args) {}
});
</script> {% endhighlight %}




### load

Triggers while the gauge start to Load, you can use [`load`](../api/js/ejlineargauge#events:load)event.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   load: function (args) {}
});
</script> {% endhighlight %}





### mouseClick

Triggers when the left mouse button is clicked, you can use [`mouseClick`](../api/js/ejlineargauge#events:mouseclick) event.





#### Example


{% highlight html %}
 
<div id="LinearGauge1">
</div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   mouseClick: function (args) {}
});
</script>{% endhighlight %}







### mouseClickMove

Triggers when clicking and dragging the mouse pointer over the gauge pointer, you can use [`mouseClickMove`](../api/js/ejlineargauge#events:mouseclickmove) event.




#### Example


{% highlight html %}
 
<div id="LinearGauge1">
</div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   mouseClickMove: function (args) {}
});
</script>{% endhighlight %}






### mouseClickUp


Triggers when the mouse click is released, you can use [`mouseClickUp`](../api/js/ejlineargauge#events:mouseclickup) event.




#### Example


{% highlight html %}
 
<div id="LinearGauge1">
</div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   mouseClickUp: function (args) {}
});
</script>{% endhighlight %}







### renderComplete

Triggers while the rendering of the gauge completed, you can use [`renderComplete`](../api/js/ejlineargauge#events:rendercomplete) event.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   renderComplete: function (args) {}
});
</script> {% endhighlight %}


## Methods


### destroy()

[`Destroy`](../api/js/ejlineargauge#methods:destroy) the linear gauge all events bound using this._on will be unbind automatically and bring the control to pre-init state.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge();
var linearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
linearGaugeObj.destroy();
</script>{% endhighlight %}




### getBarDistanceFromScale()

To get bar distance from scale in number, you can use [`getBarDistanceFromScale`](../api/js/ejlineargauge#methods:getbardistancefromscale) method.


#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({value:50});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarDistanceFromScale(0,0);
</script>{% endhighlight %}


### getBarPointerValue()

To get Bar Pointer Value in number, you can use [`getBarPointerValue`](../api/js/ejlineargauge#methods:getbarpointervalue) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({value:50});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarPointerValue(0,0);
</script>{% endhighlight %}


### getBarWidth()

To get Bar Width in number, you can use [`getBarWidth`](../api/js/ejlineargauge#methods:getbarwidth) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({value:50});
// get Bar Width in number
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarWidth(0,0);
</script>{% endhighlight %}



### getCustomLabelAngle()

To get CustomLabel Angle in number, you can use [`getCustomLabelAngle`](../api/js/ejlineargauge#methods:getcustomlabelangle) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getCustomLabelAngle(0,0);
</script>{% endhighlight %}




### getCustomLabelValue()

To get CustomLabel Value in string, you can use [`getCustomLabelValue`](../api/js/ejlineargauge#methods:getcustomlabelvalue) method.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getCustomLabelValue(0,0);
</script>{% endhighlight %}



### getLabelAngle()

To get Label Angle in number, you can use [`getLabelAngle`](../api/js/ejlineargauge#methods:getlabelangle) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelAngle(0,0);
</script>{% endhighlight %}





### getLabelPlacement()

To get LabelPlacement in number, you can use [`getLabelPlacement`](../api/js/ejlineargauge#methods:getlabelplacement) method.




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelPlacement(0,0);
</script>{% endhighlight %}




### getLabelStyle()

To get LabelStyle in number, you can use [`getLabelStyle`](../api/js/ejlineargauge#methods:getlabelstyle) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelStyle(0,0);
</script>{% endhighlight %}




### getLabelXDistanceFromScale()

To get Label XDistance From Scale in number, you can use [`getLabelXDistanceFromScale`](../api/js/ejlineargauge#methods:getlabelxdistancefromscale) method.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelXDistanceFromScale(0,0);
</script>{% endhighlight %}




### getLabelYDistanceFromScale()

### getLabelYDistanceFromScale()
To get PointerValue in number, you can use [`getLabelXDistanceFromScale`](../api/js/ejlineargauge#methods:getlabelydistancefromscale) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelYDistanceFromScale(0,0);
</script>{% endhighlight %}







### getMajorIntervalValue()

To get Major Interval Value in number, you can use [`getMajorIntervalValue`](../api/js/ejlineargauge#methods:getmajorintervalvalue) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMajorIntervalValue(0);
</script>{% endhighlight %}


### getMarkerStyle()

To get MarkerStyle in number, you can use [`getMarkerStyle`](../api/js/ejlineargauge#methods:getmarkerstyle) method.


#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMarkerStyle(0,0);
</script>{% endhighlight %}



### getMaximumValue()

To get Maximum Value in number, you can use [`getMaximumValue`](../api/js/ejlineargauge#methods:getmaximumvalue) method.


#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMaximumValue(0);
</script>{% endhighlight %}



### getMinimumValue()

To get PointerValue in number, you can use [`getMinimumValue`](../api/js/ejlineargauge#methods:getminimumvalue) method.


#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMinimumValue(0,0);
</script>{% endhighlight %}


### getMinorIntervalValue()

To get Minor Interval Value in number, you can use [`getMinorIntervalValue`](../api/js/ejlineargauge#methods:getminorintervalvalue) method.


#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMinorIntervalValue(0);
</script>{% endhighlight %}


### getPointerDistanceFromScale()

To get Pointer Distance From Scale in number, you can use [`getPointerDistanceFromScale`](../api/js/ejlineargauge#methods:getpointerdistancefromscale) method.


#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerDistanceFromScale(0,0);
</script>{% endhighlight %}


### getPointerHeight()

To get PointerHeight in number, you can use [`getPointerHeight`](../api/js/ejlineargauge#methods:getpointerheight) method.


#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerHeight(0,0);
</script>{% endhighlight %}


### getPointerPlacement()

To get Pointer Placement in String, you can use [`getPointerPlacement`](../api/js/ejlineargauge#methods:getpointerplacement) method.


#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerPlacement(0,0);
</script>{% endhighlight %}


### getPointerValue()

To get PointerValue in number, you can use [`getPointerValue`](../api/js/ejlineargauge#methods:getpointervalue) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerValue(0,0);
</script>{% endhighlight %}



### getPointerWidth()

To get PointerWidth in number, you can use [`getPointerWidth`](../api/js/ejlineargauge#methods:getpointerwidth) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerWidth(0,0);
</script>{% endhighlight %}


### getRangeBorderWidth()

To get Range Border Width in number, you can use [`getRangeBorderWidth`](../api/js/ejlineargauge#methods:getrangeborderwidth) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeBorderWidth(0,0);
</script>{% endhighlight %}



### getRangeDistanceFromScale()

To get Range Distance From Scale in number, you can use [`getRangeDistanceFromScale`](../api/js/ejlineargauge#methods:getrangedistancefromscale) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeDistanceFromScale(0,0);
</script>{% endhighlight %}


### getRangeEndValue()

To get Range End Value in number, you can use [`getRangeEndValue`](../api/js/ejlineargauge#methods:getrangeendvalue) method.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeEndValue(0,0);
</script>{% endhighlight %}



### getRangeEndWidth()

To get Range End Width in number, you can use [`getRangeEndWidth`](../api/js/ejlineargauge#methods:getrangeendwidth) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeEndWidth(0,0);
</script>{% endhighlight %}




### getRangePosition()

To get Range Position in number, you can use [`getRangePosition`](../api/js/ejlineargauge#methods:getrangeposition) method.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangePosition(0,0);
</script>{% endhighlight %}



### getRangeStartValue()

To get Range Start Value in number, you can use [`getRangeStartValue`](../api/js/ejlineargauge#methods:getrangestartvalue) method.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeStartValue(0,0);
</script>{% endhighlight %}







### getRangeStartWidth()

To get Range Start Width in number, you can use [`getRangeStartWidth`](../api/js/ejlineargauge#methods:getrangestartwidth) method.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeStartWidth(0,0);
</script>{% endhighlight %}



### getScaleBarLength()

To get ScaleBarLength in number, you can use [`getScaleBarLength`](../api/js/ejlineargauge#methods:getscalebarlength) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBarLength(0);
</script>{% endhighlight %}


### getScaleBarSize()

To get Scale Bar Size in number, you can use [`getScaleBarSize`](../api/js/ejlineargauge#methods:getscalebarsize) method.



#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBarSize(0,0);
</script>{% endhighlight %}


### getScaleBorderWidth()

To get Scale Border Width in number, you can use [`getScaleBorderWidth`](../api/js/ejlineargauge#methods:getscaleborderwidth) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBorderWidth(0);
</script>{% endhighlight %}


### getScaleDirection()

To get Scale Direction in number, you can use [`getScaleDirection`](../api/js/ejlineargauge#methods:getscaledirection) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleDirection(0,0);
</script>{% endhighlight %}



### getScaleLocation()

To get Scale Location in object, you can use [`getScaleLocation`](../api/js/ejlineargauge#methods:getscalelocation) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleLocation(0);
</script>{% endhighlight %}




### getScaleStyle()

To get Scale Style in string, you can use [`getScaleStyle`](../api/js/ejlineargauge#methods:getscalestyle) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleStyle(0);
</script>{% endhighlight %}



### getTickAngle()

To get Tick Angle in number, you can use [`getTickAngle`](../api/js/ejlineargauge#methods:gettickanglen) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickAngle(0,0);
</script>{% endhighlight %}



### getTickHeight()

To get Tick Height in number, you can use [`getTickHeight`](../api/js/ejlineargauge#methods:gettickheight) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickHeight(0,0);
</script>{% endhighlight %}


### getTickPlacement()

To get getTickPlacement in number, you can use [`getTickPlacement`](../api/js/ejlineargauge#methods:gettickplacement) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickPlacement(0,0);
</script>{% endhighlight %}


### getTickStyle()

To get Tick Style in string, you can use [`getTickStyle`](../api/js/ejlineargauge#methods:gettickstyle) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickStyle(0,0);
</script>{% endhighlight %}


### getTickWidth()

To get Tick Width in number, you can use [`getTickWidth`](../api/js/ejlineargauge#methods:gettickwidth) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickWidth(0,0);
</script>{% endhighlight %}

### getTickXDistanceFromScale()

To get get Tick XDistance From Scale in number, you can use [`getTickXDistanceFromScale`](../api/js/ejlineargauge#methods:gettickxdistancefromscale) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickXDistanceFromScale(0,0);
</script>{% endhighlight %}



### getTickYDistanceFromScale()

To get Tick YDistance From Scale in number, you can use [`getTickYDistanceFromScale`](../api/js/ejlineargauge#methods:gettickydistancefromscale) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickYDistanceFromScale(0,0);
</script>{% endhighlight %}



### scales()

Specifies the scales, you can use [`scales`](../api/js/ejlineargauge#methods:scales) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{minimum:5}]});
</script>                         {% endhighlight %}



### setBarDistanceFromScale()

To set setBarDistanceFromScale, you can use [`setBarDistanceFromScale`](../api/js/ejlineargauge#methods:setbardistancefromscale) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarDistanceFromScale(0,0,30);
</script>{% endhighlight %}

### setBarPointerValue()

To set setBarPointerValue, you can use [`setBarPointerValue`](../api/js/ejlineargauge#methods:setbarpointervalue) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarPointerValue(0,0,30);
</script>{% endhighlight %}


### setBarWidth()

To set setBarWidth, you can use [`setBarWidth`](../api/js/ejlineargauge#methods:setbarwidth) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarWidth(0,0,30);
</script>{% endhighlight %}


### setCustomLabelAngle()

To set setCustomLabelAngle, you can use [`setCustomLabelAngle`](../api/js/ejlineargauge#methods:setcustomlabelangle) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setCustomLabelAngle(0,0,30);
</script>{% endhighlight %}



### setCustomLabelValue()

To set setCustomLabelValue, you can use [`setCustomLabelValue`](../api/js/ejlineargauge#methods:setcustomlabelvalue) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setCustomLabelValue(0,0,"text");
</script>{% endhighlight %}



### setLabelAngle()

To set setLabelAngle, you can use [`setLabelAngle`](../api/js/ejlineargauge#methods:setlabelangle) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelAngle(0,0,20);
</script>{% endhighlight %}




### setLabelPlacement()

To set setLabelPlacement, you can use [`setLabelPlacement`](../api/js/ejlineargauge#methods:setlabelplacement) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelPlacement(0,0,"far");
</script>{% endhighlight %}



### setLabelStyle()

To set setLabelStyle, you can use [`setLabelStyle`](../api/js/ejlineargauge#methods:setlabelstyle) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelStyle(0,0,"major");
</script>{% endhighlight %}



### setLabelXDistanceFromScale()

To set setLabelXDistanceFromScale, you can use [`setLabelXDistanceFromScale`](../api/js/ejlineargauge#methods:setlabelxdistancefromscale) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelXDistanceFromScale(0,0,20);
</script>{% endhighlight %}



### setLabelYDistanceFromScale()

To set setLabelYDistanceFromScale, you can use [`setLabelYDistanceFromScale`](../api/js/ejlineargauge#methods:setlabelydistancefromscale) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelYDistanceFromScale(0,0,20);
</script>{% endhighlight %}



### setMajorIntervalValue()

To set setMajorIntervalValue, you can use [`setMajorIntervalValue`](../api/js/ejlineargauge#methods:setmajorintervalvalue) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMajorIntervalValue(0,5);
</script>{% endhighlight %}





### setMarkerStyle()

To set setMarkerStyle, you can use [`setMarkerStyle`](../api/js/ejlineargauge#methods:setmarkerstyle) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMarkerStyle(0,0,"triangle");
</script>{% endhighlight %}




### setMaximumValue()

To set setMaximumValue, you can use [`setMaximumValue`](../api/js/ejlineargauge#methods:setmaximumvalue) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMaximumValue(0,20);
</script>{% endhighlight %}



### setMinimumValue()

To set setMinimumValue, you can use [`setMinimumValue`](../api/js/ejlineargauge#methods:setminimumvalue) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMinimumValue(0,20);
</script>{% endhighlight %}



### setMinorIntervalValue()

To set setMinorIntervalValue, you can use [`setMinorIntervalValue`](../api/js/ejlineargauge#methods:setminorintervalvalue) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMinorIntervalValue(0,2);
</script>{% endhighlight %}



### setPointerDistanceFromScale()

To set setPointerDistanceFromScale, you can use [`setPointerDistanceFromScale`](../api/js/ejlineargauge#methods:setpointerdistancefromscale) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerDistanceFromScale(0,0,30);
</script>{% endhighlight %}




### setPointerHeight()

To set PointerHeight, you can use [`setPointerHeight`](../api/js/ejlineargauge#methods:setpointerheight) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerHeight(0,0,30);
</script>{% endhighlight %}




### setPointerPlacement()

To set setPointerPlacement, you can use [`setPointerPlacement`](../api/js/ejlineargauge#methods:setpointerplacement) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerPlacement(0,0,"far");
</script>{% endhighlight %}




### setPointerValue()

To set PointerValue, you can use [`setPointerValue`](../api/js/ejlineargauge#methods:setpointervalue) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerValue(0,0,30);
</script>{% endhighlight %}





### setPointerWidth()

To set PointerWidth, you can use [`setPointerWidth`](../api/js/ejlineargauge#methods:setpointerwidth) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerWidth(0,0,30);
</script>{% endhighlight %}




### setRangeBorderWidth()

To set setRangeBorderWidth, you can use [`setRangeBorderWidth`](../api/js/ejlineargauge#methods:setrangeborderwidth) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeBorderWidth(0,0,2);
</script>{% endhighlight %}




### setRangeDistanceFromScale()

To set setRangeDistanceFromScale, you can use [`setRangeDistanceFromScale`](../api/js/ejlineargauge#methods:setrangedistancefromscale) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeDistanceFromScale(0,0,20);
</script>{% endhighlight %}




### setRangeEndValue()

To set setRangeEndValue, you can use [`setRangeEndValue`](../api/js/ejlineargauge#methods:setrangeendvalue) method.


#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeEndValue(0,0,20);
</script>{% endhighlight %}




### setRangeEndWidth()

To set setRangeEndWidth, you can use [`setRangeEndWidth`](../api/js/ejlineargauge#methods:setrangeendwidth) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeEndWidth(0,0,20);
</script>{% endhighlight %}




### setRangePosition()

To set setRangePosition, you can use [`setRangePosition`](../api/js/ejlineargauge#methods:setrangeposition) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangePosition(0,0,20);
</script>{% endhighlight %}



### setRangeStartValue()

To set setRangeStartValue, you can use [`setRangeStartValue`](../api/js/ejlineargauge#methods:setrangestartvalue) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeStartValue(0,0,20);
</script>{% endhighlight %}




### setRangeStartWidth()

To set setRangeStartWidth, you can use [`setRangeStartWidth`](../api/js/ejlineargauge#methods:setrangestartwidth) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeStartWidth(0,0,20);
</script>{% endhighlight %}





### setScaleBarLength()

To set setScaleBarLength, you can use [`setScaleBarLength`](../api/js/ejlineargauge#methods:setscalebarlength) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBarLength(0,150);
</script>{% endhighlight %}



### setScaleBarSize()

To set setScaleBarSize, you can use [`setScaleBarSize`](../api/js/ejlineargauge#methods:setscalebarsize) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBarSize(0,20);
</script>{% endhighlight %}




### setScaleBorderWidth()

To set setScaleBorderWidth, you can use [`setScaleBorderWidth`](../api/js/ejlineargauge#methods:setscaleborderwidth) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBorderWidth(0,10);
</script>{% endhighlight %}




### setScaleDirection()

To set setScaleDirection, you can use [`setScaleDirection`](../api/js/ejlineargauge#methods:setscaledirection) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleDirection(0,"counterclockwise");
</script>{% endhighlight %}



### setScaleLocation()

To set setScaleLocation, you can use [`setScaleLocation`](../api/js/ejlineargauge#methods:setscalelocation) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleLocation(0,{x:20,y:20});
</script>{% endhighlight %}





### setScaleStyle()

To set setScaleStyle, you can use [`setScaleStyle`](../api/js/ejlineargauge#methods:setscalestyle) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleStyle(0,"thermometer");
</script>{% endhighlight %}



### setTickAngle()

To set setTickAngle, you can use [`setTickAngle`](../api/js/ejlineargauge#methods:settickangle) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickAngle(0,0,20);
</script>{% endhighlight %}



### setTickHeight()

To set setTickHeight, you can use [`setTickHeight`](../api/js/ejlineargauge#methods:settickheight) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickHeight(0,0,10);
</script>{% endhighlight %}




### setTickPlacement()

To set setTickPlacement, you can use [`setTickPlacement`](../api/js/ejlineargauge#methods:settickplacement) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickPlacement(0,0,"far");
</script>{% endhighlight %}



### setTickStyle()

To set setTickStyle, you can use [`setTickStyle`](../api/js/ejlineargauge#methods:settickstyle) method.

#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickStyle(0,0,"major");
</script>{% endhighlight %}




### setTickWidth()

To set setTickWidth, you can use [`setTickWidth`](../api/js/ejlineargauge#methods:settickwidth) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickWidth(0,0,5);
</script>{% endhighlight %}




### setTickXDistanceFromScale()

To set setTickXDistanceFromScale, you can use [`setTickXDistanceFromScale`](../api/js/ejlineargauge#methods:settickxdistancefromscale) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickXDistanceFromScale(0,0,20);
</script>{% endhighlight %}




### setTickYDistanceFromScale()

To set setTickYDistanceFromScale, you can use [`setTickYDistanceFromScale`](../api/js/ejlineargauge#methods:settickydistancefromscale) method.

#### Example

{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickYDistanceFromScale(0,0,20);
</script>{% endhighlight %}




