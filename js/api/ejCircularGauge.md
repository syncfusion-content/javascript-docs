---
layout: post
title: Properties,Methods and Events of ejCircularGauge Widget
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejCircularGauge
<ts root="datavisualization" />

The Circular gauge can be easily configured to the DOM element, such as div. you can create a circular gauge with a highly customizable look and feel.





$(element).ejCircularGauge(options)




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
<td class="description last">For setting the Circular gauge</td>
</tr>
</tbody>
</table>


#### Example


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




### animationSpeed `number`
{:#members:animationspeed}




Specifies animationSpeed of circular gauge


#### Default Value



* 500




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({ animationSpeed: 500,scales: [{ pointers: [{ value: 50 }] }] });
</script>{% endhighlight %}




### backgroundColor `string`
{:#members:backgroundcolor}




Specifies the background color of circular gauge.


#### Default Value



* null




#### Example


{% highlight html %}
                     
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({  backgroundColor : "#F234F4" });
</script>{% endhighlight %}




### distanceFromCorner `number`
{:#members:distancefromcorner}




Specify distanceFromCorner value of circular gauge


#### Default Value



* center




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  gaugePosition:"center", distanceFromCorner :25});
</script>{% endhighlight %}




### enableAnimation `boolean`
{:#members:enableanimation}




Specify animate value of circular gauge


#### Default Value



* true




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                   
$("#CoreCircularGauge").ejCircularGauge({ enableAnimation: true,scales: [{ pointers: [{ value: 50 }] }] });
</script>{% endhighlight %}




### frame `object`
{:#members:frame}




Specify the frame of circular gauge


#### Default Value



* Object




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
$("#CoreCircularGauge").ejCircularGauge({ frame:{frameType:ej.datavisualization.CircularGauge.Frame.FullCircle, backgroundImageUrl:"", halfCircleFrameStartAngle:180, halfCircleFrameEndAngle:360} });
</script>{% endhighlight %}




### frame.backgroundImageUrl `string`
{:#members:frame.backgroundimageurl}




Specify the URL of the frame background image for circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({  frame:{backgroundImageUrl : "Sun.jpg" }});
</script>{% endhighlight %}




### frame.frameType `enum`
{:#members:frame.frametype}

<ts name = "ej.datavisualization.CircularGauge.FrameType"/>

Specifies the frameType of circular gauge. See <a href="global.html#Frame">Frame</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
FullCircle</td>
<td class="type">string</td> 
<td class="description">Specify the full circle frame</td>
</tr>
<tr>
<td class="name">
HalfCircle</td>
<td class="type">string</td>
<td class="description">Specify the half circle frame</td>
</tr> 
</tbody>
</table>


#### Default Value



* FullCircle




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({  frame:{frameType : "halfcircle"} });
</script>{% endhighlight %}




### frame.halfCircleFrameEndAngle `number`
{:#members:frame.halfcircleframeendangle}




Specifies the end angle for the half circular frame.


#### Default Value



* 360




#### Example


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ frame:{frameType : "halfCircle",halfCircleFrameEndAngle: 270}});
</script>{% endhighlight %}




### frame.halfCircleFrameStartAngle `number`
{:#members:frame.halfcircleframestartangle}




Specifies the start angle for the half circular frame.


#### Default Value



* 180




#### Example


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ frame:{frameType : "halfcircle",halfCircleFrameStartAngle: 0} });
</script>{% endhighlight %}




### gaugePosition `enum`
{:#members:gaugeposition}

<ts name = "ej.datavisualization.CircularGauge.gaugePosition"/>

Specify gaugePosition value of circular gauge See GaugePosition


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
TopLeft</td>
<td class="type">string</td> 
<td class="description">The gauge will be placed TopLeft corner in container</td>
</tr>
<tr>
<td class="name">
TopRight</td>
<td class="type">string</td>
<td class="description">The gauge will be placed TopRight corner in container</td>
</tr> 
<tr>
<td class="name">
TopCenter</td>
<td class="type">string</td>
<td class="description">The gauge will be placed in TopCenter</td>
</tr> 
<tr>
<td class="name">
MiddleLeft</td>
<td class="type">string</td>
<td class="description">The gauge will be placed in MiddleLeft</td>
</tr> 
<tr>
<td class="name">
MiddleRight</td>
<td class="type">string</td>
<td class="description">The gauge will be placed in MiddleRight</td>
</tr> 
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="description">The gauge will be placed center of the container</td>
</tr> 
<tr>
<td class="name">
BottomLeft</td>
<td class="type">string</td>
<td class="description">The gauge will be placed BottomLeft corner in container</td>
</tr> 
<tr>
<td class="name">
BottomRight</td>
<td class="type">string</td>
<td class="description">he gauge will be placed in BottomRight corner in container</td>
</tr> 
<tr>
<td class="name">
BottomCenter</td>
<td class="type">string</td>
<td class="description">he gauge will be placed in BottomCenter</td>
</tr> 
</tbody>
</table>



#### Default Value



* center




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  gaugePosition:"center" });
</script>{% endhighlight %}




### height `number`
{:#members:height}




Specifies the height of circular gauge.


#### Default Value



* 360




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ height: 400 });
</script>{% endhighlight %}




### interiorGradient `object`
{:#members:interiorgradient}




Specifies the interiorGradient of circular gauge.


#### Default Value



* null




#### Example


{% highlight html %}
                     
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ interiorGradient: { colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } }); 
</script>{% endhighlight %}




### isRadialGradient `boolean`
{:#members:isradialgradient}




Specify isRadialGradient value of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({  isRadialGradient : true });
</script>{% endhighlight %}




### isResponsive `boolean`
{:#members:isresponsive}




Specify isResponsive value of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({  isResponsive : true });
</script>{% endhighlight %}




### maximum `number`
{:#members:maximum}




Specifies the maximum value of circular gauge.


#### Default Value



* 100




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ maximum: 120 });
</script>{% endhighlight %}




### minimum `number`
{:#members:minimum}




Specifies the minimum value of circular gauge.


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ minimum: 10 });
</script>{% endhighlight %}




