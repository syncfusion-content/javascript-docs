---
layout: post
title: ejRangeNavigator
documentation: API
platform: js
metaname: 
metacontent: 
---

The rangenavigator can be easily configured to the DOM element, such as div. you can create a rangenavigator with a highly customizable look and feel.










## $(element).ejRangeNavigator<span class="signature">(options, options)</span>







<table class="params">
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
<td class="description last">settings for rangenavigator</td>
</tr>
<tr>
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for rangenavigator</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create RangeNavigator
$('#container').RangeNavigator();       
&lt;/script&gt;</code>
</pre>






## Requires




* module:jQuery


* module:jquery.globalize.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.chart.js


* module:ej.rangenavigator.js




## Members








### allowSnapping<span class="type-signature type boolean">boolean</span>








Toggles the placement of slider exactly on the place it left or on the nearest interval.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   allowSnapping: true;
   });
&lt;/script&gt;  </code>
</pre>






### dataSource<span class="type-signature type object">object</span>








Specifies the data source for range navigator.





Example
{:.example}

<pre class="prettyprint">
<code>     $("#container").ejRangeNavigator({
   dataSource:"data1", 
    xName: "X", 
    yName: "Y"
   });</code>
</pre>






### enableAutoResizing<span class="type-signature type boolean">boolean</span>








Sets a value whether to make the range navigator responsive on resize.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   enableAutoResizing: true;
   });
&lt;/script&gt;  </code>
</pre>






### enableDeferredUpdate<span class="type-signature type boolean">boolean</span>








Toggles the redrawing of chart on moving the sliders.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   enableDeferredUpdate:false,
   });
&lt;/script&gt;  </code>
</pre>






### enableRTL<span class="type-signature type boolean">boolean</span>








Toggles the direction of rendering the range navigator control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
  enableRTL: true,
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings<span class="type-signature type object">object</span>








Options for customizing the labels colors, font, style, size, horizontalAlignment and opacity.











### labelSettings.higherLevel<span class="type-signature type object">object</span>








Options for customizing the higher level labels in range navigator.











### labelSettings.higherLevel.border<span class="type-signature type object">object</span>








Options for customizing the border of grid lines in higher level.











### labelSettings.higherLevel.border.color<span class="type-signature type string">string</span>








Specifies the border color of grid lines.




Default Value:
{:.param}






* "transparent"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
  labelSettings:{higherLevel:{ border :{color:"#ff0000"}}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.higherLevel.border.width<span class="type-signature type string">string</span>








Specifies the border width of grid lines.




Default Value:
{:.param}






* "0.5"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ border :{width:1}}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.higherLevel.fill<span class="type-signature type string">string</span>








Specifies the fill color of higher level labels.




Default Value:
{:.param}






* "transparent"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ fill:"days"}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.higherLevel.gridLineStyle<span class="type-signature type object">object</span>








Options for customizing the grid line colors, width, dashArray, border.











### labelSettings.higherLevel.gridLineStyle.color<span class="type-signature type string">string</span>








Specifies the color of grid lines in higher level.




Default Value:
{:.param}






* "#B5B5B5"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ gridLineStyle :{color:"#ff0000"}}},
   });</code>
</pre>






### labelSettings.higherLevel.gridLineStyle.dashArray<span class="type-signature type string">string</span>








Specifies the dashArray of grid lines in higher level.




Default Value:
{:.param}






* "20 5 0"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ gridLineStyle :{dashArray:"20 10 5"}}},
   });
&lt;/script&gt; </code>
</pre>






### labelSettings.higherLevel.gridLineStyle.width<span class="type-signature type string">string</span>








Specifies the width of grid lines in higher level.




Default Value:
{:.param}






* "#B5B5B5"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ gridLineStyle :{width:1}}},
   });
&lt;/script&gt; </code>
</pre>






### labelSettings.higherLevel.intervalType<span class="type-signature type enum">enum</span>








Specifies the intervalType for higher level labels. See <a href="global.html#IntervalType">IntervalType</a>




Default Value:
{:.param}






