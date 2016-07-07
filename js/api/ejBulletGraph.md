---
layout: post
title: Properties,Methods and Events of Essential JS ejBulletGraph Widget
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Bullet graph.
<ts root="datavisualization" />










$(element).ejBulletGraph()











#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
 
<script>
// Create BulletGraph
$('#bulletGraph1').ejBulletGraph();     
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery.js


* module:ej.core.js


* module:ej.data.js


* module:ej.bulletgraph.js




## Members








### applyRangeStrokeToLabels `boolean`
{:#members:applyrangestroketolabels}








Toggles the visibility of the range stroke color of the labels.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
applyRangeStrokeToLabels : true                
});
</script>{% endhighlight %}







### applyRangeStrokeToTicks `boolean`
{:#members:applyrangestroketoticks}








Toggles the visibility of the range stroke color of the ticks.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
applyRangeStrokeToTicks : true               
});
</script>{% endhighlight %}







### captionSettings  `object`
{:#members:captionsettings}








Contains property to customize the caption in bullet graph.











### captionSettings.enableTrim `boolean`
{:#members:captionsettings-enabletrim}








Specifies whether trim the labels will be true or false.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ enableTrim : true }                    
});
</script>{% endhighlight %}







### captionSettings.font  `object`
{:#members:captionsettings-font}








Contains property to customize the font of caption.











### captionSettings.font.color `string`
{:#members:captionsettings-font-color}








Specifies the color of the text in caption.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{color : "green"}}                  
});
</script>{% endhighlight %}







### captionSettings.font.fontFamily `string`
{:#members:captionsettings-font-fontfamily}








Specifies the fontFamily of caption. Caption text render with this fontFamily




#### Default Value






* "Segoe UI"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{fontFamily : "algerian"}}
});
</script>{% endhighlight %}







### captionSettings.font.fontStyle `enum`
{:#members:captionsettings-font-fontstyle}

<ts name="ej.datavisualization.BulletGraph.FontStyle"/>

Specifies the fontStyle of caption


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description </th>
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
Italic</td>
<td class="type">string</td>
<td class="description last">The texts are displayed in italic format</td>
</tr> 
<tr>
<td class="name">
Oblique</td>
<td class="type">string</td>
<td class="description last">The texts are displayed in the oblique format</td>
</tr> 
</tbody>
</table>

Specifies the fontStyle of caption. Caption text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>




#### Default Value






* "Normal"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{fontStyle : "italic"}}                    
});
</script>{% endhighlight %}







### captionSettings.font.fontWeight `enum`
{:#members:captionsettings-font-fontweight}


<ts name="ej.datavisualization.BulletGraph.FontWeight"/>

Specifies the fontWeight of caption


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
<td class="description last">The texts are displayed in the default manner</td>
</tr>
<tr>
<td class="name">
Bold</td>
<td class="type">string</td>
<td class="description last">The texts are displayed in the Bold </td>
</tr> 
<tr>
<td class="name">
Bolder</td>
<td class="type">string</td>
<td class="description last">The texts are displayed with increased boldness compared to the bold option</td>
</tr> 
<tr>
<td class="name">
Lighter</td>
<td class="type">string</td>
<td class="description last">The texts are displayed with the decreased lightness </td>
</tr> 
</tbody>
</table>


Specifies the fontWeight of caption. Caption text render with this fontWeight. See <a href="global.html#FontWeight">FontWeight</a>




#### Default Value






* "regular"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{fontWeight : "lighter"}}                    
});
</script>{% endhighlight %}







### captionSettings.font.opacity `number`
{:#members:captionsettings-font-opacity}








Specifies the opacity of caption. Caption text render with this opacity.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{opacity : 0.5}}                    
});
</script>{% endhighlight %}







