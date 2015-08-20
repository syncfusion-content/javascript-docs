---
layout: post
title: ejLinearGauge
documentation: API
platform: js
metaname: 
metacontent: 
---

The Linera gauge can be easily configured to the DOM element, such as div. you can create a linear gauge with a highly customizable look and feel.










$(element).ejLinearGauge<span class="signature">(options)</span>







<table class="params">
<thead>
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
<td class="description last">For seting the Linear gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}


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








### animationSpeed<span class="type-signature type number">number</span>
{:#members:animationspeed}








Specifies the animationSpeed




Default Value:
{:.param}






* 500








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ animationSpeed: 1000, value:50});
</script>    {% endhighlight %}







### backgroundColor<span class="type-signature type string">string</span>
{:#members:backgroundcolor}








Specifies the backgroundColor for Linear gauge.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ backgroundColor: "Red" });   
</script> {% endhighlight %}







### borderColor<span class="type-signature type string">string</span>
{:#members:bordercolor}








Specifies the borderColor for Linear gauge.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ borderColor: "Red" });   
</script> {% endhighlight %}







### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}








Specifies the animate state




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ enableAnimation: true, value:50});  
</script> {% endhighlight %}







### enableMarkerPointerAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enablemarkerpointeranimation}








Specifies the animate state for marker pointer




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ enableMarkerPointerAnimation: true, value:50});  
</script> {% endhighlight %}







### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}








Specifies the can resize state.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ enableResize: true });   
</script> {% endhighlight %}







### frame<span class="type-signature type object">object</span>
{:#members:frame}








Specify frame of linear gauge




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
  
<div id="LinearGauge1">
</div> 
 
<script>                  
$("#LinearGauge1").ejLinearGauge({ frame: { backgroundImageUrl:null, outerWidth:12, innerWidth:8 } });
</script>{% endhighlight %}







### frame.backgroundImageUrl<span class="type-signature type string">string</span>
{:#members:frame-backgroundimageurl}








Specifies the frame backgroundimageurl of linear gauge




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
        $("#LinearGauge1").ejLinearGauge({ frame:{backgroundImageUrl: "bg.png"} });  
</script> {% endhighlight %}







### frame.innerWidth<span class="type-signature type number">number</span>
{:#members:frame-innerwidth}








Specifies the frame InnerWidth




Default Value:
{:.param}






* 8








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ frame:{innerWidth: 9}});   
</script> {% endhighlight %}







### frame.outerWidth<span class="type-signature type number">number</span>
{:#members:frame-outerwidth}








Specifies the frame OuterWidth




Default Value:
{:.param}






* 12








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ frame:{outerWidth: 13 }});   
</script> {% endhighlight %}







### height<span class="type-signature type number">number</span>
{:#members:height}








Specifies the height of Linear gauge.




Default Value:
{:.param}






* 400








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({ height: 360 }); 
</script>   {% endhighlight %}







### labelColor<span class="type-signature type string">string</span>
{:#members:labelcolor}








Specifies the labelColor for Linear gauge.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ labelColor: "Red" });   
</script> {% endhighlight %}







### maximum<span class="type-signature type number">number</span>
{:#members:maximum}








Specifies the maximum value of Linear gauge.




Default Value:
{:.param}






* 100








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ maximum: 110 }); 
</script>    {% endhighlight %}







### minimum<span class="type-signature type number">number</span>
{:#members:minimum}








Specifies the minimum value of Linear gauge.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({ minimum: 10 });  
</script>   {% endhighlight %}







### orientation<span class="type-signature type string">string</span>
{:#members:orientation}








Specifies the orientation for Linear gauge.




Default Value:
{:.param}






* "Vertical"








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ orientation: "Vertical" });   
</script> {% endhighlight %}







### outerCustomLabelPosition<span class="type-signature type enum">enum</span>
{:#members:outercustomlabelposition}








Specify enableResize value of Linear gauge See <a href="global.html#OuterCustomLabelPosition">OuterCustomLabelPosition</a>




Default Value:
{:.param}






* bottom








Example
{:.example}


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  outerCustomLabelPosition:"top" });
</script>{% endhighlight %}







### pointerGradient1<span class="type-signature type object">Object</span>
{:#members:pointergradient1}








Specifies the pointerGradient1 for Linear gauge.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({ pointerGradient1: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } });  
</script>  {% endhighlight %}







### pointerGradient2<span class="type-signature type object">object</span>
{:#members:pointergradient2}








Specifies the pointerGradient2 for Linear gauge.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ pointerGradient2: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } });  
</script>  {% endhighlight %}







### readOnly<span class="type-signature type boolean">boolean</span>
{:#members:readonly}








Specifies the read only state.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ readOnly: false });   
</script> {% endhighlight %}







### scales<span class="type-signature type object">Object</span>
{:#members:scales}








Specifies the scales




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ scales: [{}]});   
</script> {% endhighlight %}







### scales.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales-backgroundcolor}








Specifies the backgroundColor of the Scale.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{backgroundColor:"red"}]}); 
</script>                         {% endhighlight %}







### scales.barPointers<span class="type-signature type array">Array</span>
{:#members:scales-barpointers}








Specifies the scaleBar Gradient of bar pointer




Default Value:
{:.param}






* Array








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{}]}]});                              
</script>                  {% endhighlight %}







### scales.barPointers.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales-barpointers-backgroundcolor}








Specifies the backgroundColor of bar pointer




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, backgroundColor: "red"}]}]});              
</script>                 {% endhighlight %}







### scales.barPointers.border<span class="type-signature type object">object</span>
{:#members:scales-barpointers-border}








Specifies the border of bar pointer




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, border:{color: "red", width:1.5}}]}]});    
</script>                                 {% endhighlight %}







### scales.barPointers.border.color<span class="type-signature type string">string</span>
{:#members:scales-barpointers-border-color}








Specifies the border Color of bar pointer




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, border:{color: "red"}}]}]});       
</script>                                 {% endhighlight %}







