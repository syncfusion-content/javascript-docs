---
layout: post
title: Constraints
description: constraints
platform: js
control: Diagram
documentation: ug
---

# Constraints

Diagram provides support to enable or disable certain diagram behaviors.

<table>
<tr>
<th>
Constraints</th><th>
Description</th></tr>
<tr>
<td>
None</td><td>
Disables all DiagramConstraints.</td></tr>
<tr>
<td>
PageEditable</td><td>
Enables or Disables page editing.</td></tr>
<tr>
<td>
Bridging</td><td>
Enables or Disables line briding.</td></tr>
<tr>
<td>
Zoomable</td><td>
Enables or Disables zooming.</td></tr>
<tr>
<td>
PannableX</td><td>
Enables or Disables panning on horizontal axis.</td></tr>
<tr>
<td>
PannableY</td><td>
Enables or Disables panning on vertical axis.</td></tr>
<tr>
<td>
Pannable</td><td>
Enables or Disables panning.</td></tr>
<tr>
<td>
Undoable</td><td>
Enables or Disables undo actions.</td></tr>
<tr>
<td>
Default</td><td>
Enables all the constraints.</td></tr>
</table>


Default value for the `diagram`'s `constraints` property is `ej.datavisualization.Diagram.DiagramConstraints.Default`.

{% highlight js %}

var diagramConstraints = ej.datavisualization.Diagram.DiagramConstraints;

//Disable PageEditing 
$("#diagram").ejDiagram({
    constraints: diagramConstraints.Default &~ diagramConstraints.PageEditable 
});

{% endhighlight %}