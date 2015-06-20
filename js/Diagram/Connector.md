---
layout: post
title: Connector
description: connector
platform: js
control: Diagram
documentation: ug
---

# Connector

Connectors are objects used to create a link between two nodes. A connector is a line that has connection points at the ends of the line and stays connected to the elements that you attach it to.

{% include image.html url="/js/Diagram/Connector_images/Connector_img1.jpg" Caption="Connector"%}

## Create Connector

**Connector** is created from JSON data and added to the Diagram model using Diagram Model’s **connectors** property. The connector’s name must be unique. By default, the connector type is “straight”. The following code illustrates how to create a Connector and add it to **Diagram**.

{% highlight js %}

//create a connector 
var connectors = [{
   name: "connector",
   lineWidth: 2,
   sourcePoint: {
      x: 300,
      y: 40
   },
   targetPoint: {
      x: 400,
      y: 150
   }
}];
//add connectors to diagram
$("#Diagram").ejDiagram({
   connectors: connectors
});
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img2.png" Caption="Connector"%}

## Segments

The connector has three types of segments.

* Orthogonal Segments
* Straight Segments
* Bezier Segments

### Orthogonal Segments

Orthogonal segments are visually represented based on the specified length and direction values. The following code example illustrates how to add a **Connector** with an **Orthogonal Segment.**

{% highlight js %}

//initializing model.connectors
var connectors = [];
//Default Orthogonal Segment
var segments = [{ type: "orthogonal"}];

//create a connector 
var connectors = [{
   name: "connector",
   lineWidth: 2,
   segments: segments,
   sourcePoint: {
      x: 300,
      y: 40
   },
   targetPoint: {
      x: 400,
      y: 150
   }
}];
//add connectors to diagram model
$("#Diagram").ejDiagram({
   connectors: connectors
});
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img3.png" Caption="Orthogonal Segment"%}

The following code illustrates how to customize **Orthogonal Segment**.

{% highlight js %}

//Segments with direction and length
var segments = [{
   type: "orthogonal",
   direction: "bottom",
   length: 90
}];
//create a connector 
var connectors = [{
   name: "connector",
   lineWidth: 2,
   segments: segments,
   sourcePoint: {
      x: 300,
      y: 40
   },
   targetPoint: {
      x: 400,
      y: 150
   }
}];
//add connectors to diagram model
$("#Diagram").ejDiagram({
   connectors: connectors
});
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img4.png" Caption="Orthogonal Segment"%}

### Straight Segment

The straight segments can be added by specifying points as to where the line has to be drawn. The segment end point links the source point and target point of the connector. The following code example illustrates how to add **Straight Segment** through code.

{% highlight js %}

//Adding straight segments
var segments = [{
   type: "straight",
   point: {
      x: 400,
      y: 150
   }
}, {
   type: "straight",
   point: {
      x: 300,
      y: 10
   }
}];
var connector = [{
   segments: segments,
   targetPoint: {
      x: 300,
      y: 150
   },
   sourcePoint: {
      x: 300,
      y: 150
   }
}];
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img5.png" Caption="Polyline"%}

{% include image.html url="/js/Diagram/Connector_images/Connector_img6.png" Caption="Single Line"%}

The control points can be added or deleted at runtime with shortcut key combination **ctrl + shift +click** on the control point.

### Bezier Segment

Bezier segments can be added through points or vector.

* **Points (point1, point2)** are absolute and are specified based on the origin of page.
* **Vectors (vector1, vector2)** are relative and are specified based on the length and angle between end points and control points.

The following code example illustrates how to add Bezier segments.

{% highlight js %}

//Adding segments with control points
//Adding Control Points
var segments = [{
   type: "bezier",
   point1: {
      x: 40,
      y: 80
   },
   point2: {
      x: 40,
      y: 72
   }
}];
var connector = [{
   segments: segments,
   sourcePoint: {
      x: 290,
      y: 150
   },
   targetPoint: {
      x: 210,
      y: 40
   }
}];
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img7.png" Caption="Bezier Segments"%}

The following code example illustrates how to add vector point for Bezier segments.

{% highlight js %}
//Adding Bezier through vectors
var segments = [{ type: "bezier", 

   //Length and angle between source point and control point 1
   vector1: {
      angle: 180,
      distance: 120
   },
   //Length and angle between target point and control point 2
   vector2: {
      angle: 10,
      distance: 140
   }
}];
var connectors = [{
   segments: segments,
   sourcePoint: {
      x: 310,
      y: 180
   },
   targetPoint: {
      x: 190,
      y: 40
   }
}];
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img8.png" Caption="Bezier segment with vectors"%}

### Editing Segments

The segments can be edited during runtime by dragging control thumbs. Segments can be updated when neighboring segments are adjusted.

{% include image.html url="/js/Diagram/Connector_images/Connector_img9.png" Caption="Segment Editing"%}

## Connector Padding

**Connector Padding** allows you to adjust the space between connector’s end point and the object to which it is connected (Node, Group, or Port). 

### Endpoint adjustment specific to connector ends

Padding distance between source or target end with its connected end (Node, Group, or Port) can be adjusted by using **sourcePadding** and **targetPadding,** respectively. The following code examples illustrate how to adjust the distance by using **padding** property.

{% highlight js %}

//Sets padding for the Connector.
var connector = [{
   sourcePadding: 15,
   targetPadding: 20
}];
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img10.png" Caption="Endpoint’s adjustment specific to connector’s ends"%}

### Endpoint adjustment specific to nodes

**ConnectorPadding** property of a node is used to specify the amount of space needed in pixels between a node and all its connected edges. The following code examples illustrate how to pad edges connected to a node.

{% highlight js %}

//Sets padding for a Node.
var node = [{
   connectorPadding: 20
}];
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img11.png" Caption="Endpoint’s adjustment specific to nodes"%}

### Endpoint adjustment specific to ports

**ConnectorPadding** property of a port is used to specify the amount of space needed in pixels between a port and all its connected edges. The following code examples illustrate how to pad edges connected to a port.

{% highlight js %}

//Sets Padding for a port.
var port = [{
   connectorPadding: 20
}];
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img12.png" Caption="Endpoint’s adjustment with specific to ports"%}

## Line Bridging

**Line Bridging** creates a bridge for lines to smartly cross over other lines, at points of intersection. When two line connectors meet each other, the line with the higher z-order draws an arc over the line with lower z-order. Only straight and orthogonal connectors support line bridging. Line bridging is disabled by default, you can enable it by adding **ConnectorConstraints.Bridging** in constraints. The following code illustrates how to enable line bridging.

{% highlight js %}

//Enable Line Bridging for a single connector
var constraints = ej.datavisualization.Diagram.ConnectorConstraints;

var constraint = constraints.Bridging | constraints.Default;
var connector = [{
   constraints: constraint
}];


//Enable Line Bridging for all connectors added to diagram model
var constraints = ej.datavisualization.Diagram.DiagramConstraints;

var constraint = constraints1.Bridging | constraints1.Default;

//Initialize the diagram
$("#diagram").ejDiagram({
constraints: constraint;
});
});
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img13.png" Caption="Line Bridging"%}

When the connector constraint is set as **ConnectorConstraints.InheritBridging,** bridging is based on **DiagramConstraints**.

### Line Bridging Direction

Direction of the Line Bridge can be customized using the **BridgeDirection** property. This property decides the intersecting segment that shows a bridge based on your preferred direction. The default value for the Diagram model’s **BridgeDirection** property is **ej.datavisualization.Diagram.BridgeDirection.Top**.

<table>
<tr>
<td>
<b> Properties</b></td><td>
<b>Description</b></td><td>
<b>Value</b></td></tr>
<tr>
<td>
bridgeDirection</td><td>
Gets or sets the BridgeDirection for horizontal and vertical lines.</td><td>
Enum<br/>
BridgeDirection.Left<br/>BridgeDirection.Right<br/>BridgeDirection.Top<br/>BridgeDirection.Bottom</td></tr>
</table>

_BridgeDirection Property_

The following code example is used to set Bridge Direction.

**Example 1:** Bridge for Horizontal Connector, with BridgeDirection as Top.

{% highlight js %}

//setting the Bridge Direction
$("#diagram").ejDiagram({
   bridgeDirection: ej.datavisualization.Diagram.BridgeDirection.Top
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img14.png" Caption="BridgeDirection.Top"%}

**Example 2:** Bridge for Vertical Connector, with BridgeDirection as Left.

{% highlight js %}

//setting the Bridge Direction
$("#diagram").ejDiagram({
   bridgeDirection: ej.datavisualization.Diagram.BridgeDirection.Left
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img15.png" Caption="BridgeDirection.Left"%}

The following API method is used to change the BridgeDirection at runtime.                                                                                                

{% highlight js %}

var diagram = $("#diagram").ejDiagram("instance");
//update the Bridge Direction at runtime.
diagram.update({
         bridgeDirection: ej.datavisualization.Diagram.BridgeDirection.Top
      });
{% endhighlight %}

## Corner Radius

**Corner Radius** support enables you to create connectors with rounded corners. The following code example illustrates how to set corner radius for connectors.

{% highlight js %}
//For node creation refer the link Node Creation
//For Creating connection refer the link Connecting nodes
//Adding corner radius for connector
var connector = {
   cornerRadius: 20
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img16.png" Caption="Corner Radius"%}

## Connecting Nodes

Connector is connected to the bounds of the node and at a specific point on the node .You are required to assign the source node name to connector’s **sourceNode** property and target node name to connector’s **targetNode** property, in order to establish the connection. The port to port connection between specific points on node is established by assigning the name of the node’s port to connector’s **targetPort /sourcePort**. At runtime, you can change the point of connection while dragging or rotating node.

{% highlight js %}

//for node creation refer the link Node creation
//create a connection between headNode/tailNode using connector

var connector = [{
   segment: type: ej.datavisualization.Diagram.Segment.Orthogonal
}, sourceNode: "headNode", //set name of sourceNode
targetNode: "tailNode" //set name of targetNode
}];
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img17.jpeg" Caption="Node to Node Connection"%}

The point of connection is changed optimally at runtime while performing operations such as Rotating and Dragging on **Source/Target Node** of Connector. In case of static or specific point connection at runtime, the **Port** assists to maintain specific point connection between Nodes.

## Connecting Ports

**Port** establishes the connection with nodes at a specific point. For creating specific port connection, refer the link [Port to Port Connection.](/js/Diagram/Port)

## Appearance

You can customize the appearance of the connector by setting a desired value to the appropriate appearance properties. The following code illustrates how to customize the appearance of connector.

<table>
<tr>
<td>
<b>Properties</b></td><td>
<b>Data Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
linewidth</td><td>
number</td><td>
Gets or sets the width of the line</td></tr>
<tr>
<td>
lineDashArray</td><td>
string</td><td>
Gets or sets the pattern of dashes and gaps used to stroke connector border.</td></tr>
<tr>
<td>
lineColor</td><td>
String</td><td>
Gets or sets the line color of the connector</td></tr>
<tr>
<td>
opacity</td><td>
number</td><td>
Gets or sets the opacity of the connector</td></tr>
</table>


{% highlight js %}
//set various appearance properties to connector
var segments = [{
   type: "orthogonal"
}];

connectors = [{
   name: "connector1",
   lineWidth: 2,
   segments: segments,
   sourcePoint: {
      x: 210,
      y: 40
   },
   targetPoint: {
      x: 450,
      y: 150
   },
   lineColor: "black"
}];
{% endhighlight %}

## Decorator

You can decorate the source point and target point of the connector using decorator shape. The **sourceDecorator** and **targetDecorator** properties are used to add decorators to connector. The following code illustrates how decorator is created and added at connector’s target point.

{% highlight js %}

//set targetDecorator and sourceDecorator
var connector = [{
   targetDecorator: {
      shape: ej.datavisualization.Diagram.DecoratorShapes.Arrow,
      width: 10,
      height: 10
   },
   sourceDecorator: {
      shape: ej.datavisualization.Diagram.DecoratorShapes.Circle,
      width: 10,
      height: 10
   }
}];

{% endhighlight %}

### Decorator Appearance

Decorator appearance is customized by setting desired value to the appropriate appearance properties.

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
Gets or sets the width of the decorator.</td></tr>
<tr>
<td>
 height</td><td>
 number</td><td>
Gets or sets the height of the decorator.</td></tr>
<tr>
<td>
 borderColor</td><td>
 string</td><td>
Gets or sets the border color of the decorator.</td></tr>
<tr>
<td>
 fillColor</td><td>
 string</td><td>
Gets or sets the fill color of the decorator.</td></tr>
<tr>
<td>
 shape</td><td>
 ej.datavisualization.Diagram.DecoratorShapes</td><td>
Gets or sets the shape of the decorator.</td></tr>
<tr>
<td>
 pathData</td><td>
 string</td><td>
Gets or sets the path data of the decorator.</td></tr>
</table>

_Decorator Appearance_

The following code illustrates how to customize Decorator Shape.

{% highlight js %}

//set various appearance properties to decorator
var connector = [{
   targetDecorator: {
      shape: ej.datavisualization.Diagram.DecoratorShapes.Arrow
   },
   sourceDecorator: {
      shape: ej.datavisualization.Diagram.DecoratorShapes.Circle,
      fillColor: "#606060",
      borderColor: "black",
      width: 8,
      height: 8
   }
}];

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img18.jpeg" Caption="Decorator Shape"%}

## Constraints

You can enable or disable certain behaviors of Connectors using the **constraints** property.

<table>
<tr>
<td>
<b>Constraints</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
None</td><td>
Disable all the constraints.</td></tr>
<tr>
<td>
Select</td><td>
Enables or disables selection.</td></tr>
<tr>
<td>
Delete</td><td>
Enables or disables deletion.</td></tr>
<tr>
<td>
Drag</td><td>
Enables or disables dragging.</td></tr>
<tr>
<td>
DragSourceEnd</td><td>
Enables or disables the source end to be dragged.</td></tr>
<tr>
<td>
DragTargetEnd</td><td>
Enables or disables the target end to be dragged.</td></tr>
<tr>
<td>
DragsegmentThumbs</td><td>
Enables or disables control point and end point of every segment in a connector for editing.</td></tr>
<tr>
<td>
Bridging</td><td>
Enables or disables bridging to the connector.</td></tr>
<tr>
<td>
DragLabel</td><td>
Enables or disables label of node to be dragged.</td></tr>
<tr>
<td>
InheritBridging</td><td>
Enables or disables bridging based on the diagram constraints.</td></tr>
<tr>
<td>
Default</td><td>
Enables all constraints.</td></tr>
</table>

_Constraints_

The default value for the connector constraints property is ej.datavisualization.Diagram.ConnectorConstraints.Default.

**Example**

The following code illustrates how to disable select constraints of connector. Disabling select constraints does not allow you to select connector.

{% highlight js %}

//disable select constraint
connector.constraints = connector.Constraints & ~(ej.datavisualization.Diagram.ConnectorConstraints.Select);
{% endhighlight %}

> **Note:** Connector’s constraints property is manipulated using bitwise operations. For more information about bitwise operations, see [Bitwise Operations](/js/Diagram/How-To/Bitwise-Operations). 
