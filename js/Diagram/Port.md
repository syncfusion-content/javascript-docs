---
layout: post
title: Port
description: port
platform: js
control: Diagram
documentation: ug
---

# Port

**Port** is a specific connection point on node to make a static connection with node. You can define any number of ports on a node. 

## Create Port

The following code illustrates how to create a port and add it to nodes port array.

{% highlight js %}
//create a port and it to node’s ports array. 
var node = {
   ports: [{
      name: "port1",
      offset: {
         x: 0,
         y: 0.5
      },
      fillColor: "yellow",
      visibility: ej.datavisualization.Diagram.PortVisibility.Visible
   }]
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Port_images/Port_img1.png" %}

## Connecting Ports

The connection between specific ports on the node is established by assigning the name of the node’s port to connector’s target port/source port. The following code illustrates how to establish a port connection:

{% highlight js %}
//create nodes with ports
var nodes = [
    {
        name: "node1",
        offsetX: 300,
        offsetY: 300,
        width: 100,
        height: 100,
        ports: [
            { name: "port1", offset: { x: 0, y: 0.5 } },
            { name: "port2", offset: { x: 0.5, y: 0 } },
            { name: "port3", offset: { x: 1, y: 0.5 } },
            { name: "port4", offset: { x: 0.5, y: 1 } }
        ]
    },
    {
        name: "node2",
        offsetX: 450,
        offsetY: 500,
        width: 100,
        height: 100,
        ports: [
            { name: "port1", offset: { x: 0, y: 0.5 } },
            { name: "port2", offset: { x: 0.5, y: 0 } },
            { name: "port3", offset: { x: 1, y: 0.5 } },
            { name: "port4", offset: { x: 0.5, y: 1 } }
        ]
    }
];


//create connector and connect ports
var connector = {
   name: "connector",
   sourceNode: "node1",
   targetNode: "node2",
   sourcePort: "port4",
   targetPort: "port1"
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Port_images/Port_img2.png" %}

## Appearance

You can customize the Port appearance by setting desired values to the appropriate appearance property.

<table>
<tr>
<th>
Properties</th><th>
Data Type</th><th>
Description</th></tr>
<tr>
<td>
visibility</td><td>
boolean</td><td>
Gets or sets the visibility of port</td></tr>
<tr>
<td>
size</td><td>
number</td><td>
Gets or sets the size of the port</td></tr>
<tr>
<td>
offset</td><td>
points</td><td>
Gets or sets the offset of the port</td></tr>
<tr>
<td>
borderColor</td><td>
string</td><td>
Gets or sets the border color of the port</td></tr>
<tr>
<td>
borderWidth</td><td>
number</td><td>
Gets or sets the border width of the port</td></tr>
<tr>
<td>
fillColor</td><td>
string</td><td>
Gets or sets the fill color of the port</td></tr>
<tr>
<td>
pathData</td><td>
string</td><td>
Gets or sets the path data of the port</td></tr>
</table>

The following code illustrates how to customize the port.

{% highlight js %}
//set various appearance properties to port
var port = {
   visibility: true,
   fillColor: "yellow",
   shape: {
      type: "circle"
   },
   size: 12,
   borderColor: "black",
   borderWidth: 2
};
{% endhighlight %}

## Constraints

You can enable or disable certain behaviors of Port using `Port`’s `constraints` property. 

<table>
<tr>
<th>
Constraints</th><th>
Description</th></tr>
<tr>
<td>
None</td><td>
Disable all constraints</td></tr>
<tr>
<td>
Connect</td><td>
Enables connections with connector</td></tr>
</table>

The following code illustrates how to set port constraints.

{% highlight js %}

//set port’s "Connect" constraint
var port = {
   constraints: ej.datavisualization.Diagram.PortConstraints.Connect
};
{% endhighlight %}

> **Note:** Port’s constraints property is manipulated using bitwise operations. For more information about bitwise operations, see [Bitwise Operations](/js/Diagram/How-To/Bitwise-Operations).
