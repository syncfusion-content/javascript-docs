---
layout: post
title: Constraints | Diagram | Javascript | Syncfusion
description: This section explains how to use the Constraints to enable or disable certain behaviors of the diagram, node, and connector in ejDiagram.
platform: js
control: Diagram
documentation: ug
api: /api/js/ejdiagram
---

# Constraints
Constraints are used to enable/disable certain behaviors of the diagram, node and connector. Constraints are provided as flagged enumerations, so that multiple behaviors can be enabled/disabled with bitwise operators (`&`, `|`, `~`, `<<`, etc.).
To know more about bitwise operators, refer to [Bitwise Operations](#bitwise-operations) 

## DiagramConstraints
Diagram constraints allow to enable or disable the following behaviors.

* Page Editing
* Line Bridging
* Zoom and Pan
* Undo Redo
* Crisp Edges
* Resizing

For more information about Diagram constraints, refer to [Diagram Constraints](/api/js/ejdiagram#members:constraints "Diagram Constraints").

**Example**

The following example illustrates how to disable page editing.

{% highlight javascript %}

var DiagramConstraints = ej.datavisualization.Diagram.DiagramConstraints;
//Disables PageEditing
$("#diagram").ejDiagram({
	constraints: DiagramConstraints.Default & ~DiagramConstraints.PageEditable
});

{% endhighlight %}

## NodeConstraints

NodeConstraints allows to enable or disable the following behaviors of node.

* Selection
* Deletion
* Drag
* Resize
* Rotate
* Connect
* Drop shadow
* Drag label
* Define tooltip
* Crisp Edges
* Interaction

For more information about node constraints, refer to [Node Constraints](/api/js/ejdiagram#members:nodes-constraints "Node Constraints")

**Example**

The following code illustrates how to disable rotation.

{% highlight javascript %}

//Disables rotation
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
var nodes = [{
	name: "node",
	constraints: NodeConstraints.Default & ~NodeConstraints.Rotate
}];

$("#diagram").ejDiagram({
	nodes: nodes,
});

{% endhighlight %}

## ConnectorConstraints

ConnectorConstraints allow to enable or disable certain behaviors of Connectors. They are as follows.

* Selection
* Deletion
* Drag
* Segment editing
* Define tooltip
* Bridging
* Label dragging
* Crisp Edges
* Interaction

For more information about connector constraints, refer to [Connector Constraints](/api/js/ejdiagram#members:connectors-constraints "Connector Constraints")

**Example**

The following code illustrates how to disable selection.

{% highlight javascript %}

//Disables selection
var ConnectorConstraints = ej.datavisualization.Diagram.ConnectorConstraints;
var connectors = [{
	name: "connector",
	constraints: ConnectorConstraints.Default & ~ConnectorConstraints.Select
}];

$("#diagram").ejDiagram({
	connectors: connectors,
});

{% endhighlight %}

## PortConstraints

You can enable or disable certain behaviors of Port. They are as follows.

* Connect
* ConnectOnDrag

For more information about port constraints, refer to [Port Constraints](/api/js/ejdiagram#members:nodes-ports-constraints "Port Constraints")

**Example**

The following code illustrates how to disable creating connections with a port.

{% highlight javascript %}

var PortConstraints = ej.datavisualization.Diagram.PortConstraints;
var nodes = [{
	name: "node",
	ports: [{
		//Sets the port as not getting connected
		constraints: PortConstraints.None
	}]
}];

$("#diagram").ejDiagram({
	nodes: nodes,
});

{% endhighlight %}

## SelectorConstraints
Selector visually represents the selected elements with certain editable thumbs. The visibility of the thumbs can be controlled with selector constraints. The part of selector is categorized as follows.

* Resizer
* Rotator
* User handles

For more information about Selector constraints, refer to [Selector Constraints](/api/js/ejdiagram#members:selecteditems-constraints "Selector Constraints")

**Example**

The following code illustrates how to hide rotator.

{% highlight javascript %}

var SelectorConstraints = ej.datavisualization.Diagram.SelectorConstraints;
$("#diagram").ejDiagram({
	selectedItems: {
		//Hides rotator
		constraints:SelectorConstraints.All & ~SelectorConstraints.Rotator
	}
});

{% endhighlight %}

## SnapConstraints

Snap Constraints control the visibility of gridlines and enable/disable snapping. Snap constraints allow to set the following behaviors.

* Show only horizontal or vertical gridlines
* Show both horizontal and vertical gridlines
* Snap to either horizontal or vertical gridlines
* Snap to both horizontal and vertical gridlines

For more information about snap constraints, refer to [Snap Constraints](/api/js/ejdiagram#members:snapsettings-snapconstraints "Snap Constraints")

**Example**

The following code illustrates how to show only horizontal gridlines.

{% highlight javascript %}

$("#diagram").ejDiagram({
	snapSettings: {
		//Shows horizontal gridlines
		snapConstraints: ej.datavisualization.Diagram.SnapConstraints.ShowHorizontalLines
	}
});

{% endhighlight %}

## Inherit behaviors

Some of the behaviors can be defined through both the specific object(node/connector) and Diagram. When the behaviors are contradictorily defined through both, the actual behavior is set through inherit options.

The following code example illustrates how to inherit the line bridging behavior from the Diagram model.

{% highlight javascript %}

// Enables/disables line bridging based on the Diagram constraints
var ConnectorConstraints = ej.datavisualization.Diagram.ConnectorConstraints;
var DiagramConstraints = ej.datavisualization.Diagram.DiagramConstraints;
var connectors = [{
	name: "connector",
	sourcePoint: { x: 100, y: 100 },
	targetPoint: { x: 200, y: 200 },

	//Sets to inherit bridging from model
	constraints: ConnectorConstraints.Default | ConnectorConstraints.InheritBridging
}];

$("#diagram").ejDiagram({
	connectors: connectors,

	//Enables line bridging for all connectors
	constraints: DiagramConstraints.Default | DiagramConstraints.Bridging
});

{% endhighlight %}


## Bitwise Operations

**Bitwise Operations** are used to manipulate the flagged enumerations [enum]. In this section, Bitwise Operations are illustrated by using node Constraints. The same is applicable while working with Node Constraints, Connector Constraints, or Port Constraints.

### Add Operation

You can **add** or **enable** multiple values at a time by using **Bitwise** ‘\|’ (OR) **operator**.

{% highlight javascript %}

node.constraints = ej.datavisualization.Diagram.NodeConstraints.Select | ej.datavisualization.Diagram.NodeConstraints.Rotate;

{% endhighlight %}

In the above example, you can do both the selection and rotation.

### Remove Operation

You can **remove** or **disable** values by using **Bitwise** ‘&~’ (XOR) **operator**.

{% highlight javascript %}

var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
node.constraints = node.constraints & ~(NodeConstraints.Rotate);

{% endhighlight %}

In the above example, **Rotation** is disabled but other constraints are enabled.

### Check Operation

You can check any value by using **Bitwise** ‘&’ (AND) **operator**.

{% highlight javascript %}

if ((node.constraints & (ej.datavisualization.Diagram.NodeConstraints.Rotate)) == (ej.datavisualization.Diagram.NodeConstraints.Rotate));

{% endhighlight %}

In the above example, you can check whether the rotate constraints are enabled in a Node. When Node constraints have rotate constraints, the expression returns a rotate constraint.
