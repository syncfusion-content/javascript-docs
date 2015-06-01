---
layout: post
title: ejLinearGauge
documentation: API
platform: js
metaname: 
metacontent: 
---

The Linera gauge can be easily configured to the DOM element, such as div. you can create a linear gauge with a highly customizable look and feel.










#### $(element).ejLinearGauge<span class="signature">(options)</span>







<table class="params">
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
<td class="description last">For seting the Linear gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$('#LinearGauge1').ejLinearGauge();     
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:ej.common.all


* module:excanvas.js




### Members








#### animationSpeed<span class="type-signature type number">number</span>








Specifies the animationSpeed




Default Value:






* 500








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ animationSpeed: 1000, value:50});
&lt;/script&gt;    </code>
</pre>






#### backgroundColor<span class="type-signature type string">string</span>








Specifies the backgroundColor for Linear gauge.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ backgroundColor: "Red" });   
&lt;/script&gt; </code>
</pre>






#### borderColor<span class="type-signature type string">string</span>








Specifies the borderColor for Linear gauge.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ borderColor: "Red" });   
&lt;/script&gt; </code>
</pre>






#### enableAnimation<span class="type-signature type boolean">boolean</span>








Specifies the animate state




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ enableAnimation: true, value:50});  
&lt;/script&gt; </code>
</pre>






#### enableMarkerPointerAnimation<span class="type-signature type boolean">boolean</span>








Specifies the animate state for marker pointer




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ enableMarkerPointerAnimation: true, value:50});  
&lt;/script&gt; </code>
</pre>






#### enableResize<span class="type-signature type boolean">boolean</span>








Specifies the can resize state.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ enableResize: true });   
&lt;/script&gt; </code>
</pre>






#### frame<span class="type-signature type object">object</span>








Specify frame of linear gauge




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code>  
&lt;div id="LinearGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#LinearGauge1").ejLinearGauge({ frame: { backgroundImageUrl:null, outerWidth:12, innerWidth:8 } });
&lt;/script&gt;</code>
</pre>






#### frame.backgroundImageUrl<span class="type-signature type string">string</span>








Specifies the frame backgroundimageurl of linear gauge




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;  
        $("#LinearGauge1").ejLinearGauge({ frame:{backgroundImageUrl: "bg.png"} });  
&lt;/script&gt; </code>
</pre>






#### frame.innerWidth<span class="type-signature type number">number</span>








Specifies the frame InnerWidth




Default Value:






* 8








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ frame:{innerWidth: 9}});   
&lt;/script&gt; </code>
</pre>






#### frame.outerWidth<span class="type-signature type number">number</span>








Specifies the frame OuterWidth




Default Value:






* 12








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ frame:{outerWidth: 13 }});   
&lt;/script&gt; </code>
</pre>






#### height<span class="type-signature type number">number</span>








Specifies the height of Linear gauge.




Default Value:






* 400








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({ height: 360 }); 
&lt;/script&gt;   </code>
</pre>






#### labelColor<span class="type-signature type string">string</span>








Specifies the labelColor for Linear gauge.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ labelColor: "Red" });   
&lt;/script&gt; </code>
</pre>






#### maximum<span class="type-signature type number">number</span>








Specifies the maximum value of Linear gauge.




Default Value:






* 100








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ maximum: 110 }); 
&lt;/script&gt;    </code>
</pre>






#### minimum<span class="type-signature type number">number</span>








Specifies the minimum value of Linear gauge.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({ minimum: 10 });  
&lt;/script&gt;   </code>
</pre>






#### orientation<span class="type-signature type string">string</span>








Specifies the orientation for Linear gauge.




Default Value:






* "Vertical"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ orientation: "Vertical" });   
&lt;/script&gt; </code>
</pre>






#### outerCustomLabelPosition<span class="type-signature type enum">enum</span>








Specify enableResize value of Linear gauge See <a href="global.html#OuterCustomLabelPosition">OuterCustomLabelPosition</a>




Default Value:






* bottom








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="CoreLinearGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreLinearGauge").ejLinearGauge({  outerCustomLabelPosition:"top" });
&lt;/script&gt;</code>
</pre>






#### pointerGradient1<span class="type-signature type object">Object</span>








Specifies the pointerGradient1 for Linear gauge.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({ pointerGradient1: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } });  
&lt;/script&gt;  </code>
</pre>






#### pointerGradient2<span class="type-signature type object">object</span>








Specifies the pointerGradient2 for Linear gauge.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ pointerGradient2: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } });  
&lt;/script&gt;  </code>
</pre>






#### readOnly<span class="type-signature type boolean">boolean</span>








Specifies the read only state.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ readOnly: false });   
&lt;/script&gt; </code>
</pre>






#### scales<span class="type-signature type object">Object</span>








Specifies the scales




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ scales: [{}]});   
&lt;/script&gt; </code>
</pre>






#### scales.backgroundColor<span class="type-signature type string">string</span>








Specifies the backgroundColor of the Scale.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{backgroundColor:"red"}]}); 
&lt;/script&gt;                         </code>
</pre>






#### scales.barPointers<span class="type-signature type array">Array</span>








Specifies the scaleBar Gradient of bar pointer




Default Value:






* Array








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{}]}]});                              
&lt;/script&gt;                  </code>
</pre>






#### scales.barPointers.backgroundColor<span class="type-signature type string">string</span>








Specifies the backgroundColor of bar pointer




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, backgroundColor: "red"}]}]});              
&lt;/script&gt;                 </code>
</pre>






#### scales.barPointers.border<span class="type-signature type object">object</span>








Specifies the border of bar pointer




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, border:{color: "red", width:1.5}}]}]});    
&lt;/script&gt;                                 </code>
</pre>






#### scales.barPointers.border.color<span class="type-signature type string">string</span>








Specifies the border Color of bar pointer




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, border:{color: "red"}}]}]});       
&lt;/script&gt;                                 </code>
</pre>






#### scales.barPointers.border.width<span class="type-signature type number">number</span>








Specifies the border Width of bar pointer




Default Value:






* 1.5








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, border:{width: 2}}]}]});           
&lt;/script&gt;                                 </code>
</pre>






#### scales.barPointers.distanceFromScale<span class="type-signature type number">number</span>








Specifies the distanceFromScale of bar pointer




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, distanceFromScale: 20}]}]});               
&lt;/script&gt;                         </code>
</pre>






#### scales.barPointers.gradients<span class="type-signature type object">object</span>








Specifies the scaleBar Gradient of bar pointer




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, gradients: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}]}]});               
&lt;/script&gt; </code>
</pre>






