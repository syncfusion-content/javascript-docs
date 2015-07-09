---
layout: post
title: ejBulletGraph
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Bullet graph.










$(element).ejBulletGraph<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create BulletGraph
$('#bulletGraph1').ejBulletGraph();     
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery.js


* module:ej.core.js


* module:ej.data.js


* module:ej.bulletgraph.js




## Members








### applyRangeStrokeToLabels<span class="type-signature type boolean">boolean</span>
{:#members:applyrangestroketolabels}








Toggles the visibility of the range stroke color of the labels.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
applyRangeStrokeToLabels : true                
});
&lt;/script&gt;</code>
</pre>






### applyRangeStrokeToTicks<span class="type-signature type boolean">boolean</span>
{:#members:applyrangestroketoticks}








Toggles the visibility of the range stroke color of the ticks.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
applyRangeStrokeToTicks : true               
});
&lt;/script&gt;</code>
</pre>






### captionSettings<span class="type-signature type object">object</span>
{:#members:captionsettings}








Contains property to customize the caption in bullet graph.











### captionSettings.enableTrim<span class="type-signature type boolean">boolean</span>
{:#members:captionsettings-enabletrim}








Specifies whether trim the labels will be true or false.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ enableTrim : true }                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.font<span class="type-signature type object">object</span>
{:#members:captionsettings-font}








Contains property to customize the font of caption.











### captionSettings.font.color<span class="type-signature type string">string</span>
{:#members:captionsettings-font-color}








Specifies the color of the text in caption.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{color : "green"}}                  
});
&lt;/script&gt;</code>
</pre>






### captionSettings.font.fontFamily<span class="type-signature type string">string</span>
{:#members:captionsettings-font-fontfamily}








Specifies the fontFamily of caption. Caption text render with this fontFamily




Default Value:
{:.param}






* "Segoe UI"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{fontFamily : "algerian"}}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:captionsettings-font-fontstyle}








Specifies the fontStyle of caption. Caption text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>




Default Value:
{:.param}






* "Normal"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{fontStyle : "italic"}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:captionsettings-font-fontweight}








Specifies the fontWeight of caption. Caption text render with this fontWeight. See <a href="global.html#FontWeight">FontWeight</a>




Default Value:
{:.param}






