---
layout: post
title: ejCircularGauge
documentation: API
platform: js
metaname: 
metacontent: 
---

The Circular gauge can be easily configured to the DOM element, such as div. you can create a circular gauge with a highly customizable look and feel.





$(element).ejCircularGauge<span class="signature">(options)</span>




<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">For seting the Circular gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$(function () {
        $("#CoreCircularGauge").ejCircularGauge({
        });
    });
</script>{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:ej.common.all

* module:excanvas.js


## Members




### animationSpeed<span class="type-signature type number">number</span>
{:#members:animationspeed}




Specifies animationSpeed of circular gauge


Default Value:
{:.param}



* 500




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({ animationSpeed: 500,scales: [{ pointers: [{ value: 50 }] }] });
</script>{% endhighlight %}




### backgroundColor<span class="type-signature type string">string</span>
{:#members:backgroundcolor}




Specifies the backgroundcolor of circular gauge.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
                     
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({  backgroundColor : "#F234F4" });
</script>{% endhighlight %}




### distanceFromCorner<span class="type-signature type enum">enum</span>
{:#members:distancefromcorner}




Specify distanceFromCorner value of circular gauge


Default Value:
{:.param}



* center




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  gaugePosition:"center", distanceFromCorner :25});
</script>{% endhighlight %}




### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}




Specify animate value of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                   
$("#CoreCircularGauge").ejCircularGauge({ enableAnimation: true,scales: [{ pointers: [{ value: 50 }] }] });
</script>{% endhighlight %}




### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}




Specify enableResize value of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({  enableResize : true });
</script>{% endhighlight %}




### frame<span class="type-signature type object">object</span>
{:#members:frame}




Specify the frame of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
$("#CoreCircularGauge").ejCircularGauge({ frame:{frameType:ej.datavisualization.CircularGauge.Frame.FullCircle, backgroundImageUrl:"", halfCircleFrameStartAngle:180, halfCircleFrameEndAngle:360} });
</script>{% endhighlight %}




### frame.backgroundImageUrl<span class="type-signature type string">string</span>
{:#members:frame.backgroundimageurl}




Specify the url of the frame background image for circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({  frame:{backgroundImageUrl : "Sun.jpg" }});
</script>{% endhighlight %}




### frame.frameType<span class="type-signature type enum">enum</span>
{:#members:frame.frametype}




Specifies the frameType of circular gauge. See <a href="global.html#Frame">Frame</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.Frame.FullCircle




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({  frame:{frameType : "halfcircle"} });
</script>{% endhighlight %}




### frame.halfCircleFrameEndAngle<span class="type-signature type number">number</span>
{:#members:frame.halfcircleframeendangle}




Specifies the end angle for the half circular frame.


Default Value:
{:.param}



* 360




Example
{:.example}


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ frame:{frameType : "halfCircle",halfCircleFrameEndAngle: 270}});
</script>{% endhighlight %}




### frame.halfCircleFrameStartAngle<span class="type-signature type number">number</span>
{:#members:frame.halfcircleframestartangle}




Specifies the start angle for the half circular frame.


Default Value:
{:.param}



* 180




Example
{:.example}


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ frame:{frameType : "halfcircle",halfCircleFrameStartAngle: 0} });
</script>{% endhighlight %}




### gaugePosition<span class="type-signature type enum">enum</span>
{:#members:gaugeposition}




Specify gaugePosition value of circular gauge See GaugePosition


Default Value:
{:.param}



* center




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  gaugePosition:"center" });
</script>{% endhighlight %}




### height<span class="type-signature type number">number</span>
{:#members:height}




Specifies the height of circular gauge.


Default Value:
{:.param}



* 360




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ height: 400 });
</script>{% endhighlight %}




### interiorGradient<span class="type-signature type object">object</span>
{:#members:interiorgradient}




Specifies the interiorGradient of circular gauge.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
                     
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ interiorGradient: { colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } }); 
</script>{% endhighlight %}




### isRadialGradient<span class="type-signature type boolean">boolean</span>
{:#members:isradialgradient}




Specify isRadialGradient value of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({  isRadialGradient : true });
</script>{% endhighlight %}




### maximum<span class="type-signature type number">number</span>
{:#members:maximum}




Specifies the maximum value of circular gauge.


Default Value:
{:.param}



* 100




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ maximum: 120 });
</script>{% endhighlight %}




### minimum<span class="type-signature type number">number</span>
{:#members:minimum}




Specifies the minimum value of circular gauge.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ minimum: 10 });
</script>{% endhighlight %}




### outerCustomLabelPosition<span class="type-signature type enum">enum</span>
{:#members:outercustomlabelposition}




Specify outerCustomLabelPosition value of circular gauge See <a href="global.html#OuterCustomLabelPosition">OuterCustomLabelPosition</a>


Default Value:
{:.param}



* bottom




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  outerCustomLabelPosition:"top" });
</script>{% endhighlight %}




### radius<span class="type-signature type number">number</span>
{:#members:radius}




Specifies the radius of circular gauge.


Default Value:
{:.param}



* 180




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ radius: 100 });
</script>{% endhighlight %}




### readOnly<span class="type-signature type boolean">boolean</span>
{:#members:readonly}




Specify readonly value of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
                     
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({  readOnly : false });
</script>{% endhighlight %}




### scales<span class="type-signature type object">object</span>
{:#members:scales}




Specify the pointers, ticks, labels, indicators, ranges of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{width: 1.5} }] });
</script>{% endhighlight %}




### scales.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales.backgroundcolor}




Specify backgroundColor for the scale of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, backgroundColor: "#1BA1E2" }] });
</script>{% endhighlight %}




### scales.border<span class="type-signature type object">object</span>
{:#members:scales.border}




Specify border for scales of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ border:{color:null, width:1.5 }}] });
</script>{% endhighlight %}




### scales.border.color<span class="type-signature type string">string</span>
{:#members:scales.border.color}




Specify border color for scales of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true,  border:[{color: "#1BA1E2" }]}] });
</script>{% endhighlight %}




### scales.border.width<span class="type-signature type number">number</span>
{:#members:scales.border.width}




Specify border width of circular gauge


Default Value:
{:.param}



* 1.5




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, border:{width: 1.5} }] });
</script>{% endhighlight %}




### scales.direction<span class="type-signature type enum">enum</span>
{:#members:scales.direction}




Specify scale direction of circular gauge. See <a href="global.html#Directions">Directions</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.Directions.Clockwise




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ direction: "counterclockwise" }] });
</script>{% endhighlight %}