### outerCustomLabelPosition `enum`
{:#members:outercustomlabelposition}

<ts name = "ej.datavisualization.CircularGauge.CustomLabelPositionType"/>

Specify outerCustomLabelPosition value of circular gauge See <a href="global.html#OuterCustomLabelPosition">OuterCustomLabelPosition</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Top</td>
<td class="type">string</td> 
<td class="description">Sets the label position as top</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="description">Sets the label position as Bottom</td>
</tr> 
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="description">Sets the label position as Right</td>
</tr> 
<tr>
<td class="name">
Left</td>
<td class="type">string</td>
<td class="description">Sets the label position as Left</td>
</tr> 
</tbody>
</table>



#### Default Value



* bottom




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  outerCustomLabelPosition:"top" });
</script>{% endhighlight %}




### radius `number`
{:#members:radius}




Specifies the radius of circular gauge.


#### Default Value



* 180




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ radius: 100 });
</script>{% endhighlight %}




### readOnly `boolean`
{:#members:readonly}




Specify readonly value of circular gauge


#### Default Value



* true




#### Example


{% highlight html %}
                     
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({  readOnly : false });
</script>{% endhighlight %}




### scales `object`
{:#members:scales}




Specify the pointers, ticks, labels, indicators, ranges of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{width: 1.5} }] });
</script>{% endhighlight %}




### scales.backgroundColor `string`
{:#members:scales.backgroundcolor}




Specify backgroundColor for the scale of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, backgroundColor: "#1BA1E2" }] });
</script>{% endhighlight %}




### scales.border `object`
{:#members:scales.border}




Specify border for scales of circular gauge


#### Default Value



* Object




#### Example


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ border:{color:null, width:1.5 }}] });
</script>{% endhighlight %}




### scales.border.color `string`
{:#members:scales.border.color}




Specify border color for scales of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true,  border:[{color: "#1BA1E2" }]}] });
</script>{% endhighlight %}




### scales.border.width `number`
{:#members:scales.border.width}




Specify border width of circular gauge


#### Default Value



* 1.5




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, border:{width: 1.5} }] });
</script>{% endhighlight %}




### scales.direction `enum`
{:#members:scales.direction}

<ts name = "ej.datavisualization.CircularGauge.Direction"/>

Specify scale direction of circular gauge. See <a href="global.html#Directions">Directions</a>

<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Clockwise</td>
<td class="type">string</td> 
<td class="description">Specify the clockwise direction </td>
</tr>
<tr>
<td class="name">
CounterClockwise</td>
<td class="type">string</td>
<td class="description">Specify the counterclockwise direction</td>
</tr> 
</tbody>
</table>



#### Default Value



* Clockwise




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ direction: "counterclockwise" }] });
</script>{% endhighlight %}




### scales.customLabels `Array`
{:#members:scales.customlabels}




Specify the custom labels for the scales.


#### Default Value



* Array




#### Example


{% highlight html %}

 $("#CoreCircularGauge").ejCircularGauge({ 
  
  scales: [{
    customLabels:[]
  }]                      

}); 
 
{% endhighlight %}



### scales.customLabels.value `string`
{:#members:scales.customlabels.value}




Value of the custom labels.


#### Default Value



* ""




#### Example


{% highlight html %}
 
< $("#CoreCircularGauge").ejCircularGauge({ 
  
  scales: [{
    customLabels:[{value:'Sports'}]
  }]                      

}); 

{% endhighlight %}


### scales.customLabels.color `string`
{:#members:scales.customlabels.color}




Color of the custom labels.


#### Default Value



* ""




#### Example


{% highlight html %}
 
<$("#CoreCircularGauge").ejCircularGauge({ 
  
  scales: [{
    customLabels:[{color:"#333333"}]
  }]                      

}); 

{% endhighlight %}





### scales.customLabels.position `object`
{:#members:scales.customlabels.position}




Specify position of custom labels


#### Default Value



* Object




#### Example


{% highlight html %}
 
                         
<$("#CoreCircularGauge").ejCircularGauge({ 
  
   scales: [{
    customLabels:[{position:{x:10}}]
    }]                      

}); 

{% endhighlight %}




### scales.customLabels.position.x `number`
{:#members:scales.customlabels.position.x}




Specify x-axis position of label


#### Default Value



* 0




#### Example


{% highlight html %}
 
                         
<$("#CoreCircularGauge").ejCircularGauge({ 
  
   scales: [{
    customLabels:[{position:{x:10}}]
    }]                      

}); 

{% endhighlight %}




### scales.customLabels.position.y `number`
{:#members:scales.customlabels.position.y}




Specify y-axis  position of labels.


#### Default Value



* 0




#### Example

 
{% highlight html %}
 
                         
<$("#CoreCircularGauge").ejCircularGauge({ 
  
   scales: [{
    customLabels:[{position:{y:10}}]
    }]                      

}); 

{% endhighlight %}



### scales.customLabels.font `object`
{:#members:scales.customlabels.font}




Specify font for custom labels


#### Default Value



* Object




#### Example


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ customLabels: [{ font: { size: "12px", fontFamily: "Segou", fontStyle: "Bold" } }] }] });
</script>{% endhighlight %}




### scales.customLabels.font.fontFamily `string`
{:#members:scales.customlabels.font.fontfamily}




Specify font fontFamily for custom labels.


#### Default Value



* "Arial"




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ customLabels: [{ font: { fontFamily: "Arial" } }] }] });
</script>{% endhighlight %}




