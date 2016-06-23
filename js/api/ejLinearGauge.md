---
layout: post
title: Properties, Methods and Events of ejLinearGauge Widget
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejLinearGauge
<ts root="datavisualization" />

The Linear gauge can be easily configured to the DOM element, such as div. you can create a linear gauge with a highly customizable look and feel.










$(element).ejLinearGauge(options)







<table class="params">
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
<td class="description last">For setting the Linear gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$('#LinearGauge1').ejLinearGauge();     
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.common.all


* module:excanvas.js




## Members








### animationSpeed `number`
{:#members:animationspeed}








Specifies the animationSpeed




#### Default Value






* 500








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ animationSpeed: 1000, value:50});
</script>    {% endhighlight %}







### backgroundColor `string`
{:#members:backgroundcolor}








Specifies the backgroundColor for Linear gauge.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ backgroundColor: "Red" });   
</script> {% endhighlight %}







### borderColor `string`
{:#members:bordercolor}








Specifies the borderColor for Linear gauge.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ borderColor: "Red" });   
</script> {% endhighlight %}







### enableAnimation `boolean`
{:#members:enableanimation}








Specifies the animate state




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ enableAnimation: true, value:50});  
</script> {% endhighlight %}







### enableMarkerPointerAnimation `boolean`
{:#members:enablemarkerpointeranimation}








Specifies the animate state for marker pointer




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ enableMarkerPointerAnimation: true, value:50});  
</script> {% endhighlight %}







### isResponsive `boolean`
{:#members:isresponsive}








Specifies the can resize state.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ isResponsive: true });   
</script> {% endhighlight %}







### frame `object`
{:#members:frame}








Specify frame of linear gauge




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
  
<div id="LinearGauge1">
</div> 
 
<script>                  
$("#LinearGauge1").ejLinearGauge({ frame: { backgroundImageUrl:null, outerWidth:12, innerWidth:8 } });
</script>{% endhighlight %}







### frame.backgroundImageUrl `string`
{:#members:frame-backgroundimageurl}








Specifies the frame background image URL of linear gauge




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
        $("#LinearGauge1").ejLinearGauge({ frame:{backgroundImageUrl: "bg.png"} });  
</script> {% endhighlight %}







### frame.innerWidth `number`
{:#members:frame-innerwidth}








Specifies the frame InnerWidth




#### Default Value






* 8








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ frame:{innerWidth: 9}});   
</script> {% endhighlight %}







### frame.outerWidth `number`
{:#members:frame-outerwidth}








Specifies the frame OuterWidth




#### Default Value






* 12








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ frame:{outerWidth: 13 }});   
</script> {% endhighlight %}







### height `number`
{:#members:height}








Specifies the height of Linear gauge.




#### Default Value






* 400








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({ height: 360 }); 
</script>   {% endhighlight %}







### labelColor `string`
{:#members:labelcolor}








Specifies the labelColor for Linear gauge.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ labelColor: "Red" });   
</script> {% endhighlight %}







### maximum `number`
{:#members:maximum}








Specifies the maximum value of Linear gauge.




#### Default Value






* 100








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ maximum: 110 }); 
</script>    {% endhighlight %}







### minimum `number`
{:#members:minimum}








Specifies the minimum value of Linear gauge.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({ minimum: 10 });  
</script>   {% endhighlight %}







### orientation `string`
{:#members:orientation}








Specifies the orientation for Linear gauge.




#### Default Value






* "Vertical"








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ orientation: "Vertical" });   
</script> {% endhighlight %}







### outerCustomLabelPosition `enum`
{:#members:outercustomlabelposition}


<ts name = "ej.datavisualization.LinearGauge.OuterCustomLabelPosition"/>

Specify labelPosition value of Linear gauge See <a href="global.html#OuterCustomLabelPosition">OuterCustomLabelPosition</a>



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
Left</td>
<td class="type">string</td> 
<td class="description">Label will be placed on left side of the gauge</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="description">Label will be placed on right side of the gauge</td>
</tr> 
<tr>
<td class="name">
Top</td>
<td class="type">string</td>
<td class="description">Label will be placed on top of the gauge</td>
</tr> 
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="description">Label will be placed on bottom of the gauge</td>
</tr> 
</tbody>
</table>





#### Default Value






* bottom








#### Example


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  outerCustomLabelPosition:"top" });
</script>{% endhighlight %}







### pointerGradient1 `object`
{:#members:pointergradient1}








Specifies the pointerGradient1 for Linear gauge.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({ pointerGradient1: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } });  
</script>  {% endhighlight %}







### pointerGradient2 `object`
{:#members:pointergradient2}








Specifies the pointerGradient2 for Linear gauge.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ pointerGradient2: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } });  
</script>  {% endhighlight %}







### readOnly `boolean`
{:#members:readonly}








Specifies the read only state.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ readOnly: false });   
</script> {% endhighlight %}







### scales `object`
{:#members:scales}








Specifies the scales




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ scales: [{}]});   
</script> {% endhighlight %}







### scales.backgroundColor `string`
{:#members:scales-backgroundcolor}








Specifies the backgroundColor of the Scale.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{backgroundColor:"red"}]}); 
</script>                         {% endhighlight %}







### scales.barPointers `Array`
{:#members:scales-barpointers}








Specifies the scaleBar Gradient of bar pointer




#### Default Value






* Array








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{}]}]});                              
</script>                  {% endhighlight %}







### scales.barPointers.backgroundColor `string`
{:#members:scales-barpointers-backgroundcolor}








Specifies the backgroundColor of bar pointer




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, backgroundColor: "red"}]}]});              
</script>                 {% endhighlight %}







### scales.barPointers.border `object`
{:#members:scales-barpointers-border}








Specifies the border of bar pointer




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, border:{color: "red", width:1.5}}]}]});    
</script>                                 {% endhighlight %}







### scales.barPointers.border.color `string`
{:#members:scales-barpointers-border-color}








Specifies the border Color of bar pointer




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, border:{color: "red"}}]}]});       
</script>                                 {% endhighlight %}







### scales.barPointers.border.width `number`
{:#members:scales-barpointers-border-width}








Specifies the border Width of bar pointer




#### Default Value






* 1.5








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, border:{width: 2}}]}]});           
</script>                                 {% endhighlight %}







### scales.barPointers.distanceFromScale `number`
{:#members:scales-barpointers-distancefromscale}








Specifies the distanceFromScale of bar pointer




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, distanceFromScale: 20}]}]});               
</script>                         {% endhighlight %}







### scales.barPointers.gradients `object`
{:#members:scales-barpointers-gradients}








Specifies the scaleBar Gradient of bar pointer




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, gradients: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}]}]});               
</script> {% endhighlight %}







### scales.barPointers.opacity `number`
{:#members:scales-barpointers-opacity}








Specifies the opacity of bar pointer




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, opacity: 0.5}]}]});        
</script> {% endhighlight %}







### scales.barPointers.value `number`
{:#members:scales-barpointers-value}








Specifies the value of bar pointer




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value: 100}]}]});            
</script>                         {% endhighlight %}