### scales.indicators<span class="type-signature type array">Array</span>
{:#members:scales.indicators}




Specify representating state of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  height: 30,width: 10,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243", borderColor: "#5DF243", text: "", textColor: "#870505" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608", borderColor: "#145608", text: "", textColor: "#870505" }]}]}]});
</script>{% endhighlight %}




### scales.indicators.height<span class="type-signature type number">number</span>
{:#members:scales.indicators.height}




Specify indicator height of circular gauge


Default Value:
{:.param}



* 15




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  height: 30,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.imageUrl<span class="type-signature type string">string</span>
{:#members:scales.indicators.imageurl}




Specify imageUrl of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "image",value: 0,imageUrl:"Sun.jpeg",position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.position<span class="type-signature type object">object</span>
{:#members:scales.indicators.position}




Specify position of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y: 150 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.position.x<span class="type-signature type number">number</span>
{:#members:scales.indicators.position.x}




Specify x-axis of position of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185,y:0 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.position.y<span class="type-signature type number">number</span>
{:#members:scales.indicators.position.y}




Specify y-axis of position of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x:0,y: 185 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges<span class="type-signature type array">Array</span>
{:#members:scales.indicators.stateranges}




Specify the various states of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales.indicators.stateranges.backgroundcolor}




Specify backgroundColor for indicator of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "Red" },
  { endValue: 200, startValue: 70, backgroundColor: "Yellow"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.borderColor<span class="type-signature type string">string</span>
{:#members:scales.indicators.stateranges.bordercolor}




Specify borderColor for indicator of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243",borderColor:"Red" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608", borderColor:"yellow"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.endValue<span class="type-signature type number">number</span>
{:#members:scales.indicators.stateranges.endvalue}




Specify end value for each specified state of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.font<span class="type-signature type object">object</span>
{:#members:scales.indicators.stateranges.font}




Specify value of the font as the indicator when the indicator style is set with the value "text" of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
$("#CoreCircularGauge").ejCircularGauge({
scales: [{showIndicators: true, indicators: [{
width: 30, type: "text", value: 0, position: { x: 185, y: 300 },
stateRanges: [{ endValue: 70, startValue: 0, text: "staterange1" },
{ endValue: 200, startValue: 70, text: "staterange1", font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" } }]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.startValue<span class="type-signature type number">number</span>
{:#members:scales.indicators.stateranges.startvalue}




Specify start value for each specified state of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.text<span class="type-signature type string">string</span>
{:#members:scales.indicators.stateranges.text}




Specify value of the text as the indicator when the indicator style is set with the value "text" of circular gauge


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
$("#CoreCircularGauge").ejCircularGauge({
scales: [{showIndicators: true, indicators: [{
width: 30, type: "text", value: 0, position: { x: 185, y: 300 },
stateRanges: [{ endValue: 70, startValue: 0, text: "staterange1" },
{ endValue: 200, startValue: 70, text: "staterange1" }]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.textColor<span class="type-signature type string">string</span>
{:#members:scales.indicators.stateranges.textcolor}




Specify value of the textColor as the indicator when the indicator style is set with the value "text" of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({
scales: [{showIndicators: true, indicators: [{
width: 30, type: "text", value: 0, position: { x: 185, y: 300 },
stateRanges: [{ endValue: 70, startValue: 0, text: "staterange1", textColor: "Yellow" },
{ endValue: 200, startValue: 70, text: "staterange1", textColor: "Yellow" }]}]}]});
</script>{% endhighlight %}




### scales.indicators.type<span class="type-signature type enum">enum</span>
{:#members:scales.indicators.type}




Specify indicator style of circular gauge. See <a href="global.html#IndicatorType">IndicatorType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.IndicatorType.Circle




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.width<span class="type-signature type number">number</span>
{:#members:scales.indicators.width}




Specify indicator width of circular gauge


Default Value:
{:.param}



* 15




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.labels<span class="type-signature type array">Array</span>
{:#members:scales.labels}




Specify the text values displayed in a meaningful manner alongside the ticks of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ angle: 10, opacity: 0.4 }] }] });
</script>{% endhighlight %}




### scales.labels.angle<span class="type-signature type number">number</span>
{:#members:scales.labels.angle}




Specify the angle for the labels of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ angle: 10 }] }] });
</script>{% endhighlight %}




### scales.labels.autoAngle<span class="type-signature type boolean">boolean</span>
{:#members:scales.labels.autoangle}




Specify labels autoAngle value of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels:[{autoAngle: true}] }] });
</script>{% endhighlight %}




### scales.labels.color<span class="type-signature type string">string</span>
{:#members:scales.labels.color}




Specify label color of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ color: "Red" }] }] });
</script>{% endhighlight %}




### scales.labels.distanceFromScale<span class="type-signature type number">number</span>
{:#members:scales.labels.distancefromscale}




Specify distanceFromScale value for labels of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ distanceFromScales: 10 }] }] });
</script>{% endhighlight %}




### scales.labels.font<span class="type-signature type object">object</span>
{:#members:scales.labels.font}




Specify font for labels of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { size: "12px", fontFamily: "Segou", fontStyle: "Bold" } }] }] });
</script>{% endhighlight %}




### scales.labels.font.fontFamily<span class="type-signature type string">String</span>
{:#members:scales.labels.font.fontfamily}




Specify font fontFamily for labels of circular gauge


Default Value:
{:.param}



* "Arial"




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { fontFamily: "Arial" } }] }] });
</script>{% endhighlight %}




### scales.labels.font.fontStyle<span class="type-signature type string">string</span>
{:#members:scales.labels.font.fontstyle}




Specify font Style for labels of circular gauge


Default Value:
{:.param}



* "Bold"




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { fontStyle: "Bold" } }] }] });
</script>{% endhighlight %}




### scales.labels.font.size<span class="type-signature type string">string</span>
{:#members:scales.labels.font.size}




Specify font size for labels of circular gauge


Default Value:
{:.param}



* "11px"




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { size: "12px" } }] }] });
</script>{% endhighlight %}




### scales.labels.includeFirstValue<span class="type-signature type boolean">boolean</span>
{:#members:scales.labels.includefirstvalue}




Specify includeFirstValue of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ includeFirstValue: false }] }] });
</script>{% endhighlight %}




### scales.labels.opacity<span class="type-signature type number">number</span>
{:#members:scales.labels.opacity}




Specify opacity value for labels of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ opacity: 0.4 }] }] });
</script>{% endhighlight %}




### scales.labels.placement<span class="type-signature type enum">enum</span>
{:#members:scales.labels.placement}




Specify label placement of circular gauge. See <a href="global.html#LabelPlacement">LabelPlacement</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.LabelPlacement.Near




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ placement: "near" }] }] });
</script>{% endhighlight %}




