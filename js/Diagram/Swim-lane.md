---
layout: post
title: Swim-lane
description: swim lane 
platform: js
control: Diagram
documentation: ug
---

# Swim lane 

A swim lane is a visual element used in process flow diagrams or flowcharts. A typical swim lane contains a header, and a collection of lanes that can be arranged horizontally or vertically.

{% include image.html url="/js/Diagram/Swim-lane_images/Swim-lane_img1.png" %}

**Swim lane** shape contains the following properties.

<table>
<tr>
<th>
Property</th><th>
Data type</th><th>
Description</th></tr>
<tr>
<td>
header</td><td>
object</td><td>
Gets or sets the header value of the swim lane.</td></tr>
<tr>
<td>
orientation</td><td>
string</td><td>
Gets or sets the orientation of the swim lane.</td></tr>
<tr>
<td>
offset</td><td>
number</td><td>
Gets or sets the offsetX value of the swim lane.</td></tr>
<tr>
<td>
offset</td><td>
number</td><td>
Gets or sets the offsetY value of the swim lane.</td></tr>
<tr>
<td>
minHeight</td><td>
number</td><td>
Gets or sets the minHeight value of the swim lane.</td></tr>
<tr>
<td>
minWidth</td><td>
number</td><td>
Gets or sets the minWidth value of the swim lane.</td></tr>
<tr>
<td>
maxHeight</td><td>
number</td><td>
Gets or sets the maxHeight value of the swim lane.</td></tr>
<tr>
<td>
maxWidth</td><td>
number</td><td>
Gets or sets the maxWidth value of the swim lane.</td></tr>
<tr>
<td>
lanes</td><td>
array</td><td>
Gets or sets the lanes as collection.</td></tr>
<tr>
<td>
phases</td><td>
array</td><td>
Gets or sets the phases as collection.</td></tr>
</table>

## Lane

The lane is an object that controls the diagram elements in the swim lane. Lane has the following properties.

<table>
<tr>
<th>
Property</th><th>
Data type</th><th>
Description</th><th></tr>
<tr>
<td>
header</td><td>
object</td><td>
Gets or sets the lane header.</td></tr>
<tr>
<td>
name</td><td>
string</td><td>
Gets or sets the name of the header.</td></tr>
<tr>
<td>
children</td><td>
array</td><td>
Gets or set the child nodes as collection.</td></tr>
<tr>
<td>
orientation</td><td>
string</td><td>
Gets or sets the orientation of the swim lane.</td></tr>
</table>

## Header

This is used to define header for a swim lane. It has the following properties.

<table>
<tr>
<th>
Property</th><th>
Data type</th><th>
Description</th></tr>
<tr>
<td>
width</td><td>
number</td><td>
Gets or sets the width of the header.</td></tr>
<tr>
<td>
text</td><td>
string</td><td>
Gets or sets the text value for the header.</td></tr>
</table>

## Phase

A Phase is a line that separates the swim lane. Phase has following properties.

<table>
<tr>
<th>
Property</th><th>
Data type</th><th>
Description</th></tr>
<tr>
<td>
name</td><td>
string</td><td>
Gets or set the name of the phase.</td></tr>
<tr>
<td>
offset</td><td>
number</td><td>
Gets or set the offset value of the phase.</td></tr>
<tr>
<td>
lineWidth</td><td>
number</td><td>
Gets or set the stroke width of the phase.</td></tr>
<tr>
<td>
lineDashArray</td><td>
string</td><td>
Gets or set the stroke dash array of the phase.</td></tr>
<tr>
<td>
lineColor</td><td>
string</td><td>
Gets or set the stroke colour of the phase.</td></tr>
<tr>
<td>
parent</td><td>
string</td><td>
Gets or sets the parent of the phase</td></tr>
</table>

The following code illustrates how to create a simple **swim lane**.

{% highlight js %}
var nodes = [];
var node =
   //creating the swimlane and set its type as swimlane
   {
      type: "swimlane",
      name: "swimlane",
      
      //initialize swimlane header
      header: {
         text: "HEADER",
         height: 50,
         fillColor: "#C7D4DF",
         fontSize: 11
      },
      
      fillColor: "#f5f5f5",
      orientation: "horizontal",
      offsetX: 350,
      offsetY: 290,
      height: 100,
      width: 450,
      
      //add lanes
      lanes: [{
         name: "stackCanvas1",
         fillColor: "#f5f5f5",
         height: 120,
         
         header: {
            text: "HEADER",
            width: 50,
            fillColor: "#C7D4DF",
            fontSize: 11
         },         
         
         children: [{
            shape: { type: "path", pathData: pathData },
            name: "Node1",
            labels: [{ text: "Node1", fontSize: 11 }],
            marginLeft: 100,
            marginTop: 10,
         }, {
            shape: { type: "path", pathData: pathData },
            name: "Node2",
            labels: [{ text: "Node2", fontSize: 11 }],
            marginLeft: 250,
            marginTop: 10,
         }]
      }],
      
      phases: [],
      phaseSize: 20,
   }

nodes.push(node);
//add nodes to Diagram
$("#Diagram").ejDiagram({
   nodes: nodes
});
{% endhighlight %}