---
layout: post
title: Properties, Methods and Events of ejDigitalGauge Widget
documentation: API
platform: js
metaname: 
metacontent: 
---

# DigitalGauge
<ts root="datavisualization" />

The Digital gauge can be easily configured to the DOM element, such as div. you can create a digital gauge with a highly customizable look and feel.










$(element).ejDigitalGauge(options)







<table class="params">
<thead>
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
<td class="description last">For setting the Digital gauge</td>
</tr>
</tbody>
</table>




#### Example


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








### frame`object`
{:#members:frame}








Specifies the frame of the Digital gauge.




#### Default Value






* {backgroundImageUrl: null, innerWidth: 6, outerWidth: 10}








#### Example


{% highlight html %}
  
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ frame:{backgroundImageUrl: null, innerWidth:6, outerWidth:10}});
</script>{% endhighlight %}







### frame.backgroundImageUrl `string`
{:#members:frame-backgroundimageurl}








Specifies the URL of an image to be displayed as background of the Digital gauge.




#### Default Value






* null








#### Example


{% highlight html %}
  
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({frame:{ backgroundImageUrl: "styles\images\Car.png" }});
</script>{% endhighlight %}







### frame.innerWidth `number`
{:#members:frame-innerwidth}








Specifies the inner width for the frame, when the background image has been set for the Digital gauge..




#### Default Value






* 6








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({frame:{ innerWidth: 30 }});
</script>{% endhighlight %}







### frame.outerWidth `number`
{:#members:frame-outerwidth}








Specifies the outer width of the frame, when the background image has been set for the Digital gauge.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({frame: { outerWidth: 30 } });
</script>{% endhighlight %}







### height `number`
{:#members:height}








Specifies the height of the DigitalGauge.




#### Default Value






* 150








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ height: 60 }); 
</script>{% endhighlight %}







### isResponsive `boolean`
{:#members:isresponsive}








Specifies the resize option of the DigitalGauge.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ isResponsive: true }); 
</script>{% endhighlight %}







### items`array`
{:#members:items}








Specifies the items for the DigitalGauge.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({width: 500});
</script>{% endhighlight %}







### items.characterSettings`object`
{:#members:items-charactersettings}








Specifies the Character settings for the DigitalGauge.




#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {count: 4} }] });
</script>{% endhighlight %}







### items.characterSettings.count `number`
{:#members:items-charactersettings-count}








Specifies the CharacterCount value for the DigitalGauge.




#### Default Value






* 4








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {count: 4} }] });
</script>{% endhighlight %}







### items.characterSettings.opacity `number`
{:#members:items-charactersettings-opacity}








Specifies the opacity value for the DigitalGauge.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {opacity: 1} }] });
</script>{% endhighlight %}







### items.characterSettings.spacing `number`
{:#members:items-charactersettings-spacing}








Specifies the value for spacing between the characters




#### Default Value






* 2








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ characterSettings: {spacing: 3} }] });
</script> {% endhighlight %}







### items.characterSettings.type `enum`
{:#members:items-charactersettings-type}

<ts name="ej.datavisualization.DigitalGauge.CharacterType"/>

Specifies the character type for the text to be displayed.



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
SevenSegment</td>
<td class="type">string</td> 
<td class="description last">Characters are displayed in Seven Segment Format</td>
</tr>
<tr>
<td class="name">
FourteenSegment</td>
<td class="type">string</td>
<td class="description last">Characters are displayed in Fourteen Segment Format</td>
</tr> 
<tr>
<td class="name">
SixteenSegment</td>
<td class="type">string</td>
<td class="description last">Characters are displayed in Sixteen Segment format</td>
</tr> 
<tr>
<td class="name">
EightCrossEightDotMatrix</td>
<td class="type">string</td>
<td class="description last">Characters are displayed in EightCrossEightDotMatrix format</td>
</tr> 
<tr>
<td class="name">
EightCrossEightSquareMatrix</td>
<td class="type">string</td>
<td class="description last">Characters are displayed in EightCrossEightSquareMatrix format</td>
</tr> 
</tbody>
</table>




Specifies the character type for the text to be displayed. See <a href="global.html#CharacterType">CharacterType</a>




#### Default Value






* ej.datavisualization.DigitalGauge.CharacterType.EightCrossEightDotMatrix








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{characterSettings:{ type: "eightcrosseightdotmatrix" }}] });
</script> {% endhighlight %}







### items.enableCustomFont `boolean`
{:#members:items-enablecustomfont}








Enable/Disable the custom font to be applied to the text in the gauge.





#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ enableCustomFont: true }] });
</script>{% endhighlight %}







### items.font`object`
{:#members:items-font}








Set the specific font for the text, when the enableCustomFont is set to true





#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true ,font: { size: "12px",fontFamily: "Segou",fontStyle: "bold"}}]});
</script>{% endhighlight %}







### items.font.fontFamily `string`
{:#members:items-font-fontfamily}








Set the font family value





#### Default Value






* Arial








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true ,font: { fontFamily: "Segou"}}]});
</script>{% endhighlight %}







### items.font.fontStyle `enum`
{:#members:items-font-fontstyle}

<ts name="ej.datavisualization.DigitalGauge.FontStyle"/>

Set the font style for the font



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
Normal</td>
<td class="type">string</td> 
<td class="description last">The texts are displayed in the default format</td>
</tr>
<tr>
<td class="name">
Bold</td>
<td class="type">string</td>
<td class="description last">The texts are displayed in the bold format</td>
</tr> 
<tr>
<td class="name">
Italic</td>
<td class="type">string</td>
<td class="description last">The texts are displayed in  italic  format</td>
</tr> 
<tr>
<td class="name">
Underline</td>
<td class="type">string</td>
<td class="description last">The texts are displayed in underlined format</td>
</tr>
<tr>
<td class="name">
Strikeout</td>
<td class="type">string</td>
<td class="description last">The texts are displayed in the strike out format</td>
</tr>
</tbody>
</table>





Set the font style for the font. See <a href="global.html#FontStyle">FontStyle</a>





#### Default Value






* italic








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true ,font: { fontStyle: "bold" }}]});
</script>{% endhighlight %}







### items.font.size `string`
{:#members:items-font-size}








Set the font size value





#### Default Value






* 11px








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{enableCustomFont: true,font: { size: "18px"}}]});
</script>{% endhighlight %}







### items.position`object`
{:#members:items-position}








Set the location for the text, where it needs to be placed within the gauge.





#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{position: { x: 10, y: 20 } }]});
</script>{% endhighlight %}







### items.position.x `number`
{:#members:items-position-x}








Set the horizontal location for the text, where it needs to be placed within the gauge.





#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{position : { x: 10,y:0} }]});
</script>{% endhighlight %}







### items.position.y `number`
{:#members:items-position-y}








Set the vertical location for the text, where it needs to be placed within the gauge.





#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{position: { x:0,y: 20 } }]});
</script>{% endhighlight %}







### items.segmentSettings`object`
{:#members:items-segmentsettings}








Set the segment settings for the digital gauge.





#### Default Value






{:.param}
* null








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {length: 2} }] });
</script>{% endhighlight %}







### items.segmentSettings.color `string`
{:#members:items-segmentsettings-color}








Set the color for the text segments.





#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {color: "#FF1F2F"} }] });
</script>{% endhighlight %}







### items.segmentSettings.gradient`object`
{:#members:items-segmentsettings-gradient}








Set the gradient for the text segments.





#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {gradient: { colorInfo: [{ colorStop: 0, color: "Green" }, { colorStop: 1, color: "Yellow" }] } } }] });
</script>{% endhighlight %}







### items.segmentSettings.length `number`
{:#members:items-segmentsettings-length}








Set the length for the text segments.





#### Default Value






* 2








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {length: 2} }] });
</script>{% endhighlight %}