### scales.labels.type<span class="type-signature type enum">enum</span>
{:#members:scales.labels.type}




Specify label Style of circular gauge. See <a href="global.html#LabelType">LabelType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.LabelType.Major




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ type: "major" }] }] });
</script>{% endhighlight %}




### scales.labels.unitText<span class="type-signature type string">string</span>
{:#members:scales.labels.unittext}




Specify unitText of circular gauge


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ unitText: "kmph" }] }] });
</script>{% endhighlight %}




### scales.labels.unitTextPosition<span class="type-signature type enum">enum</span>
{:#members:scales.labels.unittextposition}




Specify unitTextPosition of circular gauge. See UnitTextPosition


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.LabelType.Back




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ unitText: "kmph",unitTextPosition: "front" }] }] });
</script>{% endhighlight %}




### scales.majorIntervalValue<span class="type-signature type number">number</span>
{:#members:scales.majorintervalvalue}




Specify majorIntervalValue of circular gauge


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ majorIntervalValue: 5 }] });
</script>{% endhighlight %}




### scales.maximum<span class="type-signature type number">number</span>
{:#members:scales.maximum}




Specify maximum scale value of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ maximum: 200 }] });
</script>{% endhighlight %}




### scales.minimum<span class="type-signature type number">number</span>
{:#members:scales.minimum}




Specify minimum scale value of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ minimum: 20 }] });
</script>{% endhighlight %}




### scales.minorIntervalValue<span class="type-signature type number">number</span>
{:#members:scales.minorintervalvalue}




Specify minorIntervalValue of circular gauge


Default Value:
{:.param}



* 2




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ minorIntervalValue: 1 }] });
</script>{% endhighlight %}




### scales.opacity<span class="type-signature type number">number</span>
{:#members:scales.opacity}




Specify opacity value of circular gauge


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
     
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, opacity:0.5 }] });
</script>{% endhighlight %}




### scales.pointerCap<span class="type-signature type object">object</span>
{:#members:scales.pointercap}




Specify pointer cap of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{radius: 7, borderWidth:3, interiorGradient:null, borderColor:null } }] });
</script>{% endhighlight %}




### scales.pointerCap.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales.pointercap.backgroundcolor}




Specify cap backgroundColor of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap: {backgroundColor: "Green"} }] });
</script>{% endhighlight %}




### scales.pointerCap.borderColor<span class="type-signature type string">string</span>
{:#members:scales.pointercap.bordercolor}




Specify cap borderColor of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap: {borderColor: "Brown" }}] });
</script>{% endhighlight %}




### scales.pointerCap.borderWidth<span class="type-signature type number">number</span>
{:#members:scales.pointercap.borderwidth}




Specify pointerCap borderWidth value of circular gauge


Default Value:
{:.param}



* 3




Example
{:.example}


{% highlight html %}
     
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{borderWidth: 8 } }] });
</script>{% endhighlight %}




### scales.pointerCap.interiorGradient<span class="type-signature type object">Object</span>
{:#members:scales.pointercap.interiorgradient}




Specify cap interiorGradient value of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
             
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{interiorGradient: {colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}}] });
</script>{% endhighlight %}




### scales.pointerCap.radius<span class="type-signature type number">number</span>
{:#members:scales.pointercap.radius}




Specify pointerCap Radius value of circular gauge


Default Value:
{:.param}



* 7




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{radius: 10} }] });
</script>{% endhighlight %}




### scales.pointers<span class="type-signature type array">Array</span>
{:#members:scales.pointers}




Specify pointers value of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}


{% highlight html %}
     
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ distanceFromScale: 0, showBackNeedle: false }] }] });
</script>{% endhighlight %}




### scales.pointers.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales.pointers.backgroundcolor}




Specify backgroundColor for the pointer of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ backgroundColor: "#1A1A1A" }] }] });
</script>{% endhighlight %}




### scales.pointers.backNeedleLength<span class="type-signature type number">number</span>
{:#members:scales.pointers.backneedlelength}




Specify backNeedleLength of circular gauge


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true, backNeedleLength: 10 }] }] });
</script>{% endhighlight %}




### scales.pointers.border<span class="type-signature type object">object</span>
{:#members:scales.pointers.border}




Specify the border for pointers of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers:[{border:{color:null, width:1.5 }}]}] });
</script>{% endhighlight %}




### scales.pointers.border.color<span class="type-signature type string">string</span>
{:#members:scales.pointers.border.color}




Specify border color for pointer of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ border:{color: "#1A1A1A"} }] }] });
</script>{% endhighlight %}




### scales.pointers.border.width<span class="type-signature type number">number</span>
{:#members:scales.pointers.border.width}




Specify border width for pointers of circular gauge


Default Value:
{:.param}



* 1.5




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ border:{width: 1.5 }}] }] });
</script>{% endhighlight %}




### scales.pointers.distanceFromScale<span class="type-signature type number">number</span>
{:#members:scales.pointers.distancefromscale}




Specify distanceFromScale value for pointers of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ distanceFromScale: 10 }] }] });
</script>{% endhighlight %}




### scales.pointers.gradients<span class="type-signature type object">Object</span>
{:#members:scales.pointers.gradients}




Specify pointer gradients of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ gradients: {colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}] }] });
</script>{% endhighlight %}




### scales.pointers.imageUrl<span class="type-signature type number">string</span>
{:#members:scales.pointers.imageurl}




Specify pointer image of circular gauge.It is applicable for both marker as well as needle type pointers.


Default Value:
{:.param}



* NULL




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "image", imageUrl: "football.png" }] }] });
</script>{% endhighlight %}




### scales.pointers.length<span class="type-signature type number">number</span>
{:#members:scales.pointers.length}




Specify pointer length of circular gauge


Default Value:
{:.param}



* 150




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ length: 50 }] }] });
</script>{% endhighlight %}




### scales.pointers.markerType<span class="type-signature type enum">enum</span>
{:#members:scales.pointers.markertype}




Specify marker Style value of circular gauge. See <a href="global.html#MarkerType">MarkerType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.MarkerType.Rectangle




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle" }] }] });
</script>{% endhighlight %}




### scales.pointers.needleType<span class="type-signature type enum">enum</span>
{:#members:scales.pointers.needletype}




Specify needle Style value of circular gauge. See <a href="global.html#NeedleType">NeedleType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.NeedleType.Triangle




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ needleType: "triangle" }] }] });
</script>{% endhighlight %}




