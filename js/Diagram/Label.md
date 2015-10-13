---
layout: post
title: Label
description: label
platform: js
control: Diagram
documentation: ug
---

# Label

**Label** is a block of text that can be displayed over a node or connector. Label is used to textually represent an object with a string that can be edited at run time. You can add Multiple Labels to a node/connector.

## Create Label

You can add a label to a node/connector by defining the label object and adding that to the `labels` collection of node/connector. The `text` property of label defines the text to be displayed. The following code illustrates how to create a Label. 

{% highlight js %}

    //Initialize Diagram
    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        //Initialize nodes collection
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            //Initialize labels collection
            labels: [
                // Define JSON to create a label
                {
                    //Define the text to be displayed
                    text: "Label"
                }
            ]
        }],
        //Initialize connectors collection
        connectors: [{
            name: "connector1",
            sourcePoint: {
                x: 200,
                y: 50
            },
            targetPoint: {
                x: 300,
                y: 150
            },
            segments: [{
                type: "orthogonal",
                length: 50,
                direction: "bottom"
            }],
            //Initialize labels collection
            labels: [
                //Define JSON to create a label
                {
                    //Define the text to be displayed
                    text: "Label",
                    //Define the background color of the text block
                    fillColor: "white"
                }
            ]
        }]
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img1.png" %}

To explore more label properties, refer [Label Properties](/js/api/ejdiagram "members:nodes-labels").

## Update Label at runtime
     
The client side API `updateLabel` is used to update the labels at run time.

The following code snippet illustrates how to change the label properties.

{% highlight js %}

            var diagram = $("#diagram").ejDiagram("instance");
            var selectedObject = diagram.model.selectedItems.children[0];
            diagram.updateLabel(selectedObject.name, selectedObject.labels[0], { text: "label", fillColor: "red" });

{% endhighlight %}


## Alignment

Label can be aligned relative to the node boundaries. It has margin, offset, horizontal and vertical alignment settings. It will be quite tricky when all four alignments are used together but gives you more control over alignment.

### Offset

The `offset` property of label is used to align the labels based on fractions. 0 represents top/left corner, 1 represents bottom/right corner, and 0.5 represents half of width/height.

The following image shows the relationship between the label position(black colored circle) and offset(fraction values).

{% include image.html url="/js/Diagram/Label_images/Label_img2.png" %}

### Horizontal and vertical alignements

The `horizontalAlignment` property of label is used to set how the label is horizontally aligned at the label position determined from the fraction values. The `verticalAlignment` property is used to set how label is vertically aligned at the label position. 

The following tables illustrates all possible alignment visually with **offset (0, 0).**

<table>
<tr>
<th>
Horizontal Alignment</th><th>
Vertical Alignment</th><th>
Output with Offset(0,0)</th></tr>
<tr>
<td>
Left</td><td>
Top</td><td>
<img src="/js/Diagram/Label_images/Label_img3.png" alt="" width="155pt" height="138pt"/></td></tr>
<tr>
<td>
Center</td><td>
 </td><td>
<img src="/js/Diagram/Label_images/Label_img4.png" alt="" width="155pt" height="138pt"/></td></tr>
<tr>
<td>
Right</td><td>
 </td><td>
<img src="/js/Diagram/Label_images/Label_img5.png" alt="" width="155pt" height="138pt"/></td></tr>
<tr>
<td>
Left</td><td>
Center</td><td>
<img src="/js/Diagram/Label_images/Label_img6.png" alt="" width="155pt" height="138pt"/></td></tr>
<tr>
<td>
Center</td><td>
 </td><td>
<img src="/js/Diagram/Label_images/Label_img7.png" alt="" width="155pt" height="138pt"/></td></tr>
<tr>
<td>
Right</td><td>
 </td><td>
<img src="/js/Diagram/Label_images/Label_img8.png" alt="" width="155pt" height="138pt"/></td></tr>
<tr>
<td>
Left</td><td>
Bottom</td><td>
<img src="/js/Diagram/Label_images/Label_img9.png" alt="" width="155pt" height="138pt"/></td></tr>
<tr>
<td>
Center</td><td>
 </td><td>
<img src="/js/Diagram/Label_images/Label_img10.png" alt="" width="155pt" height="138pt"/></td></tr>
<tr>
<td>
Right</td><td>
 </td><td>
<img src="/js/Diagram/Label_images/Label_img11.png" alt="" width="155pt" height="138pt"/></td></tr>
</table>

The following codes illustrates how to align labels.

{% highlight js %}

    //Initialize Diagram
    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            labels: [{
                text: "Label",
                // set offset to label
                offset: {
                    x: 0,
                    y: 0.5
                },
                // set how to align label horizontally relative to given offset 
                horizontalAlignment: ej.datavisualization.Diagram.HorizontalAlignment.Left,
                // set how to align label vertically relative to given offset
                verticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Center,
                // set text alignment to label
                textAlign: ej.datavisualization.Diagram.TextAlign.Center
            }]
        }],
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img12.png" %}

### Margin

**Margin** is an absolute value used to add some blank space in any of its four sides. You can displace the labels with the `margin` property.
Following code snippet illustrates how to align a label based on its `offset`, `horizontalAlignment`, `verticalAlignment` and `margin` values.

{% highlight js %}

    //Initialize Diagram
    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        //Set nodes collection to diagram model
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            labels: [{
                text: "Label",
                offset: {
                    x: 0.5,
                    y: 1
                },
                horizontalAlignment: ej.datavisualization.Diagram.HorizontalAlignment.Center,
                verticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Top,
                //set margin to add label outside a node 
                margin: {
                    top: 10
                }
            }]
        }],
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img13.png" %}

### Text Alignment

The `textAlign` property of label allows you to set how the text should be aligned (left, right, center or justify) inside the text block. The following codes illustrate how to set textAlign for a label.

{% highlight js %}

    //Initialize Diagram
    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            // set text alignment for a label
            labels: [{
                text: "Text Align is set as Left",
                textAlign: ej.datavisualization.Diagram.TextAlign.Left
            }]
        }],
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img14.png" %}

<table>
<tr>
<th>
TextAlign</th><th>
Image</th></tr>
<tr>
<td>
Left</td><td>
<img src="/js/Diagram/Label_images/Label_img15.png" alt="" width="128pt" height="129pt"/></td></tr>
<tr>
<td>
Right</td><td>
<img src="/js/Diagram/Label_images/Label_img16.png" alt="" width="128pt" height="129pt"/></td></tr>
<tr>
<td>
Center</td><td>
<img src="/js/Diagram/Label_images/Label_img17.png" alt="" width="128pt" height="129pt"/></td></tr>
<tr>
<td>
Justify</td><td>
<img src="/js/Diagram/Label_images/Label_img18.png" alt="" width="128pt" height="129pt"/></td></tr>
</table>

## Wrapping

When text overflows node boundaries, we can control it using text wrapping, so it will be wrapped into multiple lines. The `wrapping` property of label defines how the text should be wrapped. The following code illustrates how to wrap a text in a node.

{% highlight js %}

    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            //Enable Text-wrapping
            labels: [{
                text: "Label Text Wrapping",
                wrapping: ej.datavisualization.Diagram.TextWrapping.Wrap
            }]
        }],
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img19.png" %}

<table>
<tr>
<th>
Values</th><th>
Description</th><th>
Image</th></tr>
<tr>
<td>
NoWrap</td><td>
Text will not be wrapped </td><td>
<img src="/js/Diagram/Label_images/Label_img20.png" alt="" width="145pt" height="128pt"/></td></tr>
<tr>
<td>
Wrap</td><td>
Text-wrapping occurs when the text overflows beyond the available node width. </td><td>
<img src="/js/Diagram/Label_images/Label_img21.png" alt="" width="145pt" height="128pt"/></td></tr>
<tr>
<td>
WrapWithOverflow (Default)</td><td>
Text-wrapping occurs when the text overflows beyond the available node width. However, the text may overflow beyond the node width in the case of a very long word.</td><td>
<img src="/js/Diagram/Label_images/Label_img22.png" alt="" width="145pt" height="128pt"/></td></tr>
</table>

## Appearance

You can change the font style of the labels with the font specific properties(`fontSize`,`fontFamily`,`fontColor`.,). The following code illustrates how to customize the appearance of a label.

{% highlight js %}

    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        //Set nodes collection to diagram model
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            labels: [{
                text: "Label Text",
                //Set styles to a label 
                fontSize: 12,
                fontFamily: "TimesNewRoman",
                fontColor: "black",
                bold: true,
                italic: true,
                textDecoration: ej.datavisualization.Diagram.TextDecorations.Underline
            }]
        }],
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img23.png" %}

The fill and border appearance of the text also can be customized with appearance specific properties of label.The following code illustrates how to customize background and border of a label.

{% highlight js %}

    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        //Set nodes collection to diagram model
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            labels: [{
                text: "Label Text",
                //Customize background and borders of a label 
                fillColor: "white",
                borderColor: "black",
                borderWidth: 1,
            }]
        }],
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img24.png" %}

## Drag

A **Label** can be displaced from its original position to any preferred location interactively. Dragging is disabled by default. You can enable label dragging with the `constraints` property of node/connector. The following code illustrates how to enable label **dragging**.

{% highlight js %}

    var nodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
    var nodes = [{
        name: "node",
        width: 100,
        height: 100,
        offsetX: 100,
        offsetY: 100,
        borderColor: "black",
        fillColor: "#1BA0E2",
        //Enable Label Dragging for node.
        constraints: nodeConstraints.Default | nodeConstraints.DragLabel,
        labels: [{
            text: "Label Text"
        }]
    }];
    
    var connectorConstraints = ej.datavisualization.Diagram.ConnectorConstraints;
    var connectors = [{
        name: "connector1",
        sourcePoint: {
            x: 200,
            y: 50
        },
        targetPoint: {
            x: 300,
            y: 150
        },
        segments: [{
            type: "orthogonal",
            length: 50,
            direction: "bottom"
        }],
        //Enable Label Dragging for connector. 
        constraints: connectorConstraints.Default | connectorConstraints.DragLabel,
        labels: [{
            text: "Label "
        }]
    }];
    
    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        nodes: nodes,
        connectors: connectors
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img25.png" %}

## Rotate

You can rotate the labels to any desired angles. Labels will be rotated to the angle that is defined by the `rotateAngle` property of label. The following code illustrates how to rotate a label.

{% highlight js %}

    //Initialize Diagram
    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            labels: [{
                text: "Label",
                //set label's rotation Angle
                rotateAngle: 45
            }]
        }]
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img26.png" %}

N> There is no built-in support to rotate labels interactively.

## Edit

**Diagram** provides support to edit a Label at runtime, either programmatically or interactively. By default, label is in **View** mode. But it can be brought to edit mode in two ways; 

   1. By double clicking on the label.

   2. By selecting the item and pressing the **F2** key. 

Double clicking on any label will enable **editing** of that. Double clicking on the node will enable first label editing. When the focus of editor is lost, the label for the node will be updated.

You can programmatically edit the label by changing the `mode` of the label. The following code illustrates how to edit the label programmatically.

{% highlight js %}

    var diagram = $("#diagram").ejDiagram("instance");
    var node = diagram.model.selectedItems.children[0];
    //set label mode as Edit 
    var options = {
        mode: ej.datavisualization.Diagram.LabelEditMode.Edit
    };
    diagram.updateLabel(node.name, node.labels[0], options);

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img27.png" %}

### Read Only labels

Diagram allows to create read only labels. You have to set the `readOnly` property of label to enable/disable the read only mode. The following code illustrates how to enable **readOnly** mode.

{% highlight js %}

    //Initialize Diagram
    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            //set label as read-only
            labels: [{
                text: "Label",
                readOnly: true
            }]
        }],
    });

{% endhighlight %}

## Multiple labels

We can add any number of labels to a node or connector.  The following code illustrates how to add multiple labels to a node. 

{% highlight js %}

    $("#diagram").ejDiagram({
        width: "100%",
        height: "100%",
        pageSettings: {
            scrollLimit: "diagram"
        },
        nodes: [{
            name: "node",
            width: 100,
            height: 100,
            offsetX: 100,
            offsetY: 100,
            borderColor: "black",
            fillColor: "#1BA0E2",
            //adding multiple labels to a node
            labels: [{
                text: "Left",
                offset: {
                    x: 0.12,
                    y: 0.1
                }
            }, {
                text: "Center",
                offset: {
                    x: 0.5,
                    y: 0.5
                }
            }, {
                text: "Right",
                offset: {
                    x: 0.82,
                    y: 0.9
                }
            }]
        }],
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img28.png" %}

## Limitation

* To enable faster rendering, labels are rendered in a separate layer, because of this all labels will always stay on top. When two nodes are overlapped, text of underlying node will not be hidden by the overlapped node. 

<table>
<tr>
<th>Expected behavior</th>
<th>Current behavior</th>
</tr>
<tr>
<td><img src="/js/Diagram/Label_images/Label_img29.png" alt="" width="140pt" height="129pt"/></td>
<td><img src="/js/Diagram/Label_images/Label_img30.png" alt="" width="140pt" height="129pt"/></td>
</tr>

</table>