### captionSettings.font.size `string`
{:#members:captionsettings-font-size}








Specifies the size of caption. Caption text render with this size




#### Default Value






* "12px"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{size : "14px"}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator  `object`
{:#members:captionsettings-indicator}








Contains property to customize the indicator.











### captionSettings.indicator.font  `object`
{:#members:captionsettings-indicator-font}








Contains property to customize the font of indicator.











### captionSettings.indicator.font.color `string`
{:#members:captionsettings-indicator-font-color}








Specifies the color of the indicator's text.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { color :"green" }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.font.fontFamily `string`
{:#members:captionsettings-indicator-font-fontfamily}








Specifies the fontFamily of indicator. Indicator text render with this fontFamily.




#### Default Value






* "Segoe UI"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { fontFamily :"Algerian" }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.font.fontStyle `enum`
{:#members:captionsettings-indicator-font-fontstyle}

<ts ref="ej.datavisualization.BulletGraph.FontStyle"/>






Specifies the fontStyle of indicator. Indicator text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>




#### Default Value






* "Normal"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { fontStyle :"italic" }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.font.fontWeight `enum`
{:#members:captionsettings-indicator-font-fontweight}


<ts ref="ej.datavisualization.BulletGraph.FontWeight"/>





Specifies the fontWeight of indicator. Indicator text render with this fontWeight. See <a href="global.html#FontWeight">FontWeight</a>




#### Default Value






* "regular"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { fontWeight :"lighter" }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.font.opacity `number`
{:#members:captionsettings-indicator-font-opacity}








Specifies the opacity of indicator text. Indicator text render with this Opacity.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { opacity : 0.5 }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.font.size `string`
{:#members:captionsettings-indicator-font-size}








Specifies the size of indicator. Indicator text render with this size.




#### Default Value






* "12px"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { size :"14px" }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.location  `object`
{:#members:captionsettings-indicator-location}








Contains property to customize the location of indicator.











### captionSettings.indicator.location.x `number`
{:#members:captionsettings-indicator-location-x}








Specifies the horizontal position of the indicator.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{location : { x :12 }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.location.y `number`
{:#members:captionsettings-indicator-location-y}








Specifies the vertical position of the indicator.




#### Default Value






* 60








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{location : { y :60 }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.padding `number`
{:#members:captionsettings-indicator-padding}








Specifies the padding to be applied when text position is used.




#### Default Value






* 2








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator: {padding: 5}}                 
});
</script>{% endhighlight %}







### captionSettings.indicator.symbol  `object`
{:#members:captionsettings-indicator-symbol}








Contains property to customize the symbol of indicator.











### captionSettings.indicator.symbol.border  `object`
{:#members:captionsettings-indicator-symbol-border}








Contains property to customize the border of indicator symbol.











### captionSettings.indicator.symbol.border.color `string`
{:#members:captionsettings-indicator-symbol-border-color}








Specifies the border color of indicator symbol.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { border: { color :"green" } }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.symbol.border.width `number`
{:#members:captionsettings-indicator-symbol-border-width}








Specifies the border width of indicator symbol.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { border: { width : 2 } }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.symbol.color `string`
{:#members:captionsettings-indicator-symbol-color}








Specifies the color of indicator symbol.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { color :"green" }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.symbol.imageURL `string`
{:#members:captionsettings-indicator-symbol-imageurl}








Specifies the URL of image that represents indicator symbol.




#### Default Value






* ""








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { imageURL :"../BulletIndicator.png" }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.symbol.opacity `number`
{:#members:captionsettings-indicator-symbol-opacity}








Specifies the opacity of indicator symbol.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { opacity :0.5 }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.symbol.shape `string`
{:#members:captionsettings-indicator-symbol-shape}








Specifies the shape of indicator symbol.




#### Default Value






* ""








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { shape :"triangle" }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.symbol.size  `object`
{:#members:captionsettings-indicator-symbol-size}








Contains property to customize the size of indicator symbol.











### captionSettings.indicator.symbol.size.height `number`
{:#members:captionsettings-indicator-symbol-size-height}








Specifies the height of indicator symbol.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { size : { height: 10 } }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.symbol.size.width `number`
{:#members:captionsettings-indicator-symbol-size-width}








Specifies the width of indicator symbol.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { size : { width: 10 }}}                    
});
</script>{% endhighlight %}







### captionSettings.indicator.text `string`
{:#members:captionsettings-indicator-text}








Specifies the text to be displayed as indicator text. By default difference between current value and target will be displayed




#### Default Value






* ""








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator :{text : "Power Production"} }
});
</script>e{% endhighlight %}







### captionSettings.indicator.textAlignment `enum`
{:#members:captionsettings-indicator-textalignment}

<ts name="ej.datavisualization.BulletGraph.TextAlignment"/>

Specifies the alignment of indicator with respect to scale based on text position


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
<td class="description last">The text is  aligned near to the scale</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="description last">The text is aligned far from the scale</td>
</tr> 
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="description last">The text is aligned center of the scale </td>
</tr> 
</tbody>
</table>




Specifies the alignment of indicator with respect to scale based on text position. Alignment will not be applied for float position.




#### Default Value






* 'Near'








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator:{textAlignment: 'Far'}}
});
</script>{% endhighlight %}







### captionSettings.indicator.textAnchor `enum`
{:#members:captionsettings-indicator-textanchor}


<ts name="ej.datavisualization.BulletGraph.TextAnchor"/>

Specifies where indicator text should be anchored when indicator overlaps with other caption group text. Text will be anchored when overlapping caption group text are at same position. Anchoring is not applicable for float position.


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
Start</td>
<td class="type">string</td> 
<td class="description last">The Start is used to anchor the text from beginning</td>
</tr>
<tr>
<td class="name">
Middle</td>
<td class="type">string</td>
<td class="description last">The Middle is used to anchor the text from the center</td>
</tr> 
<tr>
<td class="name">
End</td>
<td class="type">string</td>
<td class="description last">The End is used to anchor the text from the end</td>
</tr> 
</tbody>
</table>

Specifies where indicator text should be anchored when indicator overlaps with other caption group text. Text will be anchored when overlapping caption group text are at same position. Anchoring is not applicable for float position.




#### Default Value






* 'start'








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator: {textAnchor: 'end'}}
});
</script>{% endhighlight %}







### captionSettings.indicator.textAngle `number`
{:#members:captionsettings-indicator-textangle}








indicator text render in the specified angle.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator :{textAngle :10} }                    
});
</script>{% endhighlight %}







### captionSettings.indicator.textPosition `enum`
{:#members:captionsettings-indicator-textposition}


<ts name="ej.datavisualization.BulletGraph.TextPosition"/>

Specifies where indicator should be placed


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
<td class="description last">The texts are positioned on the top of the quantitative scales</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="description last">The texts are positioned to the right of the quantitative scales</td>
</tr> 
<tr>
<td class="name">
Left</td>
<td class="type">string</td>
<td class="description last">The texts are positioned to the left of the quantitative scales</td>
</tr> 
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="description last">The texts are positioned to the bottom of the quantitative scales</td>
</tr> 
<tr>
<td class="name">
Float</td>
<td class="type">string</td>
<td class="description last">The text can be placed at any location using the float property</td>
</tr> 
</tbody>
</table>


Specifies where indicator should be placed.




#### Default Value






* 'float'








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator: {textPosition: 'Top'}}
});
</script>{% endhighlight %}







### captionSettings.indicator.textSpacing `number`
{:#members:captionsettings-indicator-textspacing}








Specifies the space between indicator symbol and text.




#### Default Value






* 3








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator :{textSpacing :10} }                    
});
</script>{% endhighlight %}







### captionSettings.indicator.visible `boolean`
{:#members:captionsettings-indicator-visible}








Specifies whether indicator will be visible or not.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator :{visible : true} }                    
});
</script>{% endhighlight %}







### captionSettings.location  `object`
{:#members:captionsettings-location}








Contains property to customize the location.











### captionSettings.location.x `number`
{:#members:captionsettings-location-x}








Specifies the position in horizontal direction




#### Default Value






* 17








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{location :{x :15}}            
});
</script>{% endhighlight %}







### captionSettings.location.y `number`
{:#members:captionsettings-location-y}








Specifies the position in horizontal direction




#### Default Value






* 30








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{location :{y :15}}
});
</script>{% endhighlight %}







### captionSettings.padding `number`
{:#members:captionsettings-padding}








Specifies the padding to be applied when text position is used.




#### Default Value






* 5








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{padding: 2}                 
});
</script>{% endhighlight %}







### captionSettings.subTitle  `object`
{:#members:captionsettings-subtitle}








Contains property to customize the subtitle.











### captionSettings.subTitle.font  `object`
{:#members:captionsettings-subtitle-font}








Contains property to customize the font of subtitle.











### captionSettings.subTitle.font.color `string`
{:#members:captionsettings-subtitle-font-color}








Specifies the color of the subtitle's text.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { color :"green" }}}                    
});
</script>{% endhighlight %}







### captionSettings.subTitle.font.fontFamily `string`
{:#members:captionsettings-subtitle-font-fontfamily}








Specifies the fontFamily of subtitle. Subtitle text render with this fontFamily.




#### Default Value






* "Segoe UI"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { fontFamily :"Algerian" }}}                    
});
</script>{% endhighlight %}







### captionSettings.subTitle.font.fontStyle `enum`
{:#members:captionsettings-subtitle-font-fontstyle}

<ts ref="ej.datavisualization.BulletGraph.FontStyle"/>






Specifies the fontStyle of subtitle. Subtitle text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>




#### Default Value




* "Normal"







#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { fontStyle :"italic" }}}                    
});
</script>{% endhighlight %}







### captionSettings.subTitle.font.fontWeight `enum`
{:#members:captionsettings-subtitle-font-fontweight}

<ts ref="ej.datavisualization.BulletGraph.FontWeight"/>





Specifies the fontWeight of subtitle. Subtitle text render with this fontWeight. See <a href="global.html#FontWeight">FontWeight</a>




#### Default Value






* "regular"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { fontWeight :"lighter" }}}                    
});
</script>{% endhighlight %}