### scales.pointers.opacity<span class="type-signature type number">number</span>
{:#members:scales.pointers.opacity}




Specify opacity value for pointer of circular gauge


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ opacity: 0.3 }] }] });
</script>{% endhighlight %}




### scales.pointers.placement<span class="type-signature type enum">enum</span>
{:#members:scales.pointers.placement}




Specify pointer Placement value of circular gauge. See <a href="global.html#PointerPlacement">PointerPlacement</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.PointerPlacement.Near




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ placement: "far" }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText<span class="type-signature type object">object</span>
{:#members:scales.pointers.pointervaluetext}




Specify pointer value text of circular gauge.


Default Value:
{:.param}



* Object




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: false, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.angle<span class="type-signature type number">number</span>
{:#members:scales.pointers.pointervaluetext.angle}




Specify pointer text angle of circular gauge.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 0.5, autoAngle: false, angle: 30, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.autoAngle<span class="type-signature type boolean">boolean</span>
{:#members:scales.pointers.pointervaluetext.autoangle}




Specify pointer text auto angle of circular gauge.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 0.5, autoAngle: true, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.color<span class="type-signature type string">string</span>
{:#members:scales.pointers.pointervaluetext.color}




Specify pointer value text color of circular gauge.


Default Value:
{:.param}



* #8c8c8c




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.distance<span class="type-signature type number">number</span>
{:#members:scales.pointers.pointervaluetext.distance}




Specify pointer value text distance from pointer of circular gauge.


Default Value:
{:.param}



* 20




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.font<span class="type-signature type object">object</span>
{:#members:scales.pointers.pointervaluetext.font}




Specify pointer value text font option of circular gauge.


Default Value:
{:.param}



* object




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.font.fontFamily<span class="type-signature type string">string</span>
{:#members:scales.pointers.pointervaluetext.font.fontfamily}




Specify pointer value text font family of circular gauge.


Default Value:
{:.param}



* Arial




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "12px", fontFamily: "Seogo UI", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.font.fontStyle<span class="type-signature type string">string</span>
{:#members:scales.pointers.pointervaluetext.font.fontstyle}




Specify pointer value text font style of circular gauge.


Default Value:
{:.param}



* Bold




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "12px", fontFamily: "Seogo UI", fontStyle: "Normal" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.font.size<span class="type-signature type string">string</span>
{:#members:scales.pointers.pointervaluetext.font.size}




Specify pointer value text size of circular gauge.


Default Value:
{:.param}



* 11px




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "12px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.opacity<span class="type-signature type number">number</span>
{:#members:scales.pointers.pointervaluetext.opacity}




Specify pointer value text opacity of circular gauge.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 0.5, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.showValue<span class="type-signature type boolean">boolean</span>
{:#members:scales.pointers.pointervaluetext.showvalue}




enable pointer value text visibility of circular gauge.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.showBackNeedle<span class="type-signature type boolean">boolean</span>
{:#members:scales.pointers.showbackneedle}




Specify showBackNeedle value of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true, backNeedleLength: 10 }] }] });
</script>{% endhighlight %}




### scales.pointers.type<span class="type-signature type enum">enum</span>
{:#members:scales.pointers.type}




Specify pointer type value of circular gauge. See <a href="global.html#PointerType">PointerType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.PointerType.Needle




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker" }] }] });
</script>{% endhighlight %}




### scales.pointers.value<span class="type-signature type number">number</span>
{:#members:scales.pointers.value}




Specify value of the pointer of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ value: 50 }] }] });
</script>{% endhighlight %}




### scales.pointers.width<span class="type-signature type number">number</span>
{:#members:scales.pointers.width}




Specify pointer width of circular gauge


Default Value:
{:.param}



* 7




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ width: 7 }] }] });
</script>{% endhighlight %}




### scales.radius<span class="type-signature type number">number</span>
{:#members:scales.radius}




Specify scale radius of circular gauge


Default Value:
{:.param}



* 170




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, radius: 100 }] });
</script>{% endhighlight %}




### scales.ranges<span class="type-signature type array">Array</span>
{:#members:scales.ranges}




Specify ranges value of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true [{ ranges: [{ distanceFromScale: 25, size: 5}] }] }]});
</script>{% endhighlight %}




### scales.ranges.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales.ranges.backgroundcolor}




Specify backgroundColor for the ranges of circular gauge


Default Value:
{:.param}



* "#32b3c6"




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,backgroundColor: "Red" }]  }]});
</script>{% endhighlight %}




### scales.ranges.border<span class="type-signature type object">object</span>
{:#members:scales.ranges.border}




Specify border for ranges of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ ranges:[{border:{color:null, width:1.5 }}]}] });
</script>{% endhighlight %}




### scales.ranges.border.color<span class="type-signature type string">string</span>
{:#members:scales.ranges.border.color}




Specify border color for ranges of circular gauge


Default Value:
{:.param}



* "#32b3c6"




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,border:{color: "#32b3c6"} }] }] });
</script>{% endhighlight %}




### scales.ranges.border.width<span class="type-signature type number">number</span>
{:#members:scales.ranges.border.width}




Specify border width for ranges of circular gauge


Default Value:
{:.param}



* 1.5




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,distanceFromScale: -25,border:{width: 1.5} }] }] });
</script>{% endhighlight %}




### scales.ranges.distanceFromScale<span class="type-signature type number">number</span>
{:#members:scales.ranges.distancefromscale}




Specify distanceFromScale value for ranges of circular gauge


Default Value:
{:.param}



* 25




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
</script>{% endhighlight %}




### scales.ranges.endValue<span class="type-signature type number">number</span>
{:#members:scales.ranges.endvalue}




Specify endValue for ranges of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true, ranges: [{ startValue: 10, endValue: 100,distanceFromScale: -25 }] }]});
</script>{% endhighlight %}




### scales.ranges.endWidth<span class="type-signature type number">number</span>
{:#members:scales.ranges.endwidth}




Specify endWidth for ranges of circular gauge


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
</script>{% endhighlight %}




### scales.ranges.gradients<span class="type-signature type object">object</span>
{:#members:scales.ranges.gradients}




Specify range gradients of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{startValue: 10, endValue: 100, gradients: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}] }]});
</script>{% endhighlight %}




### scales.ranges.opacity<span class="type-signature type number">number</span>
{:#members:scales.ranges.opacity}




Specify opacity value for ranges of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,distanceFromScale: -25,opacity: 0.5 }] }] });
</script>{% endhighlight %}




### scales.ranges.placement<span class="type-signature type enum">enum</span>
{:#members:scales.ranges.placement}




Specify placement of circular gauge. See <a href="global.html#RangePlacement">RangePlacement</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.RangePlacement.Near




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70,placement: "center"}]}]});
</script>{% endhighlight %}




