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
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">For seting the Circular gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$(function () {
        $("#CoreCircularGauge").ejCircularGauge({
        });
    });
&lt;/script&gt;</code>
</pre>



Requires
{:.require}


* module:jQuery

* module:ej.common.all

* module:excanvas.js


## Members




### animationSpeed<span class="type-signature type number">number</span>
{:#animationSpeed}




Specifies animationSpeed of circular gauge


Default Value:
{:.param}



* 500




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
        $("#CoreCircularGauge").ejCircularGauge({ animationSpeed: 500,scales: [{ pointers: [{ value: 50 }] }] });
&lt;/script&gt;</code>
</pre>



### backgroundColor<span class="type-signature type string">string</span>
{:#backgroundColor}




Specifies the backgroundcolor of circular gauge.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code>                     
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({  backgroundColor : "#F234F4" });
&lt;/script&gt;</code>
</pre>



### distanceFromCorner<span class="type-signature type enum">enum</span>
{:#distanceFromCorner}




Specify distanceFromCorner value of circular gauge


Default Value:
{:.param}



* center




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({  gaugePosition:"center", distanceFromCorner :25});
&lt;/script&gt;</code>
</pre>



### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#enableAnimation}




Specify animate value of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                   
$("#CoreCircularGauge").ejCircularGauge({ enableAnimation: true,scales: [{ pointers: [{ value: 50 }] }] });
&lt;/script&gt;</code>
</pre>



### enableResize<span class="type-signature type boolean">boolean</span>
{:#enableResize}




Specify enableResize value of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({  enableResize : true });
&lt;/script&gt;</code>
</pre>



### frame<span class="type-signature type object">object</span>
{:#frame}




Specify the frame of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
$("#CoreCircularGauge").ejCircularGauge({ frame:{frameType:ej.datavisualization.CircularGauge.Frame.FullCircle, backgroundImageUrl:"", halfCircleFrameStartAngle:180, halfCircleFrameEndAngle:360} });
&lt;/script&gt;</code>
</pre>



### frame.backgroundImageUrl<span class="type-signature type string">string</span>
{:#frame-backgroundImageUrl}




Specify the url of the frame background image for circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({  frame:{backgroundImageUrl : "Sun.jpg" }});
&lt;/script&gt;</code>
</pre>



### frame.frameType<span class="type-signature type enum">enum</span>
{:#frame-frameType}




Specifies the frameType of circular gauge. See <a href="global.html#Frame">Frame</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.Frame.FullCircle




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({  frame:{frameType : "halfcircle"} });
&lt;/script&gt;</code>
</pre>



### frame.halfCircleFrameEndAngle<span class="type-signature type number">number</span>
{:#frame-halfCircleFrameEndAngle}




Specifies the end angle for the half circular frame.


Default Value:
{:.param}



* 360




Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ frame:{frameType : "halfCircle",halfCircleFrameEndAngle: 270}});
&lt;/script&gt;</code>
</pre>



### frame.halfCircleFrameStartAngle<span class="type-signature type number">number</span>
{:#frame-halfCircleFrameStartAngle}




Specifies the start angle for the half circular frame.


Default Value:
{:.param}



* 180




Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ frame:{frameType : "halfcircle",halfCircleFrameStartAngle: 0} });
&lt;/script&gt;</code>
</pre>



### gaugePosition<span class="type-signature type enum">enum</span>
{:#gaugePosition}




Specify gaugePosition value of circular gauge See GaugePosition


Default Value:
{:.param}



* center




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({  gaugePosition:"center" });
&lt;/script&gt;</code>
</pre>



### height<span class="type-signature type number">number</span>
{:#height}




Specifies the height of circular gauge.


Default Value:
{:.param}



* 360




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ height: 400 });
&lt;/script&gt;</code>
</pre>



### interiorGradient<span class="type-signature type object">object</span>
{:#interiorGradient}




Specifies the interiorGradient of circular gauge.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code>                     
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ interiorGradient: { colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } }); 
&lt;/script&gt;</code>
</pre>



### isRadialGradient<span class="type-signature type boolean">boolean</span>
{:#isRadialGradient}




Specify isRadialGradient value of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({  isRadialGradient : true });
&lt;/script&gt;</code>
</pre>



### maximum<span class="type-signature type number">number</span>
{:#maximum}




Specifies the maximum value of circular gauge.


Default Value:
{:.param}



* 100




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ maximum: 120 });
&lt;/script&gt;</code>
</pre>



### minimum<span class="type-signature type number">number</span>
{:#minimum}




Specifies the minimum value of circular gauge.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ minimum: 10 });
&lt;/script&gt;</code>
</pre>



### outerCustomLabelPosition<span class="type-signature type enum">enum</span>
{:#outerCustomLabelPosition}




Specify outerCustomLabelPosition value of circular gauge See <a href="global.html#OuterCustomLabelPosition">OuterCustomLabelPosition</a>


Default Value:
{:.param}



* bottom




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({  outerCustomLabelPosition:"top" });
&lt;/script&gt;</code>
</pre>



### radius<span class="type-signature type number">number</span>
{:#radius}




Specifies the radius of circular gauge.


Default Value:
{:.param}



* 180




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ radius: 100 });
&lt;/script&gt;</code>
</pre>



### readOnly<span class="type-signature type boolean">boolean</span>
{:#readOnly}




Specify readonly value of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code>                     
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({  readOnly : false });
&lt;/script&gt;</code>
</pre>



### scales<span class="type-signature type object">object</span>
{:#scales}




Specify the pointers, ticks, labels, indicators, ranges of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{width: 1.5} }] });
&lt;/script&gt;</code>
</pre>



### scales.backgroundColor<span class="type-signature type string">string</span>
{:#scales-backgroundColor}




Specify backgroundColor for the scale of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, backgroundColor: "#1BA1E2" }] });
&lt;/script&gt;</code>
</pre>



### scales.border<span class="type-signature type object">object</span>
{:#scales-border}




Specify border for scales of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ border:{color:null, width:1.5 }}] });
&lt;/script&gt;</code>
</pre>



### scales.border.color<span class="type-signature type string">string</span>
{:#scales-border-color}




Specify border color for scales of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true,  border:[{color: "#1BA1E2" }]}] });
&lt;/script&gt;</code>
</pre>