* "regular"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{fontWeight : "lighter"}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.font.opacity<span class="type-signature type number">number</span>
{:#members:captionsettings-font-opacity}








Specifies the opacity of caption. Caption text render with this opacity.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{opacity : 0.5}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.font.size<span class="type-signature type string">string</span>
{:#members:captionsettings-font-size}








Specifies the size of caption. Caption text render with this size




Default Value:
{:.param}






* "12px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{font :{size : "14px"}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator<span class="type-signature type object">object</span>
{:#members:captionsettings-indicator}








Contains property to customize the indicator.











### captionSettings.indicator.font<span class="type-signature type object">object</span>
{:#members:captionsettings-indicator-font}








Contains property to customize the font of indicator.











### captionSettings.indicator.font.color<span class="type-signature type string">string</span>
{:#members:captionsettings-indicator-font-color}








Specifies the color of the indicator's text.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { color :"green" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.font.fontFamily<span class="type-signature type string">string</span>
{:#members:captionsettings-indicator-font-fontfamily}








Specifies the fontFamily of indicator. Indicator text render with this fontFamily.




Default Value:
{:.param}






* "Segoe UI"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { fontFamily :"Algerian" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:captionsettings-indicator-font-fontstyle}








Specifies the fontStyle of indicator. Indicator text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>




Default Value:
{:.param}






* "Normal"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { fontStyle :"italic" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:captionsettings-indicator-font-fontweight}








Specifies the fontWeight of indicator. Indicator text render with this fontWeight. See <a href="global.html#FontWeight">FontWeight</a>




Default Value:
{:.param}






* "regular"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { fontWeight :"lighter" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.font.opacity<span class="type-signature type number">Number</span>
{:#members:captionsettings-indicator-font-opacity}








Specifies the opacity of indicator text. Indicator text render with this Opacity.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { opacity : 0.5 }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.font.size<span class="type-signature type string">string</span>
{:#members:captionsettings-indicator-font-size}








Specifies the size of indicator. Indicator text render with this size.




Default Value:
{:.param}






* "12px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{font : { size :"14px" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.location<span class="type-signature type object">object</span>
{:#members:captionsettings-indicator-location}








Contains property to customize the location of indicator.











### captionSettings.indicator.location.x<span class="type-signature type number">number</span>
{:#members:captionsettings-indicator-location-x}








Specifies the horizontal position of the indicator.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{location : { x :12 }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.location.y<span class="type-signature type number">number</span>
{:#members:captionsettings-indicator-location-y}








Specifies the vertical position of the indicator.




Default Value:
{:.param}






* 60








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{location : { y :60 }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.padding<span class="type-signature type number">number</span>
{:#members:captionsettings-indicator-padding}








Specifies the padding to be applied when text position is used.




Default Value:
{:.param}






* 2








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator: {padding: 5}}                 
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.symbol<span class="type-signature type object">object</span>
{:#members:captionsettings-indicator-symbol}








Contains property to customize the symbol of indicator.











### captionSettings.indicator.symbol.border<span class="type-signature type object">object</span>
{:#members:captionsettings-indicator-symbol-border}








Contains property to customize the border of indicator symbol.











### captionSettings.indicator.symbol.border.color<span class="type-signature type string">string</span>
{:#members:captionsettings-indicator-symbol-border-color}








Specifies the border color of indicator symbol.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { border: { color :"green" } }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.symbol.border.width<span class="type-signature type number">Number</span>
{:#members:captionsettings-indicator-symbol-border-width}








Specifies the border width of indicator symbol.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { border: { width : 2 } }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.symbol.color<span class="type-signature type string">string</span>
{:#members:captionsettings-indicator-symbol-color}








Specifies the color of indicator symbol.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { color :"green" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.symbol.imageURL<span class="type-signature type string">string</span>
{:#members:captionsettings-indicator-symbol-imageurl}








Specifies the url of image that represents indicator symbol.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { imageURL :"../BulletIndicator.png" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.symbol.opacity<span class="type-signature type number">number</span>
{:#members:captionsettings-indicator-symbol-opacity}








Specifies the opacity of indicator symbol.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { opacity :0.5 }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.symbol.shape<span class="type-signature type string">string</span>
{:#members:captionsettings-indicator-symbol-shape}








Specifies the shape of indicator symbol.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { shape :"triangle" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.symbol.size<span class="type-signature type object">object</span>
{:#members:captionsettings-indicator-symbol-size}








Contains property to customize the size of indicator symbol.











### captionSettings.indicator.symbol.size.height<span class="type-signature type number">number</span>
{:#members:captionsettings-indicator-symbol-size-height}








Specifies the height of indicator symbol.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { size : { height: 10 } }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.symbol.size.width<span class="type-signature type number">number</span>
{:#members:captionsettings-indicator-symbol-size-width}








Specifies the width of indicator symbol.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{indicator :{symbol : { size : { width: 10 }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.text<span class="type-signature type string">string</span>
{:#members:captionsettings-indicator-text}








Specifies the text to be displayed as indicator text. By default difference between current value and target will be displayed




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator :{text : "Power Production"} }
});
&lt;/script&gt;e</code>
</pre>






### captionSettings.indicator.textAlignment<span class="type-signature type enum">enum</span>
{:#members:captionsettings-indicator-textalignment}








Specifies the alignment of indicator with respect to scale based on text position. Alignment will not be applied for float position.




Default Value:
{:.param}






* 'Near'








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator:{textAlignment: 'Far'}}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.textAnchor<span class="type-signature type enum">enum</span>
{:#members:captionsettings-indicator-textanchor}








Specifies where indicator text should be anchored when indicator overlaps with other caption group text. Text will be anchored when overlapping caption group text are at same position. Anchoring is not applicable for float position.




Default Value:
{:.param}






* 'start'








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator: {textAnchor: 'end'}}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.textAngle<span class="type-signature type number">number</span>
{:#members:captionsettings-indicator-textangle}








indicator text render in the specified angle.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator :{textAngle :10} }                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.textPosition<span class="type-signature type enum">enum</span>
{:#members:captionsettings-indicator-textposition}








Specifies where indicator should be placed.




Default Value:
{:.param}






* 'float'








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator: {textPosition: 'Top'}}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.textSpacing<span class="type-signature type number">number</span>
{:#members:captionsettings-indicator-textspacing}








Specifies the space between indicator symbol and text.




Default Value:
{:.param}






* 3








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator :{textSpacing :10} }                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.indicator.visibile<span class="type-signature type boolean">boolean</span>
{:#members:captionsettings-indicator-visibile}








Specifies whether indicator will be visible or not.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ indicator :{visible : true} }                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.location<span class="type-signature type object">object</span>
{:#members:captionsettings-location}








Contains property to customize the location.











### captionSettings.location.x<span class="type-signature type number">number</span>
{:#members:captionsettings-location-x}








Specifies the position in horizontal direction




Default Value:
{:.param}






* 17








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{location :{x :15}}            
});
&lt;/script&gt;</code>
</pre>






### captionSettings.location.y<span class="type-signature type number">number</span>
{:#members:captionsettings-location-y}








Specifies the position in horizontal direction




Default Value:
{:.param}






* 30








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{location :{y :15}}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.padding<span class="type-signature type number">number</span>
{:#members:captionsettings-padding}








Specifies the padding to be applied when text position is used.




Default Value:
{:.param}






* 5








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{padding: 2}                 
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle<span class="type-signature type object">object</span>
{:#members:captionsettings-subtitle}








Contains property to customize the subtitle.











### captionSettings.subTitle.font<span class="type-signature type object">object</span>
{:#members:captionsettings-subtitle-font}








Contains property to customize the font of subtitle.











### captionSettings.subTitle.font.color<span class="type-signature type string">string</span>
{:#members:captionsettings-subtitle-font-color}








Specifies the color of the subtitle's text.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { color :"green" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.font.fontFamily<span class="type-signature type string">string</span>
{:#members:captionsettings-subtitle-font-fontfamily}








Specifies the fontFamily of subtitle. Subtitle text render with this fontFamily.




Default Value:
{:.param}






* "Segoe UI"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { fontFamily :"Algerian" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:captionsettings-subtitle-font-fontstyle}








Specifies the fontStyle of subtitle. Subtitle text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>




Default Value:
{:.param}






* "Normal"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { fontStyle :"italic" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:captionsettings-subtitle-font-fontweight}








Specifies the fontWeight of subtitle. Subtitle text render with this fontWeight. See <a href="global.html#FontWeight">FontWeight</a>




Default Value:
{:.param}






* "regular"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { fontWeight :"lighter" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.font.opacity<span class="type-signature type number">number</span>
{:#members:captionsettings-subtitle-font-opacity}








Specifies the opacity of subtitle. Subtitle text render with this opacity.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { opacity :0.5 }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.font.size<span class="type-signature type string">string</span>
{:#members:captionsettings-subtitle-font-size}








Specifies the size of subtitle. Subtitle text render with this size.




Default Value:
{:.param}






* "12px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{font : { size :"14px" }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.location<span class="type-signature type object">object</span>
{:#members:captionsettings-subtitle-location}








Contains property to customize the location of subtitle.











### captionSettings.subTitle.location.x<span class="type-signature type number">number</span>
{:#members:captionsettings-subtitle-location-x}








Specifies the horizontal position of the subtitle.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{location : { x :12 }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.location.y<span class="type-signature type number">number</span>
{:#members:captionsettings-subtitle-location-y}








Specifies the vertical position of the subtitle.




Default Value:
{:.param}






* 45








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle :{location : { y :50 }}}                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.padding<span class="type-signature type number">number</span>
{:#members:captionsettings-subtitle-padding}








Specifies the padding to be applied when text position is used.




Default Value:
{:.param}






* 5








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle:{padding: 8}}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.text<span class="type-signature type string">string</span>
{:#members:captionsettings-subtitle-text}








Specifies the text to be displayed as subtitle.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ subTitle :{text : "Power Production"} }
});
&lt;/script&gt;e</code>
</pre>






### captionSettings.subTitle.textAlignment<span class="type-signature type enum">enum</span>
{:#members:captionsettings-subtitle-textalignment}








Specifies the alignment of sub title text with respect to scale. Alignment will not be applied in float position.




Default Value:
{:.param}






* 'Near'








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{subTitle:{textAlignment: 'Far'}}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.textAnchor<span class="type-signature type enum">enum</span>
{:#members:captionsettings-subtitle-textanchor}








Specifies where subtitle text should be anchored when sub title text overlaps with other caption group text. Text will be anchored when overlapping caption group text are at same position. Anchoring is not applicable for float position.




Default Value:
{:.param}






* 'start'








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ subTitle: {textAnchor: 'end'}}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.textAngle<span class="type-signature type number">number</span>
{:#members:captionsettings-subtitle-textangle}








Subtitle render in the specified angle.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ subTitle :{textAngle :10} }                    
});
&lt;/script&gt;</code>
</pre>






### captionSettings.subTitle.textPosition<span class="type-signature type enum">enum</span>
{:#members:captionsettings-subtitle-textposition}








Specifies where sub title text should be placed.




Default Value:
{:.param}






* 'float'








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{ subTitle:{textPosition: 'Right'}}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.text<span class="type-signature type string">string</span>
{:#members:captionsettings-text}








Specifies the text to be displayed on bullet graph.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{text : "Production"}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.textAlignment<span class="type-signature type enum">enum</span>
{:#members:captionsettings-textalignment}








Specifies the alignment of caption text with respect to scale. This property will not be applied when text position is float.




Default Value:
{:.param}






* 'Near'








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{textAlignment: 'Center'}                 
});
&lt;/script&gt;</code>
</pre>






### captionSettings.textAnchor<span class="type-signature type enum">enum</span>
{:#members:captionsettings-textanchor}








Specifies caption text anchoring when caption text overlaps with other caption group text. Text will be anchored when overlapping caption group text are at same position. Anchoring is not applicable for float position.




Default Value:
{:.param}






* 'start'








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{textAnchor: 'middle'}
});
&lt;/script&gt;</code>
</pre>






### captionSettings.textAngle<span class="type-signature type number">number</span>
{:#members:captionsettings-textangle}








Specifies the angel in which the caption is rendered.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{textAngle : 5}                 
});
&lt;/script&gt;</code>
</pre>






### captionSettings.textPosition<span class="type-signature type enum">enum</span>
{:#members:captionsettings-textposition}








Specifies how caption text should be placed.




Default Value:
{:.param}






* 'float'








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
captionSettings :{textPosition: 'Top'}                 
});
&lt;/script&gt;</code>
</pre>






### comparativeMeasureValue<span class="type-signature type number">number</span>
{:#members:comparativemeasurevalue}








Comparative measure bar in bullet graph render till the specified value.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
comparativeMeasureValue : 1                    
});
&lt;/script&gt;  </code>
</pre>






### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}








Toggles the animation of bullet graph.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
enableAnimation : false                 
});
&lt;/script&gt;</code>
</pre>






### enableResizing<span class="type-signature type boolean">boolean</span>
{:#members:enableresizing}








Sets a value whether to make the bullet graph responsive on resize.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
enableResizing : false                  
});
&lt;/script&gt;</code>
</pre>






### flowDirection<span class="type-signature type enum">enum</span>
{:#members:flowdirection}








Specifies the direction of flow in bullet graph. Neither it may be backward nor forward. See <a href="global.html#FlowDirection">FlowDirection</a>




Default Value:
{:.param}






* "forward"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
flowDirection : "backward"                   
});
&lt;/script&gt; </code>
</pre>






### height<span class="type-signature type number">number</span>
{:#members:height}








Specifies the height of the bullet graph.




Default Value:
{:.param}






* 90








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
height : 600                    
});
&lt;/script&gt;  </code>
</pre>






### orientation<span class="type-signature type enum">enum</span>
{:#members:orientation}








Bullet graph will render in the specified orientation.




Default Value:
{:.param}






* "horizontal"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
orientation : "vertical"                   
});
&lt;/script&gt; </code>
</pre>






### qualitativeRanges<span class="type-signature type array">array</span>
{:#members:qualitativeranges}








Contains property to customize the qualitative ranges.











### qualitativeRanges.rangeEnd<span class="type-signature type number">number</span>
{:#members:qualitativeranges-rangeend}








Specifies the ending range to which the qualitative ranges will render.




Default Value:
{:.param}






* 3








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeEnd : 4.5}]                  
});
&lt;/script&gt;</code>
</pre>






### qualitativeRanges.rangeEnd<span class="type-signature type number">number</span>
{:#members:qualitativeranges-rangeend}








Specifies the ending range to which the qualitative ranges will render.




Default Value:
{:.param}






* 7.3








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeEnd : 7}]                 
});
&lt;/script&gt;</code>
</pre>






### qualitativeRanges.rangeEnd<span class="type-signature type number">number</span>
{:#members:qualitativeranges-rangeend}








Specifies the ending range to which the qualitative ranges will render.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeEnd : 5}]                 
});
&lt;/script&gt;</code>
</pre>






### qualitativeRanges.rangeOpacity<span class="type-signature type number">number</span>
{:#members:qualitativeranges-rangeopacity}








Specifies the opacity for the qualitative ranges.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeOpacity : 0.5}]                 
});
&lt;/script&gt;</code>
</pre>






### qualitativeRanges.rangeOpacity<span class="type-signature type number">number</span>
{:#members:qualitativeranges-rangeopacity}








Specifies the opacity for the qualitative ranges.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeOpacity : 0.5}]                 
});
&lt;/script&gt;</code>
</pre>






### qualitativeRanges.rangeOpacity<span class="type-signature type number">number</span>
{:#members:qualitativeranges-rangeopacity}








Specifies the opacity for the qualitative ranges.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeOpacity : 0.5}]                 
});
&lt;/script&gt;</code>
</pre>






### qualitativeRanges.rangeStroke<span class="type-signature type string">string</span>
{:#members:qualitativeranges-rangestroke}








Specifies the stroke for the qualitative ranges.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeStroke : 5}]                 
});
&lt;/script&gt;</code>
</pre>






### qualitativeRanges.rangeStroke<span class="type-signature type string">string</span>
{:#members:qualitativeranges-rangestroke}








Specifies the stroke for the qualitative ranges.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeStroke : 5}]                 
});
&lt;/script&gt;</code>
</pre>






### qualitativeRanges.rangeStroke<span class="type-signature type string">string</span>
{:#members:qualitativeranges-rangestroke}








Specifies the stroke for the qualitative ranges.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRanges :[{rangeStroke : 5}]                 
});
&lt;/script&gt;</code>
</pre>






### qualitativeRangeSize<span class="type-signature type number">number</span>
{:#members:qualitativerangesize}








Size of the qualitative range depends up on the specified value.




Default Value:
{:.param}






* 32








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
qualitativeRangeSize : 35                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleLength<span class="type-signature type number">number</span>
{:#members:quantitativescalelength}








Length of the quantitative range depends up on the specified value.




Default Value:
{:.param}






* 475








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleLength :500                 
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings}








Contains all the properties to customize quantitative scale.











### quantitativeScaleSettings.comparativeMeasureSettings<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings-comparativemeasuresettings}








Contains property to customize the comparative measure.











### quantitativeScaleSettings.comparativeMeasureSettings.stroke<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-comparativemeasuresettings-stroke}








Specifies the stroke of the comparative measure.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { comparativeMeasureSettings :{ stroke :2} }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.comparativeMeasureSettings.width<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-comparativemeasuresettings-width}








Specifies the width of the comparative measure.




Default Value:
{:.param}






* 5








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
 quantitativeScaleSettings : { comparativeMeasureSettings :{ width :6} }                     
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.featuredMeasureSettings<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings-featuredmeasuresettings}








Contains property to customize the featured measure.











### quantitativeScaleSettings.featuredMeasureSettings.stroke<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-featuredmeasuresettings-stroke}








Specifies the Stroke of the featured measure in bullet graph.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { featuredMeasureSettings :{stroke : 2} }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.featuredMeasureSettings.width<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-featuredmeasuresettings-width}








Specifies the width of the featured measure in bullet graph.




Default Value:
{:.param}






* 2








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="ejBulletGraph"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#bulletGraph1").ejBulletGraph({
   quantitativeScaleSettings: { featuredMeasureSettings: { width: 3 }},
   });
&lt;/script&gt;  </code>
</pre>






### quantitativeScaleSettings.featureMeasures<span class="type-signature type array">array</span>
{:#members:quantitativescalesettings-featuremeasures}








Contains property to customize the featured measure.











### quantitativeScaleSettings.featureMeasures.category<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-featuremeasures-category}








Specifies the category of feature measure.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { featureMeasures :[{ category :null}] }                  
});
&lt;/script&gt;</code>
</pre>






### quantitativeScaleSettings.featureMeasures.comparativeMeasureValue<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-featuremeasures-comparativemeasurevalue}








Comparative measure render till the specified value.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { featureMeasures :[{ comparativeMeasureValue :2}] }                  
});
&lt;/script&gt;</code>
</pre>






### quantitativeScaleSettings.featureMeasures.value<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-featuremeasures-value}








Feature measure render till the specified value.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { featureMeasures :[{ value :2}] }                  
});
&lt;/script&gt;</code>
</pre>






### quantitativeScaleSettings.fields<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings-fields}








Contains property to customize the fields.











### quantitativeScaleSettings.fields.category<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-fields-category}








Specifies the category of the bullet graph.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
fields :{category : "ProductId"}                  
});
&lt;/script&gt;</code>
</pre>






### quantitativeScaleSettings.fields.comparativeMeasure<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-fields-comparativemeasure}








Comparative measure render based on the values in the specified field.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
fields :{comparativeMeasure : "comparativeMeasureValue"}                  
});
&lt;/script&gt;</code>
</pre>






### quantitativeScaleSettings.fields.dataSource<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings-fields-datasource}








Specifies the dataSource for the bullet graph.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
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
           });</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
fields : {datasource :{ej.DataManger :{url : "http://mvc.syncfusion.com/Services/Northwnd.svc/" }} }                 
});
&lt;/script&gt;         </code>
</pre>






### quantitativeScaleSettings.fields.featureMeasures<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-fields-featuremeasures}








Feature measure render based on the values in the specified field.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
fields :{featureMeasures : "UnitPrice"}                  
});
&lt;/script&gt;</code>
</pre>






### quantitativeScaleSettings.fields.query<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-fields-query}








Specifies the query for fetching the values form data source to render the bullet graph.




Default Value:
{:.param}






* null














### quantitativeScaleSettings.fields.tableName<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-fields-tablename}








Specifies the name of the table.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
fields :{tableName : "Product"}                 
});
&lt;/script&gt;</code>
</pre>






### quantitativeScaleSettings.interval<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-interval}








Specifies the interval for the Graph.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { interval : 2 }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings-labelsettings}








Contains property to customize the labels.











### quantitativeScaleSettings.labelSettings.font<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings-labelsettings-font}








Contains property to customize the font of the labels in bullet graph.











### quantitativeScaleSettings.labelSettings.font.fontFamily<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-labelsettings-font-fontfamily}








Specifies the fontFamily of labels in bullet graph. Labels render with this fontFamily.




Default Value:
{:.param}






* "Segoe UI"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { font :{ fontFamily : "Algerian" } } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:quantitativescalesettings-labelsettings-font-fontstyle}








Specifies the fontStyle of labels in bullet graph. Labels render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>




Default Value:
{:.param}






* "Normal"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { font :{ fontStyle : "italic" } } }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:quantitativescalesettings-labelsettings-font-fontweight}








Specifies the fontWeight of labels in bullet graph. Labels render with this fontWeight. See <a href="global.html#FontWeight">FontWeight</a>




Default Value:
{:.param}






* "regular"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { font :{ fontWeight : "lighter" } } }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.font.opacity<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-labelsettings-font-opacity}








Specifies the opacity of labels in bullet graph. Labels render with this opacity




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { font :{ opacity : 0.5 } } }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.labelPlacement<span class="type-signature type enum">enum</span>
{:#members:quantitativescalesettings-labelsettings-labelplacement}








Specifies the placement of labels in bullet graph scale.




Default Value:
{:.param}






* outside








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { labelPlacement : "inside" } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.labelPrefix<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-labelsettings-labelprefix}








Specifies the prefix to be added with labels in bullet graph.




Default Value:
{:.param}






* Empty string








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { labelPrefix : "$" } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.labelSuffix<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-labelsettings-labelsuffix}








Specifies the suffix to be added after labels in bullet graph.




Default Value:
{:.param}






* Empty string








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { labelSuffix : "K" } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.offset<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-labelsettings-offset}