### scales.ranges.size<span class="type-signature type number">number</span>
{:#members:scales.ranges.size}




Specify size of the range value of circular gauge


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70,size:5}]}]});
</script>{% endhighlight %}




### scales.ranges.startValue<span class="type-signature type number">number</span>
{:#members:scales.ranges.startvalue}




Specify startValue for ranges of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
</script>{% endhighlight %}




### scales.ranges.startWidth<span class="type-signature type number">number</span>
{:#members:scales.ranges.startwidth}




Specify startWidth of circular gauge


Default Value:
{:.param}



* [Array.number] scale.ranges.startWidth = 10




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,distanceFromScale: -25 }] }]});
</script>{% endhighlight %}




### scales.shadowOffset<span class="type-signature type number">number</span>
{:#members:scales.shadowoffset}




Specify shadowOffset value of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ shadowOffset: 1}] });
</script>{% endhighlight %}




### scales.showIndicators<span class="type-signature type boolean">boolean</span>
{:#members:scales.showindicators}




Specify showIndicators of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showIndicators: false }] });
</script>{% endhighlight %}




### scales.showLabels<span class="type-signature type boolean">boolean</span>
{:#members:scales.showlabels}




Specify showLabels of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showLabels: true }] });
</script>{% endhighlight %}




### scales.showPointers<span class="type-signature type boolean">boolean</span>
{:#members:scales.showpointers}




Specify showPointers of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showPointers: true }] });
</script>{% endhighlight %}




### scales.showRanges<span class="type-signature type boolean">boolean</span>
{:#members:scales.showranges}




Specify showRanges of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showRanges: false }] });
</script>{% endhighlight %}




### scales.showScaleBar<span class="type-signature type boolean">boolean</span>
{:#members:scales.showscalebar}




Specify showScaleBar of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true }] });
</script>{% endhighlight %}




### scales.showTicks<span class="type-signature type boolean">boolean</span>
{:#members:scales.showticks}




Specify showTicks of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showTicks: true }] });
</script>{% endhighlight %}




### scales.size<span class="type-signature type number">number</span>
{:#members:scales.size}




Specify scaleBar size of circular gauge


Default Value:
{:.param}



* 6




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, size: 6 }] });
</script>{% endhighlight %}




### scales.startAngle<span class="type-signature type number">number</span>
{:#members:scales.startangle}




Specify startAngle of circular gauge


Default Value:
{:.param}



* 115




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ startAngle: 90 }] });
</script>{% endhighlight %}




### scales.subGauges<span class="type-signature type array">Array</span>
{:#members:scales.subgauges}




Specify subGauge of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 200, y: 150 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.height<span class="type-signature type number">number</span>
{:#members:scales.subgauges.height}




Specify subGauge Height of circular gauge


Default Value:
{:.param}



* 150




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 100 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.position<span class="type-signature type object">object</span>
{:#members:scales.subgauges.position}




Specify position for sub-gauge of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 200, y: 150 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.position.x<span class="type-signature type number">number</span>
{:#members:scales.subgauges.position.x}




Specify x-axis position for sub-gauge of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 200, y: 0 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.position.y<span class="type-signature type number">number</span>
{:#members:scales.subgauges.position.y}




Specify y-axis position for sub-gauge of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 0, y: 150 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.width<span class="type-signature type number">number</span>
{:#members:scales.subgauges.width}




Specify subGauge Width of circular gauge


Default Value:
{:.param}



* 150




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 300,position: { x: 200, y: 150 }}]}]});
</script>{% endhighlight %}




### scales.sweepAngle<span class="type-signature type number">number</span>
{:#members:scales.sweepangle}




Specify sweepAngle of circular gauge


Default Value:
{:.param}



* 310




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ sweepAngle: 200 }] });
</script>{% endhighlight %}




### scales.ticks<span class="type-signature type array">Array</span>
{:#members:scales.ticks}




Specify ticks of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ angle: 10, distanceFromScale: 10 }] }] });
</script>{% endhighlight %}




### scales.ticks.angle<span class="type-signature type number">number</span>
{:#members:scales.ticks.angle}




Specify the angle for the ticks of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ angle: 10 }] }] });
</script>{% endhighlight %}




### scales.ticks.color<span class="type-signature type string">string</span>
{:#members:scales.ticks.color}




Specify tick color of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ color: "#777777" }] }] });
</script>{% endhighlight %}




### scales.ticks.distanceFromScale<span class="type-signature type number">number</span>
{:#members:scales.ticks.distancefromscale}




Specify distanceFromScale value for ticks of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ distanceFromScale: 10 }] }] });
</script>{% endhighlight %}




### scales.ticks.height<span class="type-signature type number">number</span>
{:#members:scales.ticks.height}




Specify tick height of circular gauge


Default Value:
{:.param}



* 16




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ height: 16 }] }] });
</script>{% endhighlight %}




### scales.ticks.placement<span class="type-signature type enum">enum</span>
{:#members:scales.ticks.placement}




Specify tick placement of circular gauge. See <a href="global.html#TickPlacement">TickPlacement</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.TickPlacement.Near




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ placement: "near" }] }] });
</script>{% endhighlight %}




### scales.ticks.type<span class="type-signature type enum">enum</span>
{:#members:scales.ticks.type}




Specify tick Style of circular gauge. See <a href="global.html#TickType">TickType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.TickPlacement.Major




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ type: "major" }] }] });
</script>{% endhighlight %}




### scales.ticks.width<span class="type-signature type number">number</span>
{:#members:scales.ticks.width}




Specify tick width of circular gauge


Default Value:
{:.param}



* 3




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ width: 3 }] }] });
</script>{% endhighlight %}




### theme<span class="type-signature type string">string</span>
{:#members:theme}




Specify the theme of circular gauge.


Default Value:
{:.param}



* "flatlight"




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({  theme : "flatlight" });
</script>{% endhighlight %}




### tooltip<span class="type-signature type object">object</span>
{:#members:tooltip}




Specify tooltip option of circular gauge


Default Value:
{:.param}



* object




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showLabelTooltip: true,showCustomLabelTooltip: true,templateID: null} });
</script>{% endhighlight %}




### tooltip.showCustomLabelTooltip<span class="type-signature type boolean">boolean</span>
{:#members:tooltip.showcustomlabeltooltip}




enable showCustomLabelTooltip of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showCustomLabelTooltip: true} });
</script>{% endhighlight %}




### tooltip.showLabelTooltip<span class="type-signature type boolean">boolean</span>
{:#members:tooltip.showlabeltooltip}




enable showLabelTooltip of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showLabelTooltip: true} });
</script>{% endhighlight %}




