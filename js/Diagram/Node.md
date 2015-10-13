---
layout: post
title: Node
description: node
platform: js
control: Diagram
documentation: ug
---

# Node

Nodes are graphical objects used to visually represent the geometrical information, process flow, internal business procedure, entity or any other kind of data.

{% include image.html url="/js/Diagram/Node_images/Node_img1.png" %}

## Create Node

A node can be created and added to the Diagram, either programmatically or interactively. Nodes are stacked on diagram area from bottom to top in the order they are added.

### Add node through nodes collection

To create a node, You have to define the node object and add that to `nodes` collection of diagram model. The following code snippet illustrates how to add a node to diagram.

{% highlight js %}
// Define JSON to create a node
var node = {
    //Name of the node
    name: "node1",
    
    //Set the size
    width: 100,
    height: 100,

    //Set the position
    offsetX: 250,
    offsetY: 250,

    //Customize the appearance
    fillColor: "darkcyan",
    borderWidth: 2
    };

//add node to nodes collection
var nodes = [];
nodes.push(node);

//Initialize Diagram
$("#diagram").ejDiagram({
    width: "100%", height: "100%",
    //Initialize nodes collection
    nodes: nodes
});
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img2.png" %}

### Add node at runtime

Nodes can be added at runtime using public method `add`. The following code illustrates how to add a node using 'add' method.

{% highlight js %}
// Define JSON to create a node
var node = {
    name: "node1",
    width: 100,
    height: 100,
    
    //Set position
    offsetX: 250,
    offsetY: 250,
    fillColor: "darkcyan",
    borderWidth: 2
    };

var diagram = $("#diagram").ejDiagram("instance");

// add node to the diagram
diagram.add(node);

{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img3.png" %}

### Add node from palette

Nodes can be predefined and added to palette and can be dropped into diagram when needed. For more information about adding nodes from symbol palette, refer [Symbol Palette](/js/Diagram/Symbol-Palette).

### Create node through data source

Nodes can be generated automatically with the information provided through data source. The default properties for these nodes will be fetched from default settings. For more information about data source, refer [Data Binding](/js/Diagram/Data-Binding).

### Draw nodes

Nodes can be interactively drawn by clicking and dragging on diagram surface using **DrawingTool**. For more information about drawing nodes, refer [Draw Nodes](/js/Diagram/Tools "Drawing-Tools:Shapes").

### Update Node at runtime
     
The client side method `updateNode` is used to update the nodes at run time. The following code snippet illustrates how to update a node at runtime.

{% highlight js %}

    var diagram = $("#DiagramContent").ejDiagram("instance");
    diagram.updateNode("nodeName", {
                fillColor: "#1BA0E2",
                borderWidth: 5,
                borderColor: "#000000"
            })
{% endhighlight %}


## Position

Position of a node is controlled using its `offsetX` and `offsetY` properties. By default, these offset properties represent the distance between origin of diagram's page and node's center point. You may expect this offset values to represent the distance between page origin and node's top left corner instead of center. `pivot` property helps to solve this problem. Default value of node's pivot point is (0.5, 0.5), which means center of Node.

The following table illustrates how pivot relates offset values with node boundaries.

<table>
<tr>
<th>
Pivot</th><th>
Offset </th></tr>
<tr>
<td>
(0.5,0.5)</td><td>
offsetX and offsetY values will be considered as the node’s center point.</td></tr>
<tr>
<td>
(0,0)</td><td>
offsetX and offsetY values will be considered as the top left corner of node</td></tr>
<tr>
<td>
(1,1)</td><td>
offsetX and offsetY values will be considered as the bottom right corner of the node.</td></tr>
</table>


The following code illustrates how to change the `pivot` value.

{% highlight js %}
// Define JSON to create node

var nodes = [
    {
        name: "node", offsetX: 100, offsetY: 100,
        height: 100, width: 100,        
        shape: "rectangle",
        //Set pivot point 
        pivot: ej.datavisualization.Diagram.Point(0, 0)

    }
];
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img4.png" %}

## Types

Diagram allows to add different kind of nodes. To explore the types of nodes, refer [Types of Nodes](/js/Diagram/Shapes).

## Appearance

You can customize the appearance of a node by changing its font, fill colors, patterns, line weight and style, or shadow. The following code illustrates how to customize the appearance of the shape.

{% highlight js %}
var nodes = [{
    name: "node1",
    width: 100, height: 100,
    offsetX: 250, offsetY: 250,
    
    //Set styles to a node to customize the appearance
    fillColor: "darkcyan",
    borderWidth: 2,
    borderColor: "black",
    borderDashArray: "5 5",
}];

//Initialize Diagram
$("#diagram").ejDiagram({
    width: "100%", height: "100%",

    //Initialize nodes collection
    nodes: nodes
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img5.png" %}

### Gradient

There are two types of gradients.

* **Linear gradient -** Defines a smooth transition between a set of colors (so-called "stops") on a line. 

* **Radial gradient -** Defines a smooth transition between stops on a circle.

The `gradient` property of node allows you to define and apply the gradient effect to that node.

{% highlight js %}

//To create linear gradient

var linearGradient = {
    type: "linear",

    //start point of linear gradient
    x1: 0, y1: 0,

    //end point of linear gradient
    x2: 50, y2: 50,

    //Set an array of stop objects
    stops: [
        { color: "white", offset: 0 },
        { color: "darkCyan", offset: 100 }
    ]
};

//To create radial gradient

var radialGradient = {
    type: "radial",

    //center point of outer circle
    cx: 50, cy: 50,

    //center point of inner circle
    fx: 25, fy: 25,

    //radius of a radial gradient
    r: 50,

    //Set an array of stop objects
    stops: [
        { color: "white", offset: 0 },
        { color: "darkCyan", offset: 100 }
    ]
};

var nodes = [{
    name: "node1",
    width: 100, height: 100,
    offsetX: 250, offsetY: 250,

    //Set styles to a node to customize the appearance
    fillColor: "darkcyan",
    borderWidth: 2,
    gradient: linearGradient
 }];
{% endhighlight %}
 
{% include image.html url="/js/Diagram/Node_images/Node_img6.png" %}
 
## Shadow

**Diagram** provides support to add **shadow** effect to a node, which is disabled by default. It can be enabled with the `constraints` property of node. The following code illustrates how to drop shadow.

{% highlight js %}
var nodeConstraints = ej.datavisualization.Diagram.NodeConstraints;

//To enable Shadow effect for a node.
var constraints = nodeConstraints.Default | nodeConstraints.Shadow;

// Define JSON to create path node
var nodes = [
    {
        name: "node", offsetX: 100, offsetY: 100,
        height: 100, width:100,

        //Set shape of node
        shape: "rectangle",

        //Enables Shadow for the node.
        constraints: constraints
    }
];

{% include image.html url="/js/Diagram/Node_images/Node_img7.png" %}

The following code illustrates how to disable shadow effect at runtime.

var diagram = $("#diagram").ejDiagram("instance");
var node = diagram.findNode("node");

//To disable Shadow effect for a node.
constraints = node.constraints &~ nodeConstraints.Shadow;
diagram.updateNode("node", { constraints: constraints });
{% endhighlight %}


### Customizing Shadow

The angle, translation and opacity of the shadow can be customized with the `shadow` property of node. The following code snippet illustrates how to customize shadow.

{% highlight js %}
var nodes = [
    {
        name: "node", offsetX: 100, offsetY: 100,
        height: 100, width: 100,

        //Set shape of node 
        shape: "rectangle",

        //Enables Shadow for the node.
        constraints: constraints,

        //To customize shadow effect
        shadow: { opacity: 0.8, distance: 9, angle: 50}
    }
];
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img8.png" %}

## Interaction

Diagram provides support to drag, resize or rotate the node interactively. For more information about editing a node at runtime, refer [Interaction](/js/Diagram/Interaction).

## Constraints

The `constraints` property of node allows you to enable/disable certain features. For more information about node constraints, refer [Node Constraints](/js/Diagram/Constraints "NodeConstraints").
