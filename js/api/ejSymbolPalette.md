---
layout: post
title: ejSymbolPalette
documentation: API
platform: js
metaname: 
metacontent: 
---

defined values to render symbolpalette










## $(element).ejSymbolPalette<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
//Create symbolpalette
$("#symbolpalette").ejSymbolPalette();
&lt;/script&gt;</code>
</pre>






## Requires




* module:jQuery.js


* module:ej.common.all


* module:ej.widgets.all


* module:jquery.easing.js


* module:jquery.globalize.js


* module:jsrender.js


* module:jquery.validate.js


* module:jquery.validate.unobtrusive.js




## Members








### allowDrag<span class="type-signature type boolean">Boolean</span>








Enable or disable the Drag function of items in the palette




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({allowDrag: true});
&lt;/script&gt;</code>
</pre>






### cssClass<span class="type-signature type string">String</span>








Used to change the style of the node




Default Value:
{:.param}






* "e-symbolpalette"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({cssClass: "e-symbolpalette"});
&lt;/script&gt;</code>
</pre>






### diagramId<span class="type-signature type object">Object</span>








The diagramId of the palette




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({diagramId: "diagram"});
&lt;/script&gt;</code>
</pre>






### headerHeight<span class="type-signature type number">Number</span>








Height of the palette header




Default Value:
{:.param}






* 30








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({headerHeight: 30});
&lt;/script&gt;</code>
</pre>






### height<span class="type-signature type number">Number</span>








The height of the palette




Default Value:
{:.param}






* 400








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({height:500});
&lt;/script&gt;</code>
</pre>






### paletteItemHeight<span class="type-signature type number">Number</span>








Height of the items in palette




Default Value:
{:.param}






* 50








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({paletteItemHeight: 50});
&lt;/script&gt;</code>
</pre>






### paletteItemWidth<span class="type-signature type number">Number</span>








Width of the palette item




Default Value:
{:.param}






* 50








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({paletteItemWidth: 50});
&lt;/script&gt;</code>
</pre>






### palettes<span class="type-signature type array">Array</span>








Collection of palette items




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({palettes: palette});
&lt;/script&gt;</code>
</pre>






### previewHeight<span class="type-signature type number">Number</span>








Preview height of the palette items




Default Value:
{:.param}






* 100








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({previewHeight: 100});
&lt;/script&gt;</code>
</pre>






### previewOffset<span class="type-signature type object">Object</span>








The preview offset for the palette items




Default Value:
{:.param}






* (102, 102)








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({previewOffset: {x: 102, y: 102 }});
&lt;/script&gt;</code>
</pre>






### previewWidth<span class="type-signature type number">Number</span>








Preview width of the palette items




Default Value:
{:.param}






* 100








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({previewWidth: 100});
&lt;/script&gt;</code>
</pre>






### selectedPaletteName<span class="type-signature type number">Number</span>








The selectedPaletteName of the symbol palette




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({selectedPaletteName: "paletteName"});
&lt;/script&gt;</code>
</pre>






### showPaletteItemText<span class="type-signature type boolean">Boolean</span>








Enable or disable the palette item text




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({showPaletteItemText: true});
&lt;/script&gt;</code>
</pre>






### width<span class="type-signature type number">Number</span>








The width of the palette




Default Value:
{:.param}






* 250








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="symbolpalette"&gt;&lt;/div&gt;
&lt;script&gt;
$("#symbolpalette").ejSymbolPalette({width:300});
&lt;/script&gt;</code>
</pre>




## Events








### selectionChanged








Triggers When selection is changed

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>changetype</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return should be inserted or removed</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector which to be added or deleted</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>//  selectionChange event for diagram
$("#symbolpalette").ejSymbolPalette({
selectionChange:function (args)  {}
       });</code>
</pre>



