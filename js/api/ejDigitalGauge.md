---
layout: post
title: ejDigitalGauge
documentation: API
platform: js
metaname: 
metacontent: 
---

The Digital gauge can be easily configured to the DOM element, such as div. you can create a digital gauge with a highly customizable look and feel.










$(element).ejDigitalGauge<span class="signature">(options)</span>







<table class="params">
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
<td class="description last">For seting the Digital gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$('#DigitalCore').ejDigitalGauge();         
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery.js


* module:jquery.easing.js


* module:ej.common.all.js


* module:excanvas.js




## Members








### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}








Specifies the resize option of the DigitalGauge.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({ enableResize: true }); 
&lt;/script&gt;</code>
</pre>






### frame<span class="type-signature type object">object</span>
{:#members:frame}








Specifies the frame of the Digital gauge.




Default Value:
{:.param}






* {backgroundImageUrl: null, innerWidth: 6, outerWidth: 10}








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({ frame:{backgroundImageUrl: null, innerWidth:6, outerWidth:10}});
&lt;/script&gt;</code>
</pre>






### frame.backgroundImageUrl<span class="type-signature type string">string</span>
{:#members:frame-backgroundimageurl}








Specifies the url of an image to be displayed as background of the Digital gauge.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({frame:{ backgroundImageUrl: "styles\images\Car.png" }});
&lt;/script&gt;</code>
</pre>






### frame.innerWidth<span class="type-signature type number">number</span>
{:#members:frame-innerwidth}








Specifies the inner width for the frame, when the background image has been set for the Digital gauge..




Default Value:
{:.param}






* 6








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({frame:{ innerWidth: 30 }});
&lt;/script&gt;</code>
</pre>






### frame.outerWidth<span class="type-signature type number">number</span>
{:#members:frame-outerwidth}








Specifies the outer width of the frame, when the background image has been set for the Digital gauge.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({frame: { outerWidth: 30 } });
&lt;/script&gt;</code>
</pre>






### height<span class="type-signature type number">number</span>
{:#members:height}








Specifies the height of the DigitalGauge.




Default Value:
{:.param}






* 150








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({ height: 60 }); 
&lt;/script&gt;</code>
</pre>






### items<span class="type-signature type object">object</span>
{:#members:items}








Specifies the items for the DigitalGauge.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({width: 500});
&lt;/script&gt;</code>
</pre>






### items.characterSettings<span class="type-signature type object">Object</span>
{:#members:items-charactersettings}








Specifies the Character settings for the DigitalGauge.




Default Value:
{:.param}






* Object








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {count: 4} }] });
&lt;/script&gt;</code>
</pre>






### items.characterSettings.count<span class="type-signature type number">number</span>
{:#members:items-charactersettings-count}








Specifies the CharacterCount value for the DigitalGauge.




Default Value:
{:.param}






* 4








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {count: 4} }] });
&lt;/script&gt;</code>
</pre>






### items.characterSettings.opacity<span class="type-signature type number">number</span>
{:#members:items-charactersettings-opacity}








Specifies the opacity value for the DigitalGauge.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {opacity: 1} }] });
&lt;/script&gt;</code>
</pre>






### items.characterSettings.spacing<span class="type-signature type number">number</span>
{:#members:items-charactersettings-spacing}








Specifies the value for spacing between the characters




Default Value:
{:.param}






* 2








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {spacing: 3} }] });
&lt;/script&gt; </code>
</pre>






### items.characterSettings.type<span class="type-signature type enum">enum</span>
{:#members:items-charactersettings-type}








Specifies the character type for the text to be displayed. See <a href="global.html#CharacterType">CharacterType</a>




Default Value:
{:.param}






* ej.datavisualization.DigitalGauge.CharacterType.EightCrossEightDotMatrix








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{characterSettings:{ type: "eightcrosseightdotmatrix" }}] });
&lt;/script&gt; </code>
</pre>






### items.enableCustomFont<span class="type-signature type boolean">boolean</span>
{:#members:items-enablecustomfont}








Enable/Disable the custom font to be applied to the text in the gauge.





Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ enableCustomFont: true }] });
&lt;/script&gt;</code>
</pre>






### items.font<span class="type-signature type object">Object</span>
{:#members:items-font}








Set the specific font for the text, when the enableCustomFont is set to true





Default Value:
{:.param}






* Object








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true ,font: { size: "12px",fontFamily: "Segou",fontStyle: "bold"}}]});
&lt;/script&gt;</code>
</pre>






### items.font.fontFamily<span class="type-signature type string">string</span>
{:#members:items-font-fontfamily}








Set the font family value





Default Value:
{:.param}






* Arial








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true ,font: { fontFamily: "Segou"}}]});
&lt;/script&gt;</code>
</pre>






### items.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:items-font-fontstyle}








Set the font style for the font. See <a href="global.html#FontStyle">FontStyle</a>





Default Value:
{:.param}






* italic








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true ,font: { fontStyle: "bold" }}]});
&lt;/script&gt;</code>
</pre>






### items.font.size<span class="type-signature type string">string</span>
{:#members:items-font-size}








Set the font size value





Default Value:
{:.param}






* 11px








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true,font: { size: "18px"}}]});
&lt;/script&gt;</code>
</pre>






### items.position<span class="type-signature type object">object</span>
{:#members:items-position}








Set the location for the text, where it needs to be placed within the gauge.





Default Value:
{:.param}






* Object








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{position: { x: 10, y: 20 } }]});
&lt;/script&gt;</code>
</pre>






### items.position.x<span class="type-signature type number">number</span>
{:#members:items-position-x}








Set the horizontal location for the text, where it needs to be placed within the gauge.





Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{position : { x: 10,y:0} }]});
&lt;/script&gt;</code>
</pre>






### items.position.y<span class="type-signature type number">number</span>
{:#members:items-position-y}








Set the vertical location for the text, where it needs to be placed within the gauge.





Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{position: { x:0,y: 20 } }]});
&lt;/script&gt;</code>
</pre>






### items.segmentSettings<span class="type-signature type object">Object</span>
{:#members:items-segmentsettings}








Set the segemnt settings for the digital gauge.





Default Value:
{:.param}






* Object








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {length: 2} }] });
&lt;/script&gt;</code>
</pre>






### items.segmentSettings.color<span class="type-signature type string">string</span>
{:#members:items-segmentsettings-color}








Set the color for the text segments.





Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {color: "#FF1F2F"} }] });
&lt;/script&gt;</code>
</pre>






### items.segmentSettings.gradient<span class="type-signature type object">Object</span>
{:#members:items-segmentsettings-gradient}








Set the gradient for the text segments.





Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {gradient: { colorInfo: [{ colorStop: 0, color: "Green" }, { colorStop: 1, color: "Yellow" }] } } }] });
&lt;/script&gt;</code>
</pre>






### items.segmentSettings.length<span class="type-signature type number">number</span>
{:#members:items-segmentsettings-length}








Set the length for the text segments.





Default Value:
{:.param}






* 2








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {length: 2} }] });
&lt;/script&gt;</code>
</pre>






### items.segmentSettings.opacity<span class="type-signature type number">number</span>
{:#members:items-segmentsettings-opacity}








Set the opacity for the text segments.





Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {opacity: 2} }] });
&lt;/script&gt;</code>
</pre>






### items.segmentSettings.spacing<span class="type-signature type number">number</span>
{:#members:items-segmentsettings-spacing}








Set the spacing for the text segments.





Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {spacing: 1} }] });
&lt;/script&gt;</code>
</pre>






### items.segmentSettings.width<span class="type-signature type number">number</span>
{:#members:items-segmentsettings-width}








Set the width for the text segments.





Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {width: 1} }] });
&lt;/script&gt;</code>
</pre>






### items.shadowBlur<span class="type-signature type number">number</span>
{:#members:items-shadowblur}








Set the value for enabling/disabling the blurring effect for the shadows of the text





Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ shadowBlur:  1 }] });
&lt;/script&gt;</code>
</pre>






### items.shadowColor<span class="type-signature type string">string</span>
{:#members:items-shadowcolor}








Specifies the color of the text shadow.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({ items: [{shadowColor: "#FF1F2F" }]});
&lt;/script&gt; </code>
</pre>






### items.shadowOffsetX<span class="type-signature type number">number</span>
{:#members:items-shadowoffsetx}








Set the x offset value for the shadow of the text, indicating the location where it needs to be displayed.





Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ shadowOffsetX:  2 }] });
&lt;/script&gt;</code>
</pre>






### items.shadowOffsetY<span class="type-signature type number">number</span>
{:#members:items-shadowoffsety}








Set the y offset value for the shadow of the text, indicating the location where it needs to be displayed.





Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ shadowOffsetY:  2 }] });
&lt;/script&gt;</code>
</pre>






### items.textAlign<span class="type-signature type string">string</span>
{:#members:items-textalign}








Set the alignment of the text that is displayed within the gauge.See <a href="global.html#TextAlign">TextAlign</a>




Default Value:
{:.param}






* "left"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ textAlign:  "right" }] });
&lt;/script&gt; </code>
</pre>