### scales.barPointers.width `number`
{:#members:scales-barpointers-width}








Specifies the pointer Width of bar pointer




#### Default Value






* width=30








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, width: 25}]}]});           
</script>                 {% endhighlight %}







### scales.border `object`
{:#members:scales-border}








Specifies the border of the Scale.




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{border:{color:"red", width:1.5}}]});       
</script>                                 {% endhighlight %}







### scales.border.color `string`
{:#members:scales-border-color}








Specifies the border color of the Scale.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{border:{color:"red"}}]});  
</script>                                 {% endhighlight %}







### scales.border.width `number`
{:#members:scales-border-width}








Specifies the border width of the Scale.




#### Default Value






* 1.5








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{border:{width:2.5}}]});    
</script>                                 {% endhighlight %}







### scales.customLabels `Array`
{:#members:scales-customlabels}








Specifies the customLabel




#### Default Value






* Array








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                                 {% endhighlight %}







### scales.customLabels.color `number`
{:#members:scales-customlabels-color}








Specifies the label Color in customLabels




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"yellow", font: { size: "20px",fontFamily: "Arial", fontStyle: "Bold" }}]}]});
</script>                         {% endhighlight %}







### scales.customLabels.font `object`
{:#members:scales-customlabels-font}








Specifies the font in customLabels




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                 {% endhighlight %}







### scales.customLabels.font.fontFamily `string`
{:#members:scales-customlabels-font-fontfamily}








Specifies the fontFamily in customLabels




#### Default Value






* "Arial"








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                 {% endhighlight %}







### scales.customLabels.font.fontStyle `enum`
{:#members:scales-customlabels-font-fontstyle}


<ts name = "ej.datavisualization.LinearGauge.FontStyle"/>

Specifies the fontStyle in customLabels. See <a href="global.html#FontStyle">FontStyle</a>


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
Bold</td>
<td class="type">string</td> 
<td class="description">Sets the font style as bold</td>
</tr>
<tr>
<td class="name">
Italic</td>
<td class="type">string</td>
<td class="description">Sets the font style as italic</td>
</tr> 
<tr>
<td class="name">
Regular</td>
<td class="type">string</td>
<td class="description">Sets the font style as regular</td>
</tr> 
<tr>
<td class="name">
Strikeout</td>
<td class="type">string</td>
<td class="description">Sets the font style as strikeout</td>
</tr> 
<tr>
<td class="name">
Underline</td>
<td class="type">string</td>
<td class="description">Sets the font style as underline</td>
</tr> 
</tbody>
</table>




#### Default Value
* Bold








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script> {% endhighlight %}







### scales.customLabels.font.size `string`
{:#members:scales-customlabels-font-size}








Specifies the font size in customLabels




#### Default Value






* "11px"








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                         {% endhighlight %}







### scales.customLabels.opacity `string`
{:#members:scales-customlabels-opacity}








Specifies the opacity in customLabels




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606",opacity:0.5, font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                                 {% endhighlight %}







### scales.customLabels.position `object`
{:#members:scales-customlabels-position}








Specifies the position in customLabels




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});           
</script>         {% endhighlight %}







### scales.customLabels.position.x `number`
{:#members:scales-customlabels-position-x}








Specifies the position x in customLabels




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ textAngle: 20,value:"LinearGauge", position:{x:10,y:50}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});              
</script>                 {% endhighlight %}







### scales.customLabels.position.y `number`
{:#members:scales-customlabels-position-y}








Specifies the y in customLabels




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ textAngle: 20,value:"LinearGauge", position:{x:49,y:10}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});              
</script>                         {% endhighlight %}







### scales.customLabels.positionType `object`
{:#members:scales-customlabels-positiontype}








Specifies the positionType in customLabels.See <a href="global.html#CustomLabelPositionType">CustomLabelPositionType</a>




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ positionType:"outer",value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});              
</script>         {% endhighlight %}







### scales.customLabels.textAngle `number`
{:#members:scales-customlabels-textangle}








Specifies the textAngle in customLabels




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ textAngle: 20,value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});             
</script>                         {% endhighlight %}







### scales.customLabels.value `string`
{:#members:scales-customlabels-value}








Specifies the label Value in customLabels




#### Default Value






* ""








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                 {% endhighlight %}







### scales.direction `enum`
{:#members:scales-direction}


<ts name = "ej.datavisualization.LinearGauge.Direction"/>

Specifies the scale Direction of the Scale. See <a href="global.html#Directions">Directions</a>


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
<td class="description">Specify the scale direction as clockwise</td>
</tr>
<tr>
<td class="name">
CounterClockwise</td>
<td class="type">string</td>
<td class="description">Specify the scale direction as counterclockwise</td>
</tr> 
</tbody>
</table>





#### Default Value






* CounterClockwise








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{direction:ej.datavisualization.LinearGauge.Directions.Clockwise}]});       
</script>                                 {% endhighlight %}







### scales.indicators `Array`
{:#members:scales-indicators}








Specifies the indicator




#### Default Value






* Array








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({scales: [{showBarPointers: false, showIndicators: true, length: 310, indicators: [{
   font: {size: "11px",fontFamily: "Arial",fontStyle: "bold"},height: 30,
   type: "rectangle",width: 30,position: {x: 60,y: 70},textLocation: {x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 50,backgroundColor: "Red",borderColor: "Green",textColor: null}],
   value: 0, backgroundColor: "Red", border:{color: "Red", width: 1.5}, opacity: NaN}]}]});             
</script>                 {% endhighlight %}







### scales.indicators.backgroundColor `string`
{:#members:scales-indicators-backgroundcolor}








Specifies the backgroundColor in bar indicators




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   backgroundColor:"green"}]}]});       
</script>         {% endhighlight %}







### scales.indicators.border `number`
{:#members:scales-indicators-border}








Specifies the border in bar indicators




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   border:{color:"red", width: 5}}]}]});                
</script>                 {% endhighlight %}







### scales.indicators.border.color `string`
{:#members:scales-indicators-border-color}








Specifies the border Color in bar indicators




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   border:{color: "Red"}}]}]}); 
</script>         {% endhighlight %}







### scales.indicators.border.width `number`
{:#members:scales-indicators-border-width}








Specifies the border Width in bar indicators




#### Default Value






* 1.5








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   border:{width: 5}}]}]});             
</script>                 {% endhighlight %}







