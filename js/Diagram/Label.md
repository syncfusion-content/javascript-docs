---
layout: post
title: Add text annotations to Diagram objects to textually describe them
description: How to textually describe nodes and connectors?
platform: js
control: Diagram
documentation: ug
---

# Label

**Label** is a block of text that can be displayed over a node or connector. Label is used to textually represent an object with a string that can be edited at run time. You can add Multiple Labels to a node/connector.

## Create Label

You can add a label to a node/connector by defining the label object and adding that to the `labels` collection of node/connector. The `text` property of label defines the text to be displayed. The following code illustrates how to create a Label. 

{% highlight javascript %}

//Initializes Diagram
$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	//Initializes nodes collection
	nodes: [{
		name: "node",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderColor: "black",
		fillColor: "#1BA0E2",
		//Initializes labels collection
		labels: [
			// Defines JSON to create a label
			{
				//Defines the text to be displayed
				text: "Label"
			}
		]
	}],
	//Initializes connectors collection
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
		//Initializes labels collection
		labels: [
			//Defines JSON to create a label
			{
				//Defines the text to be displayed
				text: "Label",
				//Defines the background color of the text block
				fillColor: "white"
			}
		]
	}]
});

{% endhighlight %}

![](/js/Diagram/Label_images/Label_img1.png)

To explore more label properties, refer to [Label Properties](/api/js/ejdiagram#members:nodes-labels "Label Properties").

### Add Labels at runtime

Labels can be added at runtime by using the client side method `addLabel`. The following code illustrates how to add a label to a node. 

{% highlight js %}

        var diagram = $("#sourceDiagram").ejDiagram("instance");

        // Defines JSON to create a label
        var label = { name: "label", text: "Node" };
        diagram.addLabel("node1", label); 
		
		//Insert label at a specific index of labels collection
    	var label = { name: "label", text: "New Label", offset: { x: 0.1, y: 0.1 } };
    	diagram.insertLabel("node1", label, 1); 

{% endhighlight %}

![](/js/Diagram/Label_images/addlabelatruntime_img1.png)


## Update Label at runtime

The client side API `updateLabel` is used to update the labels at run time.

The following code example illustrates how to change the label properties.

{% highlight javascript %}

var diagram = $("#diagram").ejDiagram("instance");
var selectedObject = diagram.model.selectedItems.children[0];
diagram.updateLabel(selectedObject.name, selectedObject.labels[0], { text: "label", fillColor: "red" });

{% endhighlight %}


## Alignment

Label can be aligned relative to the node boundaries. It has margin, offset, horizontal and vertical alignment settings. It is quite tricky when all four alignments are used together but gives you more control over alignment.

### Offset

The `offset` property of label is used to align the labels based on fractions. 0 represents top/left corner, 1 represents bottom/right corner, and 0.5 represents half of width/height.

The following image shows the relationship between the label position (black colored circle) and offset (fraction values).

![](/js/Diagram/Label_images/Label_img2.png)

### Horizontal and vertical alignments

The `horizontalAlignment` property of label is used to set how the label is horizontally aligned at the label position determined from the fraction values. The `verticalAlignment` property is used to set how label is vertically aligned at the label position. 

The following tables illustrates all the possible alignments visually with **offset (0, 0).**

| Horizontal Alignment | Vertical Alignment | Output with Offset(0,0) |
|---|---|---|
| Left | Top | ![](/js/Diagram/Label_images/Label_img3.png) |
| Center | | ![](/js/Diagram/Label_images/Label_img4.png) |
| Right | | ![](/js/Diagram/Label_images/Label_img5.png) |
| Left | Center | ![](/js/Diagram/Label_images/Label_img6.png) |
| Center | | ![](/js/Diagram/Label_images/Label_img7.png) |
| Right | | ![](/js/Diagram/Label_images/Label_img8.png) |
| Left | Bottom | ![](/js/Diagram/Label_images/Label_img9.png) |
| Center | | ![](/js/Diagram/Label_images/Label_img10.png) |
| Right | | ![](/js/Diagram/Label_images/Label_img11.png) |

The following codes illustrates how to align labels.

{% highlight javascript %}

//Initializes Diagram
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
			// Sets offset to label
			offset: {
				x: 0,
				y: 0.5
			},
			// Sets to align label horizontally relative to given offset 
			horizontalAlignment: ej.datavisualization.Diagram.HorizontalAlignment.Left,
			// Sets to align label vertically relative to given offset
			verticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Center,
			// Sets text alignment to label
			textAlign: ej.datavisualization.Diagram.TextAlign.Center
		}]
	}],
});

{% endhighlight %}

![](/js/Diagram/Label_images/Label_img12.png)

### Label alignment with respect to Segments

 `segmentOffset` and `alignment` properties of label allows you to align the connector labels with respect to the segments. In the following image, the labels are placed exactly over the segments regardless of its rectangular bounds.
 
 ![](/js/Diagram/Label_images/Label_img32.png)
 
 Following code example illustrates how to align connector labels.
 
 {% highlight javascript %}

 var nodes = [
          { name: "node1", width: 50, height: 40, offsetX: 200, offsetY: 200, labels: [{ "text": "Task 1" }] },
          { name: "node2", width: 50, height: 40, offsetX: 400, offsetY: 200, labels: [{ "text": "Task 2" }] }
		  ];
		  var connectors = [
		  { name: "connector1", sourceNode: "node1", targetNode: "node2"}
		  ];
		  //Initializes Diagram
		  $("#diagram").ejDiagram({
            width: "100%",
            height: "100%",
            nodes: nodes,
            connectors: connectors,
            snapSettings: ej.datavisualization.Diagram.SnapConstraints.None,
            defaultSettings: {
                connector: {
                    segments: [{ type: "orthogonal" }], 
					// Sets labels for segments
					labels: [{
                            text: "0",
                            fontColor: "black",
							
							// Aligns the label either top or left(before) of the connector segment
                            alignment: "before",
							
							// Sets the position of the label with respect to the segment
                            segmentOffset: 0
                        },{
                            text: "1",
                            fontColor: "black",
							
							// Aligns the label either bottom or right(after) of the connector segment
                            alignment: "after",
							
							// Sets segmentOffset as 1
                            segmentOffset: 1,
							
							// Enables boundaryConstraints for the label should be docked within the label bounds
                            boundaryConstraints: true,
							
                        }], lineWidth: 2
						},
						node: { borderColor: "#000000", fillColor: "#1BA0E2", labels: [{ "fontColor": "black", }]},
            },
        });
		
{% endhighlight %}

![](/js/Diagram/Label_images/Label_img31.png)

By default, connector labels will be aligned with respect to the segments. The `relativeMode` property of label allows you to disable this segment specific label alignment. Following code example illustrates how to disable the segment specific label alignment.

{% highlight javascript %}

 var nodes = [
          { name: "node1", width: 50, height: 40, offsetX: 200, offsetY: 200, labels: [{ "text": "Task 1" }] },
          { name: "node2", width: 50, height: 40, offsetX: 400, offsetY: 200, labels: [{ "text": "Task 2" }] }
		  ];
		  var connectors = [
		  { name: "connector1", sourceNode: "node1", targetNode: "node2",
		  lineWidth: 2,
		  segments: [{ type: "orthogonal" }],
		  
		  // Sets labels for segments
		   labels: [{
		   text: "0",
		   fontColor: "black",
		   
		   //Sets the relativeMode as segmentpath
		   relativeMode: "segmentpath",
		   }]
		   }];
		  //Initializes Diagram
		  $("#diagram").ejDiagram({
            width: "100%",
            height: "100%",
            connectors: connectors,
            snapSettings: ej.datavisualization.Diagram.SnapConstraints.None
			});
		
{% endhighlight %}

### Margin

**Margin** is an absolute value used to add some blank space in any one of its four sides. You can displace the labels with the `margin` property.
The following code example illustrates how to align a label based on its `offset`, `horizontalAlignment`, `verticalAlignment` and `margin` values.

{% highlight javascript %}

//Initializes Diagram
$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	//Sets nodes collection to Diagram model
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
			//Sets margin to add label outside a node 
			margin: {
				top: 10
			}
		}]
	}],
});

{% endhighlight %}

![](/js/Diagram/Label_images/Label_img13.png)

### Text Alignment

The `textAlign` property of label allows you to set how the text should be aligned (left, right, center, or justify) inside the text block. The following codes illustrate how to set textAlign for a label.

{% highlight javascript %}

//Initializes Diagram
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
		// Sets text alignment for a label
		labels: [{
			text: "Text Align is set as Left",
			textAlign: ej.datavisualization.Diagram.TextAlign.Left
		}]
	}],
});

{% endhighlight %}

![](/js/Diagram/Label_images/Label_img14.png)

| TextAlign | Image |
|---|---|
| Left | ![](/js/Diagram/Label_images/Label_img15.png) |
| Right | ![](/js/Diagram/Label_images/Label_img16.png) |
| Center | ![](/js/Diagram/Label_images/Label_img17.png) |
| Justify | ![](/js/Diagram/Label_images/Label_img18.png) |

## Hyperlink

**Diagram** provides a support to add a hyperlink for the nodes label. It can also be customized.

{% highlight javascript %}

// Defines JSON to create a node
var nodes = [{
	name: "hyperlinknode", 
	fillColor: "white",
	width: 150, height: 60,
	offsetX: 100, offsetY: 100,
	// Sets the hyperlink for the node label
	labels: [{ "hyperText": "https://www.syncfusion.com" }]
	}];

//Initializes Diagram
$("#diagram").ejDiagram({
	width: "100%", height: "100%",
	//Initializes nodes collection
	nodes: nodes
});

{% endhighlight %}

![](/js/Diagram/Label_images/Label_img33.png)

## Wrapping

When text overflows node boundaries, you can control it by using text wrapping. So, it is wrapped into multiple lines. The `wrapping` property of label defines how the text should be wrapped. The following code illustrates how to wrap a text in a node.

{% highlight javascript %}

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
		//Enables Text-wrapping
		labels: [{
			text: "Label Text Wrapping",
			wrapping: ej.datavisualization.Diagram.TextWrapping.Wrap
		}]
	}],
});

{% endhighlight %}

![](/js/Diagram/Label_images/Label_img19.png)

| Values | Description | Image |
|---|---|---|
| NoWrap | Text will not be wrapped | ![](/js/Diagram/Label_images/Label_img20.png) |
| Wrap | Text-wrapping occurs when the text overflows beyond the available node width. | ![](/js/Diagram/Label_images/Label_img21.png) |
| WrapWithOverflow (Default) | Text-wrapping occurs when the text overflows beyond the available node width. However, the text may overflow beyond the node width in the case of a very long word. | ![](/js/Diagram/Label_images/Label_img22.png) |

## Appearance

You can change the font style of the labels with the font specific properties(`fontSize`,`fontFamily`,`fontColor`.,). The following code illustrates how to customize the appearance of a label.

{% highlight javascript %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	//Sets nodes collection to Diagram model
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
			//Sets styles to a label 
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

![](/js/Diagram/Label_images/Label_img23.png)

The fill, border and opacity appearances of the text can also be customized with appearance specific properties of label.The following code illustrates how to customize background, opacity and border of a label.

{% highlight javascript %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	//Sets nodes collection to Diagram model
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
			//Customizes background and borders of a label 
			fillColor: "white",
			borderColor: "black",
			borderWidth: 1,
			//Customize transparency of a label
			opacity: 0.7
		}]
	}],
});

{% endhighlight %}

![](/js/Diagram/Label_images/Label_img24.png)

## Drag

A **Label** can be displaced from its original position to any preferred location interactively. Dragging is disabled by default. You can enable label dragging with the `constraints` property of node/connector. The following code illustrates how to enable label **dragging**.

{% highlight javascript %}

var nodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
var nodes = [{
	name: "node",
	width: 100,
	height: 100,
	offsetX: 100,
	offsetY: 100,
	borderColor: "black",
	fillColor: "#1BA0E2",
	//Enables Label Dragging for node.
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
	//Enables Label Dragging for connector. 
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

![](/js/Diagram/Label_images/Label_img25.png)

## Rotate

You can rotate the labels to any desired angle. Labels are rotated to the angle that is defined by the `rotateAngle` property of label. The following code illustrates how to rotate a label.

{% highlight javascript %}

//Initializes Diagram
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
			//Sets label's rotation Angle
			rotateAngle: 45
		}]
	}]
});

{% endhighlight %}

![](/js/Diagram/Label_images/Label_img26.png)

N> There is no built-in support to rotate labels interactively.

## Edit

**Diagram** provides support to edit a Label at runtime, either programmatically or interactively. By default, label is in **View** mode. But it can be brought to edit mode in two ways; 

1. By double-clicking the label.
2. By selecting the item and pressing the **F2** key. 

Double-clicking any label will enables **editing** of that. Double-clicking the node enables first label editing. When the focus of editor is lost, the label for the node is updated.

You can programmatically edit the label by changing the `mode` of the label. The following code illustrates how to edit the label programmatically.

{% highlight javascript %}

var diagram = $("#diagram").ejDiagram("instance");
var node = diagram.model.selectedItems.children[0];
//Sets label mode as Edit 
var options = {
	mode: ej.datavisualization.Diagram.LabelEditMode.Edit
};
diagram.updateLabel(node.name, node.labels[0], options);

{% endhighlight %}

![](/js/Diagram/Label_images/Label_img27.png)

### Read Only labels

Diagram allows to create read only labels. You have to set the `readOnly` property of label to enable/disable the read only mode. The following code illustrates how to enable **readOnly** mode.

{% highlight javascript %}

//Initializes Diagram
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
		//Sets label as read-only
		labels: [{
			text: "Label",
			readOnly: true
		}]
	}],
});

{% endhighlight %}

## Multiple labels

You can add any number of labels to a node or connector. The following code illustrates how to add multiple labels to a node. 

{% highlight javascript %}

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
		//Adds multiple labels to a node
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

![](/js/Diagram/Label_images/Label_img28.png)

## LabelRendering Mode

Labels can be rendered in separate layer as svg or html. 

{% highlight javascript %}

 $("#diagram").ejDiagram({
	 
    //renders label in same layer
    labelRenderingMode: "svg"
 
 });

{% endhighlight %}

## Limitation

* To enable faster rendering, labels are rendered in a separate layer because of this, all the labels always stay on top. When two nodes are overlapped, text of underlying node is not hidden by the overlapped node. 

| Expected behavior | Current behavior |
|---|---|
| ![](/js/Diagram/Label_images/Label_img29.png) | ![](/js/Diagram/Label_images/Label_img30.png) |










 