### scales.customLabels.font.fontStyle `string`
{:#members:scales.customlabels.font.fontstyle}




Specify font Style for custom labels.


#### Default Value



* "Bold"




#### Example


{% highlight html %}
 
                          
$("#CoreCircularGauge").ejCircularGauge({ 
    scales: [{ customLabels: [{ font: { fontStyle: "Bold" } }] }] 
    });
 {% endhighlight %}
 
 
 
 
 
### scales.customLabels.font.size `string`
{:#members:scales.customlabels.font.size}




Specify font size for custom labels.


#### Default Value



* "12px"




#### Example


{% highlight html %}
 
                          
$("#CoreCircularGauge").ejCircularGauge({ 
    scales: [{ customLabels: [{ font: { size: "12px" } }] }] 
    });
 {% endhighlight %}






### scales.indicators `Array`
{:#members:scales.indicators}




Specify representing state of circular gauge


#### Default Value



* Array




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  height: 30,width: 10,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243", borderColor: "#5DF243", text: "", textColor: "#870505" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608", borderColor: "#145608", text: "", textColor: "#870505" }]}]}]});
</script>{% endhighlight %}




### scales.indicators.height `number`
{:#members:scales.indicators.height}




Specify indicator height of circular gauge


#### Default Value



* 15




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  height: 30,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.imageUrl `string`
{:#members:scales.indicators.imageurl}




Specify imageUrl of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "image",value: 0,imageUrl:"Sun.jpeg",position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.position `object`
{:#members:scales.indicators.position}




Specify position of circular gauge


#### Default Value



* Object




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y: 150 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.position.x `number`
{:#members:scales.indicators.position.x}




Specify x-axis of position of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185,y:0 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.position.y `number`
{:#members:scales.indicators.position.y}




Specify y-axis of position of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x:0,y: 185 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges `Array`
{:#members:scales.indicators.stateranges}




Specify the various states of circular gauge


#### Default Value



* Array




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.backgroundColor `string`
{:#members:scales.indicators.stateranges.backgroundcolor}




Specify backgroundColor for indicator of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "Red" },
  { endValue: 200, startValue: 70, backgroundColor: "Yellow"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.borderColor `string`
{:#members:scales.indicators.stateranges.bordercolor}




Specify borderColor for indicator of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243",borderColor:"Red" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608", borderColor:"yellow"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.endValue `number`
{:#members:scales.indicators.stateranges.endvalue}




Specify end value for each specified state of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.font `object`
{:#members:scales.indicators.stateranges.font}




Specify value of the font as the indicator when the indicator style is set with the value "text" of circular gauge


#### Default Value



* null




#### Example


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




### scales.indicators.stateRanges.startValue `number`
{:#members:scales.indicators.stateranges.startvalue}




Specify start value for each specified state of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y:300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.stateRanges.text `string`
{:#members:scales.indicators.stateranges.text}




Specify value of the text as the indicator when the indicator style is set with the value "text" of circular gauge


#### Default Value



* ""




#### Example


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




### scales.indicators.stateRanges.textColor `string`
{:#members:scales.indicators.stateranges.textcolor}




Specify value of the textColor as the indicator when the indicator style is set with the value "text" of circular gauge


#### Default Value



* null




#### Example


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




### scales.indicators.type `enum`
{:#members:scales.indicators.type}

<ts name = "ej.datavisualization.CircularGauge.IndicatorTypes"/>

Specify indicator style of circular gauge. See <a href="global.html#IndicatorType">IndicatorType</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Rectangle</td>
<td class="type">string</td> 
<td class="description">Style of the indicator will be rectangle</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="description">Style of the indicator will be circle</td>
</tr> 
<tr>
<td class="name">
Text</td>
<td class="type">string</td>
<td class="description">Style of the indicator will be text</td>
</tr> 
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="description">Style of the indicator will be roundedrectangle</td>
</tr> 
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="description">Style of the indicator will be image</td>
</tr> 
</tbody>
</table>



#### Default Value



* Circle




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.indicators.width `number`
{:#members:scales.indicators.width}




Specify indicator width of circular gauge


#### Default Value



* 15




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showIndicators:true,indicators: [{
  width: 30,type: "circle",value: 0,position: { x: 185, y: 300 },
  stateRanges: [{ endValue: 70, startValue: 0, backgroundColor: "#5DF243" },
  { endValue: 200, startValue: 70, backgroundColor: "#145608"}]}]}]});
</script>{% endhighlight %}




### scales.labels `Array`
{:#members:scales.labels}




Specify the text values displayed in a meaningful manner alongside the ticks of circular gauge


#### Default Value



* Array




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ angle: 10, opacity: 0.4 }] }] });
</script>{% endhighlight %}




### scales.labels.angle `number`
{:#members:scales.labels.angle}




Specify the angle for the labels of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ angle: 10 }] }] });
</script>{% endhighlight %}




### scales.labels.autoAngle `boolean`
{:#members:scales.labels.autoangle}




Specify labels autoAngle value of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels:[{autoAngle: true}] }] });
</script>{% endhighlight %}




### scales.labels.color `string`
{:#members:scales.labels.color}




Specify label color of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ color: "Red" }] }] });
</script>{% endhighlight %}




### scales.labels.distanceFromScale `number`
{:#members:scales.labels.distancefromscale}




Specify distanceFromScale value for labels of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ distanceFromScales: 10 }] }] });
</script>{% endhighlight %}




### scales.labels.font `object`
{:#members:scales.labels.font}




Specify font for labels of circular gauge


#### Default Value



* Object




#### Example


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { size: "12px", fontFamily: "Segou", fontStyle: "Bold" } }] }] });
</script>{% endhighlight %}




### scales.labels.font.fontFamily `string`
{:#members:scales.labels.font.fontfamily}




Specify font fontFamily for labels of circular gauge


#### Default Value



* "Arial"




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { fontFamily: "Arial" } }] }] });
</script>{% endhighlight %}




### scales.labels.font.fontStyle `string`
{:#members:scales.labels.font.fontstyle}




Specify font Style for labels of circular gauge


#### Default Value



* "Bold"




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { fontStyle: "Bold" } }] }] });
</script>{% endhighlight %}




### scales.labels.font.size `string`
{:#members:scales.labels.font.size}




Specify font size for labels of circular gauge


#### Default Value



* "11px"




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ font: { size: "12px" } }] }] });
</script>{% endhighlight %}




### scales.labels.includeFirstValue `boolean`
{:#members:scales.labels.includefirstvalue}




Specify includeFirstValue of circular gauge


#### Default Value



* true




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ includeFirstValue: false }] }] });
</script>{% endhighlight %}




### scales.labels.opacity `number`
{:#members:scales.labels.opacity}




Specify opacity value for labels of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ opacity: 0.4 }] }] });
</script>{% endhighlight %}




### scales.labels.placement `enum`
{:#members:scales.labels.placement}

<ts name = "ej.datavisualization.CircularGauge.Placement"/>

Specify label placement of circular gauge. See <a href="global.html#LabelPlacement">LabelPlacement</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Near</td>
<td class="type">string</td> 
<td class="description">Specify the label placement as near</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="description">Specify the label placement as far</td>
</tr> 
<td class="name">
Center</td>
<td class="type">string</td>
<td class="description">Specify the label placement as center</td>
</tr> 
</tbody>
</table>


#### Default Value



* Near




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ placement: "near" }] }] });
</script>{% endhighlight %}




### scales.labels.type `enum`
{:#members:scales.labels.type}

<ts name = "ej.datavisualization.CircularGauge.LabelType"/>

Specify label Style of circular gauge. See <a href="global.html#LabelType">LabelType</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Major</td>
<td class="type">string</td> 
<td class="description"> Label style will be major</td>
</tr>
<tr>
<td class="name">
Minor</td>
<td class="type">string</td>
<td class="description">Label style will be minor</td>
</tr> 
</tbody>
</table>

#### Default Value



* Major




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ type: "major" }] }] });
</script>{% endhighlight %}