### scales.indicators.font `object`
{:#members:scales-indicators-font}








Specifies the font of bar indicators




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "bold" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>                         {% endhighlight %}







### scales.indicators.font.fontFamily `string`
{:#members:scales-indicators-font-fontfamily}








Specifies the fontFamily of font in bar indicators




#### Default Value






* "Arial"








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Segoe UI", fontStyle: "bold" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});                       
</script> {% endhighlight %}







### scales.indicators.font.fontStyle `enum`
{:#members:scales-indicators-font-fontstyle}


<ts ref = "ej.datavisualization.LinearGauge.FontStyle"/>





Specifies the fontStyle of font in bar indicators. See <a href="global.html#FontStyle">FontStyle</a>




#### Default Value






* ej.datavisualization.LinearGauge.FontStyle.Bold








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
</script>                 {% endhighlight %}







### scales.indicators.font.size `string`
{:#members:scales-indicators-font-size}








Specifies the size of font in bar indicators




#### Default Value






* "11px"








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "20px", fontFamily: "Arial", fontStyle: "bold" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
</script>                         {% endhighlight %}







### scales.indicators.height `number`
{:#members:scales-indicators-height}








Specifies the indicator Height of bar indicators




#### Default Value






* 30








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   type: "rectangle",height: 50,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});   
</script>                                  {% endhighlight %}







### scales.indicators.opacity `number`
{:#members:scales-indicators-opacity}








Specifies the opacity in bar indicators




#### Default Value






* NaN








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ readonly:false, scales: [{showBarPointers: false, showIndicators: true, indicators: [{height: 30,
type: "rectangle",position: {x: 80,y: 110},
stateRanges: [{endValue: 80,startValue: 50,backgroundColor: "Red",borderColor: "Green",textColor: null}],
value: 0, backgroundColor: "Red", border:{color: "Green"}, opacity:0.5}]}]});
</script>                 {% endhighlight %}







### scales.indicators.position `object`
{:#members:scales-indicators-position}








Specifies the position in bar indicators




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});           
</script>         {% endhighlight %}







### scales.indicators.position.x `number`
{:#members:scales-indicators-position-x}








Specifies the x position in bar indicators




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 20,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});           
</script>         {% endhighlight %}







### scales.indicators.position.y `number`
{:#members:scales-indicators-position-y}








Specifies the y position in bar indicators




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 100},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});
</script>                 {% endhighlight %}







### scales.indicators.stateRanges `Array`
{:#members:scales-indicators-stateranges}








Specifies the state ranges in bar indicators




#### Default Value






* Array








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
</script>                 {% endhighlight %}







### scales.indicators.stateRanges.backgroundColor `string`
{:#members:scales-indicators-stateranges-backgroundcolor}








Specifies the backgroundColor in bar indicators state ranges




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Red",borderColor: "Green"}],
   border:{width: 1.5}}]}]});
</script> {% endhighlight %}







### scales.indicators.stateRanges.borderColor `string`
{:#members:scales-indicators-stateranges-bordercolor}








Specifies the borderColor in bar indicators state ranges




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   border:{width: 1.5}}]}]});
</script> {% endhighlight %}







### scales.indicators.stateRanges.endValue `number`
{:#members:scales-indicators-stateranges-endvalue}








Specifies the endValue in bar indicators state ranges




#### Default Value






* 60








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>         {% endhighlight %}







### scales.indicators.stateRanges.startValue `number`
{:#members:scales-indicators-stateranges-startvalue}








Specifies the startValue in bar indicators state ranges




#### Default Value






* 50








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>                                 {% endhighlight %}







### scales.indicators.stateRanges.text `string`
{:#members:scales-indicators-stateranges-text}








Specifies the text in bar indicators state ranges




#### Default Value






* ""








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 20, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Green", text: "Linear Gauge" }],opacity: 0.5}]}]}); 
</script>                                 {% endhighlight %}







### scales.indicators.stateRanges.textColor `string`
{:#members:scales-indicators-stateranges-textcolor}








Specifies the textColor in bar indicators state ranges




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Red", text: "Linear" }],opacity: 0.5}]}]}); 
</script>                                 {% endhighlight %}







### scales.indicators.textLocation `object`
{:#members:scales-indicators-textlocation}








Specifies the textLocation in bar indicators




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
</script>         {% endhighlight %}







### scales.indicators.textLocation.x `number`
{:#members:scales-indicators-textlocation-x}








Specifies the textLocation position in bar indicators




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 0 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>         {% endhighlight %}







### scales.indicators.textLocation.y `number`
{:#members:scales-indicators-textlocation-y}








Specifies the Y position in bar indicators




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>                 {% endhighlight %}







### scales.indicators.type `enum`
{:#members:scales-indicators-type}



<ts name = "ej.datavisualization.LinearGauge.IndicatorTypes"/>

Specifies the indicator Style of font in bar indicators


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
<td class="description">Style of the indicator will be Circle</td>
</tr> 
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="description">Style of the indicator will be rounded rectangle</td>
</tr> 
<tr>
<td class="name">
Text</td>
<td class="type">string</td>
<td class="description">Style of the indicator will be text</td>
</tr> 
</tbody>
</table>




#### Default Value






* ej.datavisualization.LinearGauge.IndicatorType.Rectangle








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});
</script> {% endhighlight %}







### scales.indicators.width `number`
{:#members:scales-indicators-width}








Specifies the indicator Width in bar indicators




#### Default Value






* 30








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   type: "rectangle",width: 50,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});
</script>                         {% endhighlight %}







### scales.labels `Array`
{:#members:scales-labels}








Specifies the labels.




#### Default Value






* Array








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{y:1}}]}]});                    
</script> {% endhighlight %}







### scales.labels.angle `number`
{:#members:scales-labels-angle}








Specifies the angle of labels.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{angle:30}]}]});                           
</script> {% endhighlight %}







### scales.labels.distanceFromScale `object`
{:#members:scales-labels-distancefromscale}








Specifies the DistanceFromScale of labels.




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{x:10, y:10}}]}]});             
</script>                         {% endhighlight %}







### scales.labels.distanceFromScale.x `number`
{:#members:scales-labels-distancefromscale-x}








Specifies the xDistanceFromScale of labels.




#### Default Value






* -10








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{x:10}}]}]});           
</script>                         {% endhighlight %}







### scales.labels.distanceFromScale.y `number`
{:#members:scales-labels-distancefromscale-y}








Specifies the yDistanceFromScale of labels.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{y:20}}]}]});           
</script> {% endhighlight %}







### scales.labels.font `object`
{:#members:scales-labels-font}








Specifies the font of labels.




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{size: "11px"}}]}]});                
</script>         {% endhighlight %}







### scales.labels.font.fontFamily `string`
{:#members:scales-labels-font-fontfamily}








Specifies the fontFamily of font.




#### Default Value






* "Arial"








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{fontFamily: "Segoe UI"}}]}]});              
</script>                         {% endhighlight %}







### scales.labels.font.fontStyle `enum`
{:#members:scales-labels-font-fontstyle}


<ts ref = "ej.datavisualization.LinearGauge.FontStyle"/>





Specifies the fontStyle of font.See <a href="global.html#FontStyle">FontStyle</a>




#### Default Value






* ej.datavisualization.LinearGauge.FontStyle.Bold








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{fontStyle: ej.datavisualization.LinearGauge.FontStyle.Normal}}]}]});                
</script>                 {% endhighlight %}







### scales.labels.font.size `string`
{:#members:scales-labels-font-size}








Specifies the size of font.




#### Default Value






* "11px"








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{size: "18px"}}]}]});                
</script>                 {% endhighlight %}







### scales.labels.includeFirstValue `boolean`
{:#members:scales-labels-includefirstvalue}








need to includeFirstValue.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{includeFirstValue: false}]}]});           
</script>                 {% endhighlight %}







### scales.labels.opacity `number`
{:#members:scales-labels-opacity}








Specifies the opacity of label.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{opacity: 0.5}]}]});               
</script>                         {% endhighlight %}