* "years"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ intervalType:"days"}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.higherLevel.labelPlacement<span class="type-signature type enum">enum</span>








Specifies the position of the labels to render either inside or outside of plot area. See <a href="global.html#LabelPlacement">LabelPlacement</a>




Default Value:
{:.param}






* "outside"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ labelPlacement:"inside"}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.higherLevel.position<span class="type-signature type enum">enum</span>








Specifies the position of the labels in higher level.See <a href="global.html#Position">Position</a>




Default Value:
{:.param}






* "top"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ position:"bottom"}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.higherLevel.style<span class="type-signature type object">object</span>








Options for customizing the style of higher level labels.











### labelSettings.higherLevel.style.font<span class="type-signature type object">object</span>








Options for customizing the font properties.











### labelSettings.higherLevel.style.font.color<span class="type-signature type string">string</span>








Specifies the label font color. Labels render with the specified font color.




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{color: "red"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.higherLevel.style.font.fontFamily<span class="type-signature type string">string</span>








Specifies the label font family. Labels render with the specified font family.




Default Value:
{:.param}






* "Segoe UI"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{fontFamily: "Algerian"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.higherLevel.style.font.fontStyle<span class="type-signature type string">string</span>








Specifies the label font style. Labels render with the specified font style.




Default Value:
{:.param}






* "Normal"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{fontStyle: "Italic"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.higherLevel.style.font.fontWeight<span class="type-signature type string">string</span>








Specifies the label font weight. Labels render with the specified font weight.




Default Value:
{:.param}






* "regular"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{fontWeight: "regular"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.higherLevel.style.font.opacity<span class="type-signature type string">string</span>








Specifies the label opacity. Labels render with the specified opacity.




Default Value:
{:.param}






* "12px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{opacity: "14px"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.higherLevel.style.font.size<span class="type-signature type string">string</span>








Specifies the label font size. Labels render with the specified font size.




Default Value:
{:.param}






* "12px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{size: "14px"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.higherLevel.style.horizontalAlignment<span class="type-signature type string">string</span>








Specifies the horizontal text alignment of the text in label.




Default Value:
{:.param}






* "middle"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{horizontalAlignment: "left"}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.higherLevel.visible<span class="type-signature type boolean">boolean</span>








Toggles the visibility of higher level labels.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ visible:false}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.lowerLevel<span class="type-signature type object">object</span>








Options for customizing the labels in lower level.











### labelSettings.lowerLevel.border<span class="type-signature type object">object</span>








Options for customizing the border of grid lines in lower level.











### labelSettings.lowerLevel.border.color<span class="type-signature type string">string</span>








Specifies the border color of grid lines.




Default Value:
{:.param}






* "transparent"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ border :{color:"#ff0000"}}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.lowerLevel.border.width<span class="type-signature type string">string</span>








Specifies the border width of grid lines.




Default Value:
{:.param}






* "0.5"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ border :{width:1}}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.lowerLevel.fill<span class="type-signature type string">string</span>








Specifies the fill color of labels in lower level.




Default Value:
{:.param}






* "transparent"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
  labelSettings:{lowerLevel:{ fill:"days"}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.lowerLevel.gridLineStyle<span class="type-signature type object">object</span>








Options for customizing the grid lines in lower level.











### labelSettings.lowerLevel.gridLineStyle.color<span class="type-signature type string">string</span>








Specifies the color of grid lines in lower level.




Default Value:
{:.param}






* "#B5B5B5"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ gridLineStyle :{color:"#ff0000"}}},
   });
&lt;/script&gt; </code>
</pre>






### labelSettings.lowerLevel.gridLineStyle.dashArray<span class="type-signature type string">string</span>








Specifies the dashArray of gridLines in lowerLevel.




Default Value:
{:.param}






* "20 5 0"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   lowerLevel:{ gridLineStyle :{dashArray:"20 10 5"}}},
   });
&lt;/script&gt; </code>
</pre>






### labelSettings.lowerLevel.gridLineStyle.width<span class="type-signature type string">string</span>








Specifies the width of grid lines in lower level.




Default Value:
{:.param}