### items.textColor<span class="type-signature type string">string</span>
{:#members:items-textcolor}








Specifies the color of the text.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({ items: [{textColor: "#FF1F2F" }]});
&lt;/script&gt;  </code>
</pre>






### items.value<span class="type-signature type string">string</span>
{:#members:items-value}








Specifies the text value.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({ items: [{value: "Welcome" }]});
&lt;/script&gt;  </code>
</pre>






### matrixSegmentData
{:#members:matrixsegmentdata}








Specifies the matrixSegmentData for the DigitalGauge.











### segmentData
{:#members:segmentdata}








Specifies the segmentData for the DigitalGauge.











### themes<span class="type-signature type string">string</span>
{:#members:themes}








Specifies the themes for the Digital gauge. See <a href="global.html#Themes">Themes</a>




Default Value:
{:.param}






* flatlight








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({ themes: "flatlight" });
&lt;/script&gt;</code>
</pre>






### value<span class="type-signature type string">string</span>
{:#members:value}








Specifies the value to the DigitalGauge.




Default Value:
{:.param}






* text








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({items: [{ value: "Welcome" }] });
&lt;/script&gt;</code>
</pre>






### width<span class="type-signature type number">number</span>
{:#members:width}








Specifies the width for the Digital gauge.




Default Value:
{:.param}






* 400








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({ width: 300 }); 
&lt;/script&gt;</code>
</pre>




## Methods








### destroy<span class="signature">()</span>
{:#methods:destroy}








To destroy the digital gauge





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalGauge1"&gt;Digital Gauge&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalGauge1").ejDigitalGauge();
var gphObj = $("#DigitalGauge1").data("ejDigitalGauge");
gphObj.destroy();
&lt;/script&gt;</code>
</pre>






### exportImage<span class="signature">(fileName, fileType)</span>
{:#methods:exportimage}








To export Digital Gauge as Image

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>fileName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fileName for the Image</td>
</tr>
<tr>
<td class="name"><code>fileType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fileType for the Image</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalGauge"&gt;DigitalGauge1&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalGauge").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge").data("ejDigitalGauge");
DigitalGaugeObj.exportImage("myImage","jpeg");
&lt;/script&gt;</code>
</pre>






### getPosition<span class="signature">(itemIndex)</span>
{:#methods:getposition}








Gets the location of an item that is displayed on the gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>itemIndex</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">Position value of an item that is displayed on the gauge.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.getPosition(0); 
&lt;/script&gt;</code>
</pre>






### getValue<span class="signature">(itemIndex)</span>
{:#methods:getvalue}








ClientSideMethod getValue Gets the value of an item that is displayed on the gauge

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>itemIndex</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">Index value of an item that displayed on the gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.getValue(0);    
&lt;/script&gt;</code>
</pre>






### refresh<span class="signature">()</span>
{:#methods:refresh}








Refresh the digital gauge widget





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalGauge1").ejDigitalGauge();
var GaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
GaugeObj.refresh();
&lt;/script&gt;     </code>
</pre>






### setPosition<span class="signature">(itemIndex, value)</span>
{:#methods:setposition}








ClientSideMethod Set Position Sets the location of an item to be displayed in the gauge

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>itemIndex</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">Index value of the digital gauge item</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Location value of the digital gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.setPosition(0,{ x:50, y:40 });  
&lt;/script&gt;</code>
</pre>






### setValue<span class="signature">(itemIndex, value)</span>
{:#methods:setvalue}








ClientSideMethod SetValue Sets the value of an item to be displayed in the gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>itemIndex</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">Index value of the digital gauge item</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Text value to be displayed in the gaugeS</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalGauge1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.setValue(0,"Welcome");
&lt;/script&gt;</code>
</pre>




## Events








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
<td class="name"><code>args.items</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"></td>
<td class="type"></td>
<td class="description last"></td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({
   init: function (args) {}
});      
&lt;/script&gt;</code>
</pre>






### itemRendering
{:#events:itemrendering}








Triggers when the gauge item rendering.

<table class="params">
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
<td class="name"><code>args.items</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({
   itemRendering: function (args) {}
});      
&lt;/script&gt;</code>
</pre>






### load
{:#events:load}








Triggers when the gauge is start to load.

<table class="params">
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
<td class="name"><code>args.items</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({
   load: function (args) {}
});      
&lt;/script&gt;</code>
</pre>






### renderComplete
{:#events:rendercomplete}








Triggers when the gauge render is completed.

<table class="params">
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
<td class="name"><code>args.items</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name"><code>args.context</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the gauge model</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="DigitalCore"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#DigitalCore").ejDigitalGauge({
   renderComplete: function (args) {}
});       
&lt;/script&gt;</code>
</pre>