### scales.labels.placement `enum`
{:#members:scales-labels-placement}

<ts name = "ej.datavisualization.LinearGauge.PointerPlacement"/>

Specifies the label Placement of label. See <a href="global.html#LabelPlacement">LabelPlacement</a>


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
<tr>
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
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{placement: ej.datavisualization.LinearGauge.LabelPlacement.Far}]}]});     
</script>                         {% endhighlight %}







### scales.labels.textColor `string`
{:#members:scales-labels-textcolor}








Specifies the textColor of font.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{textColor: "green"}]}]});         
</script> {% endhighlight %}







### scales.labels.type `enum`
{:#members:scales-labels-type}



<ts name = "ej.datavisualization.LinearGauge.ScaleType"/>

Specifies the label Style of label. See <a href="global.html#LabelType">LabelType</a>


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
<td class="description">Specifies the label style as major</td>
</tr>
<tr>
<td class="name">
Minor</td>
<td class="type">string</td>
<td class="description">Specifies the label style as minor</td>
</tr> 
</tbody>
</table>




#### Default Value






* ej.datavisualization.LinearGauge.LabelType.Major








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{type: ej.datavisualization.LinearGauge.LabelType.Major}]}]});     
</script>                         {% endhighlight %}







### scales.labels.unitText `string`
{:#members:scales-labels-unittext}








Specifies the unitText of label.




#### Default Value






* ""








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{unitText: "F"}]}]});      
</script>                                 {% endhighlight %}







### scales.labels.unitTextPlacement `enum`
{:#members:scales-labels-unittextplacement}


<ts name = "ej.datavisualization.LinearGauge.UnitTextPlacement"/>

Specifies the unitText Position of label.See <a href="global.html#UnitTextPlacement">UnitTextPlacement</a>


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
<td class="description">The unit text will be placed on back side of the gauge</td>
</tr>
<tr>
<td class="name">
From</td>
<td class="type">string</td>
<td class="description">The unit text will be placed on front side of the gauge</td>
</tr> 
</tbody>
</table>










#### Default Value






* Back








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{unitText: "F",unitTextPlacement: "front"}]}]});                           
</script>         {% endhighlight %}







### scales.length `number`
{:#members:scales-length}








Specifies the scaleBar Length.




#### Default Value






* 290








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{length:300}]});
</script>                                         {% endhighlight %}







### scales.majorIntervalValue `number`
{:#members:scales-majorintervalvalue}








Specifies the majorIntervalValue of the Scale.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{majorIntervalValue:10}]});
</script>                                         {% endhighlight %}







### scales.markerPointers `Array`
{:#members:scales-markerpointers}








Specifies the markerPointers




#### Default Value






* Array








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{type: "triangle"}]}]});   
</script>                         {% endhighlight %}







### scales.markerPointers.backgroundColor `string`
{:#members:scales-markerpointers-backgroundcolor}








Specifies the backgroundColor of marker pointer




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{backgroundColor: "blue"}]}]});            
</script> {% endhighlight %}







### scales.markerPointers.border `object`
{:#members:scales-markerpointers-border}








Specifies the border of marker pointer




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{border:{color: "blue", width: 1.5}}]}]});         
</script>         {% endhighlight %}







### scales.markerPointers.border.color `string`
{:#members:scales-markerpointers-border-color}








Specifies the border color of marker pointer




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{border:{color: "blue", width: 1.5}}]}]});         
</script>         {% endhighlight %}







### scales.markerPointers.border.width `number`
{:#members:scales-markerpointers-border-width}








Specifies the border of marker pointer




#### Default Value






* number








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{border:{color: "blue", width: 1.5}}]}]});         
</script>         {% endhighlight %}







### scales.markerPointers.distanceFromScale `number`
{:#members:scales-markerpointers-distancefromscale}








Specifies the distanceFromScale of marker pointer




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{distanceFromScale: 2}]}]});               
</script>                 {% endhighlight %}







### scales.markerPointers.gradients `object`
{:#members:scales-markerpointers-gradients}








Specifies the pointer Gradient of marker pointer




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{gradients: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}]}]});              
</script>                 {% endhighlight %}







### scales.markerPointers.length `number`
{:#members:scales-markerpointers-length}








Specifies the pointer Length of marker pointer




#### Default Value






* 30








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{length: 25}]}]});         
</script>                 {% endhighlight %}







### scales.markerPointers.opacity `number`
{:#members:scales-markerpointers-opacity}








Specifies the opacity of marker pointer




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{opacity: 0.5}]}]});               
</script>                 {% endhighlight %}







### scales.markerPointers.placement `enum`
{:#members:scales-markerpointers-placement}



<ts ref = "ej.datavisualization.LinearGauge.PointerPlacement"/>




Specifies the pointer Placement of marker pointer See <a href="global.html#PointerPlacement">PointerPlacement</a>




#### Default Value






* Far








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{placement: ej.datavisualization.LinearGauge.PointerPlacement.Near}]}]});          
</script>                 {% endhighlight %}







### scales.markerPointers.type `enum`
{:#members:scales-markerpointers-type}

<ts name = "ej.datavisualization.LinearGauge.MarkerType"/>

Specifies the marker Style of marker pointerSee <a href="global.html#MarkerType">MarkerType</a>


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
<td class="description">Style of the marker will be rectangle</td>
</tr>
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="description">Style of the marker will be triangle</td>
</tr> 
<tr>
<td class="name">
Ellipse</td>
<td class="type">string</td>
<td class="description">Style of the marker will be ellipse</td>
</tr> 
<tr>
<td class="name">
Diamond</td>
<td class="type">string</td>
<td class="description">Style of the marker will be diamond</td>
</tr> 
<tr>
<td class="name">
Pentagon</td>
<td class="type">string</td>
<td class="description">Style of the marker will be pentagon</td>
</tr> 
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="description">Style of the marker will be circle</td>
</tr> 
<tr>
<td class="name">
Star</td>
<td class="type">string</td>
<td class="description">Style of the marker will be star</td>
</tr> 
<tr>
<td class="name">
Slider</td>
<td class="type">string</td>
<td class="description">Style of the marker will be slider</td>
</tr> 
<tr>
<td class="name">
Pointer</td>
<td class="type">string</td>
<td class="description">Style of the marker will be pointer</td>
</tr> 
<tr>
<td class="name">
Wedge</td>
<td class="type">string</td>
<td class="description">Style of the marker will be wedge</td>
</tr> 
<tr>
<td class="name">
Trapezoid</td>
<td class="type">string</td>
<td class="description">Style of the marker will be trapezoid</td>
</tr> 
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="description">Style of the marker will be rounded rectangle</td>
</tr> 
</tbody>
</table>








#### Default Value






* Triangle








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{type: ej.datavisualization.LinearGauge.MarkerType.Rectangle}]}]});                
</script>                 {% endhighlight %}







### scales.markerPointers.value `number`
{:#members:scales-markerpointers-value}








Specifies the value of marker pointer




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{value: 25}]}]});          
</script>                         {% endhighlight %}