Specifies the horizontal/vertical padding of labels.




Default Value:
{:.param}






* 15








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { offset : 25 } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.position<span class="type-signature type enum">enum</span>
{:#members:quantitativescalesettings-labelsettings-position}








Specifies the position of the labels to render either above or below the graph. See <a href="global.html#Position">Position</a>




Default Value:
{:.param}






* "below"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { position : "above" } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.size<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-labelsettings-size}








Specifies the Size of the labels.




Default Value:
{:.param}






* 12








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { size : 10 } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.labelSettings.stroke<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-labelsettings-stroke}








Specifies the stroke color of the labels in bullet graph.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { labelSettings : { stroke : "green" } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.location<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings-location}








Contains property to customize the position of the quantitative scale











### quantitativeScaleSettings.location.x<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-location-x}








This property specifies the x position for rendering quantitative scale.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { location : { x : 15 } } 
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.location.y<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-location-y}








This property specifies the y position for rendering quantitative scale.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { location : { y : 15 } }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.majorTickSettings<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings-majorticksettings}








Contains property to customize the major tick lines.











### quantitativeScaleSettings.majorTickSettings.size<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-majorticksettings-size}








Specifies the size of the major ticks.




Default Value:
{:.param}






* 13








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { majorTickSettings : { size : 15 } }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.majorTickSettings.stroke<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-majorticksettings-stroke}








Specifies the stroke color of the major tick lines.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { majorTickSettings : { stroke : "red" } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.majorTickSettings.width<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-majorticksettings-width}








Specifies the width of the major tick lines.




Default Value:
{:.param}






* 2








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { majorTickSettings : { width : 1 } }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.maximum<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-maximum}








Specifies the maximum value of the Graph.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { maximum : 8 }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.minimum<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-minimum}








Specifies the minimum value of the Graph.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minimum : 1 }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.minorTickSettings<span class="type-signature type object">object</span>
{:#members:quantitativescalesettings-minorticksettings}








Contains property to customize the minor ticks.











### quantitativeScaleSettings.minorTickSettings.size<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-minorticksettings-size}








Specifies the size of minor ticks.




Default Value:
{:.param}






* 7








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minorTickSettings : { size : 10} }                  
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.minorTickSettings.stroke<span class="type-signature type string">string</span>
{:#members:quantitativescalesettings-minorticksettings-stroke}








Specifies the stroke color of minor ticks in bullet graph.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minorTickSettings : { stroke : "green" } }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.minorTickSettings.width<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-minorticksettings-width}








Specifies the width of the minor ticks in bullet graph.




Default Value:
{:.param}






* 2








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minorTickSettings : { width : 1 } }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.minorTicksPerInterval<span class="type-signature type number">number</span>
{:#members:quantitativescalesettings-minorticksperinterval}








The specified number of minor ticks will be rendered per interval.




Default Value:
{:.param}






* 4








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { minorTicksPerInterval : 5 }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.tickPlacement<span class="type-signature type enum">enum</span>
{:#members:quantitativescalesettings-tickplacement}








Specifies the placement of ticks to render either inside or outside the scale. See <a href="global.html#LabelPlacement">LabelPlacement</a>




Default Value:
{:.param}






* ej.datavisualization.BulletGraph.TickPlacement.Outside








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { tickPlacement : "inside" }
});
&lt;/script&gt; </code>
</pre>






