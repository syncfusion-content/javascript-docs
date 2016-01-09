---
layout: post
title: Define and add the frequently used nodes/connectors to the symbol palette
description: How to add shapes to the symbol palette and drag and drop them over the drawing area?
platform: js
control: Diagram
documentation: ug
---

# Symbol Palette

The **SymbolPalette** displays a collection of palettes. The Palette shows a set of nodes and connectors. It allows you to drag and drop the nodes and connectors into the Diagram. 
## Palettes
 
A palette is both the customizable header and also the set of relevent shapes themselves.The Palette has a header that displays the name and also allows you to expand or collapse its items. 


### Palette Items
Each node or connector in the palette is called a Palette Item.It allows to drag the diagram object by clicking on it with the mouse and dragging it anywhere.

#### Create and add symbols to the Palette 

The following steps illustrate how to add palette items to symbol palette. 

#### Define the palette items

You can create a palette item as a node, group, connector, lane, or phase. To create a palette item, you first need to define that element as JSON. The following code example illustrates how to define palette items.

{% highlight js %}

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

#### Initialize a palette with palette items

To initialize a palette, define a JSON object with the property `name` that is displayed as the header text of palette. The palette items need to be defined and added to the `items` collection of the palette. The `expanded` property of palette allows to expand/collapse its palette items. 
The following code example illustrates how to define a palette with items that are defined in the previous section. 

{% highlight js %}

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

#### Add the palettes to SymbolPalette

You can add any number of palettes to the `palettes` collection of the symbol palette. The following example illustrates how to define symbol palette with a palette object that is defined in the previous step.

{% highlight js %}

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

#### Customize the size of palette items

You can customize the size of the individual palette items. The `paletteItem` property of node enables you to define the size of the symbol items. The following code example illustrates how to change the size of a palette item.

{% highlight js %}

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
                    //Defines the size of the palette item
                    width: 50,
                    height: 50, 
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
    });

{% endhighlight %}

Palette item size is set based on the precedence flow given in the following table.

| Palette Item | Rendering Size |  
|---|---|---|
| Precedence - Width | paletteItem.width > model.paletteItemWidth > node.width |  
| Precedence - Height | paletteItem.height > model.paletteItem.Height > node.height |  

Palette item size can be based on the actual size of the node, regardless of the precedence. 

#### Stretch the shape in to the Palette Item

The `enableScale` property of the palette item enables you to customize the size of the item regardless of the precedence. The following code example illustrates how to customize the palette item size.

{% highlight js %}

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


### Palette header 

Palette headers are often used to display unit of information that proceeds the information about the palette. By default, the header content is the name of the palette by default, so when you customize the header of the palette, it will update on all the palette as well.

Following code example illustrates how to define default palette header.


{% highlight js %}

        $("#symbolpalette").ejSymbolPalette({          
            diagramId: "diagram",
            //Defines the default header
            palettes: [{
                name: "Basic Shapes",
                
            }], 
        });

{% endhighlight %}


![](/js/Diagram/Symbol-Palette_images/Symbol-Palette_img7.png)

#### Customize the Palette Header

Palettes can be annotated with its header texts. Following code example illustrates how to define palette header.

Also, you can any embed Html element into a palette header. Following code example illustrates how to customize palette headers.



{% highlight html %}


    &lt;!--dependency scripts--&gt;
        &lt;script id="svgTemplate" type="text/x-jsrender"&gt;
        &lt;!--  define html element --&gt;
            &lt;svg version="1.0" xmlns="http://www.w3.org/2000/svg" width="225px" height="28px"&gt;
                &lt;g visibility="visible"&gt;
                    &lt;image width="26px" height="26px" opacity="1" xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="image.png"&gt;&lt;/image&gt;
                    &lt;text x="40" y="18" font-size="14"&gt;
                        <tspan>Basic Shapes</tspan>
                    &lt;/text&gt;
                &lt;/g&gt;
            &lt;/svg&gt;
        &lt;/script&gt;												


{% endhighlight %}


{% highlight js %}

    //Defines the JSON to create a palette
    var palette =
    {
        name: "Basic Shapes",
        //Sets the id of the HTML content 
        templateId: "svgTemplate",
    };

{% endhighlight %}

The following image shows the customized palette header

![](/js/Diagram/Symbol-Palette_images/customizethepaletteheader_img1.png)

## Symbol Previews

Image, simple snippet to customize the preview size

You can customize the preview size of the individual palette items. The `paletteItem` property of node enables you to define the preview size of the symbol items. The following code example illustrates how to change the preview size of a palette item.

{% highlight js %}

    $("#symbolpalette").ejSymbolPalette({
        //Defines the palette collection 
        palettes: [{
            name: "Basic Shapes",
            expanded: true,
            items: [
                    {
                        name: "Rectangle", height: 50, width: 50,
                        //Specifies the individual palette item preview size   
                        paletteItem: {
                            previewWidth: 50,
                            previewHeight: 50,
                        }
                    },
                    {
                        name: "Rectangle2", height: 50, width: 50, shape: "ellipse",
                    }]
        }], 
    });

{% endhighlight %}

![](/js/Diagram/Symbol-Palette_images/customizethepaletteheader_img5.png)

You can also customize the preview size of the individual palette items. The `paletteItem` property of node enables you to define the preview size of the symbol items. The following code example illustrates how to change the preview size of a palette item.

{% highlight js %}

                   $("#symbolpalette").ejSymbolPalette({
                    //Defines the palette collection 
                    diagramId: "diagram",
                    palettes: [{
                        name: "Basic Shapes",
                        expanded: true,
                        items: [
                            {
                                name: "Rectangle", height: 50, width: 50,
                                //Specifies the individual palette item preview size   
                                paletteItem: {
                                    previewWidth: 50,
                                    previewHeight: 50,
                                }
                            },
                            {
                                name: "Rectangle2", height: 50, width: 50, shape: "ellipse",
                            }]
                    }], 
                    previewWidth: 100,
                    previewHeight: 100,
                });

{% endhighlight %}

![](/js/Diagram/Symbol-Palette_images/customizethepaletteheader_img4.png)

Symbol palette allows to sets the offset of the dragging helper relative to the mouse cursor.


{% highlight js %}

              $("#symbolpalette").ejSymbolPalette({
                    //Defines the palette collection 
                    diagramId: "diagram",
                    palettes: [{
                        name: "Basic Shapes",
                        expanded: true,
                        items: [{
                            name: "Rectangle",
                            height: 50,
                            width: 50, 
                        }]
                    }], 
                    previewOffset: { x: 50, y: 50 }, 
                });

{% endhighlight %}

![](/js/Diagram/Symbol-Palette_images/customizethepaletteheader_img5.png)


preview size is set based on the precedence flow given in the following table.

| Palette Item |   Preview Size |
|---|---|---|
| Precedence - Width |  paletteItem.previewWidth > model.previewWidth > node.width |
| Precedence - Height | paletteItem.previewHeight > model.previewHeight > node.height |

Preview item size can be based on the actual size of the node, regardless of the precedence.


## Appearance 

You can show/hide the palette item texts by using the `showPaletteItemText` property of symbol palette. The following code illustrates how to customize the appearance of the symbol Palette.

{% highlight js %}

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