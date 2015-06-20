---
layout: post
title: Selector
description: selector
platform: js
control: Diagram
documentation: ug
---

# Selector

Selector behaves like a container for the selected elements and enables you to update the size, position and rotation angle of the selected elements. The properties of Selector are listed as follows.

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Type </b></td><td>
<b>Description.</b></td></tr>
<tr>
<td>
offset</td><td>
number</td><td>
Gets or sets the offset X value of the selector.</td></tr>
<tr>
<td>
offset</td><td>
number</td><td>
Gets or sets the offset Y value of the selector.</td></tr>
<tr>
<td>
Width</td><td>
number</td><td>
Gets or sets the width of the selector.</td></tr>
<tr>
<td>
height</td><td>
number</td><td>
Gets or sets the height of the selector</td></tr>
<tr>
<td>
rotateAngle</td><td>
number</td><td>
Gets or sets the rotation angle of the selector.</td></tr>
<tr>
<td>
children</td><td>
collection</td><td>
Gets or sets the collection of selected elements.</td></tr>
<tr>
<td>
constraints</td><td>
enum</td><td>
Gets or sets the value that is used to enable or disable the selector constraints.</td></tr>
<tr>
<td>
userHandles</td><td>
collection</td><td>
Gets or sets the value that is used to draw the custom handles on the selected elements.</td></tr>
</table>


### Move, Resize or Rotate selected items

The following code example is used to update the size and position of the selected elements.

{% highlight js %}
var diagram = $("#diagram").ejDiagram("instance");

//update the size and position of selected elements
diagram.updateSelector({
   offsetX: 100,
   offsetY: 100,
   width: 100,
   height: 100
});
{% endhighlight %}

### Iterate though selected items

The following code example is used to get the selected elements.

{% highlight js %}
var diagram = $("#diagram").ejDiagram("instance");
//get the selected elements.
for (var i = 0; i < diagram.model.selectedItems.children.length; i++) {
   var child = diagram.model.selectedItems.children[i];
}
{% endhighlight %}

### User Handles

The following code example is used to draw custom handles on the selected elements.

{% highlight js %}
var userHandle = [];

function createUserHandles() {
   //create a new instance of user handle.
   var cloneHandle = ej.datavisualization.Diagram.UserHandle();
   userhandle.push(cloneHandle);
}

$("#diagram").ejDiagram({
   selectedItems: {
      userHandles: userHandle
   }
});
{% endhighlight %}
