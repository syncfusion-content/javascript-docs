---
layout: post
title: Label
description: label
platform: js
control: Diagram
documentation: ug
---

# Label

**Label** is a block of text that is displayed over a node or a connector. **Label** is used to textually represent an object with a string that can be edited in run time. **Label** has properties for text appearance, customization and alignment. You can add **Multiple Labels** to a node/connector.

## Create Label

Node’s/Connector’s **labels** property holds an array of **Label** objects. The following code illustrates how to create a **Label**.

{% highlight js %}

//create a label 
var node = {
   name: "node",
   labels: [{
      "text": "Label"
   }]
};
var connector = {
   name: "connector",
   labels: [{
      "text": "Label"
   }]
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img1.png" Caption="Label"%}

## Displacement

A **Label** can be displaced from its original position both interactively, that is, by dragging and programmatically. The following code illustrates how to enable **Label Displacement** through interaction.

{% highlight js %}

//Enables Label Dragging for node.  
var constraints = ej.datavisualization.Diagram.NodeConstraints;
var constraints = constraints.Default | constraints.DragLabel;
var node = {
   constraints: constraints
};

//Enables Label Dragging for connector.
var constraints = ej.datavisualization.Diagram.ConnectorConstraints;
var constraints = constraints.Default | constraints.DragLabel;
var connector = {
   constraints: constraints
};

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img2.png" Caption="Label Dragging"%}

The following code illustrates how to displace labels through API.

{% highlight js %}

var node = {
   name: "Meeting",
   width: 150,
   height: 60,
   labels: [{
      "text": "Progress",
      margin: {
         "left": 100,
         "top": 100
      },
      offset: {
         x: 0,
         y: 0
      },
      horizontalAlignment: "left",
      verticalAlignment: "top"
   }]
}

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img3.png" Caption="Label Displacement through margin"%}

## Label Rotation

**Diagram** provides support to rotate labels. You can rotate labels to some specified angles. The following code illustrates how to specify the rotation angle for labels.

{% highlight js %}

//Label Rotate Angle for node and connector.
var node = {
   labels: [{
      text: "Label",
      rotateAngle: 45
   }]
};

var connector = {
   labels: [{
      text: "Label",
      rotateAngle: 45
   }]
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img4.png" Caption="Rotated Label"%}

> **Note:** No built-in support is added to rotate labels interactively.

## Appearance 

You can customize the **Label appearance** and position using its properties.

{% highlight js %}

//set various appearance properties to label
var label = {
   "text": "Label Text",
   "fontSize": 12,
   "fontFamily": "TimesNewRoman",
   italic: true,
   "fontColor": "black",
   "fillColor": "White",
   "borderColor": "black",
   "borderWidth": 1,
   wrapText: true,
   textDecoration: ej.datavisualization.Diagram.TextDecorations.LineThrough
};

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img5.png" Caption="Customized Label"%}

## Label Editing

Label can be edited at runtime, programmatically or interactively. By default, label is in **view** mode. But it can be brought to edit mode in two ways; by double clicking on the label, or by programmatically setting the mode to ‘**Edit’** as shown in the following code example. Label editing is automatically terminated when the Edit box loses its focus or by setting its mode back to **view**.

{% highlight js %}
//label edit mode
var label = {
   "text": "Label",
   mode: ej.datavisualization.Diagram.LabelEditMode.Edit
};
var diagram = $("#Diagram").ejDiagram("instance");
var node = diagram.model.selectedItems.children[0];
diagram.updateLabel(node.name, node.labels[0], label);

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img6.png" Caption="Label Mode"%}

## Read-only Label

To prevent label editing, set Label’s **readOnly** property as **“True”.** After setting the **Label** to **readOnly** mode, when you double clicking on the Label, it is not moved to **Edit** mode. However, even after **readOnly** is set as true, you can programmatically move the label to edit mode.

{% highlight js %}

//label readOnly mode
var label = {
   readOnly: true
};
var diagram = $("#Diagram").ejDiagram("instance");
var node = diagram.model.selectedItems.children[0];
diagram.updateLabel(node.name, node.labels[0], label);

{% endhighlight %}

## Label Alignment

You can align the Label using its alignment properties.

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
textAlign</td><td>
ej.datavisualization.Diagram.TextAlign</td><td>
Gets or sets text alignment of label</td></tr>
<tr>
<td>
horizontalAlignment</td><td>
ej.datavisualization.Diagram.HorizontalAlignment</td><td>
Gets or sets label horizontal alignment of node/connector.</td></tr>
<tr>
<td>
verticalAlignment</td><td>
ej.datavisualization.Diagram.VerticalAlignment</td><td>
Gets or sets label vertical alignment of  node/connector</td></tr>
<tr>
<td>
margin</td><td>
ej.datavisualization.Diagram.Margin</td><td>
Gets or sets the margin for the label.</td></tr>
<tr>
<td>
offset</td><td>
ej.datavisualization.Diagram.Point</td><td>
Gets or sets the position for the label.</td></tr>
</table>

_Label Alignment_

{% highlight js %}

//align label and its text
var label = {
   text: "Label",
   offset: {
      x: 0,
      y: 0.5
   },
   verticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Top,
   horizontalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Center,
   textAlign: ej.datavisualization.Diagram.TextAlign.Center
};               

{% endhighlight %}

<table>
<tr>
<td>
<b>Horizontal Alignment</b></td><td>
<b>Vertical Alignment</b></td><td>
<b>Offset</b></td><td>
<b>Image</b></td></tr>
<tr>
<td>
Center</td><td>
Top</td><td>
(0.2,1)</td><td>
<img src="/js/Diagram/Label_images/Label_img7.png" alt="" width="89pt" height="89pt"/></td></tr>
<tr>
<td>
Right</td><td>
Middle</td><td>
(0.5,0.3)</td><td>
<img src="/js/Diagram/Label_images/Label_img8.png" alt="" width="74pt" height="62pt"/></td></tr>
<tr>
<td>
Left</td><td>
Bottom</td><td>
(0.5,0.7)</td><td>
<img src="/js/Diagram/Label_images/Label_img9.png" alt="" width="68pt" height="58pt"/></td></tr>
</table>

_Alignment_

{% include image.html url="/js/Diagram/Label_images/Label_img10.png" Caption="Left align"%}

{% include image.html url="/js/Diagram/Label_images/Label_img11.png" Caption="Label Alignment"%}

## Text Wrapping

**Wrapping** property of label allows to specify whether or not to wrap the text, when it reaches the edge of the containing node. 

The following code illustrates how to wrap text.

{% highlight js %}
//label WrapText mode 
var label = {
   wrapping: ej.datavisualization.Diagram.Wrapping.Wrap
};

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img12.png" Caption="Text Wrapping"%}

<table>
<tr>
<td>
<b>Values</b></td><td>
<b>Description</b></td><td>
<b>Image</b></td></tr>
<tr>
<td>
NoWrap</td><td>
Text is not wrapped.</td><td>
<img src="/js/Diagram/Label_images/Label_img13.png" alt="" width="158pt" height="55pt" /></td></tr>
<tr>
<td>
Wrap (Default)</td><td>
Text-wrapping occurs when the text overflows beyond the available node width.</td><td>
<img src="/js/Diagram/Label_images/Label_img14.png" alt="" width="95pt" height="55pt"/></td></tr>
<tr>
<td>
WrapWithOverflow</td><td>
Text-wrapping occurs when the text overflows beyond the available node width. However, a text may overflow beyond the node width in the case of a very long word.</td><td>
<img src="/js/Diagram/Label_images/Label_img15.png" alt="" width="122pt" height="57pt"/></td></tr>
</table>

_Text Wrapping_

### Width

By default, label wraps the text based on its parent element’s size (node/group/connector). You can override this by using **width** property. When the label width is set, label acts like a container and wraps the label based on width specified. The following code example illustrates how to set the label width.

{% highlight js %}

//label width 
var label = {width: 50};

{% endhighlight %}

## Multiple Labels 

You can add **Multiple Labels** to the node /connector.

The following code illustrates how to create multiple labels to node 

{% highlight js %}

//add multiple labels to node
var node = {
   labels: [{
      text: "Left",
      offset: {
         x: 0.1,
         y: 0.1
      }
   }, {
      text: "Right",
      offset: {
         x: 0.9,
         y: 1
      }
   }, {
      text: "Center",
      offset: {
         x: 0.5,
         y: 0.5
      }
   }]
};

{% endhighlight %}

{% include image.html url="/js/Diagram/Label_images/Label_img16.png" Caption="Multiple Label and Alignment"%}