### scales.markerPointers.width `number`
{:#members:scales-markerpointers-width}








Specifies the pointer Width of marker pointer




#### Default Value






* 30








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{width: 25}]}]});          
</script>                         {% endhighlight %}







### scales.maximum `number`
{:#members:scales-maximum}








Specifies the maximum of the Scale.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{maximum:110}]});   
</script>                                 {% endhighlight %}







### scales.minimum `number`
{:#members:scales-minimum}








Specifies the minimum of the Scale.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{minimum:10}]});    
</script>                                         {% endhighlight %}







### scales.minorIntervalValue `number`
{:#members:scales-minorintervalvalue}








Specifies the minorIntervalValue of the Scale.




#### Default Value






* 2








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{minorIntervalValue:1}]});  
</script>                                         {% endhighlight %}







### scales.opacity `number`
{:#members:scales-opacity}








Specifies the opacity of the Scale.




#### Default Value






* NaN








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{opacity:0.2}]});   
</script>                                         {% endhighlight %}







### scales.position `object`
{:#members:scales-position}








Specifies the position




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{position:{x:30, y:30}}]});         
</script>                                 {% endhighlight %}







### scales.position.x `number`
{:#members:scales-position-x}








Specifies the Horizontal position




#### Default Value






* 50








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{position:{x:30}}]});               
</script>                         {% endhighlight %}







### scales.position.y `number`
{:#members:scales-position-y}








Specifies the vertical position




#### Default Value






* 50








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{position:{y:30}}]});               
</script>                                 {% endhighlight %}







### scales.ranges `Array`
{:#members:scales-ranges}








Specifies the ranges in the tick.




#### Default Value






* Array








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ranges:[{endWidth:4}]}]});         
</script>                                 {% endhighlight %}







### scales.ranges.backgroundColor `string`
{:#members:scales-ranges-backgroundcolor}








Specifies the backgroundColor in the ranges.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "Green" }] }] });                  
</script>                                 {% endhighlight %}







### scales.ranges.border `object`
{:#members:scales-ranges-border}








Specifies the border in the ranges.




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649", border:{color: "Green", width:1.5} }] }] });            
</script>                         {% endhighlight %}







### scales.ranges.border.color `string`
{:#members:scales-ranges-border-color}








Specifies the border color in the ranges.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649", border:{color: "Green"} }] }] });               
</script>                         {% endhighlight %}







### scales.ranges.border.width `number`
{:#members:scales-ranges-border-width}








Specifies the border width in the ranges.




#### Default Value






* 1.5








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649", border:{width:1.5} }] }] });            
</script>                         {% endhighlight %}







### scales.ranges.distanceFromScale `number`
{:#members:scales-ranges-distancefromscale}








Specifies the distanceFromScale in the ranges.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",distanceFromScale: 10 }] }] });  
</script>                         {% endhighlight %}







### scales.ranges.endValue `number`
{:#members:scales-ranges-endvalue}








Specifies the endValue in the ranges.




#### Default Value






* 60








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });                                        
</script>         {% endhighlight %}







### scales.ranges.endWidth `number`
{:#members:scales-ranges-endwidth}








Specifies the endWidth in the ranges.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });        
</script>                                  {% endhighlight %}







### scales.ranges.gradients `object`
{:#members:scales-ranges-gradients}








Specifies the range Gradient in the ranges.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",gradients:{ colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } }] }] });    
</script>                                 {% endhighlight %}







### scales.ranges.opacity `number`
{:#members:scales-ranges-opacity}








Specifies the opacity in the ranges.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",opacity: 0.3 }] }] });                           
</script>                 {% endhighlight %}







### scales.ranges.placement `enum`
{:#members:scales-ranges-placement}


<ts ref = "ej.datavisualization.LinearGauge.PointerPlacement"/>



Specifies the range Position in the ranges. See <a href="global.html#RangePlacement">RangePlacement</a>




#### Default Value






* Center








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",placement: "center" }] }] });
</script> {% endhighlight %}







### scales.ranges.startValue `number`
{:#members:scales-ranges-startvalue}








Specifies the startValue in the ranges.




#### Default Value






* 20








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 10, backgroundColor: "#E94649" }] }] });                       
</script>                         {% endhighlight %}







### scales.ranges.startWidth `number`
{:#members:scales-ranges-startwidth}








Specifies the startWidth in the ranges.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 20, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });                
</script>                                  {% endhighlight %}







### scales.shadowOffset `number`
{:#members:scales-shadowoffset}








Specifies the shadowOffset.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{shadowOffset:1}]});                
</script>                         {% endhighlight %}







### scales.showBarPointers `boolean`
{:#members:scales-showbarpointers}








Specifies the showBarPointers state.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showBarPointers:false}]});         
</script>                         {% endhighlight %}







### scales.showCustomLabels `boolean`
{:#members:scales-showcustomlabels}








Specifies the showCustomLabels state.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true}]}); 
</script>                                 {% endhighlight %}







### scales.showIndicators `boolean`
{:#members:scales-showindicators}








Specifies the showIndicators state.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showIndicators:true}]});   
</script>                                         {% endhighlight %}







### scales.showLabels `boolean`
{:#members:scales-showlabels}








Specifies the showLabels state.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showLabels:false}]});              
</script>                         {% endhighlight %}







### scales.showMarkerPointers `boolean`
{:#members:scales-showmarkerpointers}








Specifies the showMarkerPointers state.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showMarkerPointers:false}]});      
</script>                         {% endhighlight %}







### scales.showRanges `boolean`
{:#members:scales-showranges}








Specifies the showRanges state.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showRanges:false}]});      
</script>                                 {% endhighlight %}







### scales.showTicks `boolean`
{:#members:scales-showticks}








Specifies the showTicks state.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showTicks:false}]});                       
</script>                         {% endhighlight %}







### scales.ticks `Array`
{:#members:scales-ticks}








Specifies the ticks in the scale.




#### Default Value






* Array








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{angle:30}]}]});            
</script>                                 {% endhighlight %}







### scales.ticks.angle `number`
{:#members:scales-ticks-angle}








Specifies the angle in the tick.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{angle:20}]}]});                            
</script>                  {% endhighlight %}







### scales.ticks.color `string`
{:#members:scales-ticks-color}








Specifies the tick Color in the tick.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{color:"Blue"}]}]});        
</script>                         {% endhighlight %}







### scales.ticks.distanceFromScale `object`
{:#members:scales-ticks-distancefromscale}








Specifies the DistanceFromScale in the tick.




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{distanceFromScale:{x:10, y:10}}]}]});      
</script>                         {% endhighlight %}







### scales.ticks.distanceFromScale.x `number`
{:#members:scales-ticks-distancefromscale-x}








Specifies the xDistanceFromScale in the tick.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{distanceFromScale:{x:10}}]}]});    
</script>                         {% endhighlight %}







### scales.ticks.distanceFromScale.y `number`
{:#members:scales-ticks-distancefromscale-y}








Specifies the yDistanceFromScale in the tick.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{distanceFromScale:{y:10}}]}]});            
</script>                 {% endhighlight %}







### scales.ticks.height `number`
{:#members:scales-ticks-height}








Specifies the tick Height in the tick.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{height:8}]}]});            
</script> {% endhighlight %}