* "#B5B5B5"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ gridLineStyle :{width:1}}},
   });
&lt;/script&gt; </code>
</pre>






### labelSettings.lowerLevel.intervalTypes<span class="type-signature type enum">enum</span>








Specifies the intervalType of the labels in lower level.See <a href="global.html#IntervalType">IntervalType</a>




Default Value:
{:.param}






* "years"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ intervalType:"days"}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.lowerLevel.labelPlacement<span class="type-signature type enum">enum</span>








Specifies the position of the labels to render either inside or outside of plot area. See <a href="global.html#LabelPlacement">LabelPlacement</a>




Default Value:
{:.param}






* "outside"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ labelPlacement:"inside"}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.lowerLevel.position<span class="type-signature type enum">enum</span>








Specifies the position of the labels in lower level.See <a href="global.html#Position">Position</a>




Default Value:
{:.param}






* "bottom"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ position:"bottom"}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.lowerLevel.style<span class="type-signature type object">object</span>








Options for customizing the style of labels.











### labelSettings.lowerLevel.style.font<span class="type-signature type object">object</span>








Options for customizing the font of labels.











### labelSettings.lowerLevel.style.font.color<span class="type-signature type string">string</span>








Specifies the color of labels. Label text render in this specified color.




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{color: "red"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.lowerLevel.style.font.fontFamily<span class="type-signature type string">string</span>








Specifies the font family of labels. Label text render in this specified font family.




Default Value:
{:.param}






* "Segoe UI"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{fontFamily: "Algerian"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.lowerLevel.style.font.fontStyle<span class="type-signature type string">string</span>








Specifies the font style of labels. Label text render in this specified font style.




Default Value:
{:.param}






* "Normal"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{fontStyle: "Italic"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.lowerLevel.style.font.fontWeight<span class="type-signature type string">string</span>








Specifies the font weight of labels. Label text render in this specified font weight.




Default Value:
{:.param}






* "regular"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{fontWeight: "regular"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.lowerLevel.style.font.opacity<span class="type-signature type string">string</span>








Specifies the opacity of labels. Label text render in this specified opacity.




Default Value:
{:.param}






* "12px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{opacity: "14px"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.lowerLevel.style.font.size<span class="type-signature type string">string</span>








Specifies the size of labels. Label text render in this specified size.




Default Value:
{:.param}






* "12px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{size: "14px"}}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.lowerLevel.style.horizontalAlignment<span class="type-signature type string">string</span>








Specifies the horizontal text alignment of the text in label.




Default Value:
{:.param}






* "middle"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{horizontalAlignment: "left"}}},
   });
&lt;/script&gt;  </code>
</pre>






### labelSettings.lowerLevel.visible<span class="type-signature type boolean">boolean</span>








Toggles the visibility of labels in lower level.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ visible:false}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.style<span class="type-signature type object">object</span>








Options for customizing the style of labels in range navigator.











### labelSettings.style.font<span class="type-signature type object">object</span>








Options for customizing the font of labels in range navigator.











### labelSettings.style.font.color<span class="type-signature type string">string</span>








Specifies the label color. This color is applied to the labels in range navigator.




Default Value:
{:.param}






* "#FFFFFF"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{color:"#ff0000"}}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.style.font.family<span class="type-signature type string">string</span>








Specifies the label font family. Labels render with the specified font family.




Default Value:
{:.param}






* "Segoe UI"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{family:"Arial"}}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.style.font.opacity<span class="type-signature type number">number</span>








Specifies the label font opacity. Labels render with the specified font opacity.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{opacity:0.5}}}
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.style.font.size<span class="type-signature type string">string</span>








Specifies the label font size. Labels render with the specified font size.




Default Value:
{:.param}






* "1px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{size:"12px"}}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.style.font.style<span class="type-signature type enum">enum</span>








Specifies the label font style. Labels render with the specified font style..See <a href="global.html#FontStyle">FontStyle</a>




Default Value:
{:.param}






* "Normal"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{style:"Noraml"}}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.style.font.weight<span class="type-signature type enum">enum</span>








Specifies the label font weight. Labels render with the specified font weight. See <a href="global.html#FontWeight">FontWeight</a>




Default Value:
{:.param}






* "regular"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{weight:"Regular"}}},
   });
&lt;/script&gt;</code>
</pre>






### labelSettings.style.horizontalAlignment<span class="type-signature type enum">enum</span>








Specifies the horizontalAlignment of the label in RangeNavigator. See <a href="global.html#HorizontalAlignment">HorizontalAlignment</a>




Default Value:
{:.param}






* "middle"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
  labelSettings:{style:{ horizontalAlignment:"middle"}},
   });
&lt;/script&gt;</code>
</pre>






### locale<span class="type-signature type string">string</span>








This property is to specify the localization of range navigator.




Default Value:
{:.param}






* "en-US"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   locale: "en-US",
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings<span class="type-signature type object">object</span>








Options for customizing the range navigator.











### navigatorStyleSettings.background<span class="type-signature type string">string</span>








Specifies the background color of RangeNavigator.




Default Value:
{:.param}






* "#dddddd"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ background:"#ff0000"},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.border<span class="type-signature type object">object</span>








Options for customizing the border color and width of range navigator.











### navigatorStyleSettings.border.color<span class="type-signature type string">string</span>








Specifies the border color of range navigator.




Default Value:
{:.param}






* "transparent"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ border:{color:"#ff0000"}},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.border.dashArray<span class="type-signature type string">string</span>








Specifies the dash array of range navigator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ border:{dashArray:"2,3"}},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.border.width<span class="type-signature type number">number</span>








Specifies the border width of range navigator.




Default Value:
{:.param}






* 0.5








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ border:{width:1}},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.leftThumbTemplate<span class="type-signature type string">string</span>








Specifies the left side thumb template in range navigator we can give either div id or html string




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ leftThumbTemplate:"item"},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.majorGridLineStyle<span class="type-signature type object">object</span>








Options for customizing the major grid lines.











### navigatorStyleSettings.majorGridLineStyle.color<span class="type-signature type string">string</span>








Specifies the color of major grid lines in RangeNavigator.




Default Value:
{:.param}






* "#B5B5B5"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ majorGridLineStyle:{color:"#ff0000"}},
   });
&lt;/script&gt; </code>
</pre>






### navigatorStyleSettings.majorGridLineStyle.visible<span class="type-signature type boolean">boolean</span>








Toggles the visibility of major grid lines.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ majorGridLineStyle:{visible:false}},
   });
&lt;/script&gt; </code>
</pre>






### navigatorStyleSettings.minorGridLineStyle<span class="type-signature type object">object</span>








Options for customizing the minor grid lines.











### navigatorStyleSettings.minorGridLineStyle.color<span class="type-signature type string">string</span>








Specifies the color of minor grid lines in RangeNavigator.




Default Value:
{:.param}






* "#B5B5B5"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Gets or sets color of majorGridLines in RangeNavigator, after initialization:
        //Gets the color of majorGridLines in RangeNavigator
        $("#container").ejRangeNavigator("option", "navigatorStyleSettings.majorGridLineStyle.color");
                      
        //Sets the color of majorGridLines in RangeNavigator</code>
</pre>






### navigatorStyleSettings.minorGridLineStyle.visible<span class="type-signature type boolean">boolean</span>








Toggles the visibility of minor grid lines.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ majorGridLineStyle:{visible:false}},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.opacity<span class="type-signature type number">number</span>








Specifies the opacity of RangeNavigator.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ opacity:0.5},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.rightThumbTemplate<span class="type-signature type string">string</span>








Specifies the right side thumb template in range navigator we can give either div id or html string




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ rightThumbTemplate:"item"},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.selectedRegionColor<span class="type-signature type string">string</span>








Specifies the color of the selected region in range navigator.




Default Value:
{:.param}






* "#EFEFEF"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ selectedRegionColor:"#ff0000"}},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.selectedRegionOpacity<span class="type-signature type number">number</span>








Specifies the opacity of Selected Region.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ selectedRegionOpacity:0.5},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.thumbColor<span class="type-signature type string">string</span>








Specifies the color of the thumb in range navigator.




Default Value:
{:.param}






* "#2382C3"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ thumbColor:"#ff0000"},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.thumbRadius<span class="type-signature type number">number</span>








Specifies the radius of the thumb in range navigator.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ thumbRadius:15},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.thumbStroke<span class="type-signature type string">string</span>








Specifies the stroke color of the thumb in range navigator.




Default Value:
{:.param}






* "#303030"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ thumbStroke:"#ff0000"},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.unselectedRegionColor<span class="type-signature type string">string</span>








Specifies the color of the unselected region in range navigator.




Default Value:
{:.param}






* "#5EABDE"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ unselectedRegionColor:"#ff0000"},
   });
&lt;/script&gt;  </code>
</pre>






### navigatorStyleSettings.unselectedRegionOpacity<span class="type-signature type number">number</span>








Specifies the opacity of Unselected Region.




Default Value:
{:.param}






* 0.3








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ unselectedRegionOpacity:0.5},
   });
&lt;/script&gt;  </code>
</pre>






### padding<span class="type-signature type string">string</span>








Padding specifies the gap between the container and the range navigator.




Default Value:
{:.param}






* "0"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   padding: "15";
   });
&lt;/script&gt;  </code>
</pre>






### rangePadding<span class="type-signature type enum">enum</span>








If the range is not given explicitly, range will be calculated automatically. You can customize the automatic range calculation using rangePadding. See <a href="global.html#RangePadding">RangePadding</a>




Default Value:
{:.param}






* "none"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
  rangePadding: "normal",
   });
&lt;/script&gt;  </code>
</pre>






### rangeSettings<span class="type-signature type object">object</span>








Options for customizing the starting and ending ranges.











### rangeSettings.end<span class="type-signature type string">string</span>








Specifies the ending range of range navigator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   rangeSettings:{end:"01/05/1993"}
   });
&lt;/script&gt;  </code>
</pre>






### rangeSettings.start<span class="type-signature type string">string</span>








Specifies the starting range of range navigator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   rangeSettings:{start:"01/05/1993"},
   });</code>
</pre>






### selectedData








selectedData is for getting the data when the "rangeChanged" event trigger from clientside.











### selectedRangeSettings<span class="type-signature type object">object</span>








Options for customizing the start and end range values.











### selectedRangeSettings.end<span class="type-signature type string">string</span>








Specifies the ending range of range navigator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   selectedRangeSettings:{end:"01/05/1993"},
   });
&lt;/script&gt;  </code>
</pre>






### selectedRangeSettings.start<span class="type-signature type string">string</span>








Specifies the starting range of range navigator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
  selectedRangeSettings:{start:"01/05/1992"},
   });
&lt;/script&gt;  </code>
</pre>






### sizeSettings<span class="type-signature type object">object</span>








Contains property to customize the hight and width of range navigator.











### sizeSettings.height<span class="type-signature type string">string</span>








Specifies height of the range navigator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>                             
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   sizeSettings: { height : "130" },
   });
&lt;/script&gt;  </code>
</pre>






### sizeSettings.width<span class="type-signature type string">string</span>








Specifies width of the range navigator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   sizeSettings: { width : "900" },
   });
&lt;/script&gt;  </code>
</pre>






### theme<span class="type-signature type string">string</span>








By specifying this property the user can change the theme of the range navigator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   theme: "flatdark";
   });
&lt;/script&gt;  </code>
</pre>






### tooltipSettings<span class="type-signature type object">object</span>








Options for customizing the tooltip in range navigator.





Example
{:.example}

<pre class="prettyprint">
<code>     $("#container").ejRangeNavigator({
   tooltipSettings: { visible: true, labelFormat: "MMM/dd/yyyy", tooltipDisplayMode: "always", tooltipDisplayMode: "always" },
   });</code>
</pre>






### tooltipSettings.backgroundColor<span class="type-signature type string">string</span>








Specifies the background color of tooltip.




Default Value:
{:.param}






* "#303030"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   tooltipSettings:{backgroundColor: "#303030"},
   });
&lt;/script&gt;  </code>
</pre>






### tooltipSettings.font<span class="type-signature type object">object</span>








Options for customizing the font in tooltip.











### tooltipSettings.font.color<span class="type-signature type string">string</span>








Specifies the color of text in tooltip. Tooltip text render in the specified color.




Default Value:
{:.param}






* "#FFFFFF"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   tooltipSettings:{font:{color : "FFFFFF"}},
   });
&lt;/script&gt;</code>
</pre>






### tooltipSettings.font.family<span class="type-signature type string">string</span>








Specifies the font family of text in tooltip. Tooltip text render in the specified font family.




Default Value:
{:.param}






* "Segoe UI"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
                tooltipSettings:{font:{family:"Arial"}}
                }); 
&lt;/script&gt;</code>
</pre>






### tooltipSettings.font.fontStyle<span class="type-signature type string">string</span>








Specifies the font style of text in tooltip. Tooltip text render in the specified font style.




Default Value:
{:.param}






* ej.datavisualization.RangeNavigator.fontStyle.Normal








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   tooltipSettings:{font:{fontStyle:"Normal"}}
   });
&lt;/script&gt;</code>
</pre>






### tooltipSettings.font.opacity<span class="type-signature type number">number</span>








Specifies the opacity of text in tooltip. Tooltip text render in the specified opacity.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
  tooltipSettings:{ font:{opacity:0.5}}
   });
&lt;/script&gt;</code>
</pre>






### tooltipSettings.font.size<span class="type-signature type string">string</span>








Specifies the size of text in tooltip. Tooltip text render in the specified size.




Default Value:
{:.param}






* "10px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   tooltipSettings:{font:{size:"12px"}},
   });
&lt;/script&gt;</code>
</pre>






### tooltipSettings.font.weight<span class="type-signature type string">string</span>








Specifies the weight of text in tooltip. Tooltip text render in the specified weight.




Default Value:
{:.param}






* ej.datavisualization.RangeNavigator.weight.Regular








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   tooltipSettings:{ font:{weight:"regular"}},
   });
&lt;/script&gt;</code>
</pre>






### tooltipSettings.labelFormat<span class="type-signature type string">string</span>








Specifies the format of text to be displayed in tooltip.




Default Value:
{:.param}






* "MM/dd/yyyy"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   tooltipSettings: { labelFormat: "MM/dd/yyyy"}
   });
&lt;/script&gt;  </code>
</pre>






### tooltipSettings.tooltipDisplayMode<span class="type-signature type string">string</span>








Specifies the mode of displaying the tooltip. Neither to display the tooltip always nor on demand.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   tooltipSettings:{tooltipDisplayMode: "always"},
   });
&lt;/script&gt;  </code>
</pre>






### tooltipSettings.visible<span class="type-signature type boolean">boolean</span>








Toggles the visibility of tooltip.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   tooltipSettings:{visible: true}
   });
&lt;/script&gt;  </code>
</pre>






### valueAxisSettings<span class="type-signature type object">object</span>








Options for configuring minor grid lines, major grid lines, axis line of axis.











### valueAxisSettings.axisLine<span class="type-signature type object">object</span>








Options for customizing the axis line.











### valueAxisSettings.axisLine.visible<span class="type-signature type string">string</span>








Toggles the visibility of axis line.




Default Value:
{:.param}






* "none"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   valueAxisSettings:{axisLine: {visible: true}}
   });
&lt;/script&gt;  </code>
</pre>






### valueAxisSettings.font<span class="type-signature type object">object</span>








Options for customizing the font of the axis.











### valueAxisSettings.font.size<span class="type-signature type string">string</span>








Text in axis render with the specified size.




Default Value:
{:.param}






* "0px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   valueAxisSettings:{font: {size: '12px'}}
   });
&lt;/script&gt;  </code>
</pre>






### valueAxisSettings.majorGridLines<span class="type-signature type object">object</span>








Options for customizing the major grid lines.











### valueAxisSettings.majorGridLines.visible<span class="type-signature type boolean">boolean</span>








Toggles the visibility of major grid lines.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   valueAxisSettings:{majorGridLines: {visible: true}}
   });
&lt;/script&gt;  </code>
</pre>






### valueAxisSettings.majorTickLines<span class="type-signature type object">object</span>








Options for customizing the major tick lines in axis.











### valueAxisSettings.majorTickLines.size<span class="type-signature type number">number</span>








Specifies the size of the majorTickLines in RangeNavigator




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   valueAxisSettings:{majorTickLines: {size: 3}}
   });
&lt;/script&gt;  </code>
</pre>






### valueAxisSettings.majorTickLines.visible<span class="type-signature type boolean">boolean</span>








Toggles the visibility of major tick lines.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   valueAxisSettings:{majorTickLines: {visible: false}}
   });
&lt;/script&gt;  </code>
</pre>






### valueAxisSettings.majorTickLines.width<span class="type-signature type number">number</span>








Specifies width of the major tick lines.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   valueAxisSettings:{majorTickLines: {width: 3}}
   });
&lt;/script&gt;  </code>
</pre>






### valueAxisSettings.rangePadding<span class="type-signature type string">string</span>








If the range is not given explicitly, range will be calculated automatically. You can customize the automatic range calculation using rangePadding.




Default Value:
{:.param}






* "none"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   valueAxisSettings:{rangePadding: "normal"},
   });
&lt;/script&gt;  </code>
</pre>






### valueAxisSettings.visible<span class="type-signature type boolean">boolean</span>








Toggles the visibility of axis in range navigator.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   valueAxisSettings:{visble: true}
   });
&lt;/script&gt;  </code>
</pre>






### valueType<span class="type-signature type enum">enum</span>








You can plot data of type date time or numeric. This property determines the type of data that this axis will handle. See <a href="global.html#ValueType">ValueType</a>




Default Value:
{:.param}






* "datetime"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   valueType: "numeric",
   });
&lt;/script&gt;  </code>
</pre>






### xName<span class="type-signature type object">object</span>








Specifies the xName for dataSource. This is used to take the x values from dataSource





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   dataSource:"data1", 
   xName: "X"
   });
&lt;/script&gt; </code>
</pre>






### yName<span class="type-signature type object">object</span>








Specifies the yName for dataSource. This is used to take the y values from dataSource





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   dataSource:"data1", 
   yName: "Y"
   });
&lt;/script&gt; </code>
</pre>






### zoomSettings.zoomFactor<span class="type-signature type string">string</span>








This property determines the factor by which the axis is scaled. Value must be specified between 0 and 1.




Default Value:
{:.param}






* "1"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
                         zoomFactor:"1"
   });
&lt;/script&gt;  </code>
</pre>






### zoomSettings.zoomPosition<span class="type-signature type string">string</span>








This property determines the starting position of the zoomed axis. Value must be specified between 0 and 1.




Default Value:
{:.param}






* "0"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="RangeNavigator"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#container").ejRangeNavigator({
   zoomPosition:"0",
   });
&lt;/script&gt;  </code>
</pre>




## Methods








### _destroy<span class="signature">()</span>








destroy the RangeNavigator widget





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Destroy RangeNavigator
var obj = $("#container").data("ejRangeNavigator");
obj.destroy(); // destroy the RangeNavigator
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#container").ejRangeNavigator("destroy");    
&lt;/script&gt;</code>
</pre>




## Events








### load








Fires on load of range navigator.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from RangeNavigator</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the RangeNavigator model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//load event for chart
$("#container").ejRangeNavigator({
   load: function (args) {}
});</code>
</pre>






### loaded








Fires after range navigator is loaded.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from RangeNavigator</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the RangeNavigator model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//loaded event for chart
$("#container").ejRangeNavigator({
   loaded: function (args) {}
});</code>
</pre>






### rangeChanged








Fires on changing the range of range navigator.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from RangeNavigator</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the RangeNavigator model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
//rangeChanged event for chart
$("#container").ejRangeNavigator({
   rangeChanged: function (args) {}
});</code>
</pre>