### scales.barPointers.border.width<span class="type-signature type number">number</span>
{:#members:scales-barpointers-border-width}








Specifies the border Width of bar pointer




Default Value:
{:.param}






* 1.5








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, border:{width: 2}}]}]});           
</script>                                 {% endhighlight %}







### scales.barPointers.distanceFromScale<span class="type-signature type number">number</span>
{:#members:scales-barpointers-distancefromscale}








Specifies the distanceFromScale of bar pointer




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, distanceFromScale: 20}]}]});               
</script>                         {% endhighlight %}







### scales.barPointers.gradients<span class="type-signature type object">object</span>
{:#members:scales-barpointers-gradients}








Specifies the scaleBar Gradient of bar pointer




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, gradients: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}]}]});               
</script> {% endhighlight %}







### scales.barPointers.opacity<span class="type-signature type number">number</span>
{:#members:scales-barpointers-opacity}








Specifies the opacity of bar pointer




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, opacity: 0.5}]}]});        
</script> {% endhighlight %}







### scales.barPointers.value<span class="type-signature type number">number</span>
{:#members:scales-barpointers-value}








Specifies the value of bar pointer




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value: 100}]}]});            
</script>                         {% endhighlight %}







### scales.barPointers.width<span class="type-signature type number">number</span>
{:#members:scales-barpointers-width}








Specifies the pointer Width of bar pointer




Default Value:
{:.param}






* width=30








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, width: 25}]}]});           
</script>                 {% endhighlight %}







### scales.border<span class="type-signature type object">object</span>
{:#members:scales-border}








Specifies the border of the Scale.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{border:{color:"red", width:1.5}}]});       
</script>                                 {% endhighlight %}







### scales.border.color<span class="type-signature type string">string</span>
{:#members:scales-border-color}








Specifies the border color of the Scale.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{border:{color:"red"}}]});  
</script>                                 {% endhighlight %}







### scales.border.width<span class="type-signature type number">number</span>
{:#members:scales-border-width}








Specifies the border width of the Scale.




Default Value:
{:.param}






* 1.5








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{border:{width:2.5}}]});    
</script>                                 {% endhighlight %}







### scales.customLabels<span class="type-signature type array">Array</span>
{:#members:scales-customlabels}








Specifies the customLabel




Default Value:
{:.param}






* Array








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                                 {% endhighlight %}







### scales.customLabels.color<span class="type-signature type number">number</span>
{:#members:scales-customlabels-color}








Specifies the label Color in customLabels




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"yellow", font: { size: "20px",fontFamily: "Arial", fontStyle: "Bold" }}]}]});
</script>                         {% endhighlight %}







### scales.customLabels.font<span class="type-signature type object">object</span>
{:#members:scales-customlabels-font}








Specifies the font in customLabels




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                 {% endhighlight %}







### scales.customLabels.font.fontFamily<span class="type-signature type string">string</span>
{:#members:scales-customlabels-font-fontfamily}








Specifies the fontFamily in customLabels




Default Value:
{:.param}






* "Arial"








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                 {% endhighlight %}







### scales.customLabels.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:scales-customlabels-font-fontstyle}








Specifies the fontStyle in customLabels. See <a href="global.html#FontStyle">FontStyle</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.FontStyle.Bold








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script> {% endhighlight %}







### scales.customLabels.font.size<span class="type-signature type string">string</span>
{:#members:scales-customlabels-font-size}








Specifies the font size in customLabels




Default Value:
{:.param}






* "11px"








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                         {% endhighlight %}







### scales.customLabels.opacity<span class="type-signature type string">string</span>
{:#members:scales-customlabels-opacity}








Specifies the opacity in customLabels




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606",opacity:0.5, font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                                 {% endhighlight %}







### scales.customLabels.position<span class="type-signature type object">object</span>
{:#members:scales-customlabels-position}








Specifies the position in customLabels




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});           
</script>         {% endhighlight %}







### scales.customLabels.position.x<span class="type-signature type number">number</span>
{:#members:scales-customlabels-position-x}








Specifies the position x in customLabels




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ textAngle: 20,value:"LinearGauge", position:{x:10,y:50}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});              
</script>                 {% endhighlight %}







### scales.customLabels.position.y<span class="type-signature type number">number</span>
{:#members:scales-customlabels-position-y}








Specifies the y in customLabels




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ textAngle: 20,value:"LinearGauge", position:{x:49,y:10}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});              
</script>                         {% endhighlight %}







### scales.customLabels.positionType<span class="type-signature type object">object</span>
{:#members:scales-customlabels-positiontype}








Specifies the positionType in customLabels.See <a href="global.html#CustomLabelPositionType">CustomLabelPositionType</a>




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ positionType:"outer",value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});              
</script>         {% endhighlight %}







### scales.customLabels.textAngle<span class="type-signature type number">number</span>
{:#members:scales-customlabels-textangle}








Specifies the textAngle in customLabels




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ textAngle: 20,value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});             
</script>                         {% endhighlight %}







### scales.customLabels.value<span class="type-signature type string">string</span>
{:#members:scales-customlabels-value}








Specifies the label Value in customLabels




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
</script>                 {% endhighlight %}







### scales.direction<span class="type-signature type enum">enum</span>
{:#members:scales-direction}








Specifies the scale Direction of the Scale. See <a href="global.html#Directions">Directions</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.Directions.CounterClockwise








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{direction:ej.datavisualization.LinearGauge.Directions.Clockwise}]});       
</script>                                 {% endhighlight %}







### scales.indicators<span class="type-signature type array">Array</span>
{:#members:scales-indicators}








Specifies the indicator




Default Value:
{:.param}






* Array








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({scales: [{showBarPointers: false, showIndicators: true, length: 310, indicators: [{
   font: {size: "11px",fontFamily: "Arial",fontStyle: "bold"},height: 30,
   type: "rectangle",width: 30,position: {x: 60,y: 70},textLocation: {x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 50,backgroundColor: "Red",borderColor: "Green",textColor: null}],
   value: 0, backgroundColor: "Red", border:{color: "Red", width: 1.5}, opacity: NaN}]}]});             