### scales.border.width<span class="type-signature type number">number</span>
{:#scales-border-width}




Specify border width of circular gauge


Default Value:
{:.param}



* 1.5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, border:{width: 1.5} }] });
&lt;/script&gt;</code>
</pre>



### scales.direction<span class="type-signature type enum">enum</span>
{:#scales-direction}




Specify scale direction of circular gauge. See <a href="global.html#Directions">Directions</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.Directions.Clockwise




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ direction: "counterclockwise" }] });
&lt;/script&gt;</code>
</pre>



### scales.indicators<span class="type-signature type array">Array</span>
{:#scales-indicators}




Specify representating state of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  height: 30,width: 10,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243", borderColor: "#5DF243", text: "", textColor: "#870505" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608", borderColor: "#145608", text: "", textColor: "#870505" }]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.height<span class="type-signature type number">number</span>
{:#scales-indicators-height}




Specify indicator height of circular gauge


Default Value:
{:.param}



* 15




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  height: 30,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.imageUrl<span class="type-signature type string">string</span>
{:#scales-indicators-imageUrl}




Specify imageUrl of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "image",value: 0,imageUrl:"Sun.jpeg",position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.position<span class="type-signature type object">object</span>
{:#scales-indicators-position}




Specify position of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y: 150 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.position.x<span class="type-signature type number">number</span>
{:#scales-indicators-position-x}




Specify x-axis of position of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185,y:0 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.position.y<span class="type-signature type number">number</span>
{:#scales-indicators-position-y}




Specify y-axis of position of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x:0,y: 185 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.stateRanges<span class="type-signature type array">Array</span>
{:#scales-indicators-stateRanges}




Specify the various states of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.stateRanges.backgroundColor<span class="type-signature type string">string</span>
{:#scales-indicators-stateRanges-backgroundColor}




Specify backgroundColor for indicator of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "Red" },
  { endValue: 200, startValue: 70, backgroundColor: "Yellow"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.stateRanges.borderColor<span class="type-signature type string">string</span>
{:#scales-indicators-stateRanges-borderColor}




Specify borderColor for indicator of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243",borderColor:"Red" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608", borderColor:"yellow"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.stateRanges.endValue<span class="type-signature type number">number</span>
{:#scales-indicators-stateRanges-endValue}




Specify end value for each specified state of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.stateRanges.font<span class="type-signature type object">object</span>
{:#scales-indicators-stateRanges-font}




Specify value of the font as the indicator when the indicator style is set with the value "text" of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
$("#CoreCircularGauge").ejCircularGauge({
scales: [{showIndicators: true, indicators: [{
width: 30, type: "text", value: 0, position: { x: 185, y: 300 },
stateRanges: [{ endValue: 70, startValue: 0, text: "staterange1" },
{ endValue: 200, startValue: 70, text: "staterange1", font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" } }]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.stateRanges.startValue<span class="type-signature type number">number</span>
{:#scales-indicators-stateRanges-startValue}




Specify start value for each specified state of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.stateRanges.text<span class="type-signature type string">string</span>
{:#scales-indicators-stateRanges-text}




Specify value of the text as the indicator when the indicator style is set with the value "text" of circular gauge


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
$("#CoreCircularGauge").ejCircularGauge({
scales: [{showIndicators: true, indicators: [{
width: 30, type: "text", value: 0, position: { x: 185, y: 300 },
stateRanges: [{ endValue: 70, startValue: 0, text: "staterange1" },
{ endValue: 200, startValue: 70, text: "staterange1" }]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.stateRanges.textColor<span class="type-signature type string">string</span>
{:#scales-indicators-stateRanges-textColor}




Specify value of the textColor as the indicator when the indicator style is set with the value "text" of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({
scales: [{showIndicators: true, indicators: [{
width: 30, type: "text", value: 0, position: { x: 185, y: 300 },
stateRanges: [{ endValue: 70, startValue: 0, text: "staterange1", textColor: "Yellow" },
{ endValue: 200, startValue: 70, text: "staterange1", textColor: "Yellow" }]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.type<span class="type-signature type enum">enum</span>
{:#scales-indicators-type}




Specify indicator style of circular gauge. See <a href="global.html#IndicatorType">IndicatorType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.IndicatorType.Circle




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.indicators.width<span class="type-signature type number">number</span>
{:#scales-indicators-width}




Specify indicator width of circular gauge


Default Value:
{:.param}



* 15




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
&lt;/script&gt;</code>
</pre>



### scales.labels<span class="type-signature type array">Array</span>
{:#scales-labels}




Specify the text values displayed in a meaningful manner alongside the ticks of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ angle: 10, opacity: 0.4 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.angle<span class="type-signature type number">number</span>
{:#scales-labels-angle}




Specify the angle for the labels of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ angle: 10 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.autoAngle<span class="type-signature type boolean">boolean</span>
{:#scales-labels-autoAngle}




Specify labels autoAngle value of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels:[{autoAngle: true}] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.color<span class="type-signature type string">string</span>
{:#scales-labels-color}




Specify label color of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ color: "Red" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.distanceFromScale<span class="type-signature type number">number</span>
{:#scales-labels-distanceFromScale}




Specify distanceFromScale value for labels of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ distanceFromScales: 10 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.font<span class="type-signature type object">object</span>
{:#scales-labels-font}




Specify font for labels of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { size: "12px", fontFamily: "Segou", fontStyle: "Bold" } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.font.fontFamily<span class="type-signature type string">String</span>
{:#scales-labels-font-fontFamily}




Specify font fontFamily for labels of circular gauge


Default Value:
{:.param}



* "Arial"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { fontFamily: "Arial" } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.font.fontStyle<span class="type-signature type string">string</span>
{:#scales-labels-font-fontStyle}




Specify font Style for labels of circular gauge


Default Value:
{:.param}



* "Bold"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { fontStyle: "Bold" } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.font.size<span class="type-signature type string">string</span>
{:#scales-labels-font-size}




Specify font size for labels of circular gauge


Default Value:
{:.param}



* "11px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { size: "12px" } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.includeFirstValue<span class="type-signature type boolean">boolean</span>
{:#scales-labels-includeFirstValue}




Specify includeFirstValue of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ includeFirstValue: false }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.opacity<span class="type-signature type number">number</span>
{:#scales-labels-opacity}




Specify opacity value for labels of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ opacity: 0.4 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.placement<span class="type-signature type enum">enum</span>
{:#scales-labels-placement}




Specify label placement of circular gauge. See <a href="global.html#LabelPlacement">LabelPlacement</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.LabelPlacement.Near




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ placement: "near" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.type<span class="type-signature type enum">enum</span>
{:#scales-labels-type}




Specify label Style of circular gauge. See <a href="global.html#LabelType">LabelType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.LabelType.Major




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ type: "major" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.unitText<span class="type-signature type string">string</span>
{:#scales-labels-unitText}




Specify unitText of circular gauge


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ unitText: "kmph" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.labels.unitTextPosition<span class="type-signature type enum">enum</span>
{:#scales-labels-unitTextPosition}




Specify unitTextPosition of circular gauge. See UnitTextPosition


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.LabelType.Back




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ unitText: "kmph",unitTextPosition: "front" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.majorIntervalValue<span class="type-signature type number">number</span>
{:#scales-majorIntervalValue}




Specify majorIntervalValue of circular gauge


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ majorIntervalValue: 5 }] });
&lt;/script&gt;</code>
</pre>



### scales.maximum<span class="type-signature type number">number</span>
{:#scales-maximum}




Specify maximum scale value of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ maximum: 200 }] });
&lt;/script&gt;</code>
</pre>



### scales.minimum<span class="type-signature type number">number</span>
{:#scales-minimum}




Specify minimum scale value of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ minimum: 20 }] });
&lt;/script&gt;</code>
</pre>



### scales.minorIntervalValue<span class="type-signature type number">number</span>
{:#scales-minorIntervalValue}




Specify minorIntervalValue of circular gauge


Default Value:
{:.param}



* 2




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ minorIntervalValue: 1 }] });
&lt;/script&gt;</code>
</pre>



### scales.opacity<span class="type-signature type number">number</span>
{:#scales-opacity}




Specify opacity value of circular gauge


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code>     
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, opacity:0.5 }] });
&lt;/script&gt;</code>
</pre>



### scales.pointerCap<span class="type-signature type object">object</span>
{:#scales-pointerCap}




Specify pointer cap of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{radius: 7, borderWidth:3, interiorGradient:null, borderColor:null } }] });
&lt;/script&gt;</code>
</pre>



### scales.pointerCap.backgroundColor<span class="type-signature type string">string</span>
{:#scales-pointerCap-backgroundColor}




Specify cap backgroundColor of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap: {backgroundColor: "Green"} }] });
&lt;/script&gt;</code>
</pre>



### scales.pointerCap.borderColor<span class="type-signature type string">string</span>
{:#scales-pointerCap-borderColor}




Specify cap borderColor of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap: {borderColor: "Brown" }}] });
&lt;/script&gt;</code>
</pre>



### scales.pointerCap.borderWidth<span class="type-signature type number">number</span>
{:#scales-pointerCap-borderWidth}




Specify pointerCap borderWidth value of circular gauge


Default Value:
{:.param}



* 3




Example
{:.example}

<pre class="prettyprint">
<code>     
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{borderWidth: 8 } }] });
&lt;/script&gt;</code>
</pre>



### scales.pointerCap.interiorGradient<span class="type-signature type object">Object</span>
{:#scales-pointerCap-interiorGradient}




Specify cap interiorGradient value of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code>             
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{interiorGradient: {colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}}] });
&lt;/script&gt;</code>
</pre>



### scales.pointerCap.radius<span class="type-signature type number">number</span>
{:#scales-pointerCap-radius}




Specify pointerCap Radius value of circular gauge


Default Value:
{:.param}



* 7




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{radius: 10} }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers<span class="type-signature type array">Array</span>
{:#scales-pointers}




Specify pointers value of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}

<pre class="prettyprint">
<code>     
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ distanceFromScale: 0, showBackNeedle: false }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.backgroundColor<span class="type-signature type string">string</span>
{:#scales-pointers-backgroundColor}




Specify backgroundColor for the pointer of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ backgroundColor: "#1A1A1A" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.backNeedleLength<span class="type-signature type number">number</span>
{:#scales-pointers-backNeedleLength}




Specify backNeedleLength of circular gauge


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true, backNeedleLength: 10 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.border<span class="type-signature type object">object</span>
{:#scales-pointers-border}




Specify the border for pointers of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers:[{border:{color:null, width:1.5 }}]}] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.border.color<span class="type-signature type string">string</span>
{:#scales-pointers-border-color}




Specify border color for pointer of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ border:{color: "#1A1A1A"} }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.border.width<span class="type-signature type number">number</span>
{:#scales-pointers-border-width}




Specify border width for pointers of circular gauge


Default Value:
{:.param}



* 1.5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ border:{width: 1.5 }}] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.distanceFromScale<span class="type-signature type number">number</span>
{:#scales-pointers-distanceFromScale}




Specify distanceFromScale value for pointers of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ distanceFromScale: 10 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.gradients<span class="type-signature type object">Object</span>
{:#scales-pointers-gradients}




Specify pointer gradients of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ gradients: {colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.length<span class="type-signature type number">number</span>
{:#scales-pointers-length}




Specify pointer length of circular gauge


Default Value:
{:.param}



* 150




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ length: 50 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.markerType<span class="type-signature type enum">enum</span>
{:#scales-pointers-markerType}




Specify marker Style value of circular gauge. See <a href="global.html#MarkerType">MarkerType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.MarkerType.Rectangle




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.needleType<span class="type-signature type enum">enum</span>
{:#scales-pointers-needleType}




Specify needle Style value of circular gauge. See <a href="global.html#NeedleType">NeedleType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.NeedleType.Triangle




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ needleType: "triangle" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.opacity<span class="type-signature type number">number</span>
{:#scales-pointers-opacity}




Specify opacity value for pointer of circular gauge


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ opacity: 0.3 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.placement<span class="type-signature type enum">enum</span>
{:#scales-pointers-placement}




Specify pointer Placement value of circular gauge. See <a href="global.html#PointerPlacement">PointerPlacement</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.PointerPlacement.Near




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ placement: "far" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText<span class="type-signature type object">object</span>
{:#scales-pointers-pointerValueText}




Specify pointer value text of circular gauge.


Default Value:
{:.param}



* Object




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: false, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.angle<span class="type-signature type number">number</span>
{:#scales-pointers-pointerValueText-angle}




Specify pointer text angle of circular gauge.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 0.5, autoAngle: false, angle: 30, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.autoAngle<span class="type-signature type boolean">boolean</span>
{:#scales-pointers-pointerValueText-autoAngle}




Specify pointer text auto angle of circular gauge.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 0.5, autoAngle: true, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.color<span class="type-signature type string">string</span>
{:#scales-pointers-pointerValueText-color}




Specify pointer value text color of circular gauge.


Default Value:
{:.param}



* #8c8c8c




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 1, autoAngle: false, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.distance<span class="type-signature type number">number</span>
{:#scales-pointers-pointerValueText-distance}




Specify pointer value text distance from pointer of circular gauge.


Default Value:
{:.param}



* 20




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.font<span class="type-signature type object">object</span>
{:#scales-pointers-pointerValueText-font}




Specify pointer value text font option of circular gauge.


Default Value:
{:.param}



* object




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.font.fontFamily<span class="type-signature type string">string</span>
{:#scales-pointers-pointerValueText-font-fontFamily}




Specify pointer value text font family of circular gauge.


Default Value:
{:.param}



* Arial




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "12px", fontFamily: "Seogo UI", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.font.fontStyle<span class="type-signature type string">string</span>
{:#scales-pointers-pointerValueText-font-fontStyle}




Specify pointer value text font style of circular gauge.


Default Value:
{:.param}



* Bold




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "12px", fontFamily: "Seogo UI", fontStyle: "Normal" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.font.size<span class="type-signature type string">string</span>
{:#scales-pointers-pointerValueText-font-size}




Specify pointer value text size of circular gauge.


Default Value:
{:.param}



* 11px




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "12px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.opacity<span class="type-signature type number">number</span>
{:#scales-pointers-pointerValueText-opacity}




Specify pointer value text opacity of circular gauge.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 0.5, autoAngle: false, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.pointerValueText.showValue<span class="type-signature type boolean">boolean</span>
{:#scales-pointers-pointerValueText-showValue}




enable pointer value text visibility of circular gauge.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.showBackNeedle<span class="type-signature type boolean">boolean</span>
{:#scales-pointers-showBackNeedle}




Specify showBackNeedle value of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true, backNeedleLength: 10 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.type<span class="type-signature type enum">enum</span>
{:#scales-pointers-type}




Specify pointer type value of circular gauge. See <a href="global.html#PointerType">PointerType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.PointerType.Needle




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.value<span class="type-signature type number">number</span>
{:#scales-pointers-value}




Specify value of the pointer of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ value: 50 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.pointers.width<span class="type-signature type number">number</span>
{:#scales-pointers-width}




Specify pointer width of circular gauge


Default Value:
{:.param}



* 7




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ width: 7 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.radius<span class="type-signature type number">number</span>
{:#scales-radius}




Specify scale radius of circular gauge


Default Value:
{:.param}



* 170




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, radius: 100 }] });
&lt;/script&gt;</code>
</pre>



### scales.ranges<span class="type-signature type array">Array</span>
{:#scales-ranges}




Specify ranges value of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true [{ ranges: [{ distanceFromScale: 25, size: 5}] }] }]});
&lt;/script&gt;</code>
</pre>



### scales.ranges.backgroundColor<span class="type-signature type string">string</span>
{:#scales-ranges-backgroundColor}




Specify backgroundColor for the ranges of circular gauge


Default Value:
{:.param}



* "#32b3c6"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,backgroundColor: "Red" }]  }]});
&lt;/script&gt;</code>
</pre>



### scales.ranges.border<span class="type-signature type object">object</span>
{:#scales-ranges-border}




Specify border for ranges of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ ranges:[{border:{color:null, width:1.5 }}]}] });
&lt;/script&gt;</code>
</pre>



### scales.ranges.border.color<span class="type-signature type string">string</span>
{:#scales-ranges-border-color}




Specify border color for ranges of circular gauge


Default Value:
{:.param}



* "#32b3c6"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,border:{color: "#32b3c6"} }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ranges.border.width<span class="type-signature type number">number</span>
{:#scales-ranges-border-width}




Specify border width for ranges of circular gauge


Default Value:
{:.param}



* 1.5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,distanceFromScale: -25,border:{width: 1.5} }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ranges.distanceFromScale<span class="type-signature type number">number</span>
{:#scales-ranges-distanceFromScale}




Specify distanceFromScale value for ranges of circular gauge


Default Value:
{:.param}



* 25




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                          
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
&lt;/script&gt;</code>
</pre>



### scales.ranges.endValue<span class="type-signature type number">number</span>
{:#scales-ranges-endValue}




Specify endValue for ranges of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true, ranges: [{ startValue: 10, endValue: 100,distanceFromScale: -25 }] }]});
&lt;/script&gt;</code>
</pre>



### scales.ranges.endWidth<span class="type-signature type number">number</span>
{:#scales-ranges-endWidth}




Specify endWidth for ranges of circular gauge


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
&lt;/script&gt;</code>
</pre>



### scales.ranges.gradients<span class="type-signature type object">object</span>
{:#scales-ranges-gradients}




Specify range gradients of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{startValue: 10, endValue: 100, gradients: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}] }]});
&lt;/script&gt;</code>
</pre>



### scales.ranges.opacity<span class="type-signature type number">number</span>
{:#scales-ranges-opacity}




Specify opacity value for ranges of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,distanceFromScale: -25,opacity: 0.5 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ranges.placement<span class="type-signature type enum">enum</span>
{:#scales-ranges-placement}




Specify placement of circular gauge. See <a href="global.html#RangePlacement">RangePlacement</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.RangePlacement.Near




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70,placement: "center"}]}]});
&lt;/script&gt;</code>
</pre>



### scales.ranges.size<span class="type-signature type number">number</span>
{:#scales-ranges-size}




Specify size of the range value of circular gauge


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70,size:5}]}]});
&lt;/script&gt;</code>
</pre>



### scales.ranges.startValue<span class="type-signature type number">number</span>
{:#scales-ranges-startValue}




Specify startValue for ranges of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
&lt;/script&gt;</code>
</pre>



### scales.ranges.startWidth<span class="type-signature type number">number</span>
{:#scales-ranges-startWidth}




Specify startWidth of circular gauge


Default Value:
{:.param}



* [Array.number] scale.ranges.startWidth = 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,distanceFromScale: -25 }] }]});
&lt;/script&gt;</code>
</pre>



### scales.shadowOffset<span class="type-signature type number">number</span>
{:#scales-shadowOffset}




Specify shadowOffset value of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ shadowOffset: 1}] });
&lt;/script&gt;</code>
</pre>



### scales.showIndicators<span class="type-signature type boolean">boolean</span>
{:#scales-showIndicators}




Specify showIndicators of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showIndicators: false }] });
&lt;/script&gt;</code>
</pre>



### scales.showLabels<span class="type-signature type boolean">boolean</span>
{:#scales-showLabels}




Specify showLabels of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showLabels: true }] });
&lt;/script&gt;</code>
</pre>



### scales.showPointers<span class="type-signature type boolean">boolean</span>
{:#scales-showPointers}




Specify showPointers of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showPointers: true }] });
&lt;/script&gt;</code>
</pre>



