---
layout: post
title: Gridlines
description: gridlines
platform: js
control: Diagram
documentation: ug
---

# Gridlines

**Gridlines** are horizontal and vertical lines behind the Diagram elements. They provide visual guidance when dragging or arranging objects on the Diagram surface.

{% include image.html url="/js/Diagram/Concepts-and-Features/Gridlines_images/Gridlines_img1.png" Caption="Gridlines"%}

## SnapConstraints

The Diagram model’s **snapSettings.SnapContraints** property is used to control snap to grid behavior and visibility of gridlines. 

_SnapConstraints_

<table>
<tr>
<td>
<b>Constraints</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
SnapToHorizontalLines</td><td>
Enables snapping to horizontal Grid lines</td></tr>
<tr>
<td>
SnapToVerticalLines</td><td>
Enables snapping to vertical gridlines</td></tr>
<tr>
<td>
SnapToLines</td><td>
Enables snapping to gridlines</td></tr>
<tr>
<td>
ShowHorizontalLines</td><td>
Show or hide horizontal gridlines</td></tr>
<tr>
<td>
ShowVerticalLines</td><td>
Show or hide vertical gridlines</td></tr>
<tr>
<td>
ShowLines</td><td>
Show or hide all gridlines</td></tr>
<tr>
<td>
All</td><td>
Enable all the constraints</td></tr>
<tr>
<td>
None</td><td>
Disable all the constraints</td></tr>
</table>


The following code illustrates how to show or hide gridlines using constraints

{% highlight js %}

**[JS]**

//show horizontal gridlines
var snapSettings = {
 "snapConstraints": ej.datavisualization.Diagram.SnapConstraints.ShowHorizontalLines
};
//show vertical gridlines
 snapSettings = {
"snapConstraints": ej.datavisualization.Diagram.SnapConstraints.ShowVerticalLines }
};
//show both horizontal and vertical gridlines
 snapSettings = { "snapConstraints": ej.datavisualization.Diagram.SnapConstraints.ShowLines }
};
//hide both horizontal and vertical gridlines
 snapSettings = { "snapConstraints": ej.datavisualization.Diagram.SnapConstraints.None }
};
$("#Diagram").ejDiagram({ snapSettings: snapSettings });


{% endhighlight %}

## Appearance

You can customize the **Appearance** of the gridlines using following properties.

_Appearance_

<table>
<tr>
<td>
<b>Properties</b></td><td>
<b>Data Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
lineInterval</td><td>
array</td><td>
Gets or sets the line interval of gridlines</td></tr>
<tr>
<td>
snapInterval</td><td>
array</td><td>
Gets or sets the snap interval of gridlines</td></tr>
<tr>
<td>
lineDashArray</td><td>
string</td><td>
Gets or sets the pattern of dashes and gaps used to stroke gridlines border.</td></tr>
<tr>
<td>
lineColor</td><td>
string</td><td>
Gets or sets the line color of the gridlines</td></tr>
</table>


The following code illustrates how to customize the **Gridline****appearance**.

{% highlight js %}

**[JS]**
//set various appearance properties to gridlines
var snapSettings = {  horizontalGridlines: {  linesInterval: [1.25, 14, 0.25, 15, 0.25, 15, 0.25, 15, 0.25, 15],
 lineColor: "blue", lineDashArray: "2  2" }
};    
$("#Diagram").ejDiagram({ snapSettings: snapSettings });


{% endhighlight %}



{% include image.html url="/js/Diagram/Concepts-and-Features/Gridlines_images/Gridlines_img2.png" Caption="Customized Gridlines"%}