### items.segmentSettings.opacity `number`
{:#members:items-segmentsettings-opacity}








Set the opacity for the text segments.





#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {opacity: 2} }] });
</script>{% endhighlight %}







### items.segmentSettings.spacing `number`
{:#members:items-segmentsettings-spacing}








Set the spacing for the text segments.





#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {spacing: 1} }] });
</script>{% endhighlight %}







### items.segmentSettings.width `number`
{:#members:items-segmentsettings-width}








Set the width for the text segments.





#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ segmentSettings: {width: 1} }] });
</script>{% endhighlight %}







### items.shadowBlur `number`
{:#members:items-shadowblur}








Set the value for enabling/disabling the blurring effect for the shadows of the text





#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ shadowBlur:  1 }] });
</script>{% endhighlight %}







### items.shadowColor `string`
{:#members:items-shadowcolor}








Specifies the color of the text shadow.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ items: [{shadowColor: "#FF1F2F" }]});
</script> {% endhighlight %}







### items.shadowOffsetX `number`
{:#members:items-shadowoffsetx}








Set the x offset value for the shadow of the text, indicating the location where it needs to be displayed.





#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ shadowOffsetX:  2 }] });
</script>{% endhighlight %}







### items.shadowOffsetY `number`
{:#members:items-shadowoffsety}








Set the y offset value for the shadow of the text, indicating the location where it needs to be displayed.





#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ shadowOffsetY:  2 }] });
</script>{% endhighlight %}







### items.textAlign `string`
{:#members:items-textalign}








Set the alignment of the text that is displayed within the gauge.See <a href="global.html#TextAlign">TextAlign</a>




#### Default Value






* "left"








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ textAlign:  "right" }] });
</script> {% endhighlight %}







### items.textColor `string`
{:#members:items-textcolor}








Specifies the color of the text.




#### Default Value






* null








#### Example


{% highlight html %}
  
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ items: [{textColor: "#FF1F2F" }]});
</script>  {% endhighlight %}







### items.value `string`
{:#members:items-value}








Specifies the text value.




#### Default Value






* null








#### Example


{% highlight html %}
  
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ items: [{value: "Welcome" }]});
</script>  {% endhighlight %}







### matrixSegmentData `object`
{:#members:matrixsegmentdata}








Specifies the matrixSegmentData for the DigitalGauge.











### segmentData `object`
{:#members:segmentdata}








Specifies the segmentData for the DigitalGauge.











### themes `string`
{:#members:themes}








Specifies the themes for the Digital gauge. See <a href="global.html#Themes">Themes</a>




#### Default Value






* flatlight








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ themes: "flatlight" });
</script>{% endhighlight %}







### value `string`
{:#members:value}








Specifies the value to the DigitalGauge.




#### Default Value






* text








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({items: [{ value: "Welcome" }] });
</script>{% endhighlight %}







### width `number`
{:#members:width}








Specifies the width for the Digital gauge.




#### Default Value






* 400








#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({ width: 300 }); 
</script>{% endhighlight %}





## Methods








### destroy()
{:#methods:destroy}








To destroy the digital gauge





#### Example


{% highlight html %}
 
<div id="DigitalGauge1">Digital Gauge</div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var gphObj = $("#DigitalGauge1").data("ejDigitalGauge");
gphObj.destroy();
</script>{% endhighlight %}







### exportImage(fileName, fileType)
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




#### Example


{% highlight html %}
 
<div id="DigitalGauge">DigitalGauge1</div> 
 
<script>
$("#DigitalGauge").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge").data("ejDigitalGauge");
DigitalGaugeObj.exportImage("myImage","jpeg");
</script>{% endhighlight %}







### getPosition(itemIndex)
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
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Position value of an item that is displayed on the gauge.</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.getPosition(0); 
</script>{% endhighlight %}







### getValue(itemIndex)
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
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index value of an item that displayed on the gauge</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.getValue(0);    
</script>{% endhighlight %}







### refresh()
{:#methods:refresh}








Refresh the digital gauge widget





#### Example


{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var GaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
GaugeObj.refresh();
</script>     {% endhighlight %}







### setPosition(itemIndex, value)
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
<td class="type"><span class="param-type">number</span></td>
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




#### Example


{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.setPosition(0,{ x:50, y:40 });  
</script>{% endhighlight %}







### setValue(itemIndex, value)
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
<td class="type"><span class="param-type">number</span></td>
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




#### Example


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
items{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
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
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


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
items{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
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
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


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
items{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
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
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


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
items{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the all the options of the items.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
context{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the context element</td>
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
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
   renderComplete: function (args) {}
});       
</script>{% endhighlight %}




