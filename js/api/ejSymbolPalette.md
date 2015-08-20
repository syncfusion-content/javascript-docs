---
layout: post
title: ejSymbolPalette
documentation: API
platform: js
metaname: 
metacontent: 
---

defined values to render symbolpalette










$(element).ejSymbolPalette<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div id="symbolpalette"></div>
<script>
//Create symbolpalette
$("#symbolpalette").ejSymbolPalette();
</script>{% endhighlight %}







Requires
{:.require}




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
{:#members:allowdrag}








Enable or disable the Drag function of items in the palette




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({allowDrag: true});
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}








Used to change the style of the node




Default Value:
{:.param}






* "e-symbolpalette"








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({cssClass: "e-symbolpalette"});
</script>{% endhighlight %}







### diagramId<span class="type-signature type object">Object</span>
{:#members:diagramid}








The diagramId of the palette




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({diagramId: "diagram"});
</script>{% endhighlight %}







### headerHeight<span class="type-signature type number">Number</span>
{:#members:headerheight}








Height of the palette header




Default Value:
{:.param}






* 30








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({headerHeight: 30});
</script>{% endhighlight %}







### height<span class="type-signature type number">Number</span>
{:#members:height}








The height of the palette




Default Value:
{:.param}






* 400








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({height:500});
</script>{% endhighlight %}







### paletteItemHeight<span class="type-signature type number">Number</span>
{:#members:paletteitemheight}








Height of the items in palette




Default Value:
{:.param}






* 50








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({paletteItemHeight: 50});
</script>{% endhighlight %}







### paletteItemWidth<span class="type-signature type number">Number</span>
{:#members:paletteitemwidth}








Width of the palette item




Default Value:
{:.param}






* 50








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({paletteItemWidth: 50});
</script>{% endhighlight %}







### palettes<span class="type-signature type array">Array</span>
{:#members:palettes}








Collection of palette items




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({palettes: palette});
</script>{% endhighlight %}







### previewHeight<span class="type-signature type number">Number</span>
{:#members:previewheight}








Preview height of the palette items




Default Value:
{:.param}






* 100








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({previewHeight: 100});
</script>{% endhighlight %}







### previewOffset<span class="type-signature type object">Object</span>
{:#members:previewoffset}








The preview offset for the palette items




Default Value:
{:.param}






* (102, 102)








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({previewOffset: {x: 102, y: 102 }});
</script>{% endhighlight %}







### previewWidth<span class="type-signature type number">Number</span>
{:#members:previewwidth}








Preview width of the palette items




Default Value:
{:.param}






* 100








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({previewWidth: 100});
</script>{% endhighlight %}







### selectedPaletteName<span class="type-signature type number">Number</span>
{:#members:selectedpalettename}








The selectedPaletteName of the symbol palette




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({selectedPaletteName: "paletteName"});
</script>{% endhighlight %}







### showPaletteItemText<span class="type-signature type boolean">Boolean</span>
{:#members:showpaletteitemtext}








Enable or disable the palette item text




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({showPaletteItemText: true});
</script>{% endhighlight %}







### width<span class="type-signature type number">Number</span>
{:#members:width}








The width of the palette




Default Value:
{:.param}






* 250








Example
{:.example}


{% highlight html %}
<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({width:300});
</script>{% endhighlight %}





## Events








### selectionChanged
{:#events:selectionchanged}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
changetype{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return should be inserted or removed</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
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


{% highlight html %}
//  selectionChange event for diagram
$("#symbolpalette").ejSymbolPalette({
selectionChange:function (args)  {}
       });{% endhighlight %}