</script>                 {% endhighlight %}







### scales.indicators.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales-indicators-backgroundcolor}








Specifies the backgroundColor in bar indicators




Default Value:
{:.param}






* null








Example
{:.example}


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







### scales.indicators.border<span class="type-signature type number">number</span>
{:#members:scales-indicators-border}








Specifies the border in bar indicators




Default Value:
{:.param}






* Object








Example
{:.example}


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







### scales.indicators.border.color<span class="type-signature type string">string</span>
{:#members:scales-indicators-border-color}








Specifies the border Color in bar indicators




Default Value:
{:.param}






* null








Example
{:.example}


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







### scales.indicators.border.width<span class="type-signature type number">number</span>
{:#members:scales-indicators-border-width}








Specifies the border Width in bar indicators




Default Value:
{:.param}






* 1.5








Example
{:.example}


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







### scales.indicators.font<span class="type-signature type object">object</span>
{:#members:scales-indicators-font}








Specifies the font of bar indicators




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "bold" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>                         {% endhighlight %}







### scales.indicators.font.fontFamily<span class="type-signature type string">string</span>
{:#members:scales-indicators-font-fontfamily}








Specifies the fontFamily of font in bar indicators




Default Value:
{:.param}






* "Arial"








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Segoe UI", fontStyle: "bold" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});                       
</script> {% endhighlight %}







### scales.indicators.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:scales-indicators-font-fontstyle}








Specifies the fontStyle of font in bar indicators. See <a href="global.html#FontStyle">FontStyle</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.FontStyle.Bold








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
</script>                 {% endhighlight %}







### scales.indicators.font.size<span class="type-signature type string">string</span>
{:#members:scales-indicators-font-size}








Specifies the size of font in bar indicators




Default Value:
{:.param}






* "11px"








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "20px", fontFamily: "Arial", fontStyle: "bold" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
</script>                         {% endhighlight %}







### scales.indicators.height<span class="type-signature type number">number</span>
{:#members:scales-indicators-height}








Specifies the indicator Height of bar indicators




Default Value:
{:.param}






* 30








Example
{:.example}


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







### scales.indicators.opacity<span class="type-signature type number">number</span>
{:#members:scales-indicators-opacity}








Specifies the opacity in bar indicators




Default Value:
{:.param}






* NaN








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ readonly:false, scales: [{showBarPointers: false, showIndicators: true, indicators: [{height: 30,
type: "rectangle",position: {x: 80,y: 110},
stateRanges: [{endValue: 80,startValue: 50,backgroundColor: "Red",borderColor: "Green",textColor: null}],
value: 0, backgroundColor: "Red", border:{color: "Green"}, opacity:0.5}]}]});
</script>                 {% endhighlight %}







### scales.indicators.position<span class="type-signature type object">object</span>
{:#members:scales-indicators-position}








Specifies the position in bar indicators




Default Value:
{:.param}






* Object








Example
{:.example}


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







### scales.indicators.position.x<span class="type-signature type number">number</span>
{:#members:scales-indicators-position-x}








Specifies the x position in bar indicators




Default Value:
{:.param}






* 0








Example
{:.example}


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







### scales.indicators.position.y<span class="type-signature type number">number</span>
{:#members:scales-indicators-position-y}








Specifies the y position in bar indicators




Default Value:
{:.param}






* 0








Example
{:.example}


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







### scales.indicators.stateRanges<span class="type-signature type array">Array</span>
{:#members:scales-indicators-stateranges}








Specifies the state ranges in bar indicators




Default Value:
{:.param}






* Array








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
</script>                 {% endhighlight %}







### scales.indicators.stateRanges.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales-indicators-stateranges-backgroundcolor}








Specifies the backgroundColor in bar indicators state ranges




Default Value:
{:.param}






* null








Example
{:.example}


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







### scales.indicators.stateRanges.borderColor<span class="type-signature type string">string</span>
{:#members:scales-indicators-stateranges-bordercolor}








Specifies the borderColor in bar indicators state ranges




Default Value:
{:.param}






* null








Example
{:.example}


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







### scales.indicators.stateRanges.endValue<span class="type-signature type number">number</span>
{:#members:scales-indicators-stateranges-endvalue}








Specifies the endValue in bar indicators state ranges




Default Value:
{:.param}






* 60








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>         {% endhighlight %}







### scales.indicators.stateRanges.startValue<span class="type-signature type number">number</span>
{:#members:scales-indicators-stateranges-startvalue}








Specifies the startValue in bar indicators state ranges




Default Value:
{:.param}






* 50








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>                                 {% endhighlight %}







### scales.indicators.stateRanges.text<span class="type-signature type string">string</span>
{:#members:scales-indicators-stateranges-text}








Specifies the text in bar indicators state ranges




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 20, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Green", text: "Linear Gauge" }],opacity: 0.5}]}]}); 
</script>                                 {% endhighlight %}







### scales.indicators.stateRanges.textColor<span class="type-signature type string">string</span>
{:#members:scales-indicators-stateranges-textcolor}








Specifies the textColor in bar indicators state ranges




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Red", text: "Linear" }],opacity: 0.5}]}]}); 
</script>                                 {% endhighlight %}







### scales.indicators.textLocation<span class="type-signature type object">object</span>
{:#members:scales-indicators-textlocation}








Specifies the textLocation in bar indicators




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
</script>         {% endhighlight %}







### scales.indicators.textLocation.x<span class="type-signature type number">number</span>
{:#members:scales-indicators-textlocation-x}








Specifies the textLocation position in bar indicators




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 0 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>         {% endhighlight %}







### scales.indicators.textLocation.y<span class="type-signature type number">number</span>
{:#members:scales-indicators-textlocation-y}








Specifies the Y position in bar indicators




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
</script>                 {% endhighlight %}







### scales.indicators.type<span class="type-signature type enum">enum</span>
{:#members:scales-indicators-type}








Specifies the indicator Style of font in bar indicators




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.IndicatorType.Rectangle








Example
{:.example}


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







### scales.indicators.width<span class="type-signature type number">number</span>
{:#members:scales-indicators-width}








Specifies the indicator Width in bar indicators




Default Value:
{:.param}






* 30








Example
{:.example}


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







### scales.labels<span class="type-signature type array">Array</span>
{:#members:scales-labels}








Specifies the labels.




Default Value:
{:.param}






* Array








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{y:1}}]}]});                    
</script> {% endhighlight %}







### scales.labels.angle<span class="type-signature type number">number</span>
{:#members:scales-labels-angle}








Specifies the angle of labels.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{angle:30}]}]});                           
</script> {% endhighlight %}







### scales.labels.distanceFromScale<span class="type-signature type object">object</span>
{:#members:scales-labels-distancefromscale}








Specifies the DistanceFromScale of labels.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{x:10, y:10}}]}]});             
</script>                         {% endhighlight %}







### scales.labels.distanceFromScale.x<span class="type-signature type number">number</span>
{:#members:scales-labels-distancefromscale-x}








Specifies the xDistanceFromScale of labels.




Default Value:
{:.param}






* -10








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{x:10}}]}]});           
</script>                         {% endhighlight %}







### scales.labels.distanceFromScale.y<span class="type-signature type number">number</span>
{:#members:scales-labels-distancefromscale-y}








Specifies the yDistanceFromScale of labels.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{y:20}}]}]});           
</script> {% endhighlight %}