### scales.showRanges<span class="type-signature type boolean">boolean</span>
{:#scales-showRanges}




Specify showRanges of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showRanges: false }] });
&lt;/script&gt;</code>
</pre>



### scales.showScaleBar<span class="type-signature type boolean">boolean</span>
{:#scales-showScaleBar}




Specify showScaleBar of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true }] });
&lt;/script&gt;</code>
</pre>



### scales.showTicks<span class="type-signature type boolean">boolean</span>
{:#scales-showTicks}




Specify showTicks of circular gauge


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showTicks: true }] });
&lt;/script&gt;</code>
</pre>



### scales.size<span class="type-signature type number">number</span>
{:#scales-size}




Specify scaleBar size of circular gauge


Default Value:
{:.param}



* 6




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, size: 6 }] });
&lt;/script&gt;</code>
</pre>



### scales.startAngle<span class="type-signature type number">number</span>
{:#scales-startAngle}




Specify startAngle of circular gauge


Default Value:
{:.param}



* 115




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ startAngle: 90 }] });
&lt;/script&gt;</code>
</pre>



### scales.subGauges<span class="type-signature type array">Array</span>
{:#scales-subGauges}




Specify subGauge of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;div id="subGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 200, y: 150 }}]}]});
&lt;/script&gt;</code>
</pre>



### scales.subGauges.height<span class="type-signature type number">number</span>
{:#scales-subGauges-height}




Specify subGauge Height of circular gauge


Default Value:
{:.param}



* 150




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;div id="subGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 100 }}]}]});
&lt;/script&gt;</code>
</pre>



### scales.subGauges.position<span class="type-signature type object">object</span>
{:#scales-subGauges-position}




Specify position for sub-gauge of circular gauge


Default Value:
{:.param}



* Object




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;div id="subGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 200, y: 150 }}]}]});
&lt;/script&gt;</code>
</pre>



### scales.subGauges.position.x<span class="type-signature type number">number</span>
{:#scales-subGauges-position-x}




Specify x-axis position for sub-gauge of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;div id="subGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 200, y: 0 }}]}]});
&lt;/script&gt;</code>
</pre>



### scales.subGauges.position.y<span class="type-signature type number">number</span>
{:#scales-subGauges-position-y}




Specify y-axis position for sub-gauge of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;div id="subGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 0, y: 150 }}]}]});
&lt;/script&gt;</code>
</pre>



### scales.subGauges.width<span class="type-signature type number">number</span>
{:#scales-subGauges-width}




Specify subGauge Width of circular gauge


Default Value:
{:.param}



* 150




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;div id="subGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 300,position: { x: 200, y: 150 }}]}]});
&lt;/script&gt;</code>
</pre>



### scales.sweepAngle<span class="type-signature type number">number</span>
{:#scales-sweepAngle}




Specify sweepAngle of circular gauge


Default Value:
{:.param}



* 310




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ sweepAngle: 200 }] });
&lt;/script&gt;</code>
</pre>



### scales.ticks<span class="type-signature type array">Array</span>
{:#scales-ticks}




Specify ticks of circular gauge


Default Value:
{:.param}



* Array




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ angle: 10, distanceFromScale: 10 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ticks.angle<span class="type-signature type number">number</span>
{:#scales-ticks-angle}




Specify the angle for the ticks of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ angle: 10 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ticks.color<span class="type-signature type string">string</span>
{:#scales-ticks-color}




Specify tick color of circular gauge


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ color: "#777777" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ticks.distanceFromScale<span class="type-signature type number">number</span>
{:#scales-ticks-distanceFromScale}




Specify distanceFromScale value for ticks of circular gauge


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ distanceFromScale: 10 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ticks.height<span class="type-signature type number">number</span>
{:#scales-ticks-height}




Specify tick height of circular gauge


Default Value:
{:.param}



* 16




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ height: 16 }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ticks.placement<span class="type-signature type enum">enum</span>
{:#scales-ticks-placement}




Specify tick placement of circular gauge. See <a href="global.html#TickPlacement">TickPlacement</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.TickPlacement.Near




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ placement: "near" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ticks.type<span class="type-signature type enum">enum</span>
{:#scales-ticks-type}




Specify tick Style of circular gauge. See <a href="global.html#TickType">TickType</a>


Default Value:
{:.param}



* ej.datavisualization.CircularGauge.TickPlacement.Major




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ type: "major" }] }] });
&lt;/script&gt;</code>
</pre>



### scales.ticks.width<span class="type-signature type number">number</span>
{:#scales-ticks-width}




Specify tick width of circular gauge


Default Value:
{:.param}



* 3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ width: 3 }] }] });
&lt;/script&gt;</code>
</pre>



### theme<span class="type-signature type string">string</span>
{:#theme}




Specify the theme of circular gauge.


Default Value:
{:.param}



* "flatlight"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
        $("#CoreCircularGauge").ejCircularGauge({  theme : "flatlight" });
&lt;/script&gt;</code>
</pre>



### tooltip<span class="type-signature type object">object</span>
{:#tooltip}




Specify tooltip option of circular gauge


Default Value:
{:.param}



* object




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showLabelTooltip: true,showCustomLabelTooltip: true,templateID: null} });
&lt;/script&gt;</code>
</pre>



### tooltip.showCustomLabelTooltip<span class="type-signature type boolean">boolean</span>
{:#tooltip-showCustomLabelTooltip}




enable showCustomLabelTooltip of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showCustomLabelTooltip: true} });
&lt;/script&gt;</code>
</pre>



### tooltip.showLabelTooltip<span class="type-signature type boolean">boolean</span>
{:#tooltip-showLabelTooltip}




enable showLabelTooltip of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showLabelTooltip: true} });
&lt;/script&gt;</code>
</pre>



### tooltip.templateID<span class="type-signature type string">string</span>
{:#tooltip-templateID}




Specify tooltip templateID of circular gauge


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showLabelTooltip: true, templateID: "template1"} });
&lt;/script&gt;</code>
</pre>