### scales.labels.unitText `string`
{:#members:scales.labels.unittext}




Specify unitText of circular gauge


#### Default Value



* ""




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ unitText: "kmph" }] }] });
</script>{% endhighlight %}




### scales.labels.unitTextPosition `enum`
{:#members:scales.labels.unittextposition}

<ts name = "ej.datavisualization.CircularGauge.UnitTextPlacement"/>

Specify unitTextPosition of circular gauge. See UnitTextPosition


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Back</td>
<td class="type">string</td> 
<td class="description">The unit text will be placed back of the gauge</td>
</tr>
<tr>
<td class="name">
Front</td>
<td class="type">string</td>
<td class="description">The unit text will be placed front of the gauge</td>
</tr> 
</tbody>
</table>


#### Default Value



* Back




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ labels: [{ unitText: "kmph",unitTextPosition: "front" }] }] });
</script>{% endhighlight %}




### scales.majorIntervalValue `number`
{:#members:scales.majorintervalvalue}




Specify majorIntervalValue of circular gauge


#### Default Value



* 10




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ majorIntervalValue: 5 }] });
</script>{% endhighlight %}




### scales.maximum `number`
{:#members:scales.maximum}




Specify maximum scale value of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ maximum: 200 }] });
</script>{% endhighlight %}




### scales.minimum `number`
{:#members:scales.minimum}




Specify minimum scale value of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ minimum: 20 }] });
</script>{% endhighlight %}




### scales.minorIntervalValue `number`
{:#members:scales.minorintervalvalue}




Specify minorIntervalValue of circular gauge


#### Default Value



* 2




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ minorIntervalValue: 1 }] });
</script>{% endhighlight %}




### scales.opacity `number`
{:#members:scales.opacity}




Specify opacity value of circular gauge


#### Default Value



* 1




#### Example


{% highlight html %}
     
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, opacity:0.5 }] });
</script>{% endhighlight %}




### scales.pointerCap `object`
{:#members:scales.pointercap}




Specify pointer cap of circular gauge


#### Default Value



* Object




#### Example


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{radius: 7, borderWidth:3, interiorGradient:null, borderColor:null } }] });
</script>{% endhighlight %}




### scales.pointerCap.backgroundColor `string`
{:#members:scales.pointercap.backgroundcolor}




Specify cap backgroundColor of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap: {backgroundColor: "Green"} }] });
</script>{% endhighlight %}




### scales.pointerCap.borderColor `string`
{:#members:scales.pointercap.bordercolor}




Specify cap borderColor of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap: {borderColor: "Brown" }}] });
</script>{% endhighlight %}




### scales.pointerCap.borderWidth `number`
{:#members:scales.pointercap.borderwidth}




Specify pointerCap borderWidth value of circular gauge


#### Default Value



* 3




#### Example


{% highlight html %}
     
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{borderWidth: 8 } }] });
</script>{% endhighlight %}




### scales.pointerCap.interiorGradient `object`
{:#members:scales.pointercap.interiorgradient}




Specify cap interiorGradient value of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
             
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{interiorGradient: {colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}}] });
</script>{% endhighlight %}




### scales.pointerCap.radius `number`
{:#members:scales.pointercap.radius}




Specify pointerCap Radius value of circular gauge


#### Default Value



* 7




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointerCap:{radius: 10} }] });
</script>{% endhighlight %}




### scales.pointers `Array`
{:#members:scales.pointers}




Specify pointers value of circular gauge


#### Default Value



* Array




#### Example


{% highlight html %}
     
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ distanceFromScale: 0, showBackNeedle: false }] }] });
</script>{% endhighlight %}




### scales.pointers.backgroundColor `string`
{:#members:scales.pointers.backgroundcolor}




Specify backgroundColor for the pointer of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ backgroundColor: "#1A1A1A" }] }] });
</script>{% endhighlight %}




### scales.pointers.backNeedleLength `number`
{:#members:scales.pointers.backneedlelength}




Specify backNeedleLength of circular gauge


#### Default Value



* 10




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true, backNeedleLength: 10 }] }] });
</script>{% endhighlight %}




### scales.pointers.border `object`
{:#members:scales.pointers.border}




Specify the border for pointers of circular gauge


#### Default Value



* Object




#### Example


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers:[{border:{color:null, width:1.5 }}]}] });
</script>{% endhighlight %}




### scales.pointers.border.color `string`
{:#members:scales.pointers.border.color}




Specify border color for pointer of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ border:{color: "#1A1A1A"} }] }] });
</script>{% endhighlight %}




### scales.pointers.border.width `number`
{:#members:scales.pointers.border.width}




Specify border width for pointers of circular gauge


#### Default Value



* 1.5




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ border:{width: 1.5 }}] }] });
</script>{% endhighlight %}




### scales.pointers.distanceFromScale `number`
{:#members:scales.pointers.distancefromscale}




Specify distanceFromScale value for pointers of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ distanceFromScale: 10 }] }] });
</script>{% endhighlight %}




### scales.pointers.gradients `object`
{:#members:scales.pointers.gradients}




Specify pointer gradients of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ gradients: {colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}] }] });
</script>{% endhighlight %}




### scales.pointers.imageUrl `string`
{:#members:scales.pointers.imageurl}




Specify pointer image of circular gauge.It is applicable for both marker as well as needle type pointers.


#### Default Value



* NULL




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "image", imageUrl: "football.png" }] }] });
</script>{% endhighlight %}




### scales.pointers.length `number`
{:#members:scales.pointers.length}




Specify pointer length of circular gauge


#### Default Value



* 150




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ length: 50 }] }] });
</script>{% endhighlight %}