### tooltip.templateID<span class="type-signature type string">string</span>
{:#members:tooltip.templateid}




Specify tooltip templateID of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showLabelTooltip: true, templateID: "template1"} });
</script>{% endhighlight %}




### value<span class="type-signature type number">number</span>
{:#members:value}




Specifies the value of circular gauge.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ value: 30 });
</script>{% endhighlight %}




### width<span class="type-signature type number">number</span>
{:#members:width}




Specifies the width of circular gauge.


Default Value:
{:.param}



* 360




Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ width: 400 });
</script>{% endhighlight %}



## Methods




### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy the circular gauge widget. all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.destroy();
</script>{% endhighlight %}




### exportImage<span class="signature">()</span>
{:#methods:exportimage}




To export Image

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.fileName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fileName for the Image</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.fileType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fileType for the Image</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.exportImage("myImage","jpeg");
</script>{% endhighlight %}




### getBackNeedleLength<span class="signature">()</span>
{:#methods:getbackneedlelength}




To get BackNeedleLength

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true }] }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getBackNeedleLength(0, 0);
</script>{% endhighlight %}




### getCustomLabelAngle<span class="signature">()</span>
{:#methods:getcustomlabelangle}




To get CustomLabelAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.customLabelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{textAngle:30,value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getCustomLabelAngle(0, 0);
</script>{% endhighlight %}




### getCustomLabelValue<span class="signature">()</span>
{:#methods:getcustomlabelvalue}




To get CustomLabelValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.customLabelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{textAngle:30,value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getCustomLabelValue(0, 0);
</script>{% endhighlight %}




### getLabelAngle<span class="signature">()</span>
{:#methods:getlabelangle}




To get LabelAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelAngle(0, 0);
</script>{% endhighlight %}




### getLabelDistanceFromScale<span class="signature">()</span>
{:#methods:getlabeldistancefromscale}




To get LabelDistanceFromScale

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelDistanceFromScale(0, 0);
</script>{% endhighlight %}




### getLabelPlacement<span class="signature">()</span>
{:#methods:getlabelplacement}




To get LabelPlacement

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelPlacement(0, 0);
</script>{% endhighlight %}




### getLabelStyle<span class="signature">()</span>
{:#methods:getlabelstyle}




To get LabelStyle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelStyle(0, 0);
</script>{% endhighlight %}




### getMajorIntervalValue<span class="signature">()</span>
{:#methods:getmajorintervalvalue}




To get MajorIntervalValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMajorIntervalValue(0);
</script>{% endhighlight %}




### getMarkerDistanceFromScale<span class="signature">()</span>
{:#methods:getmarkerdistancefromscale}




To get MarkerDistanceFromScale

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMarkerDistanceFromScale(0, 0);
</script>{% endhighlight %}




### getMarkerStyle<span class="signature">()</span>
{:#methods:getmarkerstyle}




To get MarkerStyle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMarkerStyle(0, 0);
</script>{% endhighlight %}




### getMaximumValue<span class="signature">()</span>
{:#methods:getmaximumvalue}




To get MaximumValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMaximumValue(0);
</script>{% endhighlight %}




### getMinimumValue<span class="signature">()</span>
{:#methods:getminimumvalue}




To get MinimumValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMinimumValue(0);
</script>{% endhighlight %}




### getMinorIntervalValue<span class="signature">()</span>
{:#methods:getminorintervalvalue}




To get MinorIntervalValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMinorIntervalValue(0);
</script>{% endhighlight %}




### getNeedleStyle<span class="signature">()</span>
{:#methods:getneedlestyle}




To get NeedleStyle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getNeedleStyle(0, 0);
</script>{% endhighlight %}




### getPointerCapBorderWidth<span class="signature">()</span>
{:#methods:getpointercapborderwidth}




To get PointerCapBorderWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerCapBorderWidth(0);
</script>{% endhighlight %}




### getPointerCapRadius<span class="signature">()</span>
{:#methods:getpointercapradius}




To get PointerCapRadius

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerCapRadius(0);
</script>{% endhighlight %}




### getPointerLength<span class="signature">()</span>
{:#methods:getpointerlength}




To get PointerLength

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerLength(0, 0);
</script>{% endhighlight %}




### getPointerNeedleType<span class="signature">()</span>
{:#methods:getpointerneedletype}




To get PointerNeedleType

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerNeedleType(0, 0);
</script>{% endhighlight %}




### getPointerPlacement<span class="signature">()</span>
{:#methods:getpointerplacement}




To get PointerPlacement

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerPlacement(0, 0);
</script>{% endhighlight %}




### getPointerValue<span class="signature">()</span>
{:#methods:getpointervalue}




To get PointerValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerValue(0, 0);
</script>{% endhighlight %}




### getPointerWidth<span class="signature">()</span>
{:#methods:getpointerwidth}




To get PointerWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerWidth(0, 0);
</script>{% endhighlight %}




### getRangeBorderWidth<span class="signature">()</span>
{:#methods:getrangeborderwidth}




To get RangeBorderWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeBorderWidth(0, 0);
</script>{% endhighlight %}




### getRangeDistanceFromScale<span class="signature">()</span>
{:#methods:getrangedistancefromscale}




To get RangeDistanceFromScale

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeDistanceFromScale(0, 0);
</script>{% endhighlight %}




### getRangeEndValue<span class="signature">()</span>
{:#methods:getrangeendvalue}




To get RangeEndValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeEndValue(0, 0);
</script>{% endhighlight %}




### getRangePosition<span class="signature">()</span>
{:#methods:getrangeposition}




To get RangePosition

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangePosition(0, 0);
</script>{% endhighlight %}




### getRangeSize<span class="signature">()</span>
{:#methods:getrangesize}




To get RangeSize

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeSize(0, 0);
</script>{% endhighlight %}




### getRangeStartValue<span class="signature">()</span>
{:#methods:getrangestartvalue}




To get RangeStartValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeStartValue(0, 0);
</script>{% endhighlight %}




### getScaleBarSize<span class="signature">()</span>
{:#methods:getscalebarsize}




To get ScaleBarSize

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleBarSize(0);
</script>{% endhighlight %}




### getScaleBorderWidth<span class="signature">()</span>
{:#methods:getscaleborderwidth}




To get ScaleBorderWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{Width: 1.5} }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleBorderWidth(0);
</script>{% endhighlight %}




### getScaleDirection<span class="signature">()</span>
{:#methods:getscaledirection}




To get ScaleDirection

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleDirection(0);
</script>{% endhighlight %}




### getScaleRadius<span class="signature">()</span>
{:#methods:getscaleradius}




To get ScaleRadius

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleRadius(0);
</script>{% endhighlight %}




### getStartAngle<span class="signature">()</span>
{:#methods:getstartangle}




To get StartAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getStartAngle(0);
</script>{% endhighlight %}




### getSubGaugeLocation<span class="signature">()</span>
{:#methods:getsubgaugelocation}




To get SubGaugeLocation

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.GaugeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">GaugeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<div id="subGauge1">
</div> 
 
<script>
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 150 }}]}]});
circulargaugeObj.getSubGaugeLocation(0, 0);
</script>{% endhighlight %}




### getSweepAngle<span class="signature">()</span>
{:#methods:getsweepangle}




To get SweepAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getSweepAngle(0);
</script>{% endhighlight %}




### getTickAngle<span class="signature">()</span>
{:#methods:gettickangle}




To get TickAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickAngle(0, 0);
</script>{% endhighlight %}




### getTickDistanceFromScale<span class="signature">()</span>
{:#methods:gettickdistancefromscale}




To get TickDistanceFromScale

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickDistanceFromScale(0, 0);
</script>{% endhighlight %}




### getTickHeight<span class="signature">()</span>
{:#methods:gettickheight}




To get TickHeight

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickHeight(0, 0);
</script>{% endhighlight %}




### getTickPlacement<span class="signature">()</span>
{:#methods:gettickplacement}




To get TickPlacement

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickPlacement(0, 0);
</script>{% endhighlight %}




### getTickStyle<span class="signature">()</span>
{:#methods:gettickstyle}




To get TickStyle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickStyle(0, 0);
</script>{% endhighlight %}




### getTickWidth<span class="signature">()</span>
{:#methods:gettickwidth}




To get TickWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickWidth(0, 0);
</script>{% endhighlight %}




### includeFirstValue<span class="signature">()</span>
{:#methods:includefirstvalue}




To set includeFirstValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.includeFirstValue(0, 0, false);
</script>{% endhighlight %}




### redraw<span class="signature">()</span>
{:#methods:redraw}




Switching the redraw option for the gauge

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">redraw value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.redraw("scale");
</script>{% endhighlight %}




### setBackNeedleLength<span class="signature">()</span>
{:#methods:setbackneedlelength}




To set BackNeedleLength

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true }] }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setBackNeedleLength(0, 0, 10);
</script>{% endhighlight %}




### setCustomLabelAngle<span class="signature">()</span>
{:#methods:setcustomlabelangle}




To set CustomLabelAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.customLabelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font: { size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setCustomLabelAngle(0, 0, 10);
</script>{% endhighlight %}




### setCustomLabelValue<span class="signature">()</span>
{:#methods:setcustomlabelvalue}




To set CustomLabelValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.customLabelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{value:"MyLabel",position:{x:180,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setCustomLabelValue(0, 0, "CircularGauge");
</script>{% endhighlight %}




### setLabelAngle<span class="signature">()</span>
{:#methods:setlabelangle}




To set LabelAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.angle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">angle value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelAngle(0, 0, 10);
</script>{% endhighlight %}




### setLabelDistanceFromScale<span class="signature">()</span>
{:#methods:setlabeldistancefromscale}




To set LabelDistanceFromScale

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelDistanceFromScale(0, 0, 10);
</script>{% endhighlight %}




### setLabelPlacement<span class="signature">()</span>
{:#methods:setlabelplacement}




To set LabelPlacement

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelPlacement(0, 0, "far");
</script>{% endhighlight %}




### setLabelStyle<span class="signature">()</span>
{:#methods:setlabelstyle}




To set LabelStyle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.labelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelStyle(0, 0, "major");
</script>{% endhighlight %}




### setMajorIntervalValue<span class="signature">()</span>
{:#methods:setmajorintervalvalue}




To set MajorIntervalValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMajorIntervalValue(0, 10);
</script>{% endhighlight %}




### setMarkerDistanceFromScale<span class="signature">()</span>
{:#methods:setmarkerdistancefromscale}




To set MarkerDistanceFromScale

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMarkerDistanceFromScale(0, 0, 10);
</script>{% endhighlight %}




### setMarkerStyle<span class="signature">()</span>
{:#methods:setmarkerstyle}




To set MarkerStyle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMarkerStyle(0, 0, "rectangle");
</script>{% endhighlight %}




### setMaximumValue<span class="signature">()</span>
{:#methods:setmaximumvalue}




To set MaximumValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMaximumValue(0, 130);
</script>{% endhighlight %}




### setMinimumValue<span class="signature">()</span>
{:#methods:setminimumvalue}




To set MinimumValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMinimumValue(0, 10);
</script>{% endhighlight %}




### setMinorIntervalValue<span class="signature">()</span>
{:#methods:setminorintervalvalue}




To set MinorIntervalValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMinorIntervalValue(0, 2);
</script>{% endhighlight %}




### setNeedleStyle<span class="signature">()</span>
{:#methods:setneedlestyle}




To set NeedleStyle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setNeedleStyle(0, 0, "arrow");
</script>{% endhighlight %}




### setPointerCapBorderWidth<span class="signature">()</span>
{:#methods:setpointercapborderwidth}




To set PointerCapBorderWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerCapBorderWidth(0, 5);
</script>{% endhighlight %}




### setPointerCapRadius<span class="signature">()</span>
{:#methods:setpointercapradius}




To set PointerCapRadius

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerCapRadius(0, 10);
</script>{% endhighlight %}




### setPointerLength<span class="signature">()</span>
{:#methods:setpointerlength}




To set PointerLength

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerLength(0, 0, 90);
</script>{% endhighlight %}




### setPointerNeedleType<span class="signature">()</span>
{:#methods:setpointerneedletype}




To set PointerNeedleType

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerNeedleType(0, 0, "triangle");
</script>{% endhighlight %}




### setPointerPlacement<span class="signature">()</span>
{:#methods:setpointerplacement}




To set PointerPlacement

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerPlacement(0, 0,"near");
</script>{% endhighlight %}




### setPointerValue<span class="signature">()</span>
{:#methods:setpointervalue}




To set PointerValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerValue(0, 0, 10);
</script>{% endhighlight %}




### setPointerWidth<span class="signature">()</span>
{:#methods:setpointerwidth}




To set PointerWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerWidth(0, 0, 10);
</script>{% endhighlight %}




### setRangeBorderWidth<span class="signature">()</span>
{:#methods:setrangeborderwidth}




To set RangeBorderWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeBorderWidth(0, 0, 5);
</script>{% endhighlight %}




### setRangeDistanceFromScale<span class="signature">()</span>
{:#methods:setrangedistancefromscale}




To set RangeDistanceFromScale

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeDistanceFromScale(0, 0, 10);
</script>{% endhighlight %}




### setRangeEndValue<span class="signature">()</span>
{:#methods:setrangeendvalue}




To set RangeEndValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeEndValue(0, 0, 70);
</script>{% endhighlight %}




### setRangePosition<span class="signature">()</span>
{:#methods:setrangeposition}




To set RangePosition

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangePosition(0, 0, "far");
</script>{% endhighlight %}




### setRangeSize<span class="signature">()</span>
{:#methods:setrangesize}




To set RangeSize

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeSize(0, 0, 10);
</script>{% endhighlight %}




### setRangeStartValue<span class="signature">()</span>
{:#methods:setrangestartvalue}




To set RangeStartValue

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeStartValue(0, 0, 10);
</script>{% endhighlight %}




### setScaleBarSize<span class="signature">()</span>
{:#methods:setscalebarsize}




To set ScaleBarSize

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleBarSize(0, 160);
</script>{% endhighlight %}




### setScaleBorderWidth<span class="signature">()</span>
{:#methods:setscaleborderwidth}




To set ScaleBorderWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{width: 1.5} }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleBorderWidth(0, 3);
</script>{% endhighlight %}




### setScaleDirection<span class="signature">()</span>
{:#methods:setscaledirection}




To set ScaleDirection

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleDirection(0, "clockwise");
</script>{% endhighlight %}




### setScaleRadius<span class="signature">()</span>
{:#methods:setscaleradius}




To set ScaleRadius

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleRadius(0, 140);
</script>{% endhighlight %}




### setStartAngle<span class="signature">()</span>
{:#methods:setstartangle}




To set StartAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setStartAngle(0, 10);
</script>{% endhighlight %}




### setSubGaugeLocation<span class="signature">()</span>
{:#methods:setsubgaugelocation}




To set SubGaugeLocation

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.GaugeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">GaugeIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
 
<div id="subGauge1">
</div> 
<script>
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 150 }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setSubGaugeLocation(0, 0, {x:50,y:100});
</script>{% endhighlight %}




### setSweepAngle<span class="signature">()</span>
{:#methods:setsweepangle}




To set SweepAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setSweepAngle(0, 220);
</script>{% endhighlight %}




### setTickAngle<span class="signature">()</span>
{:#methods:settickangle}




To set TickAngle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickAngle(0, 0, 10);
</script>{% endhighlight %}




### setTickDistanceFromScale<span class="signature">()</span>
{:#methods:settickdistancefromscale}




To set TickDistanceFromScale

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickDistanceFromScale(0, 0, 15);
</script>{% endhighlight %}




### setTickHeight<span class="signature">()</span>
{:#methods:settickheight}




To set TickHeight

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickHeight(0, 0, 10);
</script>{% endhighlight %}




### setTickPlacement<span class="signature">()</span>
{:#methods:settickplacement}




To set TickPlacement

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script> 
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickPlacement(0, 0, "near");
</script>{% endhighlight %}




### setTickStyle<span class="signature">()</span>
{:#methods:settickstyle}




To set TickStyle

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickStyle(0, 0, "minor");
</script>{% endhighlight %}




### setTickWidth<span class="signature">()</span>
{:#methods:settickwidth}




To set TickWidth

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.tickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickWidth(0, 0, 5);
</script>{% endhighlight %}



## Events




### drawCustomLabel
{:#events:drawcustomlabel}




Triggers while the custom labels are being drawn on the gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the custom label</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the custom label belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the custom label style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.customLabelElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current custom label element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.customLabelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the custom label.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   drawCustomLabel: function (args) {}
});
</script>{% endhighlight %}




### drawIndicators
{:#events:drawindicators}




Triggers while the indicators are being started to drawn on the gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the indicator</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the indicator belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the indicator style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.indicatorElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current indicator element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.indicatorIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the indicator.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   drawIndicators: function (args) {}
});
</script>{% endhighlight %}




### drawLabels
{:#events:drawlabels}




Triggers while the labels are being drawn on the gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the labels</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the label belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the label style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.label{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the label object of the gauge.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
angle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the labels.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current label element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the label.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.pointerValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the label.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   drawLabels: function (args) {}
});
</script>{% endhighlight %}




### drawPointerCap
{:#events:drawpointercap}




Triggers while the pointer cap is being drawn on the gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer cap.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer cap style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   drawPointerCap: function (args) {}
});
</script>{% endhighlight %}




### drawPointers
{:#events:drawpointers}




Triggers while the pointers are being drawn on the gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.pointer{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer object of the gauge.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
angle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   drawPointers: function (args) {}
});
</script>{% endhighlight %}




### drawRange
{:#events:drawrange}




Triggers when the ranges begin to be getting drawn on the gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the range</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the range belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the range style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.rangeElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current range element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the range.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   drawRange: function (args) {}
});
</script>{% endhighlight %}




### drawTicks
{:#events:drawticks}




Triggers while the ticks are being drawn on the gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the ticks</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the tick belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the ticks style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.tick{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the tick object of the gauge.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
angle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the tick.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current tick element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the tick.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.pointerValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the label value of the tick.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   drawTicks: function (args) {}
});
</script>{% endhighlight %}




### load
{:#events:load}




Triggers while the gauge start to Load.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">cancel</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type"><a href="Model.html">Model</a></span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">scaleElement</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">context</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CircularGauge1"></div> 
 
<script>
$("#CircularGauge1").ejCircularGauge({
   load: function (args) {}
});
</script> {% endhighlight %}




### mouseClick
{:#events:mouseclick}




Triggers when the left mouse button is clicked.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.pointer{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer object
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
angle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the pointer.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   mouseClick: function (args) {}
});
</script>{% endhighlight %}




### mouseClickMove
{:#events:mouseclickmove}




Triggers when clicking and dragging the mouse pointer over the gauge pointer.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.pointer{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer object
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
angle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the pointer.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   mouseClickMove: function (args) {}
});
</script>{% endhighlight %}




### mouseClickUp
{:#events:mouseclickup}




Triggers when the mouse click is released.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.pointer{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer object
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
angle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the pointer.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   mouseClickUp: function (args) {}
});
</script>{% endhighlight %}




### renderComplete
{:#events:rendercomplete}




Triggers when the rendering of the gauge is completed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   renderComplete: function (args) {}
});
</script>{% endhighlight %}



