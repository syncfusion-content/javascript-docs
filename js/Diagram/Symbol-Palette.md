---
layout: post
title: Define and add the frequently used nodes/connectors to the symbol palette
description: How to add shapes to the symbol palette and drag and drop them over the drawing area?
platform: js
control: Diagram
documentation: ug
---

# Symbol Palette

The **SymbolPalette** displays a collection of palettes. The Palette shows a set of nodes and connectors. It allows you to drag and drop the nodes and connectors into the Diagram. The Palette has a header that displays the name and also allows you to expand or collapse its items. Each node or connector in the palette is called a Palette Item.

## Create and add symbols to the Palette 

The following steps illustrate how to add palette items to symbol palette. 

### Define the palette items

You can create a palette item as a node, group, connector, lane, or phase. To create a palette item, you first need to define that element as JSON. The following code example illustrates how to define palette items.

{% highlight javascript %}

//Creates a node
var node = {
	name: "Ellipse",
	//Specifies node size
	width: 40, height: 40,
	//Specifies node offset and shape 
	offsetX: 20, offsetY: 20, shape: "ellipse",
};

//Creates a group
var group = {
	name: "group",
	//Defines the child nodes.
	children: [{
		name: "child1",
		width: 40, height: 40,
		offsetX: 20, offsetY: 20, borderWidth: 1
	},{
		name: "child2",
		width: 40, height: 40,
		offsetX: 40, offsetY: 40,
		borderWidth: 1,
	}],
	width: 40, 
	height: 40,
};

//Creates a connector 
var connector = {
	name: "Line",
	segments: [{ type: "orthogonal" }],
	//Defines the source and target points
	sourcePoint: { x: 0, y: 0 },
	targetPoint: { x: 40, y: 40 },
	//Defines the target decorator properties
	targetDecorator: { shape: "arrow" },
};

//Creates a lane 
var lane = {
	name: "lane", 
	header: {
		width: 50, 
		height: 50, 
		fillColor: "#C7D4DF"
	},
	fillColor: "#f5f5f5",
	//Specifies size for the lane 
	height: 60, 
	width: 140,
	//Specifies offset for the lane 
	offsetX: 70, 
	offsetY: 30,
	//Specifies orientation as horizontal/vertical
	orientation: "horizontal", 
	isLane: true
};

//Creates a phase
var phase = {
	name: "verticalPhase",
	type: "phase",
	// Defines the style of the phase
	lineWidth: 1, 
	lineDashArray: "3,3",
	lineColor: "#606060",
	//Defines the orientation of the phase
	orientation: "vertical", 
} 

{% endhighlight %}

### Initialize a palette with palette items

To initialize a palette, define a JSON object with the property `name` that is displayed as the header text of palette. The palette items need to be defined and added to the `items` collection of the palette. The `expanded` property of palette allows to expand/collapse its palette items. 
The following code example illustrates how to define a palette with items that are defined in the previous section. 

{% highlight javascript %}

//Defines the JSON to create a palette
var palette = 
{
	//Sets the name of the palette
	name: "Basic Shapes", 
	//Sets whether the palette expands/collapse its children
	expanded: true,
	//Adds the palette items to palette
	items: [node, group, connector, lane, phase]
};

{% endhighlight %}

### Add the palettes to SymbolPalette

You can add any number of palettes to the `palettes` collection of the symbol palette. The following example illustrates how to define symbol palette with a palette object that is defined in the previous step.

{% highlight javascript %}

//Initializes the symbol palette
$("#symbolpalette").ejSymbolPalette({ 
//Defines the palette collection 
palettes: [
	palette
],
//Specifies the symbol palette size
height: "100%", 
width: "100%"
});

{% endhighlight %}

The following image shows the symbol palette with multiple palette Items.

![](/js/Diagram/Symbol-Palette_images/Symbol-Palette_img3.png)

## Customize the size of palette items

You can customize the size of the individual palette items. The `paletteItem` property of node enables you to define the size, preview size of the symbol items. The following code example illustrates how to change the size of a palette item.

{% highlight javascript %}

$("#symbolpalette").ejSymbolPalette({
	//Defines the palette collection 
	palettes: [{
		name: "Basic Shapes",
		expanded: true,
		items: [{
			name: "Rectangle",
			height: 40,
			width: 80,
			//Specifies the size of palette Item 
			paletteItem: {
				enableScale: true,
				//Defines the size of the palette item
				width: 50,
				height: 50,
				//Defines the preview size of the palette item
				previewWidth: 100,
				previewHeight: 100,
				margin: {
					left: 20,
					right: 20,
					top: 20,
					bottom: 20
				}
			}
		}]
	}],

	//Specifies the default size to render palette items
	paletteItemWidth: 50,
	paletteItemHeight: 50,
	//Specifies the default palette item preview size
	previewWidth: 100,
	previewHeight: 100,
});

{% endhighlight %}

Palette item size is set based on the precedence flow given in the following table.

| Palette Item | Rendering Size | Preview Size |
|---|---|---|
| Precedence - Width | paletteItem.width > model.paletteItemWidth > node.width | paletteItem.previewWidth > model.previewWidth > node.width |
| Precedence - Height | paletteItem.height > model.paletteItem.Height > node.height | paletteItem.previewHeight > model.previewHeight > node.height |

Palette item size can be based on the actual size of the node, regardless of the precedence. 

The `enableScale` property of the palette item enables you to customize the size of the item regardless of the precedence. The following code example illustrates how to customize the palette item size.

{% highlight javascript %}

$("#symbolpalette").ejSymbolPalette({
	palettes: [{
		name: "Basic Shapes",
		expanded: true,
		items: [{
			name: "Rectangle",
			height: 40,
			width: 80,
			//Specifies the size of palette Item 
			paletteItem: {
				// Enables to fit the content into the specified palette item size
				enableScale: true
				// When it is set as false, the element is rendered with actual node size
			}
		}]
	}]
});

{% endhighlight %}

![](/js/Diagram/Symbol-Palette_images/Symbol-Palette_img1.png)

![](/js/Diagram/Symbol-Palette_images/Symbol-Palette_img2.png)

## Appearance 

You can show/hide the palette item texts by using the `showPaletteItemText` property of symbol palette. The following code illustrates how to customize the appearance of the symbol Palette.

{% highlight javascript %}

// Initializes symbol palette
$("#palette").ejSymbolPalette({
	palettes: palettes,
	diagramId: "DiagramContent",
	height: "100%",
	width: "100%",
	paletteItemWidth: 45,
	paletteItemHeight: 45,

	//Specifies whether palette item text should be visible or not
	showPaletteItemText: true,

	headerHeight: 30,
	selectedPaletteName: "Basic Shapes"
});

{% endhighlight %}
To explore the properties of symbol palette, refer to [Symbol Palette Properties](/js/api/ejsymbolpalette#members "Symbol Palette Properties").

## Drop nodes into diagram 

The Diagram provides support for adding nodes and connectors through the Symbol Palette. To add a node to the Diagram, drag the desired symbol from the SymbolPalette to the drawing area and release the pointer.
The `diagramId` property of symbol palette allows to define the Diagram over which the symbol items can be dragged and dropped. The following code example illustrates how to relate the symbol palette with the Diagram.

{% highlight javascript %}

//Relates Diagram to symbol palette
$("#symbolpalette").ejSymbolPalette({
	//Specifies the diagramId
	diagramId: "diagram",
});

{% endhighlight %}