### quantitativeScaleSettings.tickPosition<span class="type-signature type enum">enum</span>
{:#members:quantitativescalesettings-tickposition}








Specifies the position of the ticks to render either above, below or inside the graph. See <a href="global.html#LabelPosition">LabelPosition</a>




Default Value:
{:.param}






* ej.datavisualization.BulletGraph.TickPosition.Far








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
quantitativeScaleSettings : { tickPosition : "near" }
});
&lt;/script&gt; </code>
</pre>






### theme<span class="type-signature type string">string</span>
{:#members:theme}








By specifying this property the user can change the theme of the bullet graph.




Default Value:
{:.param}






* "flatlight"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
theme : "flatdark"                  
});
&lt;/script&gt;  </code>
</pre>






### tooltipSettings<span class="type-signature type object">object</span>
{:#members:tooltipsettings}








Contains all the properties to customize tooltip.











### tooltipSettings.captionTemplate<span class="type-signature type string">string</span>
{:#members:tooltipsettings-captiontemplate}








Specifies template for caption tooltip




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
tooltipSettings :{captionTemplate: "Tooltip"}
});
&lt;/script&gt; </code>
</pre>






### tooltipSettings.enableCaptionTooltip<span class="type-signature type boolean">boolean</span>
{:#members:tooltipsettings-enablecaptiontooltip}








Toggles the visibility of caption tooltip




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
tooltipSettings :{enableCaptionTooltip: true}
});
&lt;/script&gt; </code>
</pre>






### tooltipSettings.template<span class="type-signature type string">string</span>
{:#members:tooltipsettings-template}








Specifies the ID of a div, which is to be displayed as tooltip.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
tooltipSettings: { template : "tooltip"},
});
&lt;/script&gt; </code>
</pre>






### tooltipSettings.visible<span class="type-signature type boolean">boolean</span>
{:#members:tooltipsettings-visible}








Toggles the visibility of tooltip




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
tooltipSettings :{visible: false}
});
&lt;/script&gt; </code>
</pre>






### value<span class="type-signature type number">number</span>
{:#members:value}








Feature measure bar in bullet graph render till the specified value.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
value : 1                    
});
&lt;/script&gt;  </code>
</pre>






### width<span class="type-signature type number">number</span>
{:#members:width}








Specifies the width of the bullet graph.




Default Value:
{:.param}






* 595








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#bulletGraph1").ejBulletGraph({
width : 600                    
});
&lt;/script&gt;  </code>
</pre>




## Methods








### destroy<span class="signature">()</span>
{:#methods:destroy}








To destroy the bullet graph





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletgraph1"&gt;Bullet Graph&lt;/div&gt; 
 
&lt;script&gt;
// Destroy Bullet graph
var gphObj = $("#bulletGraph1").data("ejBulletGraph");
gphObj.destroy(); // destroy the graph
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;BulletGraph&lt;/div&gt; 
 
&lt;script&gt;
// destroy the Bullet graph
$("#bulletGraph1").ejButton("destroy"); 
&lt;/script&gt;</code>
</pre>






### redraw<span class="signature">()</span>
{:#methods:redraw}








To redraw the bulet graph





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletgraph1"&gt;Bullet Graph&lt;/div&gt; 
 
&lt;script&gt;
// Create Bullet graph
var gphObj = $("#bulletGraph1").data("ejBulletGraph");
gphObj.redraw(); // redraw the graph
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;BulletGraph&lt;/div&gt; 
 
&lt;script&gt;
// redraw the Bullet graph
$("#butbulletGraph1ton1").ejButton("redraw");   
&lt;/script&gt;</code>
</pre>






### setComparativeMeasureSymbol<span class="signature">()</span>
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
<td class="name"><code>argument.Index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the graph</td>
</tr>
<tr>
<td class="name"><code>argument.Measure</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the graph</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;BulletGraph&lt;/div&gt; 
 
&lt;script&gt;
// set the value for comparative measure
var btnObj = $("#bulletGraph1").data("ejBulletGraph");
btnObj.setComparativeMeasureSymbol(1,7); // set the value
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;BulletGraph&lt;/div&gt; 
 
&lt;script&gt;
// set the value for comparative measure
$("#bulletGraph1").ejBulletGraph("setComparativeMeasureSymbol(1,7)");   
&lt;/script&gt;</code>
</pre>






### setFeatureMeasureBarValue<span class="signature">()</span>
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
<td class="name"><code>argument.Index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the graph</td>
</tr>
<tr>
<td class="name"><code>argument.Measure</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">value for the graph</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;Bulletgraph&lt;/div&gt; 
 
&lt;script&gt;
// To set the value for feature measure bar.
var btnObj = $("#bulletGraph1").data("ejBulletGraph");
btnObj.setFeatureMeasureBarValue(1,8); // set the value
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="bulletGraph1"&gt;BulletGraph&lt;/div&gt; 
 
&lt;script&gt;
// To set the value for feature measure bar.
$("#bulletGraph1").ejBulletGraph("setFeatureMeasureBarValue(1,8)");     
&lt;/script&gt;</code>
</pre>




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
<td class="name"><code>args.Object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">scaleElement</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.captionElement</code></td>
<td class="type"><span class="param-type">captionElement</span></td>
<td class="description last">returns the current captionSettings element.</td>
</tr>
<tr>
<td class="name"><code>args.captionType</code></td>
<td class="type"><span class="param-type">captionType</span></td>
<td class="description last">returns the type of the captionSettings.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//drawCaption event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawCaption: function (args) {}
});</code>
</pre>






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
<td class="name"><code>args.Object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">scaleElement</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.categoryElement</code></td>
<td class="type"><span class="param-type">categoryElement</span></td>
<td class="description last">returns the options of category element.</td>
</tr>
<tr>
<td class="name"><code>args.Value</code></td>
<td class="type"><span class="param-type">Value</span></td>
<td class="description last">returns the text value of the category that is drawn.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//drawCategory event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawCategory: function (args) {}
});</code>
</pre>






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
<td class="name"><code>args.Object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">scaleElement</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.targetElement</code></td>
<td class="type"><span class="param-type">targetElement</span></td>
<td class="description last">returns the options of comparative measure element.</td>
</tr>
<tr>
<td class="name"><code>args.Value</code></td>
<td class="type"><span class="param-type">Value</span></td>
<td class="description last">returns the value of the comparative measure symbol.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//drawComparativeMeasureSymbol event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawComparativeMeasureSymbol: function (args) {}
});</code>
</pre>






### drawFeatureMeasureBar
{:#events:drawfeaturemeasurebar}








Fires on rednering the feature measure bar.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>args.Object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">scaleElement</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.currentElement</code></td>
<td class="type"><span class="param-type">currentElement</span></td>
<td class="description last">returns the options of feature measure element.</td>
</tr>
<tr>
<td class="name"><code>args.Value</code></td>
<td class="type"><span class="param-type">Value</span></td>
<td class="description last">returns the value of the feature measure bar.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//drawFeatureMeasureBar event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawFeatureMeasureBar: function (args) {}
});</code>
</pre>






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
<td class="name"><code>args.indicatorSettings</code></td>
<td class="type"><span class="param-type">indicatorSettings</span></td>
<td class="description last">returns an object to customize bullet graph indicator text and symbol before rendering it.</td>
</tr>
<tr>
<td class="name"><code>args.model</code></td>
<td class="type"><span class="param-type"><a href="global.html#model">model</a></span></td>
<td class="description last">returns the object of bullet graph.</td>
</tr>
<tr>
<td class="name"><code>args.type</code></td>
<td class="type"><span class="param-type">type</span></td>
<td class="description last">returns the type of event.</td>
</tr>
<tr>
<td class="name"><code>args.cancel</code></td>
<td class="type"><span class="param-type">cancel</span></td>
<td class="description last">for cancelling the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//drawIndicator event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawIndicator: function (args) {}
});</code>
</pre>






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
<td class="name"><code>args.Object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name"><code>args.scaleElement</code></td>
<td class="type"><span class="param-type">scaleElement</span></td>
<td class="description last">returns the options of the scale element.</td>
</tr>
<tr>
<td class="name"><code>args.tickElement</code></td>
<td class="type"><span class="param-type">labelElement</span></td>
<td class="description last">returns the current label element.</td>
</tr>
<tr>
<td class="name"><code>args.labelType</code></td>
<td class="type"><span class="param-type">labelType</span></td>
<td class="description last">returns the label type.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//drawLabels event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawLabels: function (args) {}
});</code>
</pre>






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
<td class="name"><code>args.Object</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the object of the bullet graph.</td>
</tr>
<tr>
<td class="name"><code>args.rangeIndex</code></td>
<td class="type"><span class="param-type">rangeIndex</span></td>
<td class="description last">returns the index of current range.</td>
</tr>
<tr>
<td class="name"><code>args.rangeOptions</code></td>
<td class="type"><span class="param-type">rangeOptions</span></td>
<td class="description last">returns the settings for current range.</td>
</tr>
<tr>
<td class="name"><code>args.rangeEndValue</code></td>
<td class="type"><span class="param-type">rangeEndValue</span></td>
<td class="description last">returns the end value of current range.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//drawQualitativeRanges event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawQualitativeRanges: function (args) {}
});</code>
</pre>






### load
{:#events:load}








Fires on loading bullet graph.





Example
{:.example}

<pre class="prettyprint">
<code> 
//drawTicks event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   load: function (args) {}
});</code>
</pre>