### captionSettings.subTitle.font.opacity `number`
{:#members:captionsettings-subtitle-font-opacity}








Specifies the opacity of subtitle. Subtitle text render with this opacity.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { opacity :0.5 }}}                    
});
</script>{% endhighlight %}







### captionSettings.subTitle.font.size `string`
{:#members:captionsettings-subtitle-font-size}








Specifies the size of subtitle. Subtitle text render with this size.




#### Default Value






* "12px"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { size :"14px" }}}                    
});
</script>{% endhighlight %}







### captionSettings.subTitle.location  `object`
{:#members:captionsettings-subtitle-location}








Contains property to customize the location of subtitle.











### captionSettings.subTitle.location.x `number`
{:#members:captionsettings-subtitle-location-x}








Specifies the horizontal position of the subtitle.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{location : { x :12 }}}                    
});
</script>{% endhighlight %}







### captionSettings.subTitle.location.y `number`
{:#members:captionsettings-subtitle-location-y}








Specifies the vertical position of the subtitle.




#### Default Value






* 45








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{location : { y :50 }}}                    
});
</script>{% endhighlight %}







### captionSettings.subTitle.padding `number`
{:#members:captionsettings-subtitle-padding}








Specifies the padding to be applied when text position is used.




#### Default Value






* 5








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle:{padding: 8}}
});
</script>{% endhighlight %}







### captionSettings.subTitle.text `string`
{:#members:captionsettings-subtitle-text}








Specifies the text to be displayed as subtitle.




#### Default Value






* ""








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ subTitle :{text : "Power Production"} }
});
</script>e{% endhighlight %}







### captionSettings.subTitle.textAlignment `enum`
{:#members:captionsettings-subtitle-textalignment}

<ts ref="ej.datavisualization.BulletGraph.TextAlignment"/>






Specifies the alignment of sub title text with respect to scale. Alignment will not be applied in float position.




#### Default Value






* 'Near'








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle:{textAlignment: 'Far'}}
});
</script>{% endhighlight %}







### captionSettings.subTitle.textAnchor `enum`
{:#members:captionsettings-subtitle-textanchor}


<ts ref="ej.datavisualization.BulletGraph.TextAnchor"/>





Specifies where subtitle text should be anchored when sub title text overlaps with other caption group text. Text will be anchored when overlapping caption group text are at same position. Anchoring is not applicable for float position.




#### Default Value






* 'start'







#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ subTitle: {textAnchor: 'end'}}
});
</script>{% endhighlight %}







### captionSettings.subTitle.textAngle `number`
{:#members:captionsettings-subtitle-textangle}








Subtitle render in the specified angle.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ subTitle :{textAngle :10} }                    
});
</script>{% endhighlight %}







### captionSettings.subTitle.textPosition `enum`
{:#members:captionsettings-subtitle-textposition}


<ts ref="ej.datavisualization.BulletGraph.TextPosition"/>






Specifies where sub title text should be placed.




#### Default Value






* 'float'








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ subTitle:{textPosition: 'Right'}}
});
</script>{% endhighlight %}







### captionSettings.text `string`
{:#members:captionsettings-text}








Specifies the text to be displayed on bullet graph.




#### Default Value






* ""








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{text : "Production"}
});
</script>{% endhighlight %}







### captionSettings.textAlignment `enum`
{:#members:captionsettings-textalignment}

<ts ref="ej.datavisualization.BulletGraph.TextAlignment"/>






Specifies the alignment of caption text with respect to scale. This property will not be applied when text position is float.




#### Default Value






* 'Near'








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{textAlignment: 'Center'}                 
});
</script>{% endhighlight %}







### captionSettings.textAnchor `enum`
{:#members:captionsettings-textanchor}

<ts ref="ej.datavisualization.BulletGraph.TextAnchor"/>






Specifies caption text anchoring when caption text overlaps with other caption group text. Text will be anchored when overlapping caption group text are at same position. Anchoring is not applicable for float position.




#### Default Value






* 'start'








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{textAnchor: 'middle'}
});
</script>{% endhighlight %}







### captionSettings.textAngle `number`
{:#members:captionsettings-textangle}








Specifies the angel in which the caption is rendered.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{textAngle : 5}                 
});
</script>{% endhighlight %}







### captionSettings.textPosition `enum`
{:#members:captionsettings-textposition}


<ts ref="ej.datavisualization.BulletGraph.TextPosition"/>





Specifies how caption text should be placed.




#### Default Value






* 'float'








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
captionSettings :{textPosition: 'Top'}                 
});
</script>{% endhighlight %}







### comparativeMeasureValue `number`
{:#members:comparativemeasurevalue}








Comparative measure bar in bullet graph render till the specified value.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
comparativeMeasureValue : 1                    
});
</script>  {% endhighlight %}







### enableAnimation `boolean`
{:#members:enableanimation}








Toggles the animation of bullet graph.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
enableAnimation : false                 
});
</script>{% endhighlight %}







### flowDirection `enum`
{:#members:flowdirection}


<ts name="ej.datavisualization.BulletGraph.FlowDirection"/>



Specifies the direction of flow in bullet graph. Neither it may be backward nor forward. 


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
Forward</td>
<td class="type">string</td> 
<td class="description last">The BulletGraph is rendered from left to right</td>
</tr>
<tr>
<td class="name">
Backward</td>
<td class="type">string</td>
<td class="description last">The BulletGraph is rendered from right to left</td>
</tr> 
</tbody>
</table>


Specifies the direction of flow in bullet graph. Neither it may be backward nor forward. 


#### Default Value






* "forward"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
flowDirection : "backward"                   
});
</script> {% endhighlight %}







### height `number`
{:#members:height}


Specifies the height of the bullet graph.




#### Default Value






* 90








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
height : 600                    
});
</script>  {% endhighlight %}







### isResponsive `boolean`
{:#members:isresponsive}








Sets a value whether to make the bullet graph responsive on resize.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
isResponsive : false                  
});
</script>{% endhighlight %}







### orientation `enum`
{:#members:orientation}


<ts name="ej.datavisualization.BulletGraph.Orientation"/>

Bullet graph will render in the specified orientation.


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
Horizontal</td>
<td class="type">string</td> 
<td class="description last">The BulletGraph is oriented in horizontal direction</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="description last">The BulletGraph is oriented in vertical direction</td>
</tr> 
</tbody>
</table>



Bullet graph will render in the specified orientation.




#### Default Value






* "horizontal"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
orientation : "vertical"                   
});
</script> {% endhighlight %}







### qualitativeRanges `array`
{:#members:qualitativeranges}








Contains property to customize the qualitative ranges.











### qualitativeRanges.rangeEnd `number`
{:#members:qualitativeranges-rangeend}








Specifies the ending range to which the qualitative ranges will render.




#### Default Value






* 3








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeEnd : 4.5}]                  
});
</script>{% endhighlight %}









### qualitativeRanges.rangeOpacity `number`
{:#members:qualitativeranges-rangeopacity}








Specifies the opacity for the qualitative ranges.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeOpacity : 0.5}]                 
});
</script>{% endhighlight %}








