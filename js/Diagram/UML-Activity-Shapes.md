---
layout: post
title:  Visually represents a static view of an application
description: How to visually represent the behavior process of a system? 
platform: js
control: Diagram
documentation: ug
---

### UML Activity Shapes

UML activity Shapes used to draw a behavior diagram which shows flow of control or object flow with emphasis on the sequence and conditions of the flow.
These diagrams are useful for analyzing a use case by describing what actions need to take place and when they should occur, describing a complicates sequential algorithm and modeling applications with parallel processes. 

To create a UMLActivity shape, the “type” of the node should be set as “umlactivity” and its “shape” should be set as any one of the built-in shape.
The following code example illustrates how to create a simple behavior diagram.
 
 {% highlight javascript %}
 
 $("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "initialnode",
		offsetX: 100,
		offsetY: 100,
        width: 80, 
        height: 50,
        //Sets type of shape
         type: "umlactivity",
         //Sets the activity shape as initialnode
         shape: ej.datavisualization.Diagram.UMLActivityShapes.InitialNode,
            }]
 }];

{% endhighlight %}	

![](/js/Diagram/Shapes_images/Shapes_img152.png)

The list of flow shapes are as follows.

![](/js/Diagram/Shapes_images/Shapes_img153.png)
