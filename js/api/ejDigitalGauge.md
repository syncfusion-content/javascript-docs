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
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">For seting the Digital gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$('#DigitalCore').ejDigitalGauge();         
</script>{% endhighlight %}







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


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ enableResize: true }); 
</script>{% endhighlight %}







### frame<span class="type-signature type object">object</span>
{:#members:frame}








Specifies the frame of the Digital gauge.




Default Value:
{:.param}






* {backgroundImageUrl: null, innerWidth: 6, outerWidth: 10}








Example
{:.example}


{% highlight html %}
  
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ frame:{backgroundImageUrl: null, innerWidth:6, outerWidth:10}});
</script>{% endhighlight %}







### frame.backgroundImageUrl<span class="type-signature type string">string</span>
{:#members:frame-backgroundimageurl}








Specifies the url of an image to be displayed as background of the Digital gauge.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
  
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({frame:{ backgroundImageUrl: "styles\images\Car.png" }});
</script>{% endhighlight %}







### frame.innerWidth<span class="type-signature type number">number</span>
{:#members:frame-innerwidth}








Specifies the inner width for the frame, when the background image has been set for the Digital gauge..




Default Value:
{:.param}






* 6








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({frame:{ innerWidth: 30 }});
</script>{% endhighlight %}







### frame.outerWidth<span class="type-signature type number">number</span>
{:#members:frame-outerwidth}








Specifies the outer width of the frame, when the background image has been set for the Digital gauge.




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({frame: { outerWidth: 30 } });
</script>{% endhighlight %}







### height<span class="type-signature type number">number</span>
{:#members:height}








Specifies the height of the DigitalGauge.




Default Value:
{:.param}






* 150








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ height: 60 }); 
</script>{% endhighlight %}







### items<span class="type-signature type object">object</span>
{:#members:items}








Specifies the items for the DigitalGauge.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({width: 500});
</script>{% endhighlight %}







### items.characterSettings<span class="type-signature type object">Object</span>
{:#members:items-charactersettings}








Specifies the Character settings for the DigitalGauge.




Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {count: 4} }] });
</script>{% endhighlight %}







### items.characterSettings.count<span class="type-signature type number">number</span>
{:#members:items-charactersettings-count}








Specifies the CharacterCount value for the DigitalGauge.




Default Value:
{:.param}






* 4








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {count: 4} }] });
</script>{% endhighlight %}







### items.characterSettings.opacity<span class="type-signature type number">number</span>
{:#members:items-charactersettings-opacity}








Specifies the opacity value for the DigitalGauge.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {opacity: 1} }] });
</script>{% endhighlight %}







### items.characterSettings.spacing<span class="type-signature type number">number</span>
{:#members:items-charactersettings-spacing}








Specifies the value for spacing between the characters




Default Value:
{:.param}






* 2








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {spacing: 3} }] });
</script> {% endhighlight %}







### items.characterSettings.type<span class="type-signature type enum">enum</span>
{:#members:items-charactersettings-type}








Specifies the character type for the text to be displayed. See <a href="global.html#CharacterType">CharacterType</a>




Default Value:
{:.param}






* ej.datavisualization.DigitalGauge.CharacterType.EightCrossEightDotMatrix








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{characterSettings:{ type: "eightcrosseightdotmatrix" }}] });
</script> {% endhighlight %}







### items.enableCustomFont<span class="type-signature type boolean">boolean</span>
{:#members:items-enablecustomfont}








Enable/Disable the custom font to be applied to the text in the gauge.





Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ enableCustomFont: true }] });
</script>{% endhighlight %}







### items.font<span class="type-signature type object">Object</span>
{:#members:items-font}








Set the specific font for the text, when the enableCustomFont is set to true





Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true ,font: { size: "12px",fontFamily: "Segou",fontStyle: "bold"}}]});
</script>{% endhighlight %}







### items.font.fontFamily<span class="type-signature type string">string</span>
{:#members:items-font-fontfamily}








Set the font family value





Default Value:
{:.param}






* Arial








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true ,font: { fontFamily: "Segou"}}]});
</script>{% endhighlight %}







### items.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:items-font-fontstyle}








Set the font style for the font. See <a href="global.html#FontStyle">FontStyle</a>





Default Value:
{:.param}






* italic








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true ,font: { fontStyle: "bold" }}]});
</script>{% endhighlight %}







### items.font.size<span class="type-signature type string">string</span>
{:#members:items-font-size}








Set the font size value





Default Value:
{:.param}






* 11px








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true,font: { size: "18px"}}]});
</script>{% endhighlight %}







### items.position<span class="type-signature type object">object</span>
{:#members:items-position}








Set the location for the text, where it needs to be placed within the gauge.





Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{position: { x: 10, y: 20 } }]});
</script>{% endhighlight %}







### items.position.x<span class="type-signature type number">number</span>
{:#members:items-position-x}








Set the horizontal location for the text, where it needs to be placed within the gauge.





Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{position : { x: 10,y:0} }]});
</script>{% endhighlight %}







### items.position.y<span class="type-signature type number">number</span>
{:#members:items-position-y}








Set the vertical location for the text, where it needs to be placed within the gauge.





Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{position: { x:0,y: 20 } }]});
</script>{% endhighlight %}







### items.segmentSettings<span class="type-signature type object">Object</span>
{:#members:items-segmentsettings}








Set the segemnt settings for the digital gauge.





Default Value:
{:.param}






* Object








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {length: 2} }] });
</script>{% endhighlight %}







### items.segmentSettings.color<span class="type-signature type string">string</span>
{:#members:items-segmentsettings-color}








Set the color for the text segments.





Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {color: "#FF1F2F"} }] });
</script>{% endhighlight %}







### items.segmentSettings.gradient<span class="type-signature type object">Object</span>
{:#members:items-segmentsettings-gradient}








Set the gradient for the text segments.





Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {gradient: { colorInfo: [{ colorStop: 0, color: "Green" }, { colorStop: 1, color: "Yellow" }] } } }] });
</script>{% endhighlight %}







### items.segmentSettings.length<span class="type-signature type number">number</span>
{:#members:items-segmentsettings-length}








Set the length for the text segments.





Default Value:
{:.param}






* 2








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {length: 2} }] });
</script>{% endhighlight %}







### items.segmentSettings.opacity<span class="type-signature type number">number</span>
{:#members:items-segmentsettings-opacity}








Set the opacity for the text segments.





Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {opacity: 2} }] });
</script>{% endhighlight %}







### items.segmentSettings.spacing<span class="type-signature type number">number</span>
{:#members:items-segmentsettings-spacing}








Set the spacing for the text segments.





Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {spacing: 1} }] });
</script>{% endhighlight %}







### items.segmentSettings.width<span class="type-signature type number">number</span>
{:#members:items-segmentsettings-width}








Set the width for the text segments.





Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {width: 1} }] });
</script>{% endhighlight %}







### items.shadowBlur<span class="type-signature type number">number</span>
{:#members:items-shadowblur}








Set the value for enabling/disabling the blurring effect for the shadows of the text





Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ shadowBlur:  1 }] });
</script>{% endhighlight %}







### items.shadowColor<span class="type-signature type string">string</span>
{:#members:items-shadowcolor}








Specifies the color of the text shadow.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ items: [{shadowColor: "#FF1F2F" }]});
</script> {% endhighlight %}







### items.shadowOffsetX<span class="type-signature type number">number</span>
{:#members:items-shadowoffsetx}








Set the x offset value for the shadow of the text, indicating the location where it needs to be displayed.





Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ shadowOffsetX:  2 }] });
</script>{% endhighlight %}







### items.shadowOffsetY<span class="type-signature type number">number</span>
{:#members:items-shadowoffsety}








Set the y offset value for the shadow of the text, indicating the location where it needs to be displayed.





Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ shadowOffsetY:  2 }] });
</script>{% endhighlight %}







### items.textAlign<span class="type-signature type string">string</span>
{:#members:items-textalign}








Set the alignment of the text that is displayed within the gauge.See <a href="global.html#TextAlign">TextAlign</a>




Default Value:
{:.param}






* "left"








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ textAlign:  "right" }] });
</script> {% endhighlight %}







### items.textColor<span class="type-signature type string">string</span>
{:#members:items-textcolor}








Specifies the color of the text.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
  
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ items: [{textColor: "#FF1F2F" }]});
</script>  {% endhighlight %}







### items.value<span class="type-signature type string">string</span>
{:#members:items-value}








Specifies the text value.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
  
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ items: [{value: "Welcome" }]});
</script>  {% endhighlight %}







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


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ themes: "flatlight" });
</script>{% endhighlight %}







### value<span class="type-signature type string">string</span>
{:#members:value}








Specifies the value to the DigitalGauge.




Default Value:
{:.param}






* text








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ value: "Welcome" }] });
</script>{% endhighlight %}







### width<span class="type-signature type number">number</span>
{:#members:width}








Specifies the width for the Digital gauge.




Default Value:
{:.param}






* 400








Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ width: 300 }); 
</script>{% endhighlight %}





## Methods








### destroy<span class="signature">()</span>
{:#methods:destroy}








To destroy the digital gauge





Example
{:.example}


{% highlight html %}
 
<div id="DigitalGauge1">Digital Gauge</div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var gphObj = $("#DigitalGauge1").data("ejDigitalGauge");
gphObj.destroy();
</script>{% endhighlight %}







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
<td class="name">{% highlight html %}
fileName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fileName for the Image</td>
</tr>
<tr>
<td class="name">{% highlight html %}
fileType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">fileType for the Image</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="DigitalGauge">DigitalGauge1</div> 
 
<script>
$("#DigitalGauge").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge").data("ejDigitalGauge");
DigitalGaugeObj.exportImage("myImage","jpeg");
</script>{% endhighlight %}







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
<td class="name">{% highlight html %}
itemIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">Position value of an item that is displayed on the gauge.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.getPosition(0); 
</script>{% endhighlight %}







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
<td class="name">{% highlight html %}
itemIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">Index value of an item that displayed on the gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.getValue(0);    
</script>{% endhighlight %}







### refresh<span class="signature">()</span>
{:#methods:refresh}








Refresh the digital gauge widget





Example
{:.example}


{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var GaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
GaugeObj.refresh();
</script>     {% endhighlight %}







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
<td class="name">{% highlight html %}
itemIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">Index value of the digital gauge item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Location value of the digital gauge</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.setPosition(0,{ x:50, y:40 });  
</script>{% endhighlight %}







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
<td class="name">{% highlight html %}
itemIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">Index value of the digital gauge item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Text value to be displayed in the gaugeS</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.setValue(0,"Welcome");
</script>{% endhighlight %}





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
args.items{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
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


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
   init: function (args) {}
});      
</script>{% endhighlight %}







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
args.items{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
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
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
   itemRendering: function (args) {}
});      
</script>{% endhighlight %}







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
args.items{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
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
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
   load: function (args) {}
});      
</script>{% endhighlight %}







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
args.items{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
args.context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
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
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
   renderComplete: function (args) {}
});       
</script>{% endhighlight %}




