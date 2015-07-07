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
{:#applyrangestroketolabels}
{:#applyRangeStrokeToLabels}








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
{:#applyrangestroketoticks}
{:#applyRangeStrokeToTicks}








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
{:#captionsettings}
{:#captionSettings}








Contains property to customize the caption in bullet graph.











### captionSettings.enableTrim<span class="type-signature type boolean">boolean</span>
{:#captionsettings-enabletrim}
{:#captionSettings-enableTrim}








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
{:#captionsettings-font}
{:#captionSettings-font}








Contains property to customize the font of caption.











### captionSettings.font.color<span class="type-signature type string">string</span>
{:#captionsettings-font-color}
{:#captionSettings-font-color}








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
{:#captionsettings-font-fontfamily}
{:#captionSettings-font-fontFamily}








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
{:#captionsettings-font-fontstyle}
{:#captionSettings-font-fontStyle}








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
{:#captionsettings-font-fontweight}
{:#captionSettings-font-fontWeight}








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
{:#captionsettings-font-opacity}
{:#captionSettings-font-opacity}








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
{:#captionsettings-font-size}
{:#captionSettings-font-size}








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
{:#captionsettings-indicator}
{:#captionSettings-indicator}








Contains property to customize the indicator.











### captionSettings.indicator.font<span class="type-signature type object">object</span>
{:#captionsettings-indicator-font}
{:#captionSettings-indicator-font}








Contains property to customize the font of indicator.











### captionSettings.indicator.font.color<span class="type-signature type string">string</span>
{:#captionsettings-indicator-font-color}
{:#captionSettings-indicator-font-color}








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
{:#captionsettings-indicator-font-fontfamily}
{:#captionSettings-indicator-font-fontFamily}








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
{:#captionsettings-indicator-font-fontstyle}
{:#captionSettings-indicator-font-fontStyle}








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
{:#captionsettings-indicator-font-fontweight}
{:#captionSettings-indicator-font-fontWeight}








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
{:#captionsettings-indicator-font-opacity}
{:#captionSettings-indicator-font-opacity}








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
{:#captionsettings-indicator-font-size}
{:#captionSettings-indicator-font-size}








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
{:#captionsettings-indicator-location}
{:#captionSettings-indicator-location}








Contains property to customize the location of indicator.











### captionSettings.indicator.location.x<span class="type-signature type number">number</span>
{:#captionsettings-indicator-location-x}
{:#captionSettings-indicator-location-x}








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
{:#captionsettings-indicator-location-y}
{:#captionSettings-indicator-location-y}








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
{:#captionsettings-indicator-padding}
{:#captionSettings-indicator-padding}








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
{:#captionsettings-indicator-symbol}
{:#captionSettings-indicator-symbol}








Contains property to customize the symbol of indicator.











### captionSettings.indicator.symbol.border<span class="type-signature type object">object</span>
{:#captionsettings-indicator-symbol-border}
{:#captionSettings-indicator-symbol-border}








Contains property to customize the border of indicator symbol.











### captionSettings.indicator.symbol.border.color<span class="type-signature type string">string</span>
{:#captionsettings-indicator-symbol-border-color}
{:#captionSettings-indicator-symbol-border-color}








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
{:#captionsettings-indicator-symbol-border-width}
{:#captionSettings-indicator-symbol-border-width}








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
{:#captionsettings-indicator-symbol-color}
{:#captionSettings-indicator-symbol-color}








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
{:#captionsettings-indicator-symbol-imageurl}
{:#captionSettings-indicator-symbol-imageURL}








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
{:#captionsettings-indicator-symbol-opacity}
{:#captionSettings-indicator-symbol-opacity}








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
{:#captionsettings-indicator-symbol-shape}
{:#captionSettings-indicator-symbol-shape}








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
{:#captionsettings-indicator-symbol-size}
{:#captionSettings-indicator-symbol-size}








Contains property to customize the size of indicator symbol.











### captionSettings.indicator.symbol.size.height<span class="type-signature type number">number</span>
{:#captionsettings-indicator-symbol-size-height}
{:#captionSettings-indicator-symbol-size-height}








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
{:#captionsettings-indicator-symbol-size-width}
{:#captionSettings-indicator-symbol-size-width}








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
{:#captionsettings-indicator-text}
{:#captionSettings-indicator-text}








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
{:#captionsettings-indicator-textalignment}
{:#captionSettings-indicator-textAlignment}








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
{:#captionsettings-indicator-textanchor}
{:#captionSettings-indicator-textAnchor}








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
{:#captionsettings-indicator-textangle}
{:#captionSettings-indicator-textAngle}








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
{:#captionsettings-indicator-textposition}
{:#captionSettings-indicator-textPosition}








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
{:#captionsettings-indicator-textspacing}
{:#captionSettings-indicator-textSpacing}








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
{:#captionsettings-indicator-visibile}
{:#captionSettings-indicator-visibile}








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
{:#captionsettings-location}
{:#captionSettings-location}








Contains property to customize the location.











### captionSettings.location.x<span class="type-signature type number">number</span>
{:#captionsettings-location-x}
{:#captionSettings-location-x}








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
{:#captionsettings-location-y}
{:#captionSettings-location-y}








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
{:#captionsettings-padding}
{:#captionSettings-padding}








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
{:#captionsettings-subtitle}
{:#captionSettings-subTitle}








Contains property to customize the subtitle.











### captionSettings.subTitle.font<span class="type-signature type object">object</span>
{:#captionsettings-subtitle-font}
{:#captionSettings-subTitle-font}








Contains property to customize the font of subtitle.











### captionSettings.subTitle.font.color<span class="type-signature type string">string</span>
{:#captionsettings-subtitle-font-color}
{:#captionSettings-subTitle-font-color}








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
{:#captionsettings-subtitle-font-fontfamily}
{:#captionSettings-subTitle-font-fontFamily}








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
{:#captionsettings-subtitle-font-fontstyle}
{:#captionSettings-subTitle-font-fontStyle}








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
{:#captionsettings-subtitle-font-fontweight}
{:#captionSettings-subTitle-font-fontWeight}








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
{:#captionsettings-subtitle-font-opacity}
{:#captionSettings-subTitle-font-opacity}








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
{:#captionsettings-subtitle-font-size}
{:#captionSettings-subTitle-font-size}








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
{:#captionsettings-subtitle-location}
{:#captionSettings-subTitle-location}








Contains property to customize the location of subtitle.











### captionSettings.subTitle.location.x<span class="type-signature type number">number</span>
{:#captionsettings-subtitle-location-x}
{:#captionSettings-subTitle-location-x}








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
{:#captionsettings-subtitle-location-y}
{:#captionSettings-subTitle-location-y}








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
{:#captionsettings-subtitle-padding}
{:#captionSettings-subTitle-padding}








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
{:#captionsettings-subtitle-text}
{:#captionSettings-subTitle-text}








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
{:#captionsettings-subtitle-textalignment}
{:#captionSettings-subTitle-textAlignment}








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
{:#captionsettings-subtitle-textanchor}
{:#captionSettings-subTitle-textAnchor}








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
{:#captionsettings-subtitle-textangle}
{:#captionSettings-subTitle-textAngle}








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
{:#captionsettings-subtitle-textposition}
{:#captionSettings-subTitle-textPosition}








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
{:#captionsettings-text}
{:#captionSettings-text}








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
{:#captionsettings-textalignment}
{:#captionSettings-textAlignment}








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
{:#captionsettings-textanchor}
{:#captionSettings-textAnchor}








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
{:#captionsettings-textangle}
{:#captionSettings-textAngle}








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
{:#captionsettings-textposition}
{:#captionSettings-textPosition}








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
{:#comparativemeasurevalue}
{:#comparativeMeasureValue}








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
{:#enableanimation}
{:#enableAnimation}








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
{:#enableresizing}
{:#enableResizing}








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
{:#flowdirection}
{:#flowDirection}








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
{:#height}
{:#height}








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
{:#orientation}
{:#orientation}








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
{:#qualitativeranges}
{:#qualitativeRanges}








Contains property to customize the qualitative ranges.











### qualitativeRanges.rangeEnd<span class="type-signature type number">number</span>
{:#qualitativeranges-rangeend}
{:#qualitativeRanges-rangeEnd}








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
{:#qualitativeranges-rangeend}
{:#qualitativeRanges-rangeEnd}








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
{:#qualitativeranges-rangeend}
{:#qualitativeRanges-rangeEnd}








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
{:#qualitativeranges-rangeopacity}
{:#qualitativeRanges-rangeOpacity}








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
{:#qualitativeranges-rangeopacity}
{:#qualitativeRanges-rangeOpacity}








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
{:#qualitativeranges-rangeopacity}
{:#qualitativeRanges-rangeOpacity}








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
{:#qualitativeranges-rangestroke}
{:#qualitativeRanges-rangeStroke}








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
{:#qualitativeranges-rangestroke}
{:#qualitativeRanges-rangeStroke}








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
{:#qualitativeranges-rangestroke}
{:#qualitativeRanges-rangeStroke}








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
{:#qualitativerangesize}
{:#qualitativeRangeSize}








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
{:#quantitativescalelength}
{:#quantitativeScaleLength}








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
{:#quantitativescalesettings}
{:#quantitativeScaleSettings}








Contains all the properties to customize quantitative scale.











### quantitativeScaleSettings.comparativeMeasureSettings<span class="type-signature type object">object</span>
{:#quantitativescalesettings-comparativemeasuresettings}
{:#quantitativeScaleSettings-comparativeMeasureSettings}








Contains property to customize the comparative measure.











### quantitativeScaleSettings.comparativeMeasureSettings.stroke<span class="type-signature type number">number</span>
{:#quantitativescalesettings-comparativemeasuresettings-stroke}
{:#quantitativeScaleSettings-comparativeMeasureSettings-stroke}








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
{:#quantitativescalesettings-comparativemeasuresettings-width}
{:#quantitativeScaleSettings-comparativeMeasureSettings-width}








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
{:#quantitativescalesettings-featuredmeasuresettings}
{:#quantitativeScaleSettings-featuredMeasureSettings}








Contains property to customize the featured measure.











### quantitativeScaleSettings.featuredMeasureSettings.stroke<span class="type-signature type number">number</span>
{:#quantitativescalesettings-featuredmeasuresettings-stroke}
{:#quantitativeScaleSettings-featuredMeasureSettings-stroke}








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
{:#quantitativescalesettings-featuredmeasuresettings-width}
{:#quantitativeScaleSettings-featuredMeasureSettings-width}








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
{:#quantitativescalesettings-featuremeasures}
{:#quantitativeScaleSettings-featureMeasures}








Contains property to customize the featured measure.











### quantitativeScaleSettings.featureMeasures.category<span class="type-signature type string">string</span>
{:#quantitativescalesettings-featuremeasures-category}
{:#quantitativeScaleSettings-featureMeasures-category}








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
{:#quantitativescalesettings-featuremeasures-comparativemeasurevalue}
{:#quantitativeScaleSettings-featureMeasures-comparativeMeasureValue}








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
{:#quantitativescalesettings-featuremeasures-value}
{:#quantitativeScaleSettings-featureMeasures-value}








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
{:#quantitativescalesettings-fields}
{:#quantitativeScaleSettings-fields}








Contains property to customize the fields.











### quantitativeScaleSettings.fields.category<span class="type-signature type string">string</span>
{:#quantitativescalesettings-fields-category}
{:#quantitativeScaleSettings-fields-category}








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
{:#quantitativescalesettings-fields-comparativemeasure}
{:#quantitativeScaleSettings-fields-comparativeMeasure}








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
{:#quantitativescalesettings-fields-datasource}
{:#quantitativeScaleSettings-fields-dataSource}








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
{:#quantitativescalesettings-fields-featuremeasures}
{:#quantitativeScaleSettings-fields-featureMeasures}








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
{:#quantitativescalesettings-fields-query}
{:#quantitativeScaleSettings-fields-query}








Specifies the query for fetching the values form data source to render the bullet graph.




Default Value:
{:.param}






* null














### quantitativeScaleSettings.fields.tableName<span class="type-signature type string">string</span>
{:#quantitativescalesettings-fields-tablename}
{:#quantitativeScaleSettings-fields-tableName}








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
{:#quantitativescalesettings-interval}
{:#quantitativeScaleSettings-interval}








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
{:#quantitativescalesettings-labelsettings}
{:#quantitativeScaleSettings-labelSettings}








Contains property to customize the labels.











### quantitativeScaleSettings.labelSettings.font<span class="type-signature type object">object</span>
{:#quantitativescalesettings-labelsettings-font}
{:#quantitativeScaleSettings-labelSettings-font}








Contains property to customize the font of the labels in bullet graph.











### quantitativeScaleSettings.labelSettings.font.fontFamily<span class="type-signature type string">string</span>
{:#quantitativescalesettings-labelsettings-font-fontfamily}
{:#quantitativeScaleSettings-labelSettings-font-fontFamily}








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
{:#quantitativescalesettings-labelsettings-font-fontstyle}
{:#quantitativeScaleSettings-labelSettings-font-fontStyle}








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
{:#quantitativescalesettings-labelsettings-font-fontweight}
{:#quantitativeScaleSettings-labelSettings-font-fontWeight}








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
{:#quantitativescalesettings-labelsettings-font-opacity}
{:#quantitativeScaleSettings-labelSettings-font-opacity}








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
{:#quantitativescalesettings-labelsettings-labelplacement}
{:#quantitativeScaleSettings-labelSettings-labelPlacement}








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
{:#quantitativescalesettings-labelsettings-labelprefix}
{:#quantitativeScaleSettings-labelSettings-labelPrefix}








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
{:#quantitativescalesettings-labelsettings-labelsuffix}
{:#quantitativeScaleSettings-labelSettings-labelSuffix}








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
{:#quantitativescalesettings-labelsettings-offset}
{:#quantitativeScaleSettings-labelSettings-offset}








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
{:#quantitativescalesettings-labelsettings-position}
{:#quantitativeScaleSettings-labelSettings-position}








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
{:#quantitativescalesettings-labelsettings-size}
{:#quantitativeScaleSettings-labelSettings-size}








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
{:#quantitativescalesettings-labelsettings-stroke}
{:#quantitativeScaleSettings-labelSettings-stroke}








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
{:#quantitativescalesettings-location}
{:#quantitativeScaleSettings-location}








Contains property to customize the position of the quantitative scale











### quantitativeScaleSettings.location.x<span class="type-signature type number">number</span>
{:#quantitativescalesettings-location-x}
{:#quantitativeScaleSettings-location-x}








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
{:#quantitativescalesettings-location-y}
{:#quantitativeScaleSettings-location-y}








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
{:#quantitativescalesettings-majorticksettings}
{:#quantitativeScaleSettings-majorTickSettings}








Contains property to customize the major tick lines.











### quantitativeScaleSettings.majorTickSettings.size<span class="type-signature type number">number</span>
{:#quantitativescalesettings-majorticksettings-size}
{:#quantitativeScaleSettings-majorTickSettings-size}








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
{:#quantitativescalesettings-majorticksettings-stroke}
{:#quantitativeScaleSettings-majorTickSettings-stroke}








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
{:#quantitativescalesettings-majorticksettings-width}
{:#quantitativeScaleSettings-majorTickSettings-width}








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
{:#quantitativescalesettings-maximum}
{:#quantitativeScaleSettings-maximum}








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
{:#quantitativescalesettings-minimum}
{:#quantitativeScaleSettings-minimum}








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
{:#quantitativescalesettings-minorticksettings}
{:#quantitativeScaleSettings-minorTickSettings}








Contains property to customize the minor ticks.











### quantitativeScaleSettings.minorTickSettings.size<span class="type-signature type number">number</span>
{:#quantitativescalesettings-minorticksettings-size}
{:#quantitativeScaleSettings-minorTickSettings-size}








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
{:#quantitativescalesettings-minorticksettings-stroke}
{:#quantitativeScaleSettings-minorTickSettings-stroke}








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
{:#quantitativescalesettings-minorticksettings-width}
{:#quantitativeScaleSettings-minorTickSettings-width}








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
{:#quantitativescalesettings-minorticksperinterval}
{:#quantitativeScaleSettings-minorTicksPerInterval}








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
{:#quantitativescalesettings-tickplacement}
{:#quantitativeScaleSettings-tickPlacement}








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
{:#quantitativescalesettings-tickposition}
{:#quantitativeScaleSettings-tickPosition}








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
{:#theme}
{:#theme}








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
{:#tooltipsettings}
{:#tooltipSettings}








Contains all the properties to customize tooltip.











### tooltipSettings.captionTemplate<span class="type-signature type string">string</span>
{:#tooltipsettings-captiontemplate}
{:#tooltipSettings-captionTemplate}








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
{:#tooltipsettings-enablecaptiontooltip}
{:#tooltipSettings-enableCaptionTooltip}








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
{:#tooltipsettings-template}
{:#tooltipSettings-template}








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
{:#tooltipsettings-visible}
{:#tooltipSettings-visible}








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
{:#value}
{:#value}








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
{:#width}
{:#width}








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
{:#destroy}
{:#destroy}








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
{:#redraw}
{:#redraw}








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
{:#setcomparativemeasuresymbol}
{:#setComparativeMeasureSymbol}








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
{:#setfeaturemeasurebarvalue}
{:#setFeatureMeasureBarValue}








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
{:#drawcaption}
{:#drawCaption}








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
{:#drawcategory}
{:#drawCategory}








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
{:#drawcomparativemeasuresymbol}
{:#drawComparativeMeasureSymbol}








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
{:#drawfeaturemeasurebar}
{:#drawFeatureMeasureBar}








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
{:#drawindicator}
{:#drawIndicator}








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
{:#drawlabels}
{:#drawLabels}








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
{:#drawqualitativeranges}
{:#drawQualitativeRanges}








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
{:#load}
{:#load}








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



