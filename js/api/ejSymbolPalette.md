---
layout: post
title: ejSymbolPalette
description: API reference for ejSymbolPalette
documentation: API
platform: js
keywords: symbolpalette, ejSymbolPalette, symbol palette api, syncfusion
---

# ejSymbolPalette

The symbol palette control provides support to predefine the frequently used nodes and connectors and it allows to drag and drop those symbols to drawing area.

#### Syntax
$(element).ejSymbolPalette()

#### Example

{% highlight html %}
 
<div id="symbolpalette"></div>
<script>
//Create symbolpalette
$("#symbolpalette").ejSymbolPalette();
</script>

{% endhighlight %}

#### Requires

* module:jQuery.js
* module:ej.common.all
* module:ej.widgets.all
* module:jquery.easing.js
* module:jquery.globalize.js
* module:jsrender.js
* module:jquery.validate.js
* module:jquery.validate.unobtrusive.js

## Members

### allowDrag `Boolean`
{:#members:allowdrag}

Enable or disable the Drag function of items in the palette

#### Default Value

* true

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({allowDrag: true});
</script>

{% endhighlight %}

### cssClass `String`
{:#members:cssclass}

Used to change the style of the node

#### Default Value

* "e-symbolpalette"

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({cssClass: "e-symbolpalette"});
</script>

{% endhighlight %}

### diagramId `Object`
{:#members:diagramid}

The diagramId of the palette

#### Default Value

* null

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({diagramId: "diagram"});
</script>

{% endhighlight %}

### headerHeight `Number`
{:#members:headerheight}

Height of the palette header

#### Default Value

* 30

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({headerHeight: 30});
</script>

{% endhighlight %}

### height `Number`
{:#members:height}

The height of the palette

#### Default Value

* 400

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({height:500});
</script>

{% endhighlight %}

### paletteItemHeight `Number`
{:#members:paletteitemheight}

Height of the items in palette

#### Default Value

* 50

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({paletteItemHeight: 50});
</script>

{% endhighlight %}

### paletteItemWidth `Number`
{:#members:paletteitemwidth}

Width of the palette item

#### Default Value

* 50

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({paletteItemWidth: 50});
</script>

{% endhighlight %}

### palettes `Array`
{:#members:palettes}

Collection of palette items

#### Default Value

* null

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({palettes: palette});
</script>

{% endhighlight %}

### previewHeight `Number`
{:#members:previewheight}

Preview height of the palette items

#### Default Value

* 100

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({previewHeight: 100});
</script>

{% endhighlight %}

### previewOffset `Object`
{:#members:previewoffset}

The preview offset for the palette items

#### Default Value

* (102, 102)

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({previewOffset: {x: 102, y: 102 }});
</script>

{% endhighlight %}

### previewWidth `Number`
{:#members:previewwidth}

Preview width of the palette items

#### Default Value

* 100

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({previewWidth: 100});
</script>

{% endhighlight %}

### selectedPaletteName `Number`
{:#members:selectedpalettename}

The selectedPaletteName of the symbol palette

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({selectedPaletteName: "paletteName"});
</script>

{% endhighlight %}

### showPaletteItemText `Boolean`
{:#members:showpaletteitemtext}

Enable or disable the palette item text

#### Default Value

* true

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({showPaletteItemText: true});
</script>

{% endhighlight %}

### width `Number`
{:#members:width}

The width of the palette

#### Default Value

* 250

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({width:300});
</script>

{% endhighlight %}

## Events

### selectionChanged
{:#events:selectionchanged}

Triggers When selection is changed

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">argument</td>
			<td class="type">Object</td>
			<td class="description">args parameter from diagram</td>
		</tr>
		<tr>
			<td class="name">argument.changetype</td>
			<td class="type">String</td>
			<td class="description">return should be inserted or removed</td>
		</tr>
		<tr>
			<td class="name">argument.element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns node or connector which to be added or deleted</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// selectionChange event for diagram
$("#symbolpalette").ejSymbolPalette({
selectionChange:function (args) {}
});

{% endhighlight %}