#### scales.barPointers.opacity<span class="type-signature type number">number</span>








Specifies the opacity of bar pointer




Default Value:






* 1








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, opacity: 0.5}]}]});        
&lt;/script&gt; </code>
</pre>






#### scales.barPointers.value<span class="type-signature type number">number</span>








Specifies the value of bar pointer




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value: 100}]}]});            
&lt;/script&gt;                         </code>
</pre>






#### scales.barPointers.width<span class="type-signature type number">number</span>








Specifies the pointer Width of bar pointer




Default Value:






* width=30








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{barPointers:[{value:50, width: 25}]}]});           
&lt;/script&gt;                 </code>
</pre>






#### scales.border<span class="type-signature type object">object</span>








Specifies the border of the Scale.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{border:{color:"red", width:1.5}}]});       
&lt;/script&gt;                                 </code>
</pre>






#### scales.border.color<span class="type-signature type string">string</span>








Specifies the border color of the Scale.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{border:{color:"red"}}]});  
&lt;/script&gt;                                 </code>
</pre>






#### scales.border.width<span class="type-signature type number">number</span>








Specifies the border width of the Scale.




Default Value:






* 1.5








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{border:{width:2.5}}]});    
&lt;/script&gt;                                 </code>
</pre>






#### scales.customLabels<span class="type-signature type array">Array</span>








Specifies the customLabel




Default Value:






* Array








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
&lt;/script&gt;                                 </code>
</pre>






#### scales.customLabels.color<span class="type-signature type number">number</span>








Specifies the label Color in customLabels




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"yellow", font: { size: "20px",fontFamily: "Arial", fontStyle: "Bold" }}]}]});
&lt;/script&gt;                         </code>
</pre>






#### scales.customLabels.font<span class="type-signature type object">object</span>








Specifies the font in customLabels




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
&lt;/script&gt;                 </code>
</pre>






#### scales.customLabels.font.fontFamily<span class="type-signature type string">string</span>








Specifies the fontFamily in customLabels




Default Value:






* "Arial"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
&lt;/script&gt;                 </code>
</pre>






#### scales.customLabels.font.fontStyle<span class="type-signature type enum">enum</span>








Specifies the fontStyle in customLabels. See <a href="global.html#FontStyle">FontStyle</a>




Default Value:






* ej.datavisualization.LinearGauge.FontStyle.Bold








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
&lt;/script&gt; </code>
</pre>






#### scales.customLabels.font.size<span class="type-signature type string">string</span>








Specifies the font size in customLabels




Default Value:






* "11px"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
&lt;/script&gt;                         </code>
</pre>






#### scales.customLabels.opacity<span class="type-signature type string">string</span>








Specifies the opacity in customLabels




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606",opacity:0.5, font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
&lt;/script&gt;                                 </code>
</pre>






#### scales.customLabels.position<span class="type-signature type object">object</span>








Specifies the position in customLabels




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});           
&lt;/script&gt;         </code>
</pre>






#### scales.customLabels.position.x<span class="type-signature type number">number</span>








Specifies the position x in customLabels




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ textAngle: 20,value:"LinearGauge", position:{x:10,y:50}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});              
&lt;/script&gt;                 </code>
</pre>






#### scales.customLabels.position.y<span class="type-signature type number">number</span>








Specifies the y in customLabels




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ textAngle: 20,value:"LinearGauge", position:{x:49,y:10}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});              
&lt;/script&gt;                         </code>
</pre>






#### scales.customLabels.positionType<span class="type-signature type object">object</span>








Specifies the positionType in customLabels.See <a href="global.html#CustomLabelPositionType">CustomLabelPositionType</a>




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ positionType:"outer",value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});              
&lt;/script&gt;         </code>
</pre>






#### scales.customLabels.textAngle<span class="type-signature type number">number</span>








Specifies the textAngle in customLabels




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ textAngle: 20,value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});             
&lt;/script&gt;                         </code>
</pre>






#### scales.customLabels.value<span class="type-signature type string">string</span>








Specifies the label Value in customLabels




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"LinearGauge", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
&lt;/script&gt;                 </code>
</pre>






#### scales.direction<span class="type-signature type enum">enum</span>








Specifies the scale Direction of the Scale. See <a href="global.html#Directions">Directions</a>




Default Value:






* ej.datavisualization.LinearGauge.Directions.CounterClockwise








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{direction:ej.datavisualization.LinearGauge.Directions.Clockwise}]});       
&lt;/script&gt;                                 </code>
</pre>






#### scales.indicators<span class="type-signature type array">Array</span>








Specifies the indicator




Default Value:






* Array








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({scales: [{showBarPointers: false, showIndicators: true, length: 310, indicators: [{
   font: {size: "11px",fontFamily: "Arial",fontStyle: "bold"},height: 30,
   type: "rectangle",width: 30,position: {x: 60,y: 70},textLocation: {x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 50,backgroundColor: "Red",borderColor: "Green",textColor: null}],
   value: 0, backgroundColor: "Red", border:{color: "Red", width: 1.5}, opacity: NaN}]}]});             
&lt;/script&gt;                 </code>
</pre>






#### scales.indicators.backgroundColor<span class="type-signature type string">string</span>








Specifies the backgroundColor in bar indicators




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   backgroundColor:"green"}]}]});       
&lt;/script&gt;         </code>
</pre>






#### scales.indicators.border<span class="type-signature type number">number</span>








Specifies the border in bar indicators




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   border:{color:"red", width: 5}}]}]});                
&lt;/script&gt;                 </code>
</pre>






#### scales.indicators.border.color<span class="type-signature type string">string</span>








Specifies the border Color in bar indicators




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   border:{color: "Red"}}]}]}); 
&lt;/script&gt;         </code>
</pre>






#### scales.indicators.border.width<span class="type-signature type number">number</span>








Specifies the border Width in bar indicators




Default Value:






* 1.5








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   border:{width: 5}}]}]});             
&lt;/script&gt;                 </code>
</pre>






#### scales.indicators.font<span class="type-signature type object">object</span>








Specifies the font of bar indicators




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "bold" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
&lt;/script&gt;                         </code>
</pre>






#### scales.indicators.font.fontFamily<span class="type-signature type string">string</span>








Specifies the fontFamily of font in bar indicators




Default Value:






* "Arial"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;  
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Segoe UI", fontStyle: "bold" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});                       
&lt;/script&gt; </code>
</pre>






#### scales.indicators.font.fontStyle<span class="type-signature type enum">enum</span>








Specifies the fontStyle of font in bar indicators. See <a href="global.html#FontStyle">FontStyle</a>




Default Value:






* ej.datavisualization.LinearGauge.FontStyle.Bold








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
&lt;/script&gt;                 </code>
</pre>






#### scales.indicators.font.size<span class="type-signature type string">string</span>








Specifies the size of font in bar indicators




Default Value:






* "11px"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "20px", fontFamily: "Arial", fontStyle: "bold" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
&lt;/script&gt;                         </code>
</pre>






#### scales.indicators.height<span class="type-signature type number">number</span>








Specifies the indicator Height of bar indicators




Default Value:






* 30








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   type: "rectangle",height: 50,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});   
&lt;/script&gt;                                  </code>
</pre>






#### scales.indicators.opacity<span class="type-signature type number">number</span>








Specifies the opacity in bar indicators




Default Value:






* NaN








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ readonly:false, scales: [{showBarPointers: false, showIndicators: true, indicators: [{height: 30,
type: "rectangle",position: {x: 80,y: 110},
stateRanges: [{endValue: 80,startValue: 50,backgroundColor: "Red",borderColor: "Green",textColor: null}],
value: 0, backgroundColor: "Red", border:{color: "Green"}, opacity:0.5}]}]});
&lt;/script&gt;                 </code>
</pre>






#### scales.indicators.position<span class="type-signature type object">object</span>








Specifies the position in bar indicators




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});           
&lt;/script&gt;         </code>
</pre>






#### scales.indicators.position.x<span class="type-signature type number">number</span>








Specifies the x position in bar indicators




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 20,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});           
&lt;/script&gt;         </code>
</pre>






#### scales.indicators.position.y<span class="type-signature type number">number</span>








Specifies the y position in bar indicators




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 100},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});
&lt;/script&gt;                 </code>
</pre>






#### scales.indicators.stateRanges<span class="type-signature type array">Array</span>








Specifies the state ranges in bar indicators




Default Value:






* Array








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
&lt;/script&gt;                 </code>
</pre>






#### scales.indicators.stateRanges.backgroundColor<span class="type-signature type string">string</span>








Specifies the backgroundColor in bar indicators state ranges




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Red",borderColor: "Green"}],
   border:{width: 1.5}}]}]});
&lt;/script&gt; </code>
</pre>






#### scales.indicators.stateRanges.borderColor<span class="type-signature type string">string</span>








Specifies the borderColor in bar indicators state ranges




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red"}],
   border:{width: 1.5}}]}]});
&lt;/script&gt; </code>
</pre>






#### scales.indicators.stateRanges.endValue<span class="type-signature type number">number</span>








Specifies the endValue in bar indicators state ranges




Default Value:






* 60








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
&lt;/script&gt;         </code>
</pre>






#### scales.indicators.stateRanges.startValue<span class="type-signature type number">number</span>








Specifies the startValue in bar indicators state ranges




Default Value:






* 50








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
&lt;/script&gt;                                 </code>
</pre>






#### scales.indicators.stateRanges.text<span class="type-signature type string">string</span>








Specifies the text in bar indicators state ranges




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 20, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Green", text: "Linear Gauge" }],opacity: 0.5}]}]}); 
&lt;/script&gt;                                 </code>
</pre>






#### scales.indicators.stateRanges.textColor<span class="type-signature type string">string</span>








Specifies the textColor in bar indicators state ranges




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;  
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 90, startValue: 40, textColor: "Red", text: "Linear" }],opacity: 0.5}]}]}); 
&lt;/script&gt;                                 </code>
</pre>






#### scales.indicators.textLocation<span class="type-signature type object">object</span>








Specifies the textLocation in bar indicators




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});       
&lt;/script&gt;         </code>
</pre>






#### scales.indicators.textLocation.x<span class="type-signature type number">number</span>








Specifies the textLocation position in bar indicators




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 50, y: 0 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
&lt;/script&gt;         </code>
</pre>






#### scales.indicators.textLocation.y<span class="type-signature type number">number</span>








Specifies the Y position in bar indicators




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
  value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
  font: { size: "11px", fontFamily: "Arial", fontStyle: "Normal" }, height: 30,
  type: "text", width: 30, position: { x: 60, y: 100 }, textLocation: { x: 0, y: 100 },
  stateRanges: [{ endValue: 60, startValue: 50, textColor: "Green", text: "Linear" }],opacity: 0.5}]}]});
&lt;/script&gt;                 </code>
</pre>






#### scales.indicators.type<span class="type-signature type enum">enum</span>








Specifies the indicator Style of font in bar indicators




Default Value:






* ej.datavisualization.LinearGauge.IndicatorType.Rectangle








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   height: 30,type: "rectangle",width: 30,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});
&lt;/script&gt; </code>
</pre>






#### scales.indicators.width<span class="type-signature type number">number</span>








Specifies the indicator Width in bar indicators




Default Value:






* 30








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   value: 50, scales: [{showBarPointers: true, showIndicators: true, length: 310, indicators: [{
   type: "rectangle",width: 50,
   position: { x: 0,y: 0},
   stateRanges: [{endValue: 60,startValue: 40,backgroundColor: "Green",borderColor: "Red",}],
   border:{width: 1.5}}]}]});
&lt;/script&gt;                         </code>
</pre>






#### scales.labels<span class="type-signature type array">Array</span>








Specifies the labels.




Default Value:






* Array








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{y:1}}]}]});                    
&lt;/script&gt; </code>
</pre>






#### scales.labels.angle<span class="type-signature type number">number</span>








Specifies the angle of labels.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{angle:30}]}]});                           
&lt;/script&gt; </code>
</pre>






#### scales.labels.distanceFromScale<span class="type-signature type object">object</span>








Specifies the DistanceFromScale of labels.




Default Value:






* object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{x:10, y:10}}]}]});             
&lt;/script&gt;                         </code>
</pre>






#### scales.labels.distanceFromScale.x<span class="type-signature type number">number</span>








Specifies the xDistanceFromScale of labels.




Default Value:






* -10








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{x:10}}]}]});           
&lt;/script&gt;                         </code>
</pre>






#### scales.labels.distanceFromScale.y<span class="type-signature type number">number</span>








Specifies the yDistanceFromScale of labels.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;  
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{distanceFromScale:{y:20}}]}]});           
&lt;/script&gt; </code>
</pre>






#### scales.labels.font<span class="type-signature type object">object</span>








Specifies the font of labels.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{size: "11px"}}]}]});                
&lt;/script&gt;         </code>
</pre>






#### scales.labels.font.fontFamily<span class="type-signature type string">string</span>








Specifies the fontFamily of font.




Default Value:






* "Arial"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{fontFamily: "Segoe UI"}}]}]});              
&lt;/script&gt;                         </code>
</pre>






#### scales.labels.font.fontStyle<span class="type-signature type enum">enum</span>








Specifies the fontStyle of font.See <a href="global.html#FontStyle">FontStyle</a>




Default Value:






* ej.datavisualization.LinearGauge.FontStyle.Bold








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{fontStyle: ej.datavisualization.LinearGauge.FontStyle.Normal}}]}]});                
&lt;/script&gt;                 </code>
</pre>






#### scales.labels.font.size<span class="type-signature type string">string</span>








Specifies the size of font.




Default Value:






* "11px"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{font:{size: "18px"}}]}]});                
&lt;/script&gt;                 </code>
</pre>






#### scales.labels.includeFirstValue<span class="type-signature type boolean">boolean</span>








need to includeFirstValue.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;  
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{includeFirstValue: false}]}]});           
&lt;/script&gt;                 </code>
</pre>






#### scales.labels.opacity<span class="type-signature type number">number</span>








Specifies the opacity of label.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{opacity: 0.5}]}]});               
&lt;/script&gt;                         </code>
</pre>






#### scales.labels.placement<span class="type-signature type enum">enum</span>








Specifies the label Placement of label. See <a href="global.html#LabelPlacement">LabelPlacement</a>




Default Value:






* ej.datavisualization.LinearGauge.LabelPlacement.Near








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{placement: ej.datavisualization.LinearGauge.LabelPlacement.Far}]}]});     
&lt;/script&gt;                         </code>
</pre>






#### scales.labels.textColor<span class="type-signature type string">string</span>








Specifies the textColor of font.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{textColor: "green"}]}]});         
&lt;/script&gt; </code>
</pre>






#### scales.labels.type<span class="type-signature type enum">enum</span>








Specifies the label Style of label. See <a href="global.html#LabelType">LabelType</a>




Default Value:






* ej.datavisualization.LinearGauge.LabelType.Major








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{type: ej.datavisualization.LinearGauge.LabelType.Major}]}]});     
&lt;/script&gt;                         </code>
</pre>






#### scales.labels.unitText<span class="type-signature type string">string</span>








Specifies the unitText of label.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{unitText: "F"}]}]});      
&lt;/script&gt;                                 </code>
</pre>






#### scales.labels.unitTextPlacement<span class="type-signature type enum">enum</span>








Specifies the unitText Position of label.See <a href="global.html#UnitTextPlacement">UnitTextPlacement</a>




Default Value:






* ej.datavisualization.LinearGauge.UnitTextPlacement.Back








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{labels:[{unitText: "F",unitTextPlacement: "front"}]}]});                           
&lt;/script&gt;         </code>
</pre>






#### scales.length<span class="type-signature type number">number</span>








Specifies the scaleBar Length.




Default Value:






* 290








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{length:300}]});
&lt;/script&gt;                                         </code>
</pre>






#### scales.majorIntervalValue<span class="type-signature type number">number</span>








Specifies the majorIntervalValue of the Scale.




Default Value:






* 10








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{majorIntervalValue:10}]});
&lt;/script&gt;                                         </code>
</pre>






#### scales.markerPointers<span class="type-signature type array">Array</span>








Specifies the markerPointers




Default Value:






* Array








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{type: "triangle"}]}]});   
&lt;/script&gt;                         </code>
</pre>






#### scales.markerPointers.backgroundColor<span class="type-signature type string">string</span>








Specifies the backgroundColor of marker pointer




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{backgroundColor: "blue"}]}]});            
&lt;/script&gt; </code>
</pre>






#### scales.markerPointers.border<span class="type-signature type object">object</span>








Specifies the border of marker pointer




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{border:{color: "blue", width: 1.5}}]}]});         
&lt;/script&gt;         </code>
</pre>






#### scales.markerPointers.border.color<span class="type-signature type string">string</span>








Specifies the border color of marker pointer




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{border:{color: "blue", width: 1.5}}]}]});         
&lt;/script&gt;         </code>
</pre>






#### scales.markerPointers.border.width<span class="type-signature type number">number</span>








Specifies the border of marker pointer




Default Value:






* number








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{border:{color: "blue", width: 1.5}}]}]});         
&lt;/script&gt;         </code>
</pre>






#### scales.markerPointers.distanceFromScale<span class="type-signature type number">number</span>








Specifies the distanceFromScale of marker pointer




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{distanceFromScale: 2}]}]});               
&lt;/script&gt;                 </code>
</pre>






#### scales.markerPointers.gradients<span class="type-signature type object">object</span>








Specifies the pointer Gradient of marker pointer




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{gradients: { colorInfo:[{ colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] }}]}]});              
&lt;/script&gt;                 </code>
</pre>






#### scales.markerPointers.length<span class="type-signature type number">number</span>








Specifies the pointer Length of marker pointer




Default Value:






* 30








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{length: 25}]}]});         
&lt;/script&gt;                 </code>
</pre>






#### scales.markerPointers.opacity<span class="type-signature type number">number</span>








Specifies the opacity of marker pointer




Default Value:






* 1








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{opacity: 0.5}]}]});               
&lt;/script&gt;                 </code>
</pre>






#### scales.markerPointers.placement<span class="type-signature type enum">enum</span>








Specifies the pointer Placement of marker pointer See <a href="global.html#PointerPlacement">PointerPlacement</a>




Default Value:






* ej.datavisualization.LinearGauge.PointerPlacement.Far








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{placement: ej.datavisualization.LinearGauge.PointerPlacement.Near}]}]});          
&lt;/script&gt;                 </code>
</pre>






#### scales.markerPointers.type<span class="type-signature type enum">enum</span>








Specifies the marker Style of marker pointerSee <a href="global.html#MarkerType">MarkerType</a>




Default Value:






* ej.datavisualization.LinearGauge.MarkerType.Triangle








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{type: ej.datavisualization.LinearGauge.MarkerType.Rectangle}]}]});                
&lt;/script&gt;                 </code>
</pre>






#### scales.markerPointers.value<span class="type-signature type number">number</span>








Specifies the value of marker pointer




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{value: 25}]}]});          
&lt;/script&gt;                         </code>
</pre>






#### scales.markerPointers.width<span class="type-signature type number">number</span>








Specifies the pointer Width of marker pointer




Default Value:






* 30








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{markerPointers:[{width: 25}]}]});          
&lt;/script&gt;                         </code>
</pre>






#### scales.maximum<span class="type-signature type number">number</span>








Specifies the maximum of the Scale.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{maximum:110}]});   
&lt;/script&gt;                                 </code>
</pre>






#### scales.minimum<span class="type-signature type number">number</span>








Specifies the minimum of the Scale.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{minimum:10}]});    
&lt;/script&gt;                                         </code>
</pre>






#### scales.minorIntervalValue<span class="type-signature type number">number</span>








Specifies the minorIntervalValue of the Scale.




Default Value:






* 2








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{minorIntervalValue:1}]});  
&lt;/script&gt;                                         </code>
</pre>






#### scales.opacity<span class="type-signature type number">number</span>








Specifies the opacity of the Scale.




Default Value:






* NaN








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{opacity:0.2}]});   
&lt;/script&gt;                                         </code>
</pre>






#### scales.position<span class="type-signature type object">object</span>








Specifies the position




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{position:{x:30, y:30}}]});         
&lt;/script&gt;                                 </code>
</pre>






#### scales.position.x<span class="type-signature type number">number</span>








Specifies the Horizontal position




Default Value:






* 50








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{position:{x:30}}]});               
&lt;/script&gt;                         </code>
</pre>






#### scales.position.y<span class="type-signature type number">number</span>








Specifies the vertical position




Default Value:






* 50








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{position:{y:30}}]});               
&lt;/script&gt;                                 </code>
</pre>






#### scales.ranges<span class="type-signature type array">Array</span>








Specifies the ranges in the tick.




Default Value:






* Array








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ranges:[{endWidth:4}]}]});         
&lt;/script&gt;                                 </code>
</pre>






#### scales.ranges.backgroundColor<span class="type-signature type string">string</span>








Specifies the backgroundColor in the ranges.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "Green" }] }] });                  
&lt;/script&gt;                                 </code>
</pre>






#### scales.ranges.border<span class="type-signature type object">Object</span>








Specifies the border in the ranges.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649", border:{color: "Green", width:1.5} }] }] });            
&lt;/script&gt;                         </code>
</pre>






#### scales.ranges.border.color<span class="type-signature type string">string</span>








Specifies the border color in the ranges.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649", border:{color: "Green"} }] }] });               
&lt;/script&gt;                         </code>
</pre>






#### scales.ranges.border.width<span class="type-signature type number">number</span>








Specifies the border width in the ranges.




Default Value:






* 1.5








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649", border:{width:1.5} }] }] });            
&lt;/script&gt;                         </code>
</pre>






#### scales.ranges.distanceFromScale<span class="type-signature type number">number</span>








Specifies the distanceFromScale in the ranges.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",distanceFromScale: 10 }] }] });  
&lt;/script&gt;                         </code>
</pre>






#### scales.ranges.endValue<span class="type-signature type number">number</span>








Specifies the endValue in the ranges.




Default Value:






* 60








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });                                        
&lt;/script&gt;         </code>
</pre>






#### scales.ranges.endWidth<span class="type-signature type number">number</span>








Specifies the endWidth in the ranges.




Default Value:






* 10








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });        
&lt;/script&gt;                                  </code>
</pre>






#### scales.ranges.gradients<span class="type-signature type object">object</span>








Specifies the range Gradient in the ranges.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",gradients:{ colorInfo:[{colorStop : 0, color:"#FFFFFF"},{colorStop : 1, color:"#AAAAAA"}] } }] }] });    
&lt;/script&gt;                                 </code>
</pre>






#### scales.ranges.opacity<span class="type-signature type number">number</span>








Specifies the opacity in the ranges.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",opacity: 0.3 }] }] });                           
&lt;/script&gt;                 </code>
</pre>






#### scales.ranges.placement<span class="type-signature type enum">enum</span>








Specifies the range Position in the ranges. See <a href="global.html#RangePlacement">RangePlacement</a>




Default Value:






* ej.datavisualization.LinearGauge.RangePlacement.Center








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649",placement: "center" }] }] });
&lt;/script&gt; </code>
</pre>






#### scales.ranges.startValue<span class="type-signature type number">number</span>








Specifies the startValue in the ranges.




Default Value:






* 20








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 10, endValue: 60, startValue: 10, backgroundColor: "#E94649" }] }] });                       
&lt;/script&gt;                         </code>
</pre>






#### scales.ranges.startWidth<span class="type-signature type number">number</span>








Specifies the startWidth in the ranges.




Default Value:






* 10








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 20, endWidth: 10, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });                
&lt;/script&gt;                                  </code>
</pre>






#### scales.shadowOffset<span class="type-signature type number">number</span>








Specifies the shadowOffset.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{shadowOffset:1}]});                
&lt;/script&gt;                         </code>
</pre>






#### scales.showBarPointers<span class="type-signature type boolean">boolean</span>








Specifies the showBarPointers state.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showBarPointers:false}]});         
&lt;/script&gt;                         </code>
</pre>






#### scales.showCustomLabels<span class="type-signature type boolean">boolean</span>








Specifies the showCustomLabels state.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true}]}); 
&lt;/script&gt;                                 </code>
</pre>






#### scales.showIndicators<span class="type-signature type boolean">boolean</span>








Specifies the showIndicators state.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showIndicators:true}]});   
&lt;/script&gt;                                         </code>
</pre>






#### scales.showLabels<span class="type-signature type boolean">boolean</span>








Specifies the showLabels state.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showLabels:false}]});              
&lt;/script&gt;                         </code>
</pre>






#### scales.showMarkerPointers<span class="type-signature type boolean">boolean</span>








Specifies the showMarkerPointers state.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{showMarkerPointers:false}]});      
&lt;/script&gt;                         </code>
</pre>






#### scales.showRanges<span class="type-signature type boolean">boolean</span>








Specifies the showRanges state.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showRanges:false}]});      
&lt;/script&gt;                                 </code>
</pre>






#### scales.showTicks<span class="type-signature type boolean">boolean</span>








Specifies the showTicks state.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{showTicks:false}]});                       
&lt;/script&gt;                         </code>
</pre>






#### scales.ticks<span class="type-signature type array">Array</span>








Specifies the ticks in the scale.




Default Value:






* Array








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{angle:30}]}]});            
&lt;/script&gt;                                 </code>
</pre>






#### scales.ticks.angle<span class="type-signature type number">number</span>








Specifies the angle in the tick.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{angle:20}]}]});                            
&lt;/script&gt;                  </code>
</pre>






#### scales.ticks.color<span class="type-signature type string">string</span>








Specifies the tick Color in the tick.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{color:"Blue"}]}]});        
&lt;/script&gt;                         </code>
</pre>






#### scales.ticks.distanceFromScale<span class="type-signature type object">object</span>








Specifies the DistanceFromScale in the tick.




Default Value:






* Object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{distanceFromScale:{x:10, y:10}}]}]});      
&lt;/script&gt;                         </code>
</pre>






#### scales.ticks.distanceFromScale.x<span class="type-signature type number">number</span>








Specifies the xDistanceFromScale in the tick.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{distanceFromScale:{x:10}}]}]});    
&lt;/script&gt;                         </code>
</pre>






#### scales.ticks.distanceFromScale.y<span class="type-signature type number">number</span>








Specifies the yDistanceFromScale in the tick.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;  
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{distanceFromScale:{y:10}}]}]});            
&lt;/script&gt;                 </code>
</pre>






#### scales.ticks.height<span class="type-signature type number">number</span>








Specifies the tick Height in the tick.




Default Value:






* 10








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{height:8}]}]});            
&lt;/script&gt; </code>
</pre>






#### scales.ticks.opacity<span class="type-signature type number">number</span>








Specifies the opacity in the tick.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{opacity:0.5}]}]});                                         
&lt;/script&gt; </code>
</pre>






#### scales.ticks.placement<span class="type-signature type enum">enum</span>








Specifies the tick Placement in the tick. See <a href="global.html#TickPlacement">TickPlacement</a>




Default Value:






* ej.datavisualization.LinearGauge.TickPlacement.Near








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{placement:ej.datavisualization.LinearGauge.TickPlacement.Far}]}]});                
&lt;/script&gt;                         </code>
</pre>






#### scales.ticks.type<span class="type-signature type enum">enum</span>








Specifies the tick Style in the tick. See <a href="global.html#TickType">TickType</a>




Default Value:






* ej.datavisualization.LinearGauge.TickType.MajorInterval








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{type:ej.datavisualization.LinearGauge.TickType.MajorInterval}]}]});                
&lt;/script&gt;         </code>
</pre>






#### scales.ticks.width<span class="type-signature type number">number</span>








Specifies the tick Width in the tick.




Default Value:






* 3








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{ticks:[{width:4}]}]});                     
&lt;/script&gt;                 </code>
</pre>






#### scales.type<span class="type-signature type enum">enum</span>








Specifies the scaleBar type .See <a href="global.html#ScaleType">ScaleType</a>




Default Value:






* ej.datavisualization.LinearGauge.ScaleType.Rectangle








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{type:ej.datavisualization.LinearGauge.ScaleType.Rectangle}]});     
&lt;/script&gt;                         </code>
</pre>






#### scales.width<span class="type-signature type number">number</span>








Specifies the scaleBar width.




Default Value:






* 30








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{width:25}]});              
&lt;/script&gt;                                 </code>
</pre>






#### theme<span class="type-signature type enum">enum</span>








Specifies the theme for Linear gauge. See LinearGauge.Themes




Default Value:






* ej.datavisualization.LinearGauge.flatlight








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ theme: ej.datavisualization.LinearGauge.flatdark });
&lt;/script&gt;   </code>
</pre>






#### tickColor<span class="type-signature type string">string</span>








Specifies the tick Color for Linear gauge.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ tickColor: "Red" });   
&lt;/script&gt; </code>
</pre>






#### tooltip<span class="type-signature type object">object</span>








Specify tooltip options of linear gauge




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="CoreLinearGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showLabelTooltip: true,showCustomLabelTooltip: true,templateID: null} });
&lt;/script&gt;</code>
</pre>






#### tooltip.showCustomLabelTooltip<span class="type-signature type boolean">boolean</span>








Specify showCustomLabelTooltip value of linear gauge




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="CoreLinearGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showCustomLabelTooltip: true} });
&lt;/script&gt;</code>
</pre>






#### tooltip.showLabelTooltip<span class="type-signature type boolean">boolean</span>








Specify showLabelTooltip value of linear gauge




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="CoreLinearGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showLabelTooltip: true} });
&lt;/script&gt;</code>
</pre>






#### tooltip.templateID<span class="type-signature type string">string</span>








Specify templateID value of linear gauge




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="CoreLinearGauge"&gt;
&lt;/div&gt; 
 
&lt;script&gt;                  
$("#CoreLinearGauge").ejLinearGauge({  tooltip:{showLabelTooltip: true, templateID: true} });
&lt;/script&gt;</code>
</pre>






#### value<span class="type-signature type number">number</span>








Specifies the value of the Gauge.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({  size: 5.5});        
&lt;/script&gt;                          </code>
</pre>






#### width<span class="type-signature type number">number</span>








Specifies the width of Linear gauge.




Default Value:






* 150








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({ width: 360 });  
&lt;/script&gt;  </code>
</pre>




### Methods








#### destroy<span class="signature">()</span>








destroy the linear gauge all events bound using this._on will be unbind automatically and bring the control to pre-init state.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var linearGaugeobj = $("#LinearGauge1").data("ejLinearGauge");
linearGaugeobj.destroy();
&lt;/script&gt;</code>
</pre>






#### exportImage<span class="signature">()</span>








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
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for the Image</td>
</tr>
<tr>
<td class="name"><code>argument.fileType</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for the Image</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.exportImage("myImage","jpeg");
&lt;/script&gt;</code>
</pre>






#### getBarDistanceFromScale<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({value:50});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarDistanceFromScale(0,0);
&lt;/script&gt;</code>
</pre>






#### getBarPointerValue<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({value:50});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarPointerValue(0,0);
&lt;/script&gt;</code>
</pre>






#### getBarWidth<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({value:50});
// get Bar Width in number
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getBarWidth(0,0);
&lt;/script&gt;</code>
</pre>






#### getCustomLabelAngle<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getCustomLabelAngle(0,0);
&lt;/script&gt;</code>
</pre>






#### getCustomLabelValue<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getCustomLabelValue(0,0);
&lt;/script&gt;</code>
</pre>






#### getLabelAngle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelAngle(0,0);
&lt;/script&gt;</code>
</pre>






#### getLabelPlacement<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelPlacement(0,0);
&lt;/script&gt;</code>
</pre>






#### getLabelStyle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelStyle(0,0);
&lt;/script&gt;</code>
</pre>






#### getLabelXDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelXDistanceFromScale(0,0);
&lt;/script&gt;</code>
</pre>






#### getLabelYDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getLabelYDistanceFromScale(0,0);
&lt;/script&gt;</code>
</pre>






#### getMajorIntervalValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMajorIntervalValue(0);
&lt;/script&gt;</code>
</pre>






#### getMarkerStyle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">vscaleIndex alue for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMarkerStyle(0,0);
&lt;/script&gt;</code>
</pre>






#### getMaximumValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMaximumValue(0);
&lt;/script&gt;</code>
</pre>






#### getMinimumValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMinimumValue(0,0);
&lt;/script&gt;</code>
</pre>






#### getMinorIntervalValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getMinorIntervalValue(0);
&lt;/script&gt;</code>
</pre>






#### getPointerDistanceFromScale<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerDistanceFromScale(0,0);
&lt;/script&gt;</code>
</pre>






#### getPointerHeight<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerHeight(0,0);
&lt;/script&gt;</code>
</pre>






#### getPointerPlacement<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerPlacement(0,0);
&lt;/script&gt;</code>
</pre>






#### getPointerValue<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerValue(0,0);
&lt;/script&gt;</code>
</pre>






#### getPointerWidth<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getPointerWidth(0,0);
&lt;/script&gt;</code>
</pre>






#### getRangeBorderWidth<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeBorderWidth(0,0);
&lt;/script&gt;</code>
</pre>






#### getRangeDistanceFromScale<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeDistanceFromScale(0,0);
&lt;/script&gt;</code>
</pre>






#### getRangeEndValue<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeEndValue(0,0);
&lt;/script&gt;</code>
</pre>






#### getRangeEndWidth<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeEndWidth(0,0);
&lt;/script&gt;</code>
</pre>






#### getRangePosition<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangePosition(0,0);
&lt;/script&gt;</code>
</pre>






#### getRangeStartValue<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeStartValue(0,0);
&lt;/script&gt;</code>
</pre>






#### getRangeStartWidth<span class="signature">()</span>








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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getRangeStartWidth(0,0);
&lt;/script&gt;</code>
</pre>






#### getScaleBarLength<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBarLength(0);
&lt;/script&gt;</code>
</pre>






#### getScaleBarSize<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBarSize(0,0);
&lt;/script&gt;</code>
</pre>






#### getScaleBorderWidth<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleBorderWidth(0);
&lt;/script&gt;</code>
</pre>






#### getScaleDirection<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleDirection(0,0);
&lt;/script&gt;</code>
</pre>






#### getScaleLocation<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleLocation(0);
&lt;/script&gt;</code>
</pre>






#### getScaleStyle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getScaleStyle(0);
&lt;/script&gt;</code>
</pre>






#### getTickAngle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickAngle(0,0);
&lt;/script&gt;</code>
</pre>






#### getTickHeight<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickHeight(0,0);
&lt;/script&gt;</code>
</pre>






#### getTickPlacement<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickPlacement(0,0);
&lt;/script&gt;</code>
</pre>






#### getTickStyle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickStyle(0,0);
&lt;/script&gt;</code>
</pre>






#### getTickWidth<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickWidth(0,0);
&lt;/script&gt;</code>
</pre>






#### getTickXDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickXDistanceFromScale(0,0);
&lt;/script&gt;</code>
</pre>






#### getTickYDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.getTickYDistanceFromScale(0,0);
&lt;/script&gt;</code>
</pre>






#### scales<span class="signature">()</span>








Specifies the scales.




Default Value:






* object








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
        $("#LinearGauge1").ejLinearGauge({  scales:[{minimum:5}]});
&lt;/script&gt;                         </code>
</pre>






#### setBarDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex,value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Bar DistanceFromScale value for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarDistanceFromScale(0,0,30);
&lt;/script&gt;</code>
</pre>






#### setBarPointerValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Bar Pointer Value for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarPointerValue(0,0,30);
&lt;/script&gt;</code>
</pre>






#### setBarWidth<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndexvalue for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Bar Width for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setBarWidth(0,0,30);
&lt;/script&gt;</code>
</pre>






#### setCustomLabelAngle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.customLabelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Custom Label Angle for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setCustomLabelAngle(0,0,30);
&lt;/script&gt;</code>
</pre>






#### setCustomLabelValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.customLabelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">customLabelIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">CustomLabel value for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({  scales:[{showCustomLabels:true,customLabels: [{ value:"MyLabel", position:{x:49,y:100}, color:"#fc0606", font: { size: "20px",fontFamily: "Arial", fontStyle: "bold" }}]}]});
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setCustomLabelValue(0,0,"text");
&lt;/script&gt;</code>
</pre>






#### setLabelAngle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Label Angle for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelAngle(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setLabelPlacement<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Label Placement for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelPlacement(0,0,"far");
&lt;/script&gt;</code>
</pre>






#### setLabelStyle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Label Style for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelStyle(0,0,"major");
&lt;/script&gt;</code>
</pre>






#### setLabelXDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Label XDistance From Scale for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelXDistanceFromScale(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setLabelYDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.labelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Label YDistance From Scale for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setLabelYDistanceFromScale(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setMajorIntervalValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Major Interval Value for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMajorIntervalValue(0,5);
&lt;/script&gt;</code>
</pre>






#### setMarkerStyle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndexvalue for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">marker Style for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMarkerStyle(0,0,"triangle");
&lt;/script&gt;</code>
</pre>






#### setMaximumValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">MaximumValue for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMaximumValue(0,20);
&lt;/script&gt;</code>
</pre>






#### setMinimumValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">MinimumValue for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMinimumValue(0,20);
&lt;/script&gt;</code>
</pre>






#### setMinorIntervalValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Minor Interval Value for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setMinorIntervalValue(0,2);
&lt;/script&gt;</code>
</pre>






#### setPointerDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerDistanceFromScale(0,0,30);
&lt;/script&gt;</code>
</pre>






#### setPointerHeight<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.height</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerHeight(0,0,30);
&lt;/script&gt;</code>
</pre>






#### setPointerPlacement<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointer placement for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerPlacement(0,0,"far");
&lt;/script&gt;</code>
</pre>






#### setPointerValue<span class="signature">()</span>








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
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pointer value for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerValue(0,0,30);
&lt;/script&gt;</code>
</pre>






#### setPointerWidth<span class="signature">()</span>








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
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.pointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">pointerIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.width</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pointer width for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setPointerWidth(0,0,30);
&lt;/script&gt;</code>
</pre>






#### setRangeBorderWidth<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range Border Width for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeBorderWidth(0,0,2);
&lt;/script&gt;</code>
</pre>






#### setRangeDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range Distance FromScale for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeDistanceFromScale(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setRangeEndValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range end value for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeEndValue(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setRangeEndWidth<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range End Width for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeEndWidth(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setRangePosition<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range Position for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangePosition(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setRangeStartValue<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">range start value for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeStartValue(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setRangeStartWidth<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">rangeIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Range Start Width for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({ scales: [{ showBarPointers: false, width: 3, length: 310, showRanges: true,ranges: [{ startWidth: 10, endWidth: 20, endValue: 60, startValue: 0, backgroundColor: "#E94649" }] }] });
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setRangeStartWidth(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setScaleBarLength<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Scale Bar Length for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBarLength(0,150);
&lt;/script&gt;</code>
</pre>






#### setScaleBarSize<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">ScaleBarSize for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBarSize(0,20);
&lt;/script&gt;</code>
</pre>






#### setScaleBorderWidth<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Scale Border Width for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleBorderWidth(0,10);
&lt;/script&gt;</code>
</pre>






#### setScaleDirection<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Scale Direction for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleDirection(0,"counterclockwise");
&lt;/script&gt;</code>
</pre>






#### setScaleLocation<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Scale position for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleLocation(0,{x:20,y:20});
&lt;/script&gt;</code>
</pre>






#### setScaleStyle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setScaleStyle(0,"thermometer");
&lt;/script&gt;</code>
</pre>






#### setTickAngle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick Angle for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickAngle(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setTickHeight<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick Height for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickHeight(0,0,10);
&lt;/script&gt;</code>
</pre>






#### setTickPlacement<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick Placement for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickPlacement(0,0,"far");
&lt;/script&gt;</code>
</pre>






#### setTickStyle<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Tick Stylefor Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickStyle(0,0,"major");
&lt;/script&gt;</code>
</pre>






#### setTickWidth<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick Width for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickWidth(0,0,5);
&lt;/script&gt;</code>
</pre>






#### setTickXDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick XDistance From Scale for Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickXDistanceFromScale(0,0,20);
&lt;/script&gt;</code>
</pre>






#### setTickYDistanceFromScale<span class="signature">()</span>








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
<td class="name"><code>argument.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">scaleIndex value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>argument.TickIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the Gauge</td>
</tr>
<tr>
<td class="name"><code>arguemnt.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Tick YDistance From Scalefor Gauge</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
  
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge();
var LinearGaugeObj = $("#LinearGauge1").data("ejLinearGauge");
LinearGaugeObj.setTickYDistanceFromScale(0,0,20);
&lt;/script&gt;</code>
</pre>




### Events








#### drawBarPointers








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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the pointer</td>
</tr>
<tr>
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="name"><code>args.barElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current Bar pointer element.</td>
</tr>
<tr>
<td class="name"><code>args.barPointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the bar pointer.</td>
</tr>
<tr>
<td class="name"><code>args.PointerValue</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the bar pointer.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   drawBarPointers: function (args) {}
});
&lt;/script&gt; </code>
</pre>






#### drawCustomLabel








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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the customLabel</td>
</tr>
<tr>
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the customLabel style</td>
</tr>
<tr>
<td class="name"><code>args.customLabelElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current customLabel element.</td>
</tr>
<tr>
<td class="name"><code>args.customLabelIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the customLabel.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   drawCustomLabel: function (args) {}
});
&lt;/script&gt; </code>
</pre>






#### drawIndicators








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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the Indicator</td>
</tr>
<tr>
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.scaleIndex</code></td>
<td class="type"><span class="param-type">numer</span></td>
<td class="description last">returns the scaleIndex to which the pointer belongs.</td>
</tr>
<tr>
<td class="name"><code>args.style</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the Indicator style</td>
</tr>
<tr>
<td class="name"><code>args.IndicatorElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current Indicator element.</td>
</tr>
<tr>
<td class="name"><code>args.IndicatorIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the Indicator.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   drawIndicators: function (args) {}
});
&lt;/script&gt; </code>
</pre>






#### drawLabels








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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the label</td>
</tr>
<tr>
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="name"><code>angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the label.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">oject</span></td>
<td class="description last">returns the current label element.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the label.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the label value of the label.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   drawLabels: function (args) {}
});
&lt;/script&gt; </code>
</pre>






#### drawMarkerPointers








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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the pointer</td>
</tr>
<tr>
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="description last">returns the ticks style</td>
</tr>
<tr>
<td class="name"><code>args.markerElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current marker pointer element.</td>
</tr>
<tr>
<td class="name"><code>args.markerPointerIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the marker pointer.</td>
</tr>
<tr>
<td class="name"><code>args.pointerValue</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the marker pointer.</td>
</tr>
<tr>
<td class="name"><code>args.pointerAngle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the marker pointer.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   drawMarkerPointers: function (args) {}
});
&lt;/script&gt; </code>
</pre>






#### drawRange








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
<td class="name"><code>args.object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the gauge.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">bolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the startX and startY of the range</td>
</tr>
<tr>
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="description last">returns the range style</td>
</tr>
<tr>
<td class="name"><code>args.rangeElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current range element.</td>
</tr>
<tr>
<td class="name"><code>args.rangeIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the range.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   drawRange: function (args) {}
});
&lt;/script&gt; </code>
</pre>






#### drawTicks








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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.position</code></td>
<td class="type"><span class="param-type">oject</span></td>
<td class="description last">returns the startX and startY of the ticks</td>
</tr>
<tr>
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">oject</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">object</span></td>
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
<td class="name"><code>angle</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the angle of the tick.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current tick element.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of the tick.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the tick value of the tick.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   drawTicks: function (args) {}
});
&lt;/script&gt; </code>
</pre>






#### init








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
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">eturns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   init: function (args) {}
});
&lt;/script&gt; </code>
</pre>






#### load








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
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   load: function (args) {}
});
&lt;/script&gt; </code>
</pre>






#### mouseClick








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
<td class="description last">returns the context element* @param {Object} args.markerpointer returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.markerpointer.index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name"><code>args.markerpointer.element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name"><code>args.markerpointer.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   mouseClick: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### mouseClickMove








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
<td class="name"><code>args.markerpointer</code></td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   mouseClickMove: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### mouseClickUp








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
<td class="description last">returns the context element* @param {Object} args.markerpointer returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.markerpointer.index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the pointer Index</td>
</tr>
<tr>
<td class="name"><code>args.markerpointer.element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the pointer element.</td>
</tr>
<tr>
<td class="name"><code>args.markerpointer.value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the pointer.</td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;
&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   mouseClickUp: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### renderComplete








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
<td class="name"><code>args.Model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the entire scale element.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="LinearGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#LinearGauge1").ejLinearGauge({
   renderComplete: function (args) {}
});
&lt;/script&gt; </code>
</pre>








<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>





<script type="text/javascript">
prettyPrint();
</script><script src="scripts/linenumber.js" type="text/javascript">
</script><script src="scripts/main.js" type="text/javascript">
</script>