### qualitativeRanges.rangeStroke `string`
{:#members:qualitativeranges-rangestroke}








Specifies the stroke for the qualitative ranges.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeStroke : 5}]                 
});
</script>{% endhighlight %}







### qualitativeRangeSize `number`
{:#members:qualitativerangesize}








Size of the qualitative range depends up on the specified value.




#### Default Value






* 32








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
qualitativeRangeSize : 35                  
});
</script> {% endhighlight %}







### quantitativeScaleLength `number`
{:#members:quantitativescalelength}








Length of the quantitative range depends up on the specified value.




#### Default Value






* 475








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleLength :500                 
});
</script> {% endhighlight %}







### quantitativeScaleSettings  `object`
{:#members:quantitativescalesettings}








Contains all the properties to customize quantitative scale.











### quantitativeScaleSettings.comparativeMeasureSettings  `object`
{:#members:quantitativescalesettings-comparativemeasuresettings}








Contains property to customize the comparative measure.











### quantitativeScaleSettings.comparativeMeasureSettings.stroke `number`
{:#members:quantitativescalesettings-comparativemeasuresettings-stroke}








Specifies the stroke of the comparative measure.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { comparativeMeasureSettings :{ stroke :2} }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.comparativeMeasureSettings.width `number`
{:#members:quantitativescalesettings-comparativemeasuresettings-width}








Specifies the width of the comparative measure.




#### Default Value






* 5








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
 quantitativeScaleSettings : { comparativeMeasureSettings :{ width :6} }                     
});
</script> {% endhighlight %}







### quantitativeScaleSettings.featuredMeasureSettings  `object`
{:#members:quantitativescalesettings-featuredmeasuresettings}








Contains property to customize the featured measure.











### quantitativeScaleSettings.featuredMeasureSettings.stroke `number`
{:#members:quantitativescalesettings-featuredmeasuresettings-stroke}








Specifies the Stroke of the featured measure in bullet graph.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { featuredMeasureSettings :{stroke : 2} }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.featuredMeasureSettings.width `number`
{:#members:quantitativescalesettings-featuredmeasuresettings-width}








Specifies the width of the featured measure in bullet graph.




#### Default Value






* 2








#### Example


{% highlight html %}
 
<div id="ejBulletGraph"></div> 
<script>
        $("#bulletGraph1").ejBulletGraph({
   quantitativeScaleSettings: { featuredMeasureSettings: { width: 3 }},
   });
</script>  {% endhighlight %}







### quantitativeScaleSettings.featureMeasures `array`
{:#members:quantitativescalesettings-featuremeasures}








Contains property to customize the featured measure.











### quantitativeScaleSettings.featureMeasures.category `string`
{:#members:quantitativescalesettings-featuremeasures-category}








Specifies the category of feature measure.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { featureMeasures :[{ category :null}] }                  
});
</script>{% endhighlight %}







### quantitativeScaleSettings.featureMeasures.comparativeMeasureValue `number`
{:#members:quantitativescalesettings-featuremeasures-comparativemeasurevalue}








Comparative measure render till the specified value.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { featureMeasures :[{ comparativeMeasureValue :2}] }                  
});
</script>{% endhighlight %}







### quantitativeScaleSettings.featureMeasures.value `number`
{:#members:quantitativescalesettings-featuremeasures-value}








Feature measure render till the specified value.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { featureMeasures :[{ value :2}] }                  
});
</script>{% endhighlight %}







### quantitativeScaleSettings.fields  `object`
{:#members:quantitativescalesettings-fields}








Contains property to customize the fields.











### quantitativeScaleSettings.fields.category `string`
{:#members:quantitativescalesettings-fields-category}








Specifies the category of the bullet graph.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
fields :{category : "ProductId"}                  
});
</script>{% endhighlight %}







### quantitativeScaleSettings.fields.comparativeMeasure `string`
{:#members:quantitativescalesettings-fields-comparativemeasure}








Comparative measure render based on the values in the specified field.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
fields :{comparativeMeasure : "comparativeMeasureValue"}                  
});
</script>{% endhighlight %}







### quantitativeScaleSettings.fields.dataSource  `object`
{:#members:quantitativescalesettings-fields-datasource}








Specifies the dataSource for the bullet graph.




#### Default Value






* null








#### Example


{% highlight html %}
 
// To initialize with local Json data to the dataSource
$("#SampleBullet").ejBulletGraph({
fields: {
dataSource: localData,
category: &ldquo;Category&rdquo;,
featureMeasures: &ldquo;FeatureValue&rdquo;,
comparativeMeasure: &ldquo;ComparativeValue&rdquo;
}
});
// where local Json data assigned to the dataSource is as the below one
var localData = [{
                   FeatureValue: 8, ComparativeValue: 7.5,
                   Category: 1
               },
               {
                   FeatureValue: 9, ComparativeValue: 5,
                   Category: 2
               }];
// To initialize with remote data to the dataSource using DataManager
$("#SampleBullet").ejBulletGraph({
     fields: {
          dataSource: dataManager,
          query: queryString,
          category: "ProductID",
          featureMeasures: "UnitPrice",
          comparativeMeasure: "Quantity"
     }
});
// Data Manager creation
           var dataManager = ej.DataManager({
               url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
           });{% endhighlight %}


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
fields : {datasource :{ej.DataManger :{url : "http://mvc.syncfusion.com/Services/Northwnd.svc/" }} }                 
});
</script>         {% endhighlight %}







### quantitativeScaleSettings.fields.featureMeasures `string`
{:#members:quantitativescalesettings-fields-featuremeasures}








Feature measure render based on the values in the specified field.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
fields :{featureMeasures : "UnitPrice"}                  
});
</script>{% endhighlight %}