### scales.ticks.opacity `number`
{:#members:scales-ticks-opacity}








Specifies the opacity in the tick.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{opacity:0.5}]}]});                                         
</script> {% endhighlight %}







### scales.ticks.placement `enum`
{:#members:scales-ticks-placement}



<ts ref = "ej.datavisualization.LinearGauge.PointerPlacement"/>




Specifies the tick Placement in the tick. See <a href="global.html#TickPlacement">TickPlacement</a>




#### Default Value






* Near








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{placement:ej.datavisualization.LinearGauge.TickPlacement.Far}]}]});                
</script>                         {% endhighlight %}







### scales.ticks.type `enum`
{:#members:scales-ticks-type}


<ts name = "ej.datavisualization.LinearGauge.TicksType"/>

Specifies the tick Style in the tick. See <a href="global.html#TickType">TickType</a>



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
Majorinterval</td>
<td class="type">string</td> 
<td class="description">Sets the tick style as major interval</td>
</tr>
<tr>
<td class="name">
Minorinterval</td>
<td class="type">string</td>
<td class="description">Sets the tick style as minor interval</td>
</tr> 
</tbody>
</table>

#### Default Value






* MajorInterval








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{type:ej.datavisualization.LinearGauge.TickType.MajorInterval}]}]});                
</script>         {% endhighlight %}







### scales.ticks.width `number`
{:#members:scales-ticks-width}








Specifies the tick Width in the tick.




#### Default Value






* 3








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{width:4}]}]});                     
</script>                 {% endhighlight %}







### scales.type `enum`
{:#members:scales-type}

<ts name = "ej.datavisualization.LinearGauge.ScaleType"/>

Specifies the scaleBar type .See <a href="global.html#ScaleType">ScaleType</a>



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
<td class="description">Type of the scale bar will be rectangle</td>
</tr>
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="description">Type of the scale bar will be roundedrectangle</td>
</tr> 
<tr>
<td class="name">
Thermometer</td>
<td class="type">string</td>
<td class="description">Type of the scale bar will be thermometer</td>
</tr> 
</tbody>
</table>


#### Default Value






* Rectangle








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{type:ej.datavisualization.LinearGauge.ScaleType.Rectangle}]});     
</script>                         {% endhighlight %}







### scales.width `number`
{:#members:scales-width}








Specifies the scaleBar width.




#### Default Value






* 30








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{width:25}]});              
</script>                                 {% endhighlight %}







### theme `enum`
{:#members:theme}


<ts name = "ej.datavisualization.LinearGauge.Themes"/>

Specifies the theme for Linear gauge. See LinearGauge.Themes


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
FlatLight</td>
<td class="type">string</td> 
<td class="description">Theme of linear gauge will be flatlight</td>
</tr>
<tr>
<td class="name">
FlatDark</td>
<td class="type">string</td>
<td class="description">Theme of linear gauge will be flatdark</td>
</tr> 
</tbody>
</table>

#### Default Value

* flatlight








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ theme: ej.datavisualization.LinearGauge.flatdark });
</script>   {% endhighlight %}







### tickColor `string`
{:#members:tickcolor}








Specifies the tick Color for Linear gauge.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ tickColor: "Red" });   
</script> {% endhighlight %}







### tooltip `object`
{:#members:tooltip}








Specify tooltip options of linear gauge




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showLabelTooltip: true,showCustomLabelTooltip: true,templateID: null} });
</script>{% endhighlight %}







### tooltip.showCustomLabelTooltip `boolean`
{:#members:tooltip-showcustomlabeltooltip}








Specify showCustomLabelTooltip value of linear gauge




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showCustomLabelTooltip: true} });
</script>{% endhighlight %}







### tooltip.showLabelTooltip `boolean`
{:#members:tooltip-showlabeltooltip}








Specify showLabelTooltip value of linear gauge




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showLabelTooltip: true} });
</script>{% endhighlight %}







### tooltip.templateID `string`
{:#members:tooltip-templateid}








Specify templateID value of linear gauge




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showLabelTooltip: true, templateID: true} });
</script>{% endhighlight %}







### value `number`
{:#members:value}








Specifies the value of the Gauge.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({  size: 5.5});        
</script>                          {% endhighlight %}







### width `number`
{:#members:width}








Specifies the width of Linear gauge.




#### Default Value






* 150








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ width: 360 });  
</script>  {% endhighlight %}





## Methods








