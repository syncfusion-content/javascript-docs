---
layout: post
title: Symbol-Palette
description: symbol palette
platform: js
control: Diagram
documentation: ug
---

# Symbol Palette

The **SymbolPalette** displays a collection of palettes. The Palette shows a set of nodes and connectors. It allows you to drag and drop the nodes and connectors into diagram. The Palette has a header that displays the name and also allows you to expand or collapse its items. Each node or connector in the palette is called a Palette Item.

## Create and add symbols to the Palette 

Following steps illustrates how to add palette items to symbol palette. 

### Define the palette items

You can create a palette item as a node, group, connector, lane or phase. To create a palette item, you first need to define that element as JSON. Following code snippet illustrates how to define palette items.

{% highlight js %}

           //create a node
            var node = {
                name: "Ellipse",
                //Specify node size
                width: 40, height: 40,
                //Specify node offset and shape 
                offsetX: 20, offsetY: 20, shape: "ellipse",
            };
            
            //create a group
            var group = {
                name: "group",
                //define the child nodes.
                children: [
                    {
                        name: "child1",
                        width: 40, height: 40,
                        offsetX: 20, offsetY: 20, borderWidth: 1
                    },
                    
                    {
                        name: "child2",
                        width: 40, height: 40,
                        offsetX: 40, offsetY: 40,
                        borderWidth: 1,
                    }, ],
                width: 40, height: 40,
            };

            //create a connector 
            var connector = {
                name: "Line",
                segments: [{ type: "orthogonal" }],
                
                //define the source and target points
                sourcePoint: { x: 0, y: 0 },
                targetPoint: { x: 40, y: 40 },
                
                //define the target decorator properties
                targetDecorator: { shape: "arrow" },
            };

            //create a lane 
            var lane = {
                name: "lane", header: {
                    width: 50, height: 50, fillColor: "#C7D4DF"
                },
                fillColor: "#f5f5f5",
                //specify size for the lane 
                height: 60, width: 140,
                //specify offset for the lane 
                offsetX: 70, offsetY: 30,
                //specify orientation as horizontal/vertical
                orientation: "horizontal", isLane: true
            };

            //create a phase
            var phase = {
                name: "verticalPhase",
                type: "phase",
                // Define the style of the phase
                lineWidth: 1, lineDashArray: "3,3", lineColor: "#606060",
                //Define the orientation of the phase
                orientation: "vertical", 
             } 
{% endhighlight %}
             
### Initialize a palette with palette items

To initialize a palette, you need to define a JSON object with the property `name`, that will be displayed as the header text of palette. The palette items need to be defined and added to the `items` collection of palette. The `expanded` property of palette allows to expand/collapse its palette items. 
The following code snippet illustrates how to define a palette with items that are defined in the previous section. 

{% highlight js %}

               //Define the JSON to create a palette
                var palette = 
                {
                      //Set the name of the palette
                      name: "Basic Shapes", 
                      //Set whether the palette expands/collapse its children
                      expanded: true,    
                      //Add the palette items to palette
                      items: [node, group, connector, lane,phase],
                };
                
{% endhighlight %}

### Add the palettes to SymbolPalette

You can add any number of palettes to the `palettes` collection of symbol palette. The following example illustrates how to define symbol palette with a palette object that is defined in the previous step.

{% highlight js %}

      //Initialize the symbol palette
      $("#symbolpalette").ejSymbolPalette({ 
          //Define the palette collection 
          palettes: [
                palette
          ],
          //specify the symbol palette size
          height: "100%", width: "100%"
        });
        
{% endhighlight %}

The below image shows the symbol palette with multiple palette Items.

{% include image.html url="/js/Diagram/Symbol-Palette_images/Symbol-Palette_img3.png" %}

## Customize the size of palette items

We can customize the size of the individual palette items. The `paletteItem` property of node enables you to define the size, preview size of the symbol items. Following code snippet illustrates how to change the size of a palette item.

{% highlight js %}

$("#symbolpalette").ejSymbolPalette({
    //Define the palette collection 
    palettes: [
        {
            name: "Basic Shapes",
            expanded: true,
            items: [
                {
                    name: "Rectangle",
                    height: 40,
                    width: 80,
                    //Specify the size of palette Item 
                    paletteItem: {
                        enableScale: true,
                        //define the size of the palette item
                        width: 50,
                        height: 50,
                        //define the preview size of the palette item
                        previewWidth: 100,
                        previewHeight: 100,
                        margin: {
                            left: 20,
                            right: 20,
                            top: 20,
                            bottom: 20
                        }
                    }
                }
            ]
        }
    ],

    //Specify the default size to render palette items
    paletteItemWidth: 50,
    paletteItemHeight: 50,
    //Specify the default palette item preview size
    previewWidth: 100,
    previewHeight: 100,
});

{% endhighlight %}

Palette item size will be set based on the precedence flow given in the following table.

<table>
<tr>
<th>
Palette Item</th><th>
Rendering Size</th><th>
Preview Size</th></tr>
<tr>
<td><b>
Precedence - Width</b> </td><td>
paletteItem.width > model.paletteItemWidth > node.width </td><td>
paletteItem.previewWidth > model.previewWidth > node.width</td></tr>
<tr>
<td><b>
Precedence - Height </b></td><td>
paletteItem.height > model.paletteItem.Height > node.height </td><td>
paletteItem.previewHeight > model.previewHeight > node.height</td></tr>
</table>
Palette item size can be based on the actual size of the node, regardless of the precedence. 

The `enableScale` property of the palette item enables you to customize the size of the item regardless of the precedence.Following code snippet illustrates how to customize the palette item size.

{% highlight js %}

    $("#symbolpalette").ejSymbolPalette({
        palettes: [{
            name: "Basic Shapes",
            expanded: true,
            items: [{
                name: "Rectangle",
                height: 40,
                width: 80,
                //Specify the size of palette Item 
                paletteItem: {
                    // Enables to fit the content into the specified palette item size
                    enableScale: true
                    // If it is set as false, the element will be rendered with actual node size
                }
            }]
        }]
    });

{% endhighlight %}
 
{% include image.html url="/js/Diagram/Symbol-Palette_images/Symbol-Palette_img1.png" caption = "Enable Scale - false" %}

{% include image.html url="/js/Diagram/Symbol-Palette_images/Symbol-Palette_img2.png" caption = "Enable Scale - true" %}

## Appearance 

 You can show/hide the palette item texts using the `showPaletteItemText` property of symbol palette. The following code illustrates how to customize the appearance of the symbol Palette.

{% highlight js %}

    // Initialize symbol palette    
    $("#palette").ejSymbolPalette({
        palettes: palettes,
        diagramId: "DiagramContent",
        height: "100%",
        width: "100%",
        paletteItemWidth: 45,
        paletteItemHeight: 45,

        //specify whether palette item text should be visible or not        
        showPaletteItemText: true,

        headerHeight: 30,
        selectedPaletteName: "Basic Shapes"
    });
       
{% endhighlight %}
To explore the properties of symbol palette, refer [Symbol Palette Properties](/js/api/ejsymbolpalette "members").


## Drop nodes into diagram 

The Diagram provides support for adding nodes and connectors through the Symbol Palette. To add a node to the Diagram, drag the desired symbol from the SymbolPalette to the drawing area and release the pointer.
The `diagramId` property of symbol palette allows to define the diagram over which the symbol items can be dragged and dropped.Following code snippet illustrates how to relate the symbol palette with diagram.

{% highlight js %}

    //Relate diagram to symbol palette
    $("#symbolpalette").ejSymbolPalette({
         //Specify the diagramId  
         diagramId: "diagram",
    });
    
{% endhighlight %}