### scales.labels.font<span class="type-signature type object">object</span>
{:#members:scales-labels-font}








Specifies the font of labels.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{size: "11px"}}]}]});                
</script>         {% endhighlight %}







### scales.labels.font.fontFamily<span class="type-signature type string">string</span>
{:#members:scales-labels-font-fontfamily}








Specifies the fontFamily of font.




Default Value:
{:.param}






* "Arial"








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{fontFamily: "Segoe UI"}}]}]});              
</script>                         {% endhighlight %}







### scales.labels.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:scales-labels-font-fontstyle}








Specifies the fontStyle of font.See <a href="global.html#FontStyle">FontStyle</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.FontStyle.Bold








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{fontStyle: ej.datavisualization.LinearGauge.FontStyle.Normal}}]}]});                
</script>                 {% endhighlight %}







### scales.labels.font.size<span class="type-signature type string">string</span>
{:#members:scales-labels-font-size}








Specifies the size of font.




Default Value:
{:.param}






* "11px"








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{size: "18px"}}]}]});                
</script>                 {% endhighlight %}







### scales.labels.includeFirstValue<span class="type-signature type boolean">boolean</span>
{:#members:scales-labels-includefirstvalue}








need to includeFirstValue.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{includeFirstValue: false}]}]});           
</script>                 {% endhighlight %}







### scales.labels.opacity<span class="type-signature type number">number</span>
{:#members:scales-labels-opacity}








Specifies the opacity of label.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{opacity: 0.5}]}]});               
</script>                         {% endhighlight %}







### scales.labels.placement<span class="type-signature type enum">enum</span>
{:#members:scales-labels-placement}








Specifies the label Placement of label. See <a href="global.html#LabelPlacement">LabelPlacement</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.LabelPlacement.Near








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{placement: ej.datavisualization.LinearGauge.LabelPlacement.Far}]}]});     
</script>                         {% endhighlight %}







### scales.labels.textColor<span class="type-signature type string">string</span>
{:#members:scales-labels-textcolor}








Specifies the textColor of font.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{textColor: "green"}]}]});         
</script> {% endhighlight %}







### scales.labels.type<span class="type-signature type enum">enum</span>
{:#members:scales-labels-type}








Specifies the label Style of label. See <a href="global.html#LabelType">LabelType</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.LabelType.Major








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{type: ej.datavisualization.LinearGauge.LabelType.Major}]}]});     
</script>                         {% endhighlight %}







### scales.labels.unitText<span class="type-signature type string">string</span>
{:#members:scales-labels-unittext}








Specifies the unitText of label.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{unitText: "F"}]}]});      
</script>                                 {% endhighlight %}







### scales.labels.unitTextPlacement<span class="type-signature type enum">enum</span>
{:#members:scales-labels-unittextplacement}








Specifies the unitText Position of label.See <a href="global.html#UnitTextPlacement">UnitTextPlacement</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.UnitTextPlacement.Back








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{unitText: "F",unitTextPlacement: "front"}]}]});                           
</script>         {% endhighlight %}







### scales.length<span class="type-signature type number">number</span>
{:#members:scales-length}








Specifies the scaleBar Length.




Default Value:
{:.param}






* 290








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{length:300}]});
</script>                                         {% endhighlight %}







### scales.majorIntervalValue<span class="type-signature type number">number</span>
{:#members:scales-majorintervalvalue}








Specifies the majorIntervalValue of the Scale.




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{majorIntervalValue:10}]});
</script>                                         {% endhighlight %}







### scales.markerPointers<span class="type-signature type array">Array</span>
{:#members:scales-markerpointers}








Specifies the markerPointers




Default Value:
{:.param}






* Array








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{type: "triangle"}]}]});   
</script>                         {% endhighlight %}







### scales.markerPointers.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales-markerpointers-backgroundcolor}








Specifies the backgroundColor of marker pointer




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{backgroundColor: "blue"}]}]});            
</script> {% endhighlight %}







### scales.markerPointers.border<span class="type-signature type object">object</span>
{:#members:scales-markerpointers-border}








Specifies the border of marker pointer




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{border:{color: "blue", width: 1.5}}]}]});         
</script>         {% endhighlight %}







### scales.markerPointers.border.color<span class="type-signature type string">string</span>
{:#members:scales-markerpointers-border-color}








Specifies the border color of marker pointer




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{border:{color: "blue", width: 1.5}}]}]});         
</script>         {% endhighlight %}







### scales.markerPointers.border.width<span class="type-signature type number">number</span>
{:#members:scales-markerpointers-border-width}








Specifies the border of marker pointer




Default Value:
{:.param}






* number








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{border:{color: "blue", width: 1.5}}]}]});         
</script>         {% endhighlight %}