### quantitativeScaleSettings.fields.query `string`
{:#members:quantitativescalesettings-fields-query}








Specifies the query for fetching the values form data source to render the bullet graph.




#### Default Value






* null














### quantitativeScaleSettings.fields.tableName `string`
{:#members:quantitativescalesettings-fields-tablename}








Specifies the name of the table.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
fields :{tableName : "Product"}                 
});
</script>{% endhighlight %}







### quantitativeScaleSettings.interval `number`
{:#members:quantitativescalesettings-interval}








Specifies the interval for the Graph.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { interval : 2 }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings  `object`
{:#members:quantitativescalesettings-labelsettings}








Contains property to customize the labels.











### quantitativeScaleSettings.labelSettings.font  `object`
{:#members:quantitativescalesettings-labelsettings-font}








Contains property to customize the font of the labels in bullet graph.











### quantitativeScaleSettings.labelSettings.font.fontFamily `string`
{:#members:quantitativescalesettings-labelsettings-font-fontfamily}








Specifies the fontFamily of labels in bullet graph. Labels render with this fontFamily.




#### Default Value






* "Segoe UI"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { font :{ fontFamily : "Algerian" } } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.font.fontStyle `enum`
{:#members:quantitativescalesettings-labelsettings-font-fontstyle}

<ts ref="ej.datavisualization.BulletGraph.FontStyle"/>






Specifies the fontStyle of labels in bullet graph. Labels render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>




#### Default Value






* "Normal"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { font :{ fontStyle : "italic" } } }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.font.fontWeight `enum`
{:#members:quantitativescalesettings-labelsettings-font-fontweight}


<ts ref="ej.datavisualization.BulletGraph.FontWeight"/>





Specifies the fontWeight of labels in bullet graph. Labels render with this fontWeight. See <a href="global.html#FontWeight">FontWeight</a>




#### Default Value






* "regular"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { font :{ fontWeight : "lighter" } } }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.font.opacity `number`
{:#members:quantitativescalesettings-labelsettings-font-opacity}








Specifies the opacity of labels in bullet graph. Labels render with this opacity




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { font :{ opacity : 0.5 } } }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.labelPlacement `enum`
{:#members:quantitativescalesettings-labelsettings-labelplacement}


<ts name="ej.datavisualization.BulletGraph.LabelPlacement"/>

Specifies the placement of labels in bullet graph scale.


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
Inside</td>
<td class="type">string</td> 
<td class="description last">The Quantitative Scale Labels are placed inside the scale</td>
</tr>
<tr>
<td class="name">
Outside</td>
<td class="type">string</td>
<td class="description last">The Quantitative Scale labels are placed outside the scale</td>
</tr> 
</tbody>
</table>


Specifies the placement of labels in bullet graph scale.




#### Default Value






* outside








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { labelPlacement : "inside" } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.labelPrefix `string`
{:#members:quantitativescalesettings-labelsettings-labelprefix}








Specifies the prefix to be added with labels in bullet graph.




#### Default Value






* Empty string








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { labelPrefix : "$" } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.labelSuffix `string`
{:#members:quantitativescalesettings-labelsettings-labelsuffix}








Specifies the suffix to be added after labels in bullet graph.




#### Default Value






* Empty string








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { labelSuffix : "K" } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.offset `number`
{:#members:quantitativescalesettings-labelsettings-offset}








Specifies the horizontal/vertical padding of labels.




#### Default Value






* 15








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { offset : 25 } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.position `enum`
{:#members:quantitativescalesettings-labelsettings-position}

<ts name= "ej.datavisualization.BulletGraph.LabelPosition"/>

Specifies the position of the labels to render either above or below the graph. See <a href="global.html#Position">Position</a>


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
Above</td>
<td class="type">string</td> 
<td class="description last">The labels are placed above the graph</td>
</tr>
<tr>
<td class="name">
Below</td>
<td class="type">string</td>
<td class="description last">The labels are placed below the graph</td>
</tr> 
</tbody>
</table>


Specifies the position of the labels to render either above or below the graph. See <a href="global.html#Position">Position</a>




#### Default Value






* "below"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { position : "above" } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.size `number`
{:#members:quantitativescalesettings-labelsettings-size}








Specifies the Size of the labels.




#### Default Value






* 12








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { size : 10 } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.labelSettings.stroke `string`
{:#members:quantitativescalesettings-labelsettings-stroke}








Specifies the stroke color of the labels in bullet graph.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { stroke : "green" } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.location  `object`
{:#members:quantitativescalesettings-location}








Contains property to customize the position of the quantitative scale











### quantitativeScaleSettings.location.x `number`
{:#members:quantitativescalesettings-location-x}








This property specifies the x position for rendering quantitative scale.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { location : { x : 15 } } 
});
</script> {% endhighlight %}







### quantitativeScaleSettings.location.y `number`
{:#members:quantitativescalesettings-location-y}








This property specifies the y position for rendering quantitative scale.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { location : { y : 15 } }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.majorTickSettings  `object`
{:#members:quantitativescalesettings-majorticksettings}








Contains property to customize the major tick lines.











### quantitativeScaleSettings.majorTickSettings.size `number`
{:#members:quantitativescalesettings-majorticksettings-size}








Specifies the size of the major ticks.




#### Default Value






* 13








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { majorTickSettings : { size : 15 } }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.majorTickSettings.stroke `string`
{:#members:quantitativescalesettings-majorticksettings-stroke}








Specifies the stroke color of the major tick lines.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { majorTickSettings : { stroke : "red" } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.majorTickSettings.width `number`
{:#members:quantitativescalesettings-majorticksettings-width}








Specifies the width of the major tick lines.




#### Default Value






* 2








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { majorTickSettings : { width : 1 } }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.maximum `number`
{:#members:quantitativescalesettings-maximum}








Specifies the maximum value of the Graph.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { maximum : 8 }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.minimum `number`
{:#members:quantitativescalesettings-minimum}








Specifies the minimum value of the Graph.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minimum : 1 }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.minorTickSettings  `object`
{:#members:quantitativescalesettings-minorticksettings}








Contains property to customize the minor ticks.











### quantitativeScaleSettings.minorTickSettings.size `number`
{:#members:quantitativescalesettings-minorticksettings-size}








Specifies the size of minor ticks.




#### Default Value






* 7








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minorTickSettings : { size : 10} }                  
});
</script> {% endhighlight %}







### quantitativeScaleSettings.minorTickSettings.stroke `string`
{:#members:quantitativescalesettings-minorticksettings-stroke}








Specifies the stroke color of minor ticks in bullet graph.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minorTickSettings : { stroke : "green" } }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.minorTickSettings.width `number`
{:#members:quantitativescalesettings-minorticksettings-width}








Specifies the width of the minor ticks in bullet graph.




#### Default Value






* 2








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minorTickSettings : { width : 1 } }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.minorTicksPerInterval `number`
{:#members:quantitativescalesettings-minorticksperinterval}








The specified number of minor ticks will be rendered per interval.




#### Default Value






* 4








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minorTicksPerInterval : 5 }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.tickPlacement `enum`
{:#members:quantitativescalesettings-tickplacement}


<ts name="ej.datavisualization.BulletGraph.TickPlacement"/>

Specifies the placement of ticks to render either inside or outside the scale.


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description </th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Inside</td>
<td class="type">string</td> 
<td class="description last">The quantitative scale ticks are placed inside the scale </td>
</tr>
<tr>
<td class="name">
Outside</td>
<td class="type">string</td>
<td class="description last">The quantitative scale ticks are placed outside the scale</td>
</tr> 
</tbody>
</table>
Specifies the placement of ticks to render either inside or outside the scale. See <a href="global.html#LabelPlacement">LabelPlacement</a>




#### Default Value






* ej.datavisualization.BulletGraph.TickPlacement.Outside








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { tickPlacement : "inside" }
});
</script> {% endhighlight %}







### quantitativeScaleSettings.tickPosition `enum`
{:#members:quantitativescalesettings-tickposition}


<ts name="ej.datavisualization.BulletGraph.TickPosition"/>

Specifies the position of the ticks to render either above,below or inside


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
Below</td>
<td class="type">string</td> 
<td class="description last">The ticks are positioned below the Quantitative scale</td>
</tr>
<tr>
<td class="name">
Above</td>
<td class="type">string</td>
<td class="description last">The ticks are positioned above the Quantitative scale</td>
</tr> 
<tr>
<td class="name">
Cross</td>
<td class="type">string</td>
<td class="description last">The ticks are placed inside the Quantitative scale</td>
</tr> 
</tbody>
</table>


Specifies the position of the ticks to render either above, below or inside the graph. See <a href="global.html#LabelPosition">LabelPosition</a>




#### Default Value






* ej.datavisualization.BulletGraph.TickPosition.Far








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { tickPosition : "near" }
});
</script> {% endhighlight %}







### theme `string`
{:#members:theme}








By specifying this property the user can change the theme of the bullet graph.




#### Default Value






* "flatlight"








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
theme : "flatdark"                  
});
</script>  {% endhighlight %}







### tooltipSettings  `object`
{:#members:tooltipsettings}








Contains all the properties to customize tooltip.











### tooltipSettings.captionTemplate `string`
{:#members:tooltipsettings-captiontemplate}








Specifies template for caption tooltip




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
tooltipSettings :{captionTemplate: "Tooltip"}
});
</script> {% endhighlight %}







### tooltipSettings.enableCaptionTooltip `boolean`
{:#members:tooltipsettings-enablecaptiontooltip}








Toggles the visibility of caption tooltip




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
tooltipSettings :{enableCaptionTooltip: true}
});
</script> {% endhighlight %}







### tooltipSettings.template `string`
{:#members:tooltipsettings-template}








Specifies the ID of a div, which is to be displayed as tooltip.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
tooltipSettings: { template : "tooltip"},
});
</script> {% endhighlight %}







### tooltipSettings.visible `boolean`
{:#members:tooltipsettings-visible}








Toggles the visibility of tooltip




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
tooltipSettings :{visible: false}
});
</script> {% endhighlight %}







### value `number`
{:#members:value}








Feature measure bar in bullet graph render till the specified value.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
value : 1                    
});
</script>  {% endhighlight %}







### width `number`
{:#members:width}








Specifies the width of the bullet graph.




#### Default Value






* 595








#### Example


{% highlight html %}
 
<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
width : 600                    
});
</script>  {% endhighlight %}





## Methods








### destroy ()
{:#methods:destroy}








To destroy the bullet graph





#### Example


{% highlight html %}
 
<div id="bulletgraph1">Bullet Graph</div> 
 
<script>
// Destroy Bullet graph
var gphObj = $("#bulletGraph1").data("ejBulletGraph");
gphObj.destroy(); // destroy the graph
</script>{% endhighlight %}


{% highlight html %}
 
<div id="bulletGraph1">BulletGraph</div> 
 
<script>
// destroy the Bullet graph
$("#bulletGraph1").ejButton("destroy"); 
</script>{% endhighlight %}







### redraw()
{:#methods:redraw}








To redraw the bullet graph





#### Example


{% highlight html %}
 
<div id="bulletgraph1">Bullet Graph</div> 
 
<script>
// Create Bullet graph
var gphObj = $("#bulletGraph1").data("ejBulletGraph");
gphObj.redraw(); // redraw the graph
</script>{% endhighlight %}


{% highlight html %}
 
<div id="bulletGraph1">BulletGraph</div> 
 
<script>
// redraw the Bullet graph
$("#butbulletGraph1ton1").ejButton("redraw");   
</script>{% endhighlight %}







### setComparativeMeasureSymbol()
{:#methods:setcomparativemeasuresymbol}








To set the value for comparative measure in bullet graph.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.Index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the graph</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.Measure{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the graph</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="bulletGraph1">BulletGraph</div> 
 
<script>
// set the value for comparative measure
var btnObj = $("#bulletGraph1").data("ejBulletGraph");
btnObj.setComparativeMeasureSymbol(1,7); // set the value
</script>{% endhighlight %}


{% highlight html %}
 
<div id="bulletGraph1">BulletGraph</div> 
 
<script>
// set the value for comparative measure
$("#bulletGraph1").ejBulletGraph("setComparativeMeasureSymbol(1,7)");   
</script>{% endhighlight %}







### setFeatureMeasureBarValue()
{:#methods:setfeaturemeasurebarvalue}








To set the value for feature measure bar.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.Index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the graph</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.Measure{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the graph</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="bulletGraph1">Bulletgraph</div> 
 
<script>
// To set the value for feature measure bar.
var btnObj = $("#bulletGraph1").data("ejBulletGraph");
btnObj.setFeatureMeasureBarValue(1,8); // set the value
</script>{% endhighlight %}


{% highlight html %}
 
<div id="bulletGraph1">BulletGraph</div> 
 
<script>
// To set the value for feature measure bar.
$("#bulletGraph1").ejBulletGraph("setFeatureMeasureBarValue(1,8)");     
</script>{% endhighlight %}





## Events








### drawCaption
{:#events:drawcaption}








Fires on rendering the caption of bullet graph.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
Object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
captionElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the current captionSettings element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
captionType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the captionSettings.</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//drawCaption event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawCaption: function (args) {}
});{% endhighlight %}







### drawCategory
{:#events:drawcategory}








Fires on rendering the category.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
Object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
categoryElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the options of category element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the text value of the category that is drawn.</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//drawCategory event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawCategory: function (args) {}
});{% endhighlight %}







### drawComparativeMeasureSymbol
{:#events:drawcomparativemeasuresymbol}








Fires on rendering the comparative measure symbol.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
Object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
targetElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the options of comparative measure element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the comparative measure symbol.</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//drawComparativeMeasureSymbol event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawComparativeMeasureSymbol: function (args) {}
});{% endhighlight %}







### drawFeatureMeasureBar
{:#events:drawfeaturemeasurebar}








Fires on rendering the feature measure bar.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
Object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the options of feature measure element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the value of the feature measure bar.</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//drawFeatureMeasureBar event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawFeatureMeasureBar: function (args) {}
});{% endhighlight %}







### drawIndicator
{:#events:drawindicator}








Fires on rendering the indicator of bullet graph.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
indicatorSettings{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns an object to customize bullet graph indicator text and symbol before rendering it.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of bullet graph.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">for canceling the event.</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//drawIndicator event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawIndicator: function (args) {}
});{% endhighlight %}







### drawLabels
{:#events:drawlabels}








Fires on rendering the labels.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
Object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
scaleElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
tickElement{% endhighlight %}</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description last">returns the current label element.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
labelType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the label type.</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//drawLabels event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawLabels: function (args) {}
});{% endhighlight %}







### drawQualitativeRanges
{:#events:drawqualitativeranges}








Fires on rendering the qualitative ranges.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
Object{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rangeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the index of current range.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rangeOptions{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the settings for current range.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rangeEndValue{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the end value of current range.</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//drawQualitativeRanges event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawQualitativeRanges: function (args) {}
});{% endhighlight %}







### load
{:#events:load}








Fires on loading bullet graph.





#### Example


{% highlight html %}
 
//drawTicks event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   load: function (args) {}
});{% endhighlight %}




