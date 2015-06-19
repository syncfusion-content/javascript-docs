---
layout: post
title: Symbol-Palette
description: symbol palette
platform: js
control: Diagram
documentation: ug
---

# Symbol Palette

The **SymbolPalette** displays a collection of palettes. The **Palette** shows nodes and connectors. It allows you to drag and drop the nodes and connectors on the **Diagram**. The **Palette** has a header that displays the name and also has an option that allows you to expand or collapse its items. Each node or connector in the palette is called a **Palette Item**.

{% include image.html url="/js/Diagram/Concepts-and-Features/Symbol-Palette_images/Symbol-Palette_img1.jpeg" Caption="SymbolPalette"%}

## Create and Add Symbols in the Palette

Node and Connector are added to the Palette as Palette Items. The following code example illustrates how to create and add symbols in Palette.

{% highlight js %}

// palette array
var paletteCollection = [];
var basiShapes = { "name": "Basic Shapes" };
var connectors = { "name": "Connectors" };

//add node/connector to palette
basiShapes.Add(createNode(name, offsetX, offsety, height, width));
connectors.Add(createConnector(name, segments, decorator));

//add palette to palette array
paletteCollection.Add(basiShapes);
paletteCollection.Add(connectors);

//create node
function createNode(name, offsetX, offsety, height, width) {
//note: for creating node refer the link Node creation
}
//create connector
function createConnector(name, segments, decorator) {
//note: for creating connector refer the link Connector creation    
}

$("#palette").ejSymbolPalette({ palettes: paletteCollection });

{% endhighlight %}

## Adding Node and Connector

The **Diagram** provides support for adding nodes and connectors through the **Symbol Palette**. To add a **node** to the **Diagram**, drag the desired symbol from the **SymbolPalette** to the drawing area and release the pointer. The desired palette item that is clicked, is added to the **Diagram** when you set the desired **Diagram** id to the Symbol Palette’s **diagramId**.

{% include image.html url="/js/Diagram/Concepts-and-Features/Symbol-Palette_images/Symbol-Palette_img2.png" Caption="Adding Nodes and Connectors through Symbol Palette"%}

## Appearance

The following properties are used to customize the appearance of **Symbol Palette**.

<table>
<tr>
<td>
<b>Properties</b></td><td>
<b>Data Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
width</td><td>
number</td><td>
Gets or sets the width of the palette.</td></tr>
<tr>
<td>
height</td><td>
number</td><td>
Gets or sets the height of the palette.</td></tr>
<tr>
<td>
paletteItemWidth</td><td>
number</td><td>
Gets or sets the palette item width.</td></tr>
<tr>
<td>
paletteItemHeight</td><td>
number</td><td>
Gets or sets the palette item height.</td></tr>
<tr>
<td>
showPaletteItemText</td><td>
boolean</td><td>
Show or hide the palette item text.</td></tr>
<tr>
<td>
allowDrag</td><td>
boolean</td><td>
Allows or prevents you from dragging node or connector from symbol palette.</td></tr>
<tr>
<td>
headerHeight</td><td>
number</td><td>
Gets or sets the palette header height.</td></tr>
<tr>
<td>
cssClass</td><td>
string</td><td>
Gets or sets the class of the palette.</td></tr>
<tr>
<td>
palettes</td><td>
array</td><td>
Gets or sets the palette items.</td></tr>
<tr>
<td>
selectedPaletteName</td><td>
string</td><td>
Gets or sets the name of the selected item in the palette</td></tr>
</table>

_Appearance_

The following code illustrates how to customize the **Appearance** of the **Palette.**

{% highlight js %}

// properties to symbol palette
$("#palette").ejSymbolPalette({ 
       palettes: collection,
       diagramId: "DiagramContent",
       height: "100%",
       width: "100%",
       paletteItemWidth: 45,
       paletteItemHeight: 45,
       showPaletteItemText: true,
       headerHeight: 30,
       allowDrag: true,
       selectedPaletteName: "Basic Shapes"
}); 

{% endhighlight %}

## Preview for Drag and Drop

Diagram provides preview support for **Palette item** during drag and drop. When you drag an item from the palette to **Diagram**, a preview of the dragged item is displayed.

**Preview Appearance**

You can customize the preview size and position using the following properties.

<table>
<tr>
<td>
<b>Properties</b></td><td>
<b>Data Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
previewWidth</td><td>
number</td><td>
Gets or sets the preview width of palette item.</td></tr>
<tr>
<td>
previewHeight</td><td>
number</td><td>
Gets or sets the preview height of palette item.</td></tr>
<tr>
<td>
previewOffset</td><td>
object</td><td>
Gets or sets the preview x and y value of palette item.</td></tr>
</table>

_Preview Appearance_

The following code example illustrates how to customize **Preview Content**.

{% highlight js %}

  //set properties to symbol palette preview
  previewWidth: 100,
  previewHeight: 100,
  previewOffset: { x: 102, y: 102 }

{% endhighlight %}