### scales.pointers.markerType `enum`
{:#members:scales.pointers.markertype}

<ts name = "ej.datavisualization.CircularGauge.MarkerType"/>

Specify marker Style value of circular gauge. See <a href="global.html#MarkerType">MarkerType</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Rectangle</td>
<td class="type">string</td> 
<td class="description">Marker style of circular gauge will be rectangle</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be circle</td>
</tr> 
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be triangle</td>
</tr> 
<tr>
<td class="name">
Ellipse</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be ellipse</td>
</tr> 
<tr>
<td class="name">
Diamond</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be diamond</td>
</tr> 
<tr>
<td class="name">
Pentagon</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be pentagon</td>
</tr> 
<tr>
<td class="name">
Slider</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be slider</td>
</tr> 
<tr>
<td class="name">
Pointer</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be pointer</td>
</tr> 
<tr>
<td class="name">
Wedge</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be wedge</td>
</tr> 
<tr>
<td class="name">
Trapezoid</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be trapezoid</td>
</tr> 
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be rounded rectangle</td>
</tr> 
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="description">Marker style of circular gauge will be image</td>
</tr> 
</tbody>
</table>


#### Default Value



* Rectangle




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle" }] }] });
</script>{% endhighlight %}




### scales.pointers.needleType `enum`
{:#members:scales.pointers.needletype}

<ts name = "ej.datavisualization.CircularGauge.NeedleType"/>

Specify needle Style value of circular gauge. See <a href="global.html#NeedleType">NeedleType</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td> 
<td class="description">Needle style of circular gauge will be triangle</td>
</tr>
<tr>
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="description">Needle style of circular gauge will be rectangle</td>
</tr> 
<tr>
<td class="name">
Arrow</td>
<td class="type">string</td>
<td class="description">Needle style of circular gauge will be arrow</td>
</tr> 
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="description">Needle style of circular gauge will be image</td>
</tr> 
<tr>
<td class="name">
Trapezoid</td>
<td class="type">string</td>
<td class="description">Needle style of circular gauge will be trapezoid</td>
</tr> 
</tbody>
</table>


#### Default Value



* Triangle




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ needleType: "triangle" }] }] });
</script>{% endhighlight %}




### scales.pointers.opacity `number`
{:#members:scales.pointers.opacity}




Specify opacity value for pointer of circular gauge


#### Default Value



* 1




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ opacity: 0.3 }] }] });
</script>{% endhighlight %}




### scales.pointers.placement `enum`
{:#members:scales.pointers.placement}


<ts ref = "ej.datavisualization.CircularGauge.Placement"/>

Specify pointer Placement value of circular gauge. See <a href="global.html#PointerPlacement">PointerPlacement</a>


#### Default Value



* Near




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ placement: "far" }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText `object`
{:#members:scales.pointers.pointervaluetext}




Specify pointer value text of circular gauge.


#### Default Value



* Object




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: false, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.angle `number`
{:#members:scales.pointers.pointervaluetext.angle}




Specify pointer text angle of circular gauge.


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 0.5, autoAngle: false, angle: 30, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.autoAngle `boolean`
{:#members:scales.pointers.pointervaluetext.autoangle}




Specify pointer text auto angle of circular gauge.


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 0.5, autoAngle: true, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.color `string`
{:#members:scales.pointers.pointervaluetext.color}




Specify pointer value text color of circular gauge.


#### Default Value



* #8c8c8c




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.distance `number`
{:#members:scales.pointers.pointervaluetext.distance}




Specify pointer value text distance from pointer of circular gauge.


#### Default Value



* 20




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.font `object`
{:#members:scales.pointers.pointervaluetext.font}




Specify pointer value text font option of circular gauge.


#### Default Value



* object




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.font.fontFamily `string`
{:#members:scales.pointers.pointervaluetext.font.fontfamily}




Specify pointer value text font family of circular gauge.


#### Default Value



* Arial




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "12px", fontFamily: "Seogo UI", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.font.fontStyle `string`
{:#members:scales.pointers.pointervaluetext.font.fontstyle}




Specify pointer value text font style of circular gauge.


#### Default Value



* Bold




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "12px", fontFamily: "Seogo UI", fontStyle: "Normal" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.font.size `string`
{:#members:scales.pointers.pointervaluetext.font.size}




Specify pointer value text size of circular gauge.


#### Default Value



* 11px




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 30, font: { size: "12px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.opacity `number`
{:#members:scales.pointers.pointervaluetext.opacity}




Specify pointer value text opacity of circular gauge.


#### Default Value



* 1




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "Red", opacity: 0.5, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.pointerValueText.showValue `boolean`
{:#members:scales.pointers.pointervaluetext.showvalue}




enable pointer value text visibility of circular gauge.


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker", markerType: "rectangle", pointerValueText:{ showValue: true, distance: 20, font: { size: "11px", fontFamily: "Arial", fontStyle: "Bold" }, color: "#8c8c8c", opacity: 1, autoAngle: false, angle: 0, } }] }] });
</script>{% endhighlight %}




### scales.pointers.showBackNeedle `boolean`
{:#members:scales.pointers.showbackneedle}




Specify showBackNeedle value of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true, backNeedleLength: 10 }] }] });
</script>{% endhighlight %}




### scales.pointers.type `enum`
{:#members:scales.pointers.type}

<ts name = "ej.datavisualization.CircularGauge.PointerType"/>

Specify pointer type value of circular gauge. See <a href="global.html#PointerType">PointerType</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Needle</td>
<td class="type">string</td> 
<td class="description">Specify the pointer type as needle</td>
</tr>
<tr>
<td class="name">
Marker</td>
<td class="type">string</td>
<td class="description">Specify the pointer type as marker</td>
</tr> 
</tbody>
</table>



#### Default Value



* Needle




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ type: "marker" }] }] });
</script>{% endhighlight %}




### scales.pointers.value `number`
{:#members:scales.pointers.value}




Specify value of the pointer of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ value: 50 }] }] });
</script>{% endhighlight %}




### scales.pointers.width `number`
{:#members:scales.pointers.width}




Specify pointer width of circular gauge


#### Default Value



* 7




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ width: 7 }] }] });
</script>{% endhighlight %}




### scales.radius `number`
{:#members:scales.radius}




Specify scale radius of circular gauge


#### Default Value



* 170




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, radius: 100 }] });
</script>{% endhighlight %}




### scales.ranges `Array`
{:#members:scales.ranges}




Specify ranges value of circular gauge


#### Default Value



* Array




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true [{ ranges: [{ distanceFromScale: 25, size: 5}] }] }]});
</script>{% endhighlight %}




### scales.ranges.backgroundColor `string`
{:#members:scales.ranges.backgroundcolor}




Specify backgroundColor for the ranges of circular gauge


#### Default Value



* "#32b3c6"




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,backgroundColor: "Red" }]  }]});
</script>{% endhighlight %}




### scales.ranges.border `object`
{:#members:scales.ranges.border}




Specify border for ranges of circular gauge


#### Default Value



* Object




#### Example


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ ranges:[{border:{color:null, width:1.5 }}]}] });
</script>{% endhighlight %}