### value<span class="type-signature type number">number</span>
{:#value}




Specifies the value of circular gauge.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ value: 30 });
&lt;/script&gt;</code>
</pre>



### width<span class="type-signature type number">number</span>
{:#width}




Specifies the width of circular gauge.


Default Value:
{:.param}



* 360




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ width: 400 });
&lt;/script&gt;</code>
</pre>


## Methods




### destroy<span class="signature">()</span>
{:#destroy}




destroy the circular gauge widget. all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.destroy();
&lt;/script&gt;</code>
</pre>



### exportImage<span class="signature">()</span>
{:#exportImage}




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
<td class="name"><code>argument.fileName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fileName for the Image</td>
</tr>
<tr>
<td class="name"><code>argument.fileType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fileType for the Image</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.exportImage("myImage","jpeg");
&lt;/script&gt;</code>
</pre>



### getBackNeedleLength<span class="signature">()</span>
{:#getBackNeedleLength}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true }] }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getBackNeedleLength(0, 0);
&lt;/script&gt;</code>
</pre>



### getCustomLabelAngle<span class="signature">()</span>
{:#getCustomLabelAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.customLabelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{textAngle:30,value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getCustomLabelAngle(0, 0);
&lt;/script&gt;</code>
</pre>



### getCustomLabelValue<span class="signature">()</span>
{:#getCustomLabelValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.customLabelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{textAngle:30,value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getCustomLabelValue(0, 0);
&lt;/script&gt;</code>
</pre>



### getLabelAngle<span class="signature">()</span>
{:#getLabelAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelAngle(0, 0);
&lt;/script&gt;</code>
</pre>



### getLabelDistanceFromScale<span class="signature">()</span>
{:#getLabelDistanceFromScale}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelDistanceFromScale(0, 0);
&lt;/script&gt;</code>
</pre>



### getLabelPlacement<span class="signature">()</span>
{:#getLabelPlacement}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelPlacement(0, 0);
&lt;/script&gt;</code>
</pre>



### getLabelStyle<span class="signature">()</span>
{:#getLabelStyle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelStyle(0, 0);
&lt;/script&gt;</code>
</pre>



### getMajorIntervalValue<span class="signature">()</span>
{:#getMajorIntervalValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMajorIntervalValue(0);
&lt;/script&gt;</code>
</pre>



### getMarkerDistanceFromScale<span class="signature">()</span>
{:#getMarkerDistanceFromScale}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMarkerDistanceFromScale(0, 0);
&lt;/script&gt;</code>
</pre>



### getMarkerStyle<span class="signature">()</span>
{:#getMarkerStyle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMarkerStyle(0, 0);
&lt;/script&gt;</code>
</pre>



### getMaximumValue<span class="signature">()</span>
{:#getMaximumValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMaximumValue(0);
&lt;/script&gt;</code>
</pre>



### getMinimumValue<span class="signature">()</span>
{:#getMinimumValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMinimumValue(0);
&lt;/script&gt;</code>
</pre>



### getMinorIntervalValue<span class="signature">()</span>
{:#getMinorIntervalValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMinorIntervalValue(0);
&lt;/script&gt;</code>
</pre>



### getNeedleStyle<span class="signature">()</span>
{:#getNeedleStyle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getNeedleStyle(0, 0);
&lt;/script&gt;</code>
</pre>



### getPointerCapBorderWidth<span class="signature">()</span>
{:#getPointerCapBorderWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerCapBorderWidth(0);
&lt;/script&gt;</code>
</pre>



### getPointerCapRadius<span class="signature">()</span>
{:#getPointerCapRadius}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerCapRadius(0);
&lt;/script&gt;</code>
</pre>



### getPointerLength<span class="signature">()</span>
{:#getPointerLength}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerLength(0, 0);
&lt;/script&gt;</code>
</pre>



### getPointerNeedleType<span class="signature">()</span>
{:#getPointerNeedleType}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerNeedleType(0, 0);
&lt;/script&gt;</code>
</pre>



### getPointerPlacement<span class="signature">()</span>
{:#getPointerPlacement}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerPlacement(0, 0);
&lt;/script&gt;</code>
</pre>



### getPointerValue<span class="signature">()</span>
{:#getPointerValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerValue(0, 0);
&lt;/script&gt;</code>
</pre>



### getPointerWidth<span class="signature">()</span>
{:#getPointerWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerWidth(0, 0);
&lt;/script&gt;</code>
</pre>



### getRangeBorderWidth<span class="signature">()</span>
{:#getRangeBorderWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeBorderWidth(0, 0);
&lt;/script&gt;</code>
</pre>



### getRangeDistanceFromScale<span class="signature">()</span>
{:#getRangeDistanceFromScale}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeDistanceFromScale(0, 0);
&lt;/script&gt;</code>
</pre>



### getRangeEndValue<span class="signature">()</span>
{:#getRangeEndValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeEndValue(0, 0);
&lt;/script&gt;</code>
</pre>



### getRangePosition<span class="signature">()</span>
{:#getRangePosition}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangePosition(0, 0);
&lt;/script&gt;</code>
</pre>



### getRangeSize<span class="signature">()</span>
{:#getRangeSize}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeSize(0, 0);
&lt;/script&gt;</code>
</pre>



### getRangeStartValue<span class="signature">()</span>
{:#getRangeStartValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeStartValue(0, 0);
&lt;/script&gt;</code>
</pre>



### getScaleBarSize<span class="signature">()</span>
{:#getScaleBarSize}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleBarSize(0);
&lt;/script&gt;</code>
</pre>



### getScaleBorderWidth<span class="signature">()</span>
{:#getScaleBorderWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{Width: 1.5} }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleBorderWidth(0);
&lt;/script&gt;</code>
</pre>



### getScaleDirection<span class="signature">()</span>
{:#getScaleDirection}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleDirection(0);
&lt;/script&gt;</code>
</pre>



### getScaleRadius<span class="signature">()</span>
{:#getScaleRadius}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleRadius(0);
&lt;/script&gt;</code>
</pre>



### getStartAngle<span class="signature">()</span>
{:#getStartAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getStartAngle(0);
&lt;/script&gt;</code>
</pre>



### getSubGaugeLocation<span class="signature">()</span>
{:#getSubGaugeLocation}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.GaugeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">GaugeIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;div id="subGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 150 }}]}]});
circulargaugeObj.getSubGaugeLocation(0, 0);
&lt;/script&gt;</code>
</pre>



### getSweepAngle<span class="signature">()</span>
{:#getSweepAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getSweepAngle(0);
&lt;/script&gt;</code>
</pre>



### getTickAngle<span class="signature">()</span>
{:#getTickAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickAngle(0, 0);
&lt;/script&gt;</code>
</pre>



### getTickDistanceFromScale<span class="signature">()</span>
{:#getTickDistanceFromScale}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickDistanceFromScale(0, 0);
&lt;/script&gt;</code>
</pre>



### getTickHeight<span class="signature">()</span>
{:#getTickHeight}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickHeight(0, 0);
&lt;/script&gt;</code>
</pre>



### getTickPlacement<span class="signature">()</span>
{:#getTickPlacement}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickPlacement(0, 0);
&lt;/script&gt;</code>
</pre>



### getTickStyle<span class="signature">()</span>
{:#getTickStyle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickStyle(0, 0);
&lt;/script&gt;</code>
</pre>



### getTickWidth<span class="signature">()</span>
{:#getTickWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the Gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickWidth(0, 0);
&lt;/script&gt;</code>
</pre>



### includeFirstValue<span class="signature">()</span>
{:#includeFirstValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.includeFirstValue(0, 0, false);
&lt;/script&gt;</code>
</pre>



### redraw<span class="signature">()</span>
{:#redraw}




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
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">redraw value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.redraw("scale");
&lt;/script&gt;</code>
</pre>



### setBackNeedleLength<span class="signature">()</span>
{:#setBackNeedleLength}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true }] }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setBackNeedleLength(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setCustomLabelAngle<span class="signature">()</span>
{:#setCustomLabelAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.customLabelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font: { size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setCustomLabelAngle(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setCustomLabelValue<span class="signature">()</span>
{:#setCustomLabelValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.customLabelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{value:"MyLabel",position:{x:180,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setCustomLabelValue(0, 0, "CircularGauge");
&lt;/script&gt;</code>
</pre>



### setLabelAngle<span class="signature">()</span>
{:#setLabelAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">angle value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelAngle(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setLabelDistanceFromScale<span class="signature">()</span>
{:#setLabelDistanceFromScale}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelDistanceFromScale(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setLabelPlacement<span class="signature">()</span>
{:#setLabelPlacement}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelPlacement(0, 0, "far");
&lt;/script&gt;</code>
</pre>



### setLabelStyle<span class="signature">()</span>
{:#setLabelStyle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">labelIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelStyle(0, 0, "major");
&lt;/script&gt;</code>
</pre>



### setMajorIntervalValue<span class="signature">()</span>
{:#setMajorIntervalValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMajorIntervalValue(0, 10);
&lt;/script&gt;</code>
</pre>



### setMarkerDistanceFromScale<span class="signature">()</span>
{:#setMarkerDistanceFromScale}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMarkerDistanceFromScale(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setMarkerStyle<span class="signature">()</span>
{:#setMarkerStyle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMarkerStyle(0, 0, "rectangle");
&lt;/script&gt;</code>
</pre>



### setMaximumValue<span class="signature">()</span>
{:#setMaximumValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMaximumValue(0, 130);
&lt;/script&gt;</code>
</pre>



### setMinimumValue<span class="signature">()</span>
{:#setMinimumValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMinimumValue(0, 10);
&lt;/script&gt;</code>
</pre>



### setMinorIntervalValue<span class="signature">()</span>
{:#setMinorIntervalValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMinorIntervalValue(0, 2);
&lt;/script&gt;</code>
</pre>



### setNeedleStyle<span class="signature">()</span>
{:#setNeedleStyle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setNeedleStyle(0, 0, "arrow");
&lt;/script&gt;</code>
</pre>



### setPointerCapBorderWidth<span class="signature">()</span>
{:#setPointerCapBorderWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerCapBorderWidth(0, 5);
&lt;/script&gt;</code>
</pre>



### setPointerCapRadius<span class="signature">()</span>
{:#setPointerCapRadius}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerCapRadius(0, 10);
&lt;/script&gt;</code>
</pre>



### setPointerLength<span class="signature">()</span>
{:#setPointerLength}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerLength(0, 0, 90);
&lt;/script&gt;</code>
</pre>



### setPointerNeedleType<span class="signature">()</span>
{:#setPointerNeedleType}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerNeedleType(0, 0, "triangle");
&lt;/script&gt;</code>
</pre>



### setPointerPlacement<span class="signature">()</span>
{:#setPointerPlacement}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerPlacement(0, 0,"near");
&lt;/script&gt;</code>
</pre>



### setPointerValue<span class="signature">()</span>
{:#setPointerValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerValue(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setPointerWidth<span class="signature">()</span>
{:#setPointerWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerWidth(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setRangeBorderWidth<span class="signature">()</span>
{:#setRangeBorderWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeBorderWidth(0, 0, 5);
&lt;/script&gt;</code>
</pre>



### setRangeDistanceFromScale<span class="signature">()</span>
{:#setRangeDistanceFromScale}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeDistanceFromScale(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setRangeEndValue<span class="signature">()</span>
{:#setRangeEndValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeEndValue(0, 0, 70);
&lt;/script&gt;</code>
</pre>



### setRangePosition<span class="signature">()</span>
{:#setRangePosition}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangePosition(0, 0, "far");
&lt;/script&gt;</code>
</pre>



### setRangeSize<span class="signature">()</span>
{:#setRangeSize}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeSize(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setRangeStartValue<span class="signature">()</span>
{:#setRangeStartValue}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeStartValue(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setScaleBarSize<span class="signature">()</span>
{:#setScaleBarSize}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleBarSize(0, 160);
&lt;/script&gt;</code>
</pre>



### setScaleBorderWidth<span class="signature">()</span>
{:#setScaleBorderWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{width: 1.5} }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleBorderWidth(0, 3);
&lt;/script&gt;</code>
</pre>



### setScaleDirection<span class="signature">()</span>
{:#setScaleDirection}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleDirection(0, "clockwise");
&lt;/script&gt;</code>
</pre>



### setScaleRadius<span class="signature">()</span>
{:#setScaleRadius}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleRadius(0, 140);
&lt;/script&gt;</code>
</pre>



### setStartAngle<span class="signature">()</span>
{:#setStartAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setStartAngle(0, 10);
&lt;/script&gt;</code>
</pre>



### setSubGaugeLocation<span class="signature">()</span>
{:#setSubGaugeLocation}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.GaugeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">GaugeIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
 
&lt;div id="subGauge1"&gt;
&lt;/div&gt; 
&lt;script&gt;
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 150 }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setSubGaugeLocation(0, 0, {x:50,y:100});
&lt;/script&gt;</code>
</pre>



### setSweepAngle<span class="signature">()</span>
{:#setSweepAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setSweepAngle(0, 220);
&lt;/script&gt;</code>
</pre>



### setTickAngle<span class="signature">()</span>
{:#setTickAngle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickAngle(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setTickDistanceFromScale<span class="signature">()</span>
{:#setTickDistanceFromScale}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickDistanceFromScale(0, 0, 15);
&lt;/script&gt;</code>
</pre>



### setTickHeight<span class="signature">()</span>
{:#setTickHeight}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickHeight(0, 0, 10);
&lt;/script&gt;</code>
</pre>



### setTickPlacement<span class="signature">()</span>
{:#setTickPlacement}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt; 
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickPlacement(0, 0, "near");
&lt;/script&gt;</code>
</pre>



### setTickStyle<span class="signature">()</span>
{:#setTickStyle}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickStyle(0, 0, "minor");
&lt;/script&gt;</code>
</pre>



### setTickWidth<span class="signature">()</span>
{:#setTickWidth}




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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.tickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">tickIndex value for the gauge</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the gauge</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickWidth(0, 0, 5);
&lt;/script&gt;</code>
</pre>


## Events




### drawCustomLabel
{:#drawCustomLabel}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the custom label</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the custom label belongs.</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the custom label style</td>
</tr>
<tr>
<td class="name"><code>args.customLabelElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current custom label element.</td>
</tr>
<tr>
<td class="name"><code>args.customLabelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the custom label.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   drawCustomLabel: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### drawIndicators
{:#drawIndicators}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the indicator</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the indicator belongs.</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the indicator style</td>
</tr>
<tr>
<td class="name"><code>args.indicatorElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current indicator element.</td>
</tr>
<tr>
<td class="name"><code>args.indicatorIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the indicator.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   drawIndicators: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### drawLabels
{:#drawLabels}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the labels</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the label belongs.</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the label style</td>
</tr>
<tr>
<td class="name"><code>args.label</code></td>
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
<td class="name"><code>angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the labels.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current label element.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the label.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>args.pointerValue</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the label.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   drawLabels: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### drawPointerCap
{:#drawPointerCap}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer cap.</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer cap style</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   drawPointerCap: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### drawPointers
{:#drawPointers}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name"><code>args.pointer</code></td>
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
<td class="name"><code>angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the pointer.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current pointer element.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the pointer.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   drawPointers: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### drawRange
{:#drawRange}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the range</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the range belongs.</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the range style</td>
</tr>
<tr>
<td class="name"><code>args.rangeElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current range element.</td>
</tr>
<tr>
<td class="name"><code>args.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the range.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   drawRange: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### drawTicks
{:#drawTicks}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the ticks</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the tick belongs.</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the ticks style</td>
</tr>
<tr>
<td class="name"><code>args.tick</code></td>
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
<td class="name"><code>angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the tick.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current tick element.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the tick.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>args.pointerValue</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the label value of the tick.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   drawTicks: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### load
{:#load}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">cancel</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type"><a href="Model.html">Model</a></span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">scaleElement</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">context</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CircularGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#CircularGauge1").ejCircularGauge({
   load: function (args) {}
});
&lt;/script&gt; </code>
</pre>



### mouseClick
{:#mouseClick}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.pointer</code></td>
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
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
</tr>
<tr>
<td class="name"><code>angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the pointer.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   mouseClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### mouseClickMove
{:#mouseClickMove}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.pointer</code></td>
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
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
</tr>
<tr>
<td class="name"><code>angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the pointer.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   mouseClickMove: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### mouseClickUp
{:#mouseClickUp}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.pointer</code></td>
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
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
</tr>
<tr>
<td class="name"><code>angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the pointer.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   mouseClickUp: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### renderComplete
{:#renderComplete}




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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="CoreCircularGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#CoreCircularGauge").ejCircularGauge({
   renderComplete: function (args) {}
});
&lt;/script&gt;</code>
</pre>


