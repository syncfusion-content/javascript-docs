---
layout: post
title: Node
description: node
platform: js
control: Diagram
documentation: ug
---

# Node

Nodes are graphical object that represents visual data to be placed on the page.

{% include image.html url="/js/Diagram/Node_images/Node_img1.png" Caption="Node"%}

## Create Node

Node is created from JSON data and added to the **Diagram** model using diagram model’s **node** property. The node’s name must be unique. The following code illustrates how to create a node and add it to the **Diagram.**

{% highlight js %}

//node array
var nodes = [];
var node =
   //create a node with default shape (Rectangle)
   {
      name: "Rect1",
      width: 100,
      height: 100,
      offsetX: 400,
      offsetY: 60,
      fillColor: "darkCyan",
      borderWidth: 2
   };
nodes.push(node);

//add nodes to Diagram
$("#Diagram").ejDiagram({
   nodes: nodes
});
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img2.png" Caption="Node"%}

List of preloaded nodes from symbol palette are added to the **Diagram** by clicking on the palette nodes or by dragging a node and dropping on the **Diagram**. The method to add node/connector to palette and drag and drop on **Diagram** is explained in palettesection

## Node Shapes

**Diagram** has a collection of predefined shapes. The shape to be drawn can be set by using a set of shape specific properties. The most commonly used shapes are:

* Rectangle (A type of basic shape)
* Ellipse (A type of basic shape)
* Html
* Text
* Native
* Path (A type of basic shape)
* Polygon (A type of basic shape)
**Rectangle**

You can create a rectangle shape by setting the type of node’s type as **ej.datavisualization.Diagram.Shapes.Basic** and node’s shape as **ej.datavisualization.Diagram.BasicShapes.Rectangle**. The following code illustrates how a rectangle node is created.

{% highlight js %}

var Diagram = ej.datavisualization.Diagram;

//create a node with rectangle shape
var node = {
   type: Diagram.Shapes.Basic,
   shape: Diagram.BasicShapes.Rectangle
};

//create a node with rounded rectangle shape
node = {
   type: Diagram.Shapes.Basic,
   shape: Diagram.BasicShapes.Rectangle,
   "cornerRadius": 5
};

//create a node with ellipse shape
node = {
   type: Diagram.Shapes.Basic,
   shape: Diagram.BasicShapes.Ellipse
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img3.png" Caption="Built-in Shapes"%}

**Html**

**Html** elements are embedded in diagram through **Html shape node**. The following code illustrates how an **Html** node is created.

{% highlight html %}
//dependency scripts
<script src = "http://borismoore.github.io/jsrender/jsrender.min.js"> </script>

<script id="htmlTemplate" type="text/x-jsrender">
    <div>
        <input type="button" value="{{:value}}" />
    </div>
</script>
{% endhighlight %}

{% highlight js %}
var node = {
    type: ej.datavisualization.Diagram.Shapes.Html,
    templateId: "htmlTemplate",
    value: "button"
}
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img4.png" Caption="Html Shape"%}

**Text Node**

You can add Text to the **Diagram** using **Text shape node**. The text shape has **textblock** that contains text, font style and align properties. The following code illustrates how to create a **Text** node.

{% highlight js %}
//create a node with text content

var Diagram = ej.datavisualization.Diagram;

var node = {
   type: Diagram.Shapes.Text,
   textBlock: {
      "text": "TextNode",
      textAlign: Diagram.TextAlign.Center
   }
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img5.png" Caption="Text Shape"%}

**Path**

You can create complex shapes using **Path shape node**. It is achieved by assigning path string to shape’s **pathData**. The following code illustrates how a **Path node** is created.

{% highlight js %}

//create a node with path shape
var Diagram = ej.datavisualization.Diagram;

var node = {
   type: Diagram.Shapes.Basic,
   shape: Diagram.BasicShapes.Path,
   pathData: "M 67.2947 100 L 67.2947 0.00102291 L 59.138 0.00102291 M 100 50 L 66.8899 50 M 33.1101 50 L 0 50 M 33.1101 0 L 67.5585 50.0015 L 33.1101 99.9995 Z"
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img6.png" Caption="Path Shape"%}

**Polygon**

You can create **Polygon** shape by setting node’s type as **ej.datavisualization.Diagram.Shapes.Polygon** and assigns the desired points to the node’s **point** property.

{% highlight js %}

var Diagram = ej.datavisualization.Diagram;

var node = {
      type: Diagram.Shapes.Basic, 
      shape: Diagram.BasicShapes.Polygon, points: [
            { x: 0, y: 20 },
            { x: 25, y: 30 },
            { x: 0, y: 100 },
            { x: 100, y: 100 },
            { x: 75, y: 30 },
            { x: 100, y: 20 },
            { x: 75, y: 20 },
            { x: 75, y: 0 },
            { x: 25, y: 0 },
            { x: 25, y: 20 },
            { x: 0, y: 20 }
      ]
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img7.png" Caption="Polygon Shape"%}

### Native 

**Diagram** supports to add **SVG** content as shape content. It is achieved by setting node’s type as **ej.datavisualization.Diagram.Shapes.Native** and assigns the template id to the **templateId** property. The **templateId** property receives **id svg** template. The following code illustrates how a **Native node** is created.

{% highlight html %}
<!-- dependency scripts -->
<script src = "http://borismoore.github.io/jsrender/jsrender.min.js"> </script>

<script id="svgTemplate" type="text/x-jsrender">
    <g id="">
        <path d="M 58.813 0 H 3.182 L 30.998 24.141 L 58.813 0 Z M 32.644 34.425 C 32.133 34.87 31.567 35.095 31 35.095 S 29.867 34.87 29.353 34.425 L 1 9.826 V 60 H 61 V 9.826 L 32.644 34.425 Z ">
        </path>
        <text x="20" y="45"> { {: text } }
        </text>
    </g>
</script>
{% endhighlight %}

{% highlight js %}
var node = {
   type: ej.datavisualization.Diagram.Shapes.Native,
   templateId: "svgTemplate",
   text: "Mail"
}
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img8.png" Caption="Native Shape"%}

> **Note:** Shapes of type Node or HTML cannot be exported to an image format, like JPEG, PNG and BMP. It is by design that while exporting, diagram is drawn in a canvas. Further this canvas is exported into image formats. Currently, drawing in a canvas equivalent from all possible HTML and SVG elements is not feasible. Hence this limitation.

> **Note:** Fill color will be applied to the Native Node only when its inline style, or fill, for an SVG child element is not specified. In the following example, the node’s fill color is overridden by the specified color for the group.

{% highlight html %}
<svg>
   <g id=”task”>
      <g fill="#fff">
      </g>
   </g>
</svg>
{% endhighlight %}

**Image**

You can add **Image** as a node to the **Diagram** by setting node’s type as **ej.datavisualization.Diagram.Shapes.Image** and set the image **URL** to **source** property of shape. The following code illustrates how an **Image** node is created.

{% highlight js %}

//create a node with image
var node = {
   type: ej.datavisualization.Diagram.Shapes.Image,
    source: "sample/Syncfusion.PNG"
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img9.png" Caption="Image Shape"%}

## Shadow

**Drop shadow effect** for a **node** can be enabled or disabled by using the **NodeConstraints.Shadow**. The following image represents the **drop shadow effect** for a **Node**.

{% include image.html url="/js/Diagram/Node_images/Node_img10.png" Caption="Shadow"%}

The following code example illustrates how to enable or disable the **shadow**.

{% highlight js %}

//Enables Shadow for the node.
var node = {
   constraints: ej.datavisualization.Diagram.NodeConstraints.Default | ej.datavisualization.Diagram.NodeConstraints.Shadow
};
//Disables shadow for the node.
var node = {
   constraints: node.Constraints & ~ej.datavisualization.Diagram.NodeConstraints.Shadow
};
{% endhighlight %}

**Customizing Shadow**

Position and opacity of the **shadow** can be customized by using opacity, angle, and distance of the **shadow**. The following code example illustrates how to customize the **shadow.**

{% highlight js %}

//Shadow Customization.
var node = {
   shadow: {
      opacity: 0.8,
      distance: 9,
      angle: 50
   }
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img11.png" Caption="Shadow Customization"%}

## Appearance

You can customize the appearance of the shapes by using following properties.

<table>
<tr>
<td>
<b>Properties</b></td><td>
<b>Data Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
visible</td><td>
boolean</td><td>
Gets or sets the visibility of the node</td></tr>
<tr>
<td>
borderColor</td><td>
string</td><td>
Gets or sets the border color of the node</td></tr>
<tr>
<td>
fillColor</td><td>
string</td><td>
Gets or sets the fill color of the node</td></tr>
<tr>
<td>
opacity</td><td>
number</td><td>
Gets or sets the opacity of the node</td></tr>
<tr>
<td>
gradient</td><td>
object</td><td>
Gets or sets the gradient fill of the node</td></tr>
<tr>
<td>
borderDashArray</td><td>
string</td><td>
Gets or sets the pattern of dashes and gaps used to stroke node border.</td></tr>
<tr>
<td>
borderWidth</td><td>
number</td><td>
Gets or sets the width of node border.</td></tr>
</table>

_Appearance_

{% highlight js %}

//create linear gradient
var linearGradient = {
   type: "linear",
   x1: 0,
   x2: 50,
   y1: 0,
   y2: 50,
   stops: [{
      color: "white",
      offset: 0
   }, {
      color: "darkCyan",
      offset: 100
   }]
};

//set various appearance properties to node
var node = {
   visible: true,
   "borderColor": "black",
   "borderWidth": 2,
   opacity: 1,
   gradient: linearGradient,
   borderDashArray: "5 5"
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img12.png" Caption="Customized Node"%}

## Constraints

**Node Constraints**

You can enable or disable certain behaviors of **Nodes** by using Node’s **constraints** property.

<table>
<tr>
<td>
<b>Constraints</b></td><td>
<b>Description</b></td></tr>
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
Resize</td><td>
Enables or disables resizing.</td></tr>
<tr>
<td>
Drag</td><td>
Enables or disables dragging.</td></tr>
<tr>
<td>
Rotate</td><td>
Enables or disables rotation.</td></tr>
<tr>
<td>
Connect</td><td>
Enables or disables connection.</td></tr>
<tr>
<td>
ResizeNorthEast</td><td>
Enables or disables resizing nodes in the north east direction.</td></tr>
<tr>
<td>
ResizeEast</td><td>
Enables or disables resizing nodes in the east.</td></tr>
<tr>
<td>
ResizeSouthEast</td><td>
Enables or disables resizing nodes in the south east.</td></tr>
<tr>
<td>
ResizeSouth </td><td>
Enables or disables resizing nodes in the south.</td></tr>
<tr>
<td>
ResizeSouthWest</td><td>
Enables or disables resizing nodes in the south west.</td></tr>
<tr>
<td>
ResizeWest</td><td>
Enables or disables resizing nodes in the west.</td></tr>
<tr>
<td>
ResizeNorthWest</td><td>
Enables or disables resizing nodes in the north west direction.</td></tr>
<tr>
<td>
ResizeNorth </td><td>
Enables or disables resizing nodes in the north.</td></tr>
<tr>
<td>
Shadow</td><td>
Enables or disables Shadow.</td></tr>
<tr>
<td>
DragLabel</td><td>
Enables or disables label dragging.</td></tr>
<tr>
<td>
AllowPan</td><td>
Enables or disables panning while dragging nodes.</td></tr>
<tr>
<td>
AspectRatio</td><td>
Enables or disables proportional  resizing of nodes.</td></tr>
<tr>
<td>
Default</td><td>
Enables all the constraints.</td></tr>
<tr>
<td>
None</td><td>
Disables all the constraints.</td></tr>
</table>
_Constraints_

The Default value for the node constraints property is **ej.datavisualization.Diagram.NodeConstraints.Default.** The following code illustrates how to enable rotate, select constraints, and disable other constraints.

{% highlight js %}
 
//Applies selection and rotation constraints only.
node.constraints = ej.datavisualization.Diagram.NodeConstraints.Select | ej.datavisualization.Diagram.NodeConstraints.Rotate;
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img13.jpeg" Caption="Rotator Constraints–Enabled"%}

The following code illustrates how to disable rotate constraints. Disabling rotate constraint does not allow you to rotate the node.

{% highlight js %}

//Disables rotate constraint.
node.constraints = node.constraints & ~(ej.datavisualization.Diagram.NodeConstraints.Rotate);
{% endhighlight %}

{% include image.html url="/js/Diagram/Node_images/Node_img14.jpeg" Caption="Rotate Constraints-disabled"%}

> **Note:** Node’s constraints property is manipulated using bitwise operations. For more information about bitwise operations, see [Bitwise Operations](/js/Diagram/How-To/Bitwise-Operations).