### scales.ranges.border.color `string`
{:#members:scales.ranges.border.color}




Specify border color for ranges of circular gauge


#### Default Value



* "#32b3c6"




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,border:{color: "#32b3c6"} }] }] });
</script>{% endhighlight %}




### scales.ranges.border.width `number`
{:#members:scales.ranges.border.width}




Specify border width for ranges of circular gauge


#### Default Value



* 1.5




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,distanceFromScale: -25,border:{width: 1.5} }] }] });
</script>{% endhighlight %}




### scales.ranges.distanceFromScale `number`
{:#members:scales.ranges.distancefromscale}




Specify distanceFromScale value for ranges of circular gauge


#### Default Value



* 25




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                          
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
</script>{% endhighlight %}




### scales.ranges.endValue `number`
{:#members:scales.ranges.endvalue}




Specify endValue for ranges of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true, ranges: [{ startValue: 10, endValue: 100,distanceFromScale: -25 }] }]});
</script>{% endhighlight %}




### scales.ranges.endWidth `number`
{:#members:scales.ranges.endwidth}




Specify endWidth for ranges of circular gauge


#### Default Value



* 10




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
</script>{% endhighlight %}




### scales.ranges.gradients `object`
{:#members:scales.ranges.gradients}




Specify range gradients of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{startValue: 10, endValue: 100, gradients: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}] }]});
</script>{% endhighlight %}




### scales.ranges.opacity `number`
{:#members:scales.ranges.opacity}




Specify opacity value for ranges of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,endWidth: 10,distanceFromScale: -25,opacity: 0.5 }] }] });
</script>{% endhighlight %}




### scales.ranges.placement `enum`
{:#members:scales.ranges.placement}

<ts ref = "ej.datavisualization.CircularGauge.Placement"/>


Specify placement of circular gauge. See <a href="global.html#RangePlacement">RangePlacement</a>


#### Default Value



* Near




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70,placement: "center"}]}]});
</script>{% endhighlight %}




### scales.ranges.size `number`
{:#members:scales.ranges.size}




Specify size of the range value of circular gauge


#### Default Value



* 5




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70,size:5}]}]});
</script>{% endhighlight %}




### scales.ranges.startValue `number`
{:#members:scales.ranges.startvalue}




Specify startValue for ranges of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
</script>{% endhighlight %}




### scales.ranges.startWidth `number`
{:#members:scales.ranges.startwidth}




Specify startWidth of circular gauge


#### Default Value



* [Array.number] scale.ranges.startWidth = 10




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showRanges:true , ranges: [{ startValue: 10, endValue: 100,startWidth: 10,distanceFromScale: -25 }] }]});
</script>{% endhighlight %}




### scales.shadowOffset `number`
{:#members:scales.shadowoffset}




Specify shadowOffset value of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
  
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ shadowOffset: 1}] });
</script>{% endhighlight %}




### scales.showIndicators `boolean`
{:#members:scales.showindicators}




Specify showIndicators of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showIndicators: false }] });
</script>{% endhighlight %}




### scales.showLabels `boolean`
{:#members:scales.showlabels}




Specify showLabels of circular gauge


#### Default Value



* true




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showLabels: true }] });
</script>{% endhighlight %}




### scales.showPointers `boolean`
{:#members:scales.showpointers}




Specify showPointers of circular gauge


#### Default Value



* true




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showPointers: true }] });
</script>{% endhighlight %}




### scales.showRanges `boolean`
{:#members:scales.showranges}




Specify showRanges of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showRanges: false }] });
</script>{% endhighlight %}




### scales.showScaleBar `boolean`
{:#members:scales.showscalebar}




Specify showScaleBar of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true }] });
</script>{% endhighlight %}




### scales.showTicks `boolean`
{:#members:scales.showticks}




Specify showTicks of circular gauge


#### Default Value



* true




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ showTicks: true }] });
</script>{% endhighlight %}




### scales.size `number`
{:#members:scales.size}




Specify scaleBar size of circular gauge


#### Default Value



* 6




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ showScaleBar: true, size: 6 }] });
</script>{% endhighlight %}




### scales.startAngle `number`
{:#members:scales.startangle}




Specify startAngle of circular gauge


#### Default Value



* 115




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ startAngle: 90 }] });
</script>{% endhighlight %}




### scales.subGauges `Array`
{:#members:scales.subgauges}




Specify subGauge of circular gauge


#### Default Value



* Array




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 200, y: 150 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.height `number`
{:#members:scales.subgauges.height}




Specify subGauge Height of circular gauge


#### Default Value



* 150




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 100 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.position `object`
{:#members:scales.subgauges.position}




Specify position for sub-gauge of circular gauge


#### Default Value



* Object




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 200, y: 150 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.position.x `number`
{:#members:scales.subgauges.position.x}




Specify x-axis position for sub-gauge of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 200, y: 0 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.position.y `number`
{:#members:scales.subgauges.position.y}




Specify y-axis position for sub-gauge of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 200,position: { x: 0, y: 150 }}]}]});
</script>{% endhighlight %}




### scales.subGauges.width `number`
{:#members:scales.subgauges.width}




Specify subGauge Width of circular gauge


#### Default Value



* 150




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<div id="subGauge1">
</div> 
 
<script>  
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 200,width: 300,position: { x: 200, y: 150 }}]}]});
</script>{% endhighlight %}




### scales.sweepAngle `number`
{:#members:scales.sweepangle}




Specify sweepAngle of circular gauge


#### Default Value



* 310




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ sweepAngle: 200 }] });
</script>{% endhighlight %}




### scales.ticks `Array`
{:#members:scales.ticks}




Specify ticks of circular gauge


#### Default Value



* Array




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ angle: 10, distanceFromScale: 10 }] }] });
</script>{% endhighlight %}




### scales.ticks.angle `number`
{:#members:scales.ticks.angle}




Specify the angle for the ticks of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ angle: 10 }] }] });
</script>{% endhighlight %}




### scales.ticks.color `string`
{:#members:scales.ticks.color}




Specify tick color of circular gauge


#### Default Value



* null




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ color: "#777777" }] }] });
</script>{% endhighlight %}




### scales.ticks.distanceFromScale `number`
{:#members:scales.ticks.distancefromscale}




Specify distanceFromScale value for ticks of circular gauge


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ distanceFromScale: 10 }] }] });
</script>{% endhighlight %}




