---
layout: post
title: Draw shapes, selection rectangles, or Pan Diagram, when you click and drag over the Digram surface
description: How to draw shapes or pan Diagram by clicking and dragging over the Diagram surface?
platform: js
control: Diagram
documentation: ug
---

# Tools

## Drawing Tools

Drawing tool allows you to draw any kind of node/connector during runtime by clicking and dragging on the Diagram page. 

### Shapes

To draw a shape, you need to set the JSON of that shape to the `drawType` property of the Diagram model and you have to activate the drawing tool by using the `tool` property. The following code example illustrates how to draw a rectangle at run time. 

{% highlight js %}

var diagram = $("#diagram").ejDiagram("instance");

//JSON to create a rectangle
diagram.model.drawType = {
    type: ej.datavisualization.Diagram.Shapes.Basic,
    shape: "rectangle",
    //customize the appearance of the shape
    fillColor: "#fcbc7c",
    borderColor: "#f89b4c",
    labels: [{
        "text": "Rectangle"
    }]
};

//To draw an object once, activate draw once
diagram.update({
    tool: ej.datavisualization.Diagram.Tool.DrawOnce,
});

//To draw an object multiple times, activate continuous draw tool
diagram.update({
    tool: ej.datavisualization.Diagram.Tool.ContinousDraw,
});

{% endhighlight %}

![]("/js/Diagram/Tools_images/Tools_img1.png")

The following code example illustrates how to draw a path.

{% highlight js %}

     var diagram = $("#diagram").ejDiagram("instance");
     diagram.model.drawType = {
         name: "Path",
         fillColor: "#fbe172",
         labels: [{
             text: "Path"
         }],
         shape: "path",
         pathData: "M13.560 67.524 L 21.941 41.731 L 0.000 25.790 L 27.120 25.790 L 35.501 0.000 L 43.882 25.790 L 71.000 25.790 L 49.061 41.731 L 57.441 67.524 L 35.501 51.583 z "
     };
     
     //To draw an object once, activate draw once
    diagram.update({
        tool: ej.datavisualization.Diagram.Tool.DrawOnce,
    });

 {% endhighlight %}

![]("/js/Diagram/Tools_images/Tools_img3.png")    

### Connectors

To draw connectors, you have to set the JSON of the connector to `drawType` property. The drawing tool can be activated by using the `tool` property as shown. The following code example illustrates how to draw a straight line connector. 

{% highlight js %}

var diagram = $("#diagram").ejDiagram("instance");
//JSON to create a straight line connector
diagram.model.drawType = {
    type: "connector",
    segments: [{
        type: "straight"
    }]
};
//To draw an object once, activate draw once
diagram.update({
    tool: ej.datavisualization.Diagram.Tool.DrawOnce
});

{% endhighlight %}

![]("/js/Diagram/Tools_images/Tools_img2.png")

### Text 

Diagram allows you to create a textNode as soon as you click on the Diagram page. The following code illustrates how to draw a text.

{% highlight js %}

var diagram = $("#diagram").ejDiagram("instance");

//JSON to draw a text 
diagram.model.drawType = { type: "text" };

diagram.update({
    tool: ej.datavisualization.Diagram.Tool.DrawOnce
});

{% endhighlight %}

Once you activate the texttool, you can also able to perform label editing of a node/connector.

## Tool Selection

There are some functionalities that can be achieved by clicking and dragging on the Diagram surface. They are as follows.

* Draw selection rectangle - MultipleSelect tool
* Pan the Diagram - Zoom pan
* Draw nodes/connectors - ContinuousDraw / DrawOnce

As all the three behaviors are completely different, You can achieve only one behavior at a time based on the tool that you choose.
When more than one of those tools are applied, a tool is activated based on the precedence given in the following table. 

<table>
<tr>
<th>
Precedence</th><th>
Tools</th><th>
Description</th></tr>
<tr>
<td>
1st </td><td>
ContinuesDraw</td><td>
Allows you to draw the nodes or connectors continuously. Once it is activated, you cannot perform any other interaction in the Diagram. </td></tr>
<tr>
<td>
2nd </td><td>
DrawOnce</td><td>
Allows you to draw single node or connector. Once you complete the drawOnce action, SingleSelect and MultipleSelect tools are automatically enabled. </td></tr>
<tr>
<td>
3rd </td><td>
ZoomPan</td><td>
Allows you to pan the Diagram. When you enable both the SingleSelect and ZoomPan tools, you can perform the basic interaction as the cursor hovers node/connector. Panning is enabled when cursor hovers the Diagram.</td></tr>
<tr>
<td>
4th </td><td>
MultipleSelect</td><td>
Allows you to select multiple nodes and connectors. When you enable both the MultipleSelect and ZoomPan tools, cursor hovers the Diagram. When panning is enabled, you cannot select multiple nodes. </td></tr>
<tr>
<td>
5th </td><td>
SingleSelect</td><td>
Allows you to select individual nodes or connectors.</td></tr>
<tr>
<td>
6th </td><td>
None</td><td>
Disables all tools</td></tr>
</table>

You can set the desired tool to the `tool` property of the Diagram model. The following code illustrates how to enable single/multiple tools.

{% highlight js %}

// To Enable Single Tool 
$("#diagram").ejDiagram({
    //Enables a Single Selection
    tool: ej.datavisualization.Diagram.Tool.SingleSelect
});

// Enables multiple tools
$("#diagram").ejDiagram({
    // Selects when you click a node and pans when you click the Diagram surface
    tool: ej.datavisualization.Diagram.Tool.SingleSelect | ej.datavisualization.Diagram.Tool.ZoomPan
});

{% endhighlight %}