---
layout: post
title: ejSymbolPalette
description: API reference for ejSymbolPalette
documentation: API
platform: js
keywords: symbolpalette, ejSymbolPalette, symbol palette api, syncfusion
---

# ejSymbolPalette
<ts root="datavisualization" />

The symbol palette control allows to predefine the frequently used nodes and connectors and to drag and drop those nodes/connectors to drawing area

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

Defines whether the symbols can be dragged from palette or not

#### Default Value

* true

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette( { allowDrag: false } );
</script>

{% endhighlight %}

### cssClass `String`
{:#members:cssclass}

Customizes the style of the symbol palette

#### Default Value

* "e-symbolpalette"

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({cssClass: "e-symbolpalette"});
</script>

{% endhighlight %}

### defaultSettings `Object`
{:#members:defaultsettings}

Defines the default properties of nodes and connectors

### defaultSettings.node `Object`
{:#members:defaultsettings-node}

Defines the default properties of the nodes

#### Default Value

* null

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({
	defaultSettings: { node : { fillColor:"red" } }
});
</script>

{% endhighlight %}

### defaultSettings.connector `Object`
{:#members:defaultsettings-connector}

Defines the default properties of the connectors

#### Default Value

* null

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({
	defaultSettings: { connector: { lineColor: "red" } }
});
</script>

{% endhighlight %}

### diagramId `String`
{:#members:diagramid}

Sets the Id of the diagram, over which the symbols will be dropped

#### Default Value

* null

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({ diagramId: "diagram" });
</script>

{% endhighlight %}

### headerHeight `Number`
{:#members:headerheight}

Sets the height of the palette headers

#### Default Value

* 30

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette( { headerHeight: 25 } );
</script>

{% endhighlight %}

### height `Number`
{:#members:height}

Defines the height of the symbol palette

#### Default Value

* 400

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette( { height:300 } );
</script>

{% endhighlight %}

### paletteItemHeight `Number`
{:#members:paletteitemheight}

Defines the height of the palette items

#### Default Value

* 50

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({ paletteItemHeight: 30 });
</script>

{% endhighlight %}

### paletteItemWidth `Number`
{:#members:paletteitemwidth}

Defines the width of the palette items

#### Default Value

* 50

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({ paletteItemWidth: 30 });
</script>

{% endhighlight %}

### palettes `Array`
{:#members:palettes}

An array of JSON objects, where each object represents a node/connector

#### Default Value

* []

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
	
var palette = {
		name: "Basic Shapes",
		expanded: true,
		items: [{
			name: "Rectangle", height: 40, width: 80
		}]
	};
	
$("#symbolpalette").ejSymbolPalette({
	//Initializes the palette collection
	palettes: [ palette ]
});

</script>

{% endhighlight %}

### palettes.name `string`
{:#members:palettes-name}

Defines the name of the palette

#### Default Value

* null

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
	
var palette = {
		name: "Basic Shapes",
		expanded: true,
		items: [{
			name: "Rectangle", height: 40, width: 80
		}]
	};
	
$("#symbolpalette").ejSymbolPalette({
	//Initializes the palette collection
	palettes: [ palette ]
});

</script>

{% endhighlight %}

### palettes.expanded `boolean`
{:#members:palettes-expanded}

Defines whether the palette must be in expanded state or in collapsed state

#### Default Value

* true

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
	
var palette = {
		name: "Basic Shapes",
		expanded: true,
		items: [{
			name: "Rectangle", expanded:true, height: 40, width: 80
		}]
	};
	
$("#symbolpalette").ejSymbolPalette({
	//Initializes the palette collection
	palettes: [ palette ]
});

</script>

{% endhighlight %}

### palettes.items `Array`
{:#members:palettes-items}

Defines the palette items

#### Default Value

* []

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
	
var palette = {
		name: "Basic Shapes",
		expanded: true,
		items: [{
			name: "Rectangle", height: 40, width: 80
		}]
	};
	
$("#symbolpalette").ejSymbolPalette({
	//Initializes the palette collection
	palettes: [ palette ]
});

</script>

{% endhighlight %}

### previewHeight `Number`
{:#members:previewheight}

Defines the preview height of the symbols

#### Default Value

* 100

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette( { previewHeight: 50 });
</script>

{% endhighlight %}

### previewOffset `Object`
{:#members:previewoffset}

Defines the offset value to be left between the mouse cursor and symbol previews

#### Default Value

* (110, 110)

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({previewOffset: {x: 50, y: 50}});
</script>

{% endhighlight %}

### previewWidth `Number`
{:#members:previewwidth}

Defines the width of the symbol previews

#### Default Value

* 100

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette( { previewWidth: 50 });
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

### selectionChange
{:#events:selectionchange}

Triggers when a palette item is selected or unselected

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
			<td class="name">changeType</td>
			<td class="type">String</td>
			<td class="description last">returns whether an element is selected or unselected</td>
		</tr>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description last">returns the node or connector that is selected or unselected</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// selectionChange event for symbol palette
$("#symbolpalette").ejSymbolPalette({
	selectionChange:function (args) {}
});

{% endhighlight %}