### destroy()
{:#methods:destroy}








destroy the linear gauge all events bound using this._on will be unbind automatically and bring the control to pre-init state.





#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge();
var linearGaugeobj = $("#LinearGauge1").data("ejLinearGauge");
linearGaugeobj.destroy();
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
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for the Image</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.fileType{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for the Image</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.exportImage("myImage","jpeg");
</script>{% endhighlight %}







### getBarDistanceFromScale()
{:#methods:getbardistancefromscale}








To get Bar Distance From Scale in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({value:50});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarDistanceFromScale(0,0);
</script>{% endhighlight %}







### getBarPointerValue()
{:#methods:getbarpointervalue}








To get Bar Pointer Value in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({value:50});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarPointerValue(0,0);
</script>{% endhighlight %}







### getBarWidth()
{:#methods:getbarwidth}








To get Bar Width in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({value:50});
// get Bar Width in number
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarWidth(0,0);
</script>{% endhighlight %}







### getCustomLabelAngle()
{:#methods:getcustomlabelangle}








To get CustomLabel Angle in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getCustomLabelAngle(0,0);
</script>{% endhighlight %}







### getCustomLabelValue()
{:#methods:getcustomlabelvalue}








To get CustomLabel Value in string

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getCustomLabelValue(0,0);
</script>{% endhighlight %}







### getLabelAngle()
{:#methods:getlabelangle}








To get Label Angle in number

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelAngle(0,0);
</script>{% endhighlight %}







### getLabelPlacement()
{:#methods:getlabelplacement}








To get LabelPlacement in number

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelPlacement(0,0);
</script>{% endhighlight %}







### getLabelStyle()
{:#methods:getlabelstyle}








To get LabelStyle in number

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelStyle(0,0);
</script>{% endhighlight %}







### getLabelXDistanceFromScale()
{:#methods:getlabelxdistancefromscale}








To get Label XDistance From Scale in number

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelXDistanceFromScale(0,0);
</script>{% endhighlight %}







### getLabelYDistanceFromScale()
{:#methods:getlabelydistancefromscale}








To get PointerValue in number

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelYDistanceFromScale(0,0);
</script>{% endhighlight %}







### getMajorIntervalValue()
{:#methods:getmajorintervalvalue}








To get Major Interval Value in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMajorIntervalValue(0);
</script>{% endhighlight %}







### getMarkerStyle()
{:#methods:getmarkerstyle}








To get MarkerStyle in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMarkerStyle(0,0);
</script>{% endhighlight %}







### getMaximumValue()
{:#methods:getmaximumvalue}








To get Maximum Value in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMaximumValue(0);
</script>{% endhighlight %}







### getMinimumValue()
{:#methods:getminimumvalue}








To get PointerValue in number

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMinimumValue(0,0);
</script>{% endhighlight %}







### getMinorIntervalValue()
{:#methods:getminorintervalvalue}








To get Minor Interval Value in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMinorIntervalValue(0);
</script>{% endhighlight %}







### getPointerDistanceFromScale()
{:#methods:getpointerdistancefromscale}








To get Pointer Distance From Scale in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerDistanceFromScale(0,0);
</script>{% endhighlight %}







### getPointerHeight()
{:#methods:getpointerheight}








To get PointerHeight in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerHeight(0,0);
</script>{% endhighlight %}







### getPointerPlacement()
{:#methods:getpointerplacement}








To get Pointer Placement in String

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerPlacement(0,0);
</script>{% endhighlight %}







### getPointerValue()
{:#methods:getpointervalue}








To get PointerValue in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerValue(0,0);
</script>{% endhighlight %}







### getPointerWidth()
{:#methods:getpointerwidth}








To get PointerWidth in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerWidth(0,0);
</script>{% endhighlight %}







### getRangeBorderWidth()
{:#methods:getrangeborderwidth}








To get Range Border Width in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeBorderWidth(0,0);
</script>{% endhighlight %}







### getRangeDistanceFromScale()
{:#methods:getrangedistancefromscale}








To get Range Distance From Scale in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeDistanceFromScale(0,0);
</script>{% endhighlight %}







### getRangeEndValue()
{:#methods:getrangeendvalue}








To get Range End Value in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeEndValue(0,0);
</script>{% endhighlight %}







### getRangeEndWidth()
{:#methods:getrangeendwidth}








To get Range End Width in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeEndWidth(0,0);
</script>{% endhighlight %}







### getRangePosition()
{:#methods:getrangeposition}








To get Range Position in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangePosition(0,0);
</script>{% endhighlight %}







### getRangeStartValue()
{:#methods:getrangestartvalue}








To get Range Start Value in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeStartValue(0,0);
</script>{% endhighlight %}







### getRangeStartWidth()
{:#methods:getrangestartwidth}








To get Range Start Width in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeStartWidth(0,0);
</script>{% endhighlight %}







### getScaleBarLength()
{:#methods:getscalebarlength}








To get ScaleBarLength in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBarLength(0);
</script>{% endhighlight %}







### getScaleBarSize()
{:#methods:getscalebarsize}








To get Scale Bar Size in number

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBarSize(0,0);
</script>{% endhighlight %}







### getScaleBorderWidth()
{:#methods:getscaleborderwidth}








To get Scale Border Width in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBorderWidth(0);
</script>{% endhighlight %}







### getScaleDirection()
{:#methods:getscaledirection}








To get Scale Direction in number

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleDirection(0,0);
</script>{% endhighlight %}







### getScaleLocation()
{:#methods:getscalelocation}








To get Scale Location in object

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleLocation(0);
</script>{% endhighlight %}







### getScaleStyle()
{:#methods:getscalestyle}








To get Scale Style in string

<table class="params">
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleStyle(0);
</script>{% endhighlight %}







### getTickAngle()
{:#methods:gettickangle}








To get Tick Angle in number

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickAngle(0,0);
</script>{% endhighlight %}







### getTickHeight()
{:#methods:gettickheight}








To get Tick Height in number

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickHeight(0,0);
</script>{% endhighlight %}







### getTickPlacement()
{:#methods:gettickplacement}








To get getTickPlacement in number

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickPlacement(0,0);
</script>{% endhighlight %}







### getTickStyle()
{:#methods:gettickstyle}








To get Tick Style in string

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickStyle(0,0);
</script>{% endhighlight %}







### getTickWidth()
{:#methods:gettickwidth}








To get Tick Width in number

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickWidth(0,0);
</script>{% endhighlight %}







### getTickXDistanceFromScale()
{:#methods:gettickxdistancefromscale}








To get get Tick XDistance From Scale in number

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickXDistanceFromScale(0,0);
</script>{% endhighlight %}







### getTickYDistanceFromScale()
{:#methods:gettickydistancefromscale}








To get Tick YDistance From Scale in number

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickYDistanceFromScale(0,0);
</script>{% endhighlight %}







### scales()
{:#methods:scales}








Specifies the scales.




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{minimum:5}]});
</script>                         {% endhighlight %}







### setBarDistanceFromScale()
{:#methods:setbardistancefromscale}








To set setBarDistanceFromScale

<table class="params">
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
<td class="description last">scaleIndex,value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Bar DistanceFromScale value for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarDistanceFromScale(0,0,30);
</script>{% endhighlight %}







### setBarPointerValue()
{:#methods:setbarpointervalue}








To set setBarPointerValue

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Bar Pointer Value for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarPointerValue(0,0,30);
</script>{% endhighlight %}







### setBarWidth()
{:#methods:setbarwidth}








To set setBarWidth

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Bar Width for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarWidth(0,0,30);
</script>{% endhighlight %}







### setCustomLabelAngle()
{:#methods:setcustomlabelangle}








To set setCustomLabelAngle

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Custom Label Angle for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setCustomLabelAngle(0,0,30);
</script>{% endhighlight %}







### setCustomLabelValue()
{:#methods:setcustomlabelvalue}








To set setCustomLabelValue

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">CustomLabel value for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setCustomLabelValue(0,0,"text");
</script>{% endhighlight %}







### setLabelAngle()
{:#methods:setlabelangle}








To set setLabelAngle

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.angle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Label Angle for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelAngle(0,0,20);
</script>{% endhighlight %}







### setLabelPlacement()
{:#methods:setlabelplacement}








To set setLabelPlacement

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Label Placement for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelPlacement(0,0,"far");
</script>{% endhighlight %}







### setLabelStyle()
{:#methods:setlabelstyle}








To set setLabelStyle

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Label Style for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelStyle(0,0,"major");
</script>{% endhighlight %}







### setLabelXDistanceFromScale()
{:#methods:setlabelxdistancefromscale}








To set setLabelXDistanceFromScale

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Label XDistance From Scale for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelXDistanceFromScale(0,0,20);
</script>{% endhighlight %}







### setLabelYDistanceFromScale()
{:#methods:setlabelydistancefromscale}








To set setLabelYDistanceFromScale

<table class="params">
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
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Label YDistance From Scale for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelYDistanceFromScale(0,0,20);
</script>{% endhighlight %}







### setMajorIntervalValue()
{:#methods:setmajorintervalvalue}








To set setMajorIntervalValue

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Major Interval Value for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMajorIntervalValue(0,5);
</script>{% endhighlight %}







### setMarkerStyle()
{:#methods:setmarkerstyle}








To set setMarkerStyle

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">marker Style for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMarkerStyle(0,0,"triangle");
</script>{% endhighlight %}







### setMaximumValue()
{:#methods:setmaximumvalue}








To set setMaximumValue

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">MaximumValue for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMaximumValue(0,20);
</script>{% endhighlight %}







### setMinimumValue()
{:#methods:setminimumvalue}








To set setMinimumValue

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">MinimumValue for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMinimumValue(0,20);
</script>{% endhighlight %}







### setMinorIntervalValue()
{:#methods:setminorintervalvalue}








To set setMinorIntervalValue

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Minor Interval Value for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMinorIntervalValue(0,2);
</script>{% endhighlight %}







### setPointerDistanceFromScale()
{:#methods:setpointerdistancefromscale}








To set setPointerDistanceFromScale

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerDistanceFromScale(0,0,30);
</script>{% endhighlight %}







### setPointerHeight()
{:#methods:setpointerheight}








To set PointerHeight

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.height{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerHeight(0,0,30);
</script>{% endhighlight %}







### setPointerPlacement()
{:#methods:setpointerplacement}








To set setPointerPlacement

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointer placement for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerPlacement(0,0,"far");
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
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pointer value for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerValue(0,0,30);
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
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.pointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.width{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pointer width for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerWidth(0,0,30);
</script>{% endhighlight %}







### setRangeBorderWidth()
{:#methods:setrangeborderwidth}








To set setRangeBorderWidth

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range Border Width for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeBorderWidth(0,0,2);
</script>{% endhighlight %}







### setRangeDistanceFromScale()
{:#methods:setrangedistancefromscale}








To set setRangeDistanceFromScale

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range Distance FromScale for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeDistanceFromScale(0,0,20);
</script>{% endhighlight %}







### setRangeEndValue()
{:#methods:setrangeendvalue}








To set setRangeEndValue

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range end value for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeEndValue(0,0,20);
</script>{% endhighlight %}







### setRangeEndWidth()
{:#methods:setrangeendwidth}








To set setRangeEndWidth

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range End Width for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeEndWidth(0,0,20);
</script>{% endhighlight %}







### setRangePosition()
{:#methods:setrangeposition}








To set setRangePosition

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range Position for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangePosition(0,0,20);
</script>{% endhighlight %}







### setRangeStartValue()
{:#methods:setrangestartvalue}








To set setRangeStartValue

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">range start value for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeStartValue(0,0,20);
</script>{% endhighlight %}







### setRangeStartWidth()
{:#methods:setrangestartwidth}








To set setRangeStartWidth

<table class="params">
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
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range Start Width for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeStartWidth(0,0,20);
</script>{% endhighlight %}







### setScaleBarLength()
{:#methods:setscalebarlength}








To set setScaleBarLength

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Scale Bar Length for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBarLength(0,150);
</script>{% endhighlight %}







### setScaleBarSize()
{:#methods:setscalebarsize}








To set setScaleBarSize

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ScaleBarSize for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBarSize(0,20);
</script>{% endhighlight %}







### setScaleBorderWidth()
{:#methods:setscaleborderwidth}








To set setScaleBorderWidth

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Scale Border Width for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBorderWidth(0,10);
</script>{% endhighlight %}







### setScaleDirection()
{:#methods:setscaledirection}








To set setScaleDirection

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Scale Direction for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleDirection(0,"counterclockwise");
</script>{% endhighlight %}







### setScaleLocation()
{:#methods:setscalelocation}








To set setScaleLocation

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Scale position for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleLocation(0,{x:20,y:20});
</script>{% endhighlight %}







### setScaleStyle()
{:#methods:setscalestyle}








To set setScaleStyle

<table class="params">
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
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleStyle(0,"thermometer");
</script>{% endhighlight %}







### setTickAngle()
{:#methods:settickangle}








To set setTickAngle

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.angle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick Angle for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickAngle(0,0,20);
</script>{% endhighlight %}







### setTickHeight()
{:#methods:settickheight}








To set setTickHeight

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick Height for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickHeight(0,0,10);
</script>{% endhighlight %}







### setTickPlacement()
{:#methods:settickplacement}








To set setTickPlacement

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick Placement for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickPlacement(0,0,"far");
</script>{% endhighlight %}







### setTickStyle()
{:#methods:settickstyle}








To set setTickStyle

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Tick Style for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickStyle(0,0,"major");
</script>{% endhighlight %}







### setTickWidth()
{:#methods:settickwidth}








To set setTickWidth

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick Width for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickWidth(0,0,5);
</script>{% endhighlight %}







### setTickXDistanceFromScale()
{:#methods:settickxdistancefromscale}








To set setTickXDistanceFromScale

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick XDistance From Scale for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickXDistanceFromScale(0,0,20);
</script>{% endhighlight %}







### setTickYDistanceFromScale()
{:#methods:settickydistancefromscale}








To set setTickYDistanceFromScale

<table class="params">
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
argument.TickIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick YDistance From Scale for Gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickYDistanceFromScale(0,0,20);
</script>{% endhighlight %}





## Events








### drawBarPointers
{:#events:drawbarpointers}








Triggers while the bar pointer are being drawn on the gauge.

<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the pointer</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
barElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current Bar pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
barPointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the bar pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
PointerValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the bar pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawBarPointers: function (args) {}
});
</script> {% endhighlight %}







### drawCustomLabel
{:#events:drawcustomlabel}








Triggers while the customLabel are being drawn on the gauge.

<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the customLabel</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the customLabel style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customLabelElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current customLabel element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customLabelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the customLabel.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawCustomLabel: function (args) {}
});
</script> {% endhighlight %}







### drawIndicators
{:#events:drawindicators}








Triggers while the Indicator are being drawn on the gauge.

<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the Indicator</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="description last">returns the Indicator style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
IndicatorElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current Indicator element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
IndicatorIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the Indicator.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawIndicators: function (args) {}
});
</script> {% endhighlight %}







### drawLabels
{:#events:drawlabels}








Triggers while the label are being drawn on the gauge.

<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the label</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the label style
<table class="params">
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
<td class="description last">returns the angle of the label.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current label element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the label.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the label value of the label.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawLabels: function (args) {}
});
</script> {% endhighlight %}







### drawMarkerPointers
{:#events:drawmarkerpointers}








Triggers while the marker are being drawn on the gauge.

<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the pointer</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="description last">returns the ticks style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
markerElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current marker pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
markerPointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the marker pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
pointerValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the marker pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
pointerAngle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the marker pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawMarkerPointers: function (args) {}
});
</script> {% endhighlight %}







### drawRange
{:#events:drawrange}








Triggers while the range are being drawn on the gauge.

<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the range</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="description last">returns the range style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rangeElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawRange: function (args) {}
});
</script> {% endhighlight %}







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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the ticks</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ticks style
<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current tick element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the tick.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the tick value of the tick.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   drawTicks: function (args) {}
});
</script> {% endhighlight %}







### init
{:#events:init}








Triggers when the gauge is initialized.

<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   init: function (args) {}
});
</script> {% endhighlight %}







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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element* @param {Object} args.markerpointer returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
markerpointerindex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
markerpointerelement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
markerpointervalue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>




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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
markerpointer{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element
<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the pointer element.</td>
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
style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the pointer style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>




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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element* @param {Object} args.markerpointer returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
markerpointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
markerpointerElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
markerpointerValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the pointer.</td>
</tr>
</tbody>
</table>




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
{:#events:rendercomplete}








Triggers while the rendering of the gauge completed.

<table class="params">
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
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   renderComplete: function (args) {}
});
</script> {% endhighlight %}