### scales.markerPointers.distanceFromScale<span class="type-signature type number">number</span>
{:#members:scales-markerpointers-distancefromscale}








Specifies the distanceFromScale of marker pointer




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{distanceFromScale: 2}]}]});               
</script>                 {% endhighlight %}







### scales.markerPointers.gradients<span class="type-signature type object">object</span>
{:#members:scales-markerpointers-gradients}








Specifies the pointer Gradient of marker pointer




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{gradients: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}]}]});              
</script>                 {% endhighlight %}







### scales.markerPointers.length<span class="type-signature type number">number</span>
{:#members:scales-markerpointers-length}








Specifies the pointer Length of marker pointer




Default Value:
{:.param}






* 30








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{length: 25}]}]});         
</script>                 {% endhighlight %}







### scales.markerPointers.opacity<span class="type-signature type number">number</span>
{:#members:scales-markerpointers-opacity}








Specifies the opacity of marker pointer




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{opacity: 0.5}]}]});               
</script>                 {% endhighlight %}







### scales.markerPointers.placement<span class="type-signature type enum">enum</span>
{:#members:scales-markerpointers-placement}








Specifies the pointer Placement of marker pointer See <a href="global.html#PointerPlacement">PointerPlacement</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.PointerPlacement.Far








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{placement: ej.datavisualization.LinearGauge.PointerPlacement.Near}]}]});          
</script>                 {% endhighlight %}







### scales.markerPointers.type<span class="type-signature type enum">enum</span>
{:#members:scales-markerpointers-type}








Specifies the marker Style of marker pointerSee <a href="global.html#MarkerType">MarkerType</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.MarkerType.Triangle








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{type: ej.datavisualization.LinearGauge.MarkerType.Rectangle}]}]});                
</script>                 {% endhighlight %}







### scales.markerPointers.value<span class="type-signature type number">number</span>
{:#members:scales-markerpointers-value}








Specifies the value of marker pointer




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{value: 25}]}]});          
</script>                         {% endhighlight %}







### scales.markerPointers.width<span class="type-signature type number">number</span>
{:#members:scales-markerpointers-width}








Specifies the pointer Width of marker pointer




Default Value:
{:.param}






* 30








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{width: 25}]}]});          
</script>                         {% endhighlight %}







### scales.maximum<span class="type-signature type number">number</span>
{:#members:scales-maximum}








Specifies the maximum of the Scale.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{maximum:110}]});   
</script>                                 {% endhighlight %}







### scales.minimum<span class="type-signature type number">number</span>
{:#members:scales-minimum}








Specifies the minimum of the Scale.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{minimum:10}]});    
</script>                                         {% endhighlight %}







### scales.minorIntervalValue<span class="type-signature type number">number</span>
{:#members:scales-minorintervalvalue}








Specifies the minorIntervalValue of the Scale.




Default Value:
{:.param}






* 2








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{minorIntervalValue:1}]});  
</script>                                         {% endhighlight %}







### scales.opacity<span class="type-signature type number">number</span>
{:#members:scales-opacity}








Specifies the opacity of the Scale.




Default Value:
{:.param}






* NaN








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{opacity:0.2}]});   
</script>                                         {% endhighlight %}







### scales.position<span class="type-signature type object">object</span>
{:#members:scales-position}








Specifies the position




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{position:{x:30, y:30}}]});         
</script>                                 {% endhighlight %}







### scales.position.x<span class="type-signature type number">number</span>
{:#members:scales-position-x}








Specifies the Horizontal position




Default Value:
{:.param}






* 50








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{position:{x:30}}]});               
</script>                         {% endhighlight %}







### scales.position.y<span class="type-signature type number">number</span>
{:#members:scales-position-y}








Specifies the vertical position




Default Value:
{:.param}






* 50








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{position:{y:30}}]});               
</script>                                 {% endhighlight %}







### scales.ranges<span class="type-signature type array">Array</span>
{:#members:scales-ranges}








Specifies the ranges in the tick.




Default Value:
{:.param}






* Array








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ranges:[{endWidth:4}]}]});         
</script>                                 {% endhighlight %}







### scales.ranges.backgroundColor<span class="type-signature type string">string</span>
{:#members:scales-ranges-backgroundcolor}








Specifies the backgroundColor in the ranges.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "Green" }] }] });                  
</script>                                 {% endhighlight %}







### scales.ranges.border<span class="type-signature type object">Object</span>
{:#members:scales-ranges-border}








Specifies the border in the ranges.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649", border:{color: "Green", width:1.5} }] }] });            
</script>                         {% endhighlight %}







### scales.ranges.border.color<span class="type-signature type string">string</span>
{:#members:scales-ranges-border-color}








Specifies the border color in the ranges.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649", border:{color: "Green"} }] }] });               
</script>                         {% endhighlight %}







### scales.ranges.border.width<span class="type-signature type number">number</span>
{:#members:scales-ranges-border-width}








Specifies the border width in the ranges.




Default Value:
{:.param}






* 1.5








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649", border:{width:1.5} }] }] });            
</script>                         {% endhighlight %}







### scales.ranges.distanceFromScale<span class="type-signature type number">number</span>
{:#members:scales-ranges-distancefromscale}








Specifies the distanceFromScale in the ranges.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",distanceFromScale: 10 }] }] });  
</script>                         {% endhighlight %}







### scales.ranges.endValue<span class="type-signature type number">number</span>
{:#members:scales-ranges-endvalue}








Specifies the endValue in the ranges.




Default Value:
{:.param}






* 60








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });                                        
</script>         {% endhighlight %}







### scales.ranges.endWidth<span class="type-signature type number">number</span>
{:#members:scales-ranges-endwidth}








Specifies the endWidth in the ranges.




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });        
</script>                                  {% endhighlight %}







### scales.ranges.gradients<span class="type-signature type object">object</span>
{:#members:scales-ranges-gradients}








Specifies the range Gradient in the ranges.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",gradients:{ colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } }] }] });    
</script>                                 {% endhighlight %}







### scales.ranges.opacity<span class="type-signature type number">number</span>
{:#members:scales-ranges-opacity}








Specifies the opacity in the ranges.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",opacity: 0.3 }] }] });                           
</script>                 {% endhighlight %}







### scales.ranges.placement<span class="type-signature type enum">enum</span>
{:#members:scales-ranges-placement}








Specifies the range Position in the ranges. See <a href="global.html#RangePlacement">RangePlacement</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.RangePlacement.Center








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",placement: "center" }] }] });
</script> {% endhighlight %}







### scales.ranges.startValue<span class="type-signature type number">number</span>
{:#members:scales-ranges-startvalue}








Specifies the startValue in the ranges.




Default Value:
{:.param}






* 20








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 10, backgroundColor: "#E94649" }] }] });                       
</script>                         {% endhighlight %}