### scales.ticks.height `number`
{:#members:scales.ticks.height}




Specify tick height of circular gauge


#### Default Value



* 16




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ height: 16 }] }] });
</script>{% endhighlight %}




### scales.ticks.placement `enum`
{:#members:scales.ticks.placement}

<ts ref = "ej.datavisualization.CircularGauge.Placement"/>


Specify tick placement of circular gauge. See <a href="global.html#TickPlacement">TickPlacement</a>


#### Default Value



* Near




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>  
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ placement: "near" }] }] });
</script>{% endhighlight %}




### scales.ticks.type `enum`
{:#members:scales.ticks.type}

<ts ref = "ej.datavisualization.CircularGauge.LabelType"/>


Specify tick Style of circular gauge. See <a href="global.html#TickType">TickType</a>


#### Default Value



* Major




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ type: "major" }] }] });
</script>{% endhighlight %}




### scales.ticks.width `number`
{:#members:scales.ticks.width}




Specify tick width of circular gauge


#### Default Value



* 3




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>          
        $("#CoreCircularGauge").ejCircularGauge({ scales: [{ ticks: [{ width: 3 }] }] });
</script>{% endhighlight %}




### theme `string`
{:#members:theme}




Specify the theme of circular gauge.


#### Default Value



* "flatlight"




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
        $("#CoreCircularGauge").ejCircularGauge({  theme : "flatlight" });
</script>{% endhighlight %}




### tooltip `object`
{:#members:tooltip}




Specify tooltip option of circular gauge


#### Default Value



* object




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showLabelTooltip: true,showCustomLabelTooltip: true,templateID: null} });
</script>{% endhighlight %}




### tooltip.showCustomLabelTooltip `boolean`
{:#members:tooltip.showcustomlabeltooltip}




enable showCustomLabelTooltip of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showCustomLabelTooltip: true} });
</script>{% endhighlight %}




### tooltip.showLabelTooltip `boolean`
{:#members:tooltip.showlabeltooltip}




enable showLabelTooltip of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showLabelTooltip: true} });
</script>{% endhighlight %}




### tooltip.templateID `string`
{:#members:tooltip.templateid}




Specify tooltip templateID of circular gauge


#### Default Value



* false




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>                  
$("#CoreCircularGauge").ejCircularGauge({  tooltip:{showLabelTooltip: true, templateID: "template1"} });
</script>{% endhighlight %}




### value `number`
{:#members:value}




Specifies the value of circular gauge.


#### Default Value



* 0




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ value: 30 });
</script>{% endhighlight %}