### scales.ranges.startWidth<span class="type-signature type number">number</span>
{:#members:scales-ranges-startwidth}








Specifies the startWidth in the ranges.




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 20, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });                
</script>                                  {% endhighlight %}







### scales.shadowOffset<span class="type-signature type number">number</span>
{:#members:scales-shadowoffset}








Specifies the shadowOffset.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{shadowOffset:1}]});                
</script>                         {% endhighlight %}







### scales.showBarPointers<span class="type-signature type boolean">boolean</span>
{:#members:scales-showbarpointers}








Specifies the showBarPointers state.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showBarPointers:false}]});         
</script>                         {% endhighlight %}







### scales.showCustomLabels<span class="type-signature type boolean">boolean</span>
{:#members:scales-showcustomlabels}








Specifies the showCustomLabels state.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true}]}); 
</script>                                 {% endhighlight %}







### scales.showIndicators<span class="type-signature type boolean">boolean</span>
{:#members:scales-showindicators}








Specifies the showIndicators state.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showIndicators:true}]});   
</script>                                         {% endhighlight %}







### scales.showLabels<span class="type-signature type boolean">boolean</span>
{:#members:scales-showlabels}








Specifies the showLabels state.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showLabels:false}]});              
</script>                         {% endhighlight %}







### scales.showMarkerPointers<span class="type-signature type boolean">boolean</span>
{:#members:scales-showmarkerpointers}








Specifies the showMarkerPointers state.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showMarkerPointers:false}]});      
</script>                         {% endhighlight %}







### scales.showRanges<span class="type-signature type boolean">boolean</span>
{:#members:scales-showranges}








Specifies the showRanges state.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showRanges:false}]});      
</script>                                 {% endhighlight %}







### scales.showTicks<span class="type-signature type boolean">boolean</span>
{:#members:scales-showticks}








Specifies the showTicks state.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{showTicks:false}]});                       
</script>                         {% endhighlight %}







### scales.ticks<span class="type-signature type array">Array</span>
{:#members:scales-ticks}








Specifies the ticks in the scale.




Default Value:
{:.param}






* Array








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{angle:30}]}]});            
</script>                                 {% endhighlight %}







### scales.ticks.angle<span class="type-signature type number">number</span>
{:#members:scales-ticks-angle}








Specifies the angle in the tick.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{angle:20}]}]});                            
</script>                  {% endhighlight %}







### scales.ticks.color<span class="type-signature type string">string</span>
{:#members:scales-ticks-color}








Specifies the tick Color in the tick.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{color:"Blue"}]}]});        
</script>                         {% endhighlight %}







### scales.ticks.distanceFromScale<span class="type-signature type object">object</span>
{:#members:scales-ticks-distancefromscale}








Specifies the DistanceFromScale in the tick.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{distanceFromScale:{x:10, y:10}}]}]});      
</script>                         {% endhighlight %}







### scales.ticks.distanceFromScale.x<span class="type-signature type number">number</span>
{:#members:scales-ticks-distancefromscale-x}








Specifies the xDistanceFromScale in the tick.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{distanceFromScale:{x:10}}]}]});    
</script>                         {% endhighlight %}







### scales.ticks.distanceFromScale.y<span class="type-signature type number">number</span>
{:#members:scales-ticks-distancefromscale-y}








Specifies the yDistanceFromScale in the tick.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>  
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{distanceFromScale:{y:10}}]}]});            
</script>                 {% endhighlight %}







### scales.ticks.height<span class="type-signature type number">number</span>
{:#members:scales-ticks-height}








Specifies the tick Height in the tick.




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{height:8}]}]});            
</script> {% endhighlight %}







### scales.ticks.opacity<span class="type-signature type number">number</span>
{:#members:scales-ticks-opacity}








Specifies the opacity in the tick.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{opacity:0.5}]}]});                                         
</script> {% endhighlight %}







### scales.ticks.placement<span class="type-signature type enum">enum</span>
{:#members:scales-ticks-placement}








Specifies the tick Placement in the tick. See <a href="global.html#TickPlacement">TickPlacement</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.TickPlacement.Near








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script> 
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{placement:ej.datavisualization.LinearGauge.TickPlacement.Far}]}]});                
</script>                         {% endhighlight %}







### scales.ticks.type<span class="type-signature type enum">enum</span>
{:#members:scales-ticks-type}








Specifies the tick Style in the tick. See <a href="global.html#TickType">TickType</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.TickType.MajorInterval








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{type:ej.datavisualization.LinearGauge.TickType.MajorInterval}]}]});                
</script>         {% endhighlight %}







### scales.ticks.width<span class="type-signature type number">number</span>
{:#members:scales-ticks-width}








Specifies the tick Width in the tick.




Default Value:
{:.param}






* 3








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{width:4}]}]});                     
</script>                 {% endhighlight %}







### scales.type<span class="type-signature type enum">enum</span>
{:#members:scales-type}








Specifies the scaleBar type .See <a href="global.html#ScaleType">ScaleType</a>




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.ScaleType.Rectangle








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{type:ej.datavisualization.LinearGauge.ScaleType.Rectangle}]});     
</script>                         {% endhighlight %}







### scales.width<span class="type-signature type number">number</span>
{:#members:scales-width}








Specifies the scaleBar width.




Default Value:
{:.param}






* 30








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{width:25}]});              
</script>                                 {% endhighlight %}







### theme<span class="type-signature type enum">enum</span>
{:#members:theme}








Specifies the theme for Linear gauge. See LinearGauge.Themes




Default Value:
{:.param}






* ej.datavisualization.LinearGauge.flatlight








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ theme: ej.datavisualization.LinearGauge.flatdark });
</script>   {% endhighlight %}







### tickColor<span class="type-signature type string">string</span>
{:#members:tickcolor}








Specifies the tick Color for Linear gauge.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ tickColor: "Red" });   
</script> {% endhighlight %}







### tooltip<span class="type-signature type object">object</span>
{:#members:tooltip}








Specify tooltip options of linear gauge




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showLabelTooltip: true,showCustomLabelTooltip: true,templateID: null} });
</script>{% endhighlight %}







### tooltip.showCustomLabelTooltip<span class="type-signature type boolean">boolean</span>
{:#members:tooltip-showcustomlabeltooltip}








Specify showCustomLabelTooltip value of linear gauge




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showCustomLabelTooltip: true} });
</script>{% endhighlight %}







### tooltip.showLabelTooltip<span class="type-signature type boolean">boolean</span>
{:#members:tooltip-showlabeltooltip}








Specify showLabelTooltip value of linear gauge




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showLabelTooltip: true} });
</script>{% endhighlight %}







### tooltip.templateID<span class="type-signature type string">string</span>
{:#members:tooltip-templateid}








Specify templateID value of linear gauge




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="CoreLinearGauge">
</div> 
 
<script>                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showLabelTooltip: true, templateID: true} });
</script>{% endhighlight %}







### value<span class="type-signature type number">number</span>
{:#members:value}








Specifies the value of the Gauge.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({  size: 5.5});        
</script>                          {% endhighlight %}







### width<span class="type-signature type number">number</span>
{:#members:width}








Specifies the width of Linear gauge.




Default Value:
{:.param}






* 150








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({ width: 360 });  
</script>  {% endhighlight %}





## Methods








### destroy<span class="signature">()</span>
{:#methods:destroy}








destroy the linear gauge all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge();
var linearGaugeobj = $("#LinearGauge1").data("ejLinearGauge");
linearGaugeobj.destroy();
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.exportImage("myImage","jpeg");
</script>{% endhighlight %}







### getBarDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({value:50});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarDistanceFromScale(0,0);
</script>{% endhighlight %}







### getBarPointerValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({value:50});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarPointerValue(0,0);
</script>{% endhighlight %}







### getBarWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({value:50});
// get Bar Width in number
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarWidth(0,0);
</script>{% endhighlight %}







### getCustomLabelAngle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getCustomLabelAngle(0,0);
</script>{% endhighlight %}







### getCustomLabelValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getCustomLabelValue(0,0);
</script>{% endhighlight %}







### getLabelAngle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelAngle(0,0);
</script>{% endhighlight %}







### getLabelPlacement<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelPlacement(0,0);
</script>{% endhighlight %}







### getLabelStyle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelStyle(0,0);
</script>{% endhighlight %}







### getLabelXDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelXDistanceFromScale(0,0);
</script>{% endhighlight %}







### getLabelYDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelYDistanceFromScale(0,0);
</script>{% endhighlight %}







### getMajorIntervalValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMajorIntervalValue(0);
</script>{% endhighlight %}







### getMarkerStyle<span class="signature">()</span>
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
<td class="description last">vscaleIndex alue for the Gauge</td>
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
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMarkerStyle(0,0);
</script>{% endhighlight %}







### getMaximumValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMaximumValue(0);
</script>{% endhighlight %}







### getMinimumValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMinimumValue(0,0);
</script>{% endhighlight %}







### getMinorIntervalValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMinorIntervalValue(0);
</script>{% endhighlight %}







### getPointerDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerDistanceFromScale(0,0);
</script>{% endhighlight %}







### getPointerHeight<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerHeight(0,0);
</script>{% endhighlight %}







### getPointerPlacement<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerPlacement(0,0);
</script>{% endhighlight %}







### getPointerValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerValue(0,0);
</script>{% endhighlight %}







### getPointerWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerWidth(0,0);
</script>{% endhighlight %}







### getRangeBorderWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeBorderWidth(0,0);
</script>{% endhighlight %}







### getRangeDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeDistanceFromScale(0,0);
</script>{% endhighlight %}







### getRangeEndValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeEndValue(0,0);
</script>{% endhighlight %}







### getRangeEndWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeEndWidth(0,0);
</script>{% endhighlight %}







### getRangePosition<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangePosition(0,0);
</script>{% endhighlight %}







### getRangeStartValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeStartValue(0,0);
</script>{% endhighlight %}







### getRangeStartWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeStartWidth(0,0);
</script>{% endhighlight %}







### getScaleBarLength<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBarLength(0);
</script>{% endhighlight %}







### getScaleBarSize<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBarSize(0,0);
</script>{% endhighlight %}







### getScaleBorderWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBorderWidth(0);
</script>{% endhighlight %}







### getScaleDirection<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleDirection(0,0);
</script>{% endhighlight %}







### getScaleLocation<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleLocation(0);
</script>{% endhighlight %}







### getScaleStyle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleStyle(0);
</script>{% endhighlight %}







### getTickAngle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickAngle(0,0);
</script>{% endhighlight %}







### getTickHeight<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickHeight(0,0);
</script>{% endhighlight %}







### getTickPlacement<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickPlacement(0,0);
</script>{% endhighlight %}







### getTickStyle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickStyle(0,0);
</script>{% endhighlight %}







### getTickWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickWidth(0,0);
</script>{% endhighlight %}







### getTickXDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickXDistanceFromScale(0,0);
</script>{% endhighlight %}







### getTickYDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickYDistanceFromScale(0,0);
</script>{% endhighlight %}







### scales<span class="signature">()</span>
{:#methods:scales}








Specifies the scales.




Default Value:
{:.param}






* object








Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
 
<script>
        $("#LinearGauge1").ejLinearGauge({  scales:[{minimum:5}]});
</script>                         {% endhighlight %}







### setBarDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarDistanceFromScale(0,0,30);
</script>{% endhighlight %}







### setBarPointerValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarPointerValue(0,0,30);
</script>{% endhighlight %}







### setBarWidth<span class="signature">()</span>
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
<td class="description last">scaleIndexvalue for the Gauge</td>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarWidth(0,0,30);
</script>{% endhighlight %}







### setCustomLabelAngle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setCustomLabelAngle(0,0,30);
</script>{% endhighlight %}







### setCustomLabelValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setCustomLabelValue(0,0,"text");
</script>{% endhighlight %}







### setLabelAngle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelAngle(0,0,20);
</script>{% endhighlight %}







### setLabelPlacement<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelPlacement(0,0,"far");
</script>{% endhighlight %}







### setLabelStyle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelStyle(0,0,"major");
</script>{% endhighlight %}







### setLabelXDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelXDistanceFromScale(0,0,20);
</script>{% endhighlight %}







### setLabelYDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelYDistanceFromScale(0,0,20);
</script>{% endhighlight %}







### setMajorIntervalValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMajorIntervalValue(0,5);
</script>{% endhighlight %}







### setMarkerStyle<span class="signature">()</span>
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
<td class="description last">pointerIndexvalue for the Gauge</td>
</tr>
<tr>
<td class="name">{% highlight html %}
arguemnt.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">marker Style for Gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMarkerStyle(0,0,"triangle");
</script>{% endhighlight %}







### setMaximumValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMaximumValue(0,20);
</script>{% endhighlight %}







### setMinimumValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMinimumValue(0,20);
</script>{% endhighlight %}







### setMinorIntervalValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMinorIntervalValue(0,2);
</script>{% endhighlight %}







### setPointerDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerDistanceFromScale(0,0,30);
</script>{% endhighlight %}







### setPointerHeight<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerHeight(0,0,30);
</script>{% endhighlight %}







### setPointerPlacement<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerPlacement(0,0,"far");
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerValue(0,0,30);
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerWidth(0,0,30);
</script>{% endhighlight %}







### setRangeBorderWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeBorderWidth(0,0,2);
</script>{% endhighlight %}







### setRangeDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeDistanceFromScale(0,0,20);
</script>{% endhighlight %}







### setRangeEndValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeEndValue(0,0,20);
</script>{% endhighlight %}







### setRangeEndWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeEndWidth(0,0,20);
</script>{% endhighlight %}







### setRangePosition<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangePosition(0,0,20);
</script>{% endhighlight %}







### setRangeStartValue<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeStartValue(0,0,20);
</script>{% endhighlight %}







### setRangeStartWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeStartWidth(0,0,20);
</script>{% endhighlight %}







### setScaleBarLength<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBarLength(0,150);
</script>{% endhighlight %}







### setScaleBarSize<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBarSize(0,20);
</script>{% endhighlight %}







### setScaleBorderWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBorderWidth(0,10);
</script>{% endhighlight %}







### setScaleDirection<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleDirection(0,"counterclockwise");
</script>{% endhighlight %}







### setScaleLocation<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleLocation(0,{x:20,y:20});
</script>{% endhighlight %}







### setScaleStyle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleStyle(0,"thermometer");
</script>{% endhighlight %}







### setTickAngle<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickAngle(0,0,20);
</script>{% endhighlight %}







### setTickHeight<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickHeight(0,0,10);
</script>{% endhighlight %}







### setTickPlacement<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickPlacement(0,0,"far");
</script>{% endhighlight %}







### setTickStyle<span class="signature">()</span>
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
<td class="description last">Tick Stylefor Gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickStyle(0,0,"major");
</script>{% endhighlight %}







### setTickWidth<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickWidth(0,0,5);
</script>{% endhighlight %}







### setTickXDistanceFromScale<span class="signature">()</span>
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




Example
{:.example}


{% highlight html %}
 
<div id="LinearGauge1"></div> 
  
<script>
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickXDistanceFromScale(0,0,20);
</script>{% endhighlight %}







### setTickYDistanceFromScale<span class="signature">()</span>
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
<td class="description last">Tick YDistance From Scalefor Gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the pointer</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
args.barElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current Bar pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.barPointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the bar pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.PointerValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the bar pointer.</td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the customLabel</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the customLabel style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.customLabelElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current customLabel element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.customLabelIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the customLabel.</td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the Indicator</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">numer</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.style{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the Indicator style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.IndicatorElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current Indicator element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.IndicatorIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the Indicator.</td>
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the label</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">oject</span></td>
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
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the pointer</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="description last">returns the ticks style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.markerElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current marker pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.markerPointerIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the marker pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.pointerValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the marker pointer.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.pointerAngle{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the marker pointer.</td>
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
args.object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">bolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the range</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="description last">returns the range style</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.rangeElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.position{% endhighlight %}</td>
<td class="type"><span class="param-type">oject</span></td>
<td class="description last">returns the startX and startY of the ticks</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">oject</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="type"><span class="param-type">oject</span></td>
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
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.type{% endhighlight %}</td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">eturns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="description last">returns the context element* @param {Object} args.markerpointer returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.markerpointer.index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.markerpointer.element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.markerpointer.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
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
args.markerpointer{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
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
<td class="type"><span class="param-type">Object</span></td>
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
<td class="description last">returns the context element* @param {Object} args.markerpointer returns the context element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.markerpointer.index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.markerpointer.element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.markerpointer.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
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
args.Model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
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
 
<div id="LinearGauge1"></div> 
 
<script>
$("#LinearGauge1").ejLinearGauge({
   renderComplete: function (args) {}
});
</script> {% endhighlight %}









<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>





<script type="text/javascript">
prettyPrint();
</script><script src="scripts/linenumber.js" type="text/javascript">
</script><script src="scripts/main.js" type="text/javascript">
</script>