### width `number`
{:#members:width}




Specifies the width of circular gauge.


#### Default Value



* 360




#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({ width: 400 });
</script>{% endhighlight %}



## Methods




### destroy()
{:#methods:destroy}




destroy the circular gauge widget. all events bound using this._on will be unbind automatically and bring the control to pre-init state.



#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.destroy();
</script>{% endhighlight %}




### exportImage()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.exportImage("myImage","jpeg");
</script>{% endhighlight %}




### getBackNeedleLength()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true }] }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getBackNeedleLength(0, 0);
</script>{% endhighlight %}




### getCustomLabelAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{textAngle:30,value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getCustomLabelAngle(0, 0);
</script>{% endhighlight %}




### getCustomLabelValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{textAngle:30,value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getCustomLabelValue(0, 0);
</script>{% endhighlight %}




### getLabelAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelAngle(0, 0);
</script>{% endhighlight %}




### getLabelDistanceFromScale()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelDistanceFromScale(0, 0);
</script>{% endhighlight %}




### getLabelPlacement()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelPlacement(0, 0);
</script>{% endhighlight %}




### getLabelStyle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getLabelStyle(0, 0);
</script>{% endhighlight %}




### getMajorIntervalValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMajorIntervalValue(0);
</script>{% endhighlight %}




### getMarkerDistanceFromScale()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMarkerDistanceFromScale(0, 0);
</script>{% endhighlight %}




### getMarkerStyle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMarkerStyle(0, 0);
</script>{% endhighlight %}




### getMaximumValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMaximumValue(0);
</script>{% endhighlight %}




### getMinimumValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMinimumValue(0);
</script>{% endhighlight %}




### getMinorIntervalValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getMinorIntervalValue(0);
</script>{% endhighlight %}




### getNeedleStyle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getNeedleStyle(0, 0);
</script>{% endhighlight %}




### getPointerCapBorderWidth()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerCapBorderWidth(0);
</script>{% endhighlight %}




### getPointerCapRadius()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerCapRadius(0);
</script>{% endhighlight %}




### getPointerLength()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerLength(0, 0);
</script>{% endhighlight %}




### getPointerNeedleType()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerNeedleType(0, 0);
</script>{% endhighlight %}




### getPointerPlacement()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerPlacement(0, 0);
</script>{% endhighlight %}




### getPointerValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerValue(0, 0);
</script>{% endhighlight %}




### getPointerWidth()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getPointerWidth(0, 0);
</script>{% endhighlight %}




### getRangeBorderWidth()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeBorderWidth(0, 0);
</script>{% endhighlight %}




### getRangeDistanceFromScale()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeDistanceFromScale(0, 0);
</script>{% endhighlight %}




### getRangeEndValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeEndValue(0, 0);
</script>{% endhighlight %}




### getRangePosition()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangePosition(0, 0);
</script>{% endhighlight %}




### getRangeSize()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeSize(0, 0);
</script>{% endhighlight %}




### getRangeStartValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getRangeStartValue(0, 0);
</script>{% endhighlight %}




### getScaleBarSize()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleBarSize(0);
</script>{% endhighlight %}




### getScaleBorderWidth()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{Width: 1.5} }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleBorderWidth(0);
</script>{% endhighlight %}




### getScaleDirection()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleDirection(0);
</script>{% endhighlight %}




### getScaleRadius()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getScaleRadius(0);
</script>{% endhighlight %}




### getStartAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getStartAngle(0);
</script>{% endhighlight %}




### getSubGaugeLocation()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<div id="subGauge1">
</div> 
 
<script>
$("#subGauge1").ejCircularGauge({backgroundColor: "#f5b43f",scales: [{radius: 150}]});
$("#CoreCircularGauge").ejCircularGauge({height: 500,width: 500,scales: [{radius: 250,subGauges: [{controlID: "subGauge1",height: 400,width: 200,position: { x: 200, y: 150 }}]}]});
circulargaugeObj.getSubGaugeLocation(0, 0);
</script>{% endhighlight %}




### getSweepAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getSweepAngle(0);
</script>{% endhighlight %}




### getTickAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickAngle(0, 0);
</script>{% endhighlight %}




### getTickDistanceFromScale()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickDistanceFromScale(0, 0);
</script>{% endhighlight %}




### getTickHeight()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickHeight(0, 0);
</script>{% endhighlight %}




### getTickPlacement()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickPlacement(0, 0);
</script>{% endhighlight %}




### getTickStyle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickStyle(0, 0);
</script>{% endhighlight %}




### getTickWidth()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.getTickWidth(0, 0);
</script>{% endhighlight %}




### includeFirstValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.includeFirstValue(0, 0, false);
</script>{% endhighlight %}




### redraw()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.redraw("scale");
</script>{% endhighlight %}




### setBackNeedleLength()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({ scales: [{ pointers: [{ showBackNeedle: true }] }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setBackNeedleLength(0, 0, 10);
</script>{% endhighlight %}




### setCustomLabelAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{value:"MyLabel",position:{x:250,y:300},color:"#fc0606",font: { size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setCustomLabelAngle(0, 0, 10);
</script>{% endhighlight %}




### setCustomLabelValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{customLabels:[{value:"MyLabel",position:{x:180,y:300},color:"#fc0606",font:{size: "20px", fontFamily: "Arial", fontStyle: "Bold" }}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setCustomLabelValue(0, 0, "CircularGauge");
</script>{% endhighlight %}




### setLabelAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelAngle(0, 0, 10);
</script>{% endhighlight %}




### setLabelDistanceFromScale()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelDistanceFromScale(0, 0, 10);
</script>{% endhighlight %}




### setLabelPlacement()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelPlacement(0, 0, "far");
</script>{% endhighlight %}




### setLabelStyle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setLabelStyle(0, 0, "major");
</script>{% endhighlight %}




### setMajorIntervalValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMajorIntervalValue(0, 10);
</script>{% endhighlight %}




### setMarkerDistanceFromScale()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMarkerDistanceFromScale(0, 0, 10);
</script>{% endhighlight %}




### setMarkerStyle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMarkerStyle(0, 0, "rectangle");
</script>{% endhighlight %}




### setMaximumValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMaximumValue(0, 130);
</script>{% endhighlight %}




### setMinimumValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMinimumValue(0, 10);
</script>{% endhighlight %}




### setMinorIntervalValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setMinorIntervalValue(0, 2);
</script>{% endhighlight %}




### setNeedleStyle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setNeedleStyle(0, 0, "arrow");
</script>{% endhighlight %}




### setPointerCapBorderWidth()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerCapBorderWidth(0, 5);
</script>{% endhighlight %}




### setPointerCapRadius()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerCapRadius(0, 10);
</script>{% endhighlight %}




### setPointerLength()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerLength(0, 0, 90);
</script>{% endhighlight %}




### setPointerNeedleType()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerNeedleType(0, 0, "triangle");
</script>{% endhighlight %}




### setPointerPlacement()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerPlacement(0, 0,"near");
</script>{% endhighlight %}




### setPointerValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerValue(0, 0, 10);
</script>{% endhighlight %}




### setPointerWidth()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setPointerWidth(0, 0, 10);
</script>{% endhighlight %}




### setRangeBorderWidth()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeBorderWidth(0, 0, 5);
</script>{% endhighlight %}




### setRangeDistanceFromScale()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeDistanceFromScale(0, 0, 10);
</script>{% endhighlight %}




### setRangeEndValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeEndValue(0, 0, 70);
</script>{% endhighlight %}




### setRangePosition()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangePosition(0, 0, "far");
</script>{% endhighlight %}




### setRangeSize()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeSize(0, 0, 10);
</script>{% endhighlight %}




### setRangeStartValue()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({scales: [{showRanges: true,ranges: [{distanceFromScale: -30,startValue: 0,endValue: 70}]}]});
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setRangeStartValue(0, 0, 10);
</script>{% endhighlight %}




### setScaleBarSize()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleBarSize(0, 160);
</script>{% endhighlight %}




### setScaleBorderWidth()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge({ scales: [{showScaleBar: true, size: 6, border:{width: 1.5} }] });
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleBorderWidth(0, 3);
</script>{% endhighlight %}




### setScaleDirection()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleDirection(0, "clockwise");
</script>{% endhighlight %}




### setScaleRadius()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setScaleRadius(0, 140);
</script>{% endhighlight %}




### setStartAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setStartAngle(0, 10);
</script>{% endhighlight %}




### setSubGaugeLocation()
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


#### Example


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




### setSweepAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setSweepAngle(0, 220);
</script>{% endhighlight %}




### setTickAngle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickAngle(0, 0, 10);
</script>{% endhighlight %}




### setTickDistanceFromScale()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickDistanceFromScale(0, 0, 15);
</script>{% endhighlight %}




### setTickHeight()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickHeight(0, 0, 10);
</script>{% endhighlight %}




### setTickPlacement()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script> 
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickPlacement(0, 0, "near");
</script>{% endhighlight %}




### setTickStyle()
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


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge"></div> 
  
<script>
$("#CoreCircularGauge").ejCircularGauge();
var circulargaugeObj = $("#CoreCircularGauge").data("ejCircularGauge");
circulargaugeObj.setTickStyle(0, 0, "minor");
</script>{% endhighlight %}




### setTickWidth()
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


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the custom label</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the custom label belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the custom label style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customLabelElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current custom label element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customLabelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the custom label.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the indicator</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the indicator belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the indicator style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
indicatorElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current indicator element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
indicatorIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the indicator.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the labels</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the label belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the label style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
label{% endhighlight %}</td>
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
pointerValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the label.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer cap.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer cap style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
pointer{% endhighlight %}</td>
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
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the range</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the range belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the range style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rangeElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the current range element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the range.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the ticks</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the tick belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the ticks style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
tick{% endhighlight %}</td>
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
pointerValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the label value of the tick.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
pointer{% endhighlight %}</td>
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
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
pointer{% endhighlight %}</td>
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
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
pointer{% endhighlight %}</td>
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
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>


#### Example


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
object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="CoreCircularGauge">
</div> 
 
<script>
$("#CoreCircularGauge").ejCircularGauge({
   renderComplete: function (args) {}
});
</script>{% endhighlight %}

