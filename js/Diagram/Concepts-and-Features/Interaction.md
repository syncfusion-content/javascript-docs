---
layout: post
title: Interaction
description: interaction
platform: js
control: Diagram
documentation: ug
---

# Interaction

## Tool

There are many interactive features over Diagram surface. A collection of predefined tools are available in Diagram.

_Tool_

<table>
<tr>
<td>
<b>Tool name	</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
panTool </td><td>
Allows you to pan the diagram</td></tr>
<tr>
<td>
move </td><td>
Allows you to move the selected Node/Connector.</td></tr>
<tr>
<td>
select</td><td>
Allows you to select the diagram node/connector objects.</td></tr>
<tr>
<td>
textTool</td><td>
Allows you to add new text or edit an existing text</td></tr>
<tr>
<td>
endPointTool</td><td>
Allow you to drag connector’s end point </td></tr>
<tr>
<td>
resizeTool</td><td>
Allow you to resize the nodes </td></tr>
<tr>
<td>
rotateTool</td><td>
Allow you to rotate nodes</td></tr>
</table>

The following code illustrates how to activate and deactivate the desired tool

{% highlight js %}

//activate pan tool
var diagram = $("#Diagram").ejDiagram("instance");
diagram.activateTool("panTool");

//deactivate current tool
diagram.deactivateTool();

{% endhighlight %}

## Selection

**Selection** feature allows you to select single or multiple Nodes/Connectors.

* Single selection

* Multiple selection

### Single selection

The Nodes/Connectors in Diagram surface is selected when the **Select** constraint is enabled. **Selection** is done through the following two ways. 

* Mouse Click

* addSelection method.

**Mouse Click**

The node/connector is selected by clicking on a desired node/connector.

**addSelection method**

Diagram provides public API **addSelection** for adding node/connector to the selection.
The following code illustrates how to add node/connector to selection.

{% highlight js %}

var node = diagram.model.nodes[0];

//add node to selection
diagram.addSelection(node);

{% endhighlight %}

{% include image.html url="/js/Diagram/Concepts-and-Features/Interaction_images/Interaction_img1.png" Caption="Single selection"%}

### Multiple Selections

**Multiple selection** is done using rubber band selection, Ctrl + Click and Ctrl + A. During **Multiple selections**, the selector binds all the selected items.

**Rubber band Selection**

**Rubber band selection** is done by clicking and dragging mouse pointer on Diagram canvas and rectangle helper appears during **Rubber band selection**. The diagram Nodes/Connectors that intersect in the selection rectangle bounds are added to the selection list.

{% include image.html url="/js/Diagram/Concepts-and-Features/Interaction_images/Interaction_img2.png" Caption="Multiple Selections"%}

## User Handle

Diagram has an option to create additional selection handles around the selector called User handles. You can create additional handles and assign their command/tool to the desired handles.

The following is the list of User handle properties.

_User Handle_

<table>
<tr>
<td>
<b>Properties</b></td><td>
<b>Data Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
name</td><td>
string</td><td>
Gets or sets the name of the User handle</td></tr>
<tr>
<td>
pathData</td><td>
string</td><td>
Gets or sets the path data of the User handle</td></tr>
<tr>
<td>
borderColor</td><td>
string</td><td>
Gets or sets the border color of the User handle</td></tr>
<tr>
<td>
borderWidth</td><td>
number</td><td>
Gets or sets the border width of the User handle</td></tr>
<tr>
<td>
backgroundColor</td><td>
string</td><td>
Gets or sets the background color of the User handle</td></tr>
<tr>
<td>
position</td><td>
ej.datavisualization.Diagram.UserHandlePositions</td><td>
Gets or sets the position of  User handle </td></tr>
<tr>
<td>
pathColor</td><td>
string</td><td>
Gets or sets the path color of the User handle</td></tr>
<tr>
<td>
tool</td><td>
string</td><td>
Gets or sets the tool that is associated with User handle</td></tr>
<tr>
<td>
size</td><td>
number</td><td>
Gets or sets the size of the User handle</td></tr>
<tr>
<td>
visible</td><td>
boolean</td><td>
Gets or sets the visibility of the User handle</td></tr>
<tr>
<td>
enableMultipleSelection</td><td>
boolean</td><td>
Gets or sets whether the User handle is enabled for  multiple selection </td></tr>
</table>

The following example describes how to create **delete user handle** in diagram.

* Create handle

* Create tool for handle

* Add handle in diagram

**Create Delete Userhandle**

The following code illustrates how to create **Delete User handle**

{% highlight js %}

//Create handle
var userHandles = [];
var deleteHandle = { name: "deleteHandle", position: ej.datavisualization.Diagram.UserHandlePositions.BottomRight, showOnMultipleSelection: false, size:30, backgoundColor: "#4D4D4D", pathData: “M33.977998,27.684L33.977998,58.102997 “ +“41.373998,58.102997 41.373998,27.684z M14.841999,27.684L14.841999,58.102997 22.237998,58.102997 “+”22.237998,27.684z M4.0319996,22.433001L52.183,22.433001 52.183,63.999001 4.0319996,63.999001z “+”M15.974,0L40.195001,0 40.195001,7.7260003 56.167001,7.7260003 56.167001,16.000999 0,16.000999 “+”0,7.7260003 15.974,7.7260003z” };
deletHandle.tool = new DeleteTool(deleteHandle.name);
userHandles.push(deletHandle);

{% endhighlight %}

**Create tool for Delete Userhandle**

The following code illustrates how to create tool for **Delete User handle.**

{% highlight js %}

//create tool for delete handle
var DeleteTool = (function (base) {

    ej.datavisualization.Diagram.extends(DeleteTool, base);
    
    function DeleteTool(name) {
        base.call(this, name);
        this.singleAction = true;
    }
    
    //mouse down for delete tool
    DeleteTool.prototype.mousedown = function (evt) {
        base.prototype.mousedown.call(this, evt);
        this.inAction = true;
        this.selectedObject = this.diagram.selectionList[0];
    };
    
    //mouse move for delete tool
    DeleteTool.prototype.mousemove = function (evt) { 
        base.prototype.mousemove.call(this, evt);
    };
    
    //mouse up for delete tool
    DeleteTool.prototype.mouseup = function (evt) {
        var diagram = $(“#diagram”).ejDiagram(“instance”);
        if (this.inAction) 
        {
           this.inAction = false;
           diagram.remove(this.selectedObject);
        }
        base.prototype.mouseup.call(this, evt);
    };
    return DeleteTool;
})

{% endhighlight %}

**Adding delete handle in Diagram**

The following code illustrates how to add **Delete handle** in diagram

{% highlight js %}

//add user handles to diagram
$(“#Diagram”).ejDiagram({ userHandles: userHandles });


{% endhighlight %}

{% include image.html url="/js/Diagram/Concepts-and-Features/Interaction_images/Interaction_img3.png" Caption="Delete-User Handle"%}

**Events**

_Events_

<table>
<tr>
<td>
<b>Events</b></td><td>
<b>Arguments</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
selectionChange</td><td>
{cancel, changeType, element, model, type}cancel :booleanchangeType: string (“insert“/ “remove”)element: object(Node/Connector to be add or remove)model: object(diagram’s model)type: string(event name “selectionChange”)</td><td>
This event is raised when the selection added to the node /connector during run time.</td></tr>
</table>

## Zoom 

The Diagram is zoomed in and out. **Zooming** is achieved in the following two ways.

* Using the zoom commands.

* Using the mouse wheel.

**MouseWheel**

Press the CTRL key and roll the mouse wheel up to zoom in or down to zoom out.

**Zoom Factor**

Diagram allows you to set the **zoomFactor** by which you can zoom in or out. This factor can be specified using the **zoomFactor** property. The default value is 0.2.

{% highlight js %}

var zoom = { zoomFactor: 0.2 };

{% endhighlight %}

**ZoomCommands**

Refer the link ZoomCommand

## Keyboard

Diagram has several keyboard functions support and they are listed as follows.

_Keyboard_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Ctrl + A</td><td>
Select all nodes/connectors in diagram</td></tr>
<tr>
<td>
Ctrl + C</td><td>
Copy the diagram selected elements</td></tr>
<tr>
<td>
Ctrl + V</td><td>
Paste the copied elements</td></tr>
<tr>
<td>
Ctrl + X</td><td>
Cut the selected elements</td></tr>
<tr>
<td>
Ctrl + Z</td><td>
Undo(Reverse the last editing action performed on diagram)</td></tr>
<tr>
<td>
Ctrl + Y</td><td>
Redo(Restores the last editing action if no other actions have occurred since the last undo on diagram)</td></tr>
<tr>
<td>
Delete</td><td>
Delete the selected elements </td></tr>
<tr>
<td>
Ctrl /Shift+ Click on object</td><td>
Multiple selection(Selector binds all selected nodes/connectors)</td></tr>
<tr>
<td>
Up Arrow</td><td>
nudgeUp(move the selected elements towards up by one pixel)</td></tr>
<tr>
<td>
Down Arrow</td><td>
nudgeDown(move the selected elements towards down by one pixel)</td></tr>
<tr>
<td>
Left Arrow</td><td>
nudgeLeft(move the selected elements towards left by one pixel)</td></tr>
<tr>
<td>
Right Arrow</td><td>
nudgeRight(move the selected elements towards right by one pixel)</td></tr>
<tr>
<td>
Ctrl+MouseScroll</td><td>
Zoom(Zoom in/Zoom out the diagram)</td></tr>
</table>

## Touch

**Touch** support for Diagram view has the following features:

* Drag and Drop from the SymbolPalette

* Dragging the Node and Line Connector on drawing area

* Panning

* Multiple selection

* Contextmenu(touch and hold)

* Text Editing(double tap)

## Snapping

**Snapping** feature handles snapping operation with gridlines and Nodes/Connectors.

* snapToGrid

* snapToObject

**SnapToGrid**

The **snap-to-grid** feature allows diagram objects to snap the nearest intersection of gridlines when being dragged or resized. This feature enables easier alignment during layout or design. 

The **snapToGrid** feature is enabled by using a snapSetting’s **SnapConstraints** property.

_SnapToGrid_

<table>
<tr>
<td>
<b>Properties</b></td><td>
<b>Data Type</b></td><td>
<b>Descriptions</b></td></tr>
<tr>
<td>
horizontalGridLines</td><td>
object</td><td>
Gets or sets the horizontal gridlines </td></tr>
<tr>
<td>
verticalGridLines</td><td>
object</td><td>
Gets or sets the vertical gridlines</td></tr>
<tr>
<td>
enableSnapToObject</td><td>
boolean</td><td>
Gets or sets whether snapping to object is enabled or not</td></tr>
<tr>
<td>
snapAngle</td><td>
number</td><td>
Gets or sets the snap angle</td></tr>
<tr>
<td>
snapConstraints</td><td>
ej.datavisualization.Diagram.SnapConstraints</td><td>
Gets or sets whether snapping to gridlines option is enabled or not</td></tr>
</table>

**Enable snapping** 

Snapping to gridlines is enabled or disabled by changing the value of snap Setting’s **SnapConstraints** as **ej.datavisualization.Diagram.SnapConstraints**

{% highlight js %}

//enable snap to horizontal gridlines constraint
var snapSettings = { snapConstraints : ej.datavisualization.Diagram.SnapConstraints.SnapToHorizontalLines };

//enable snap to vertical gridlines constraint
snapSettings = { snapConstraints: ej.datavisualization.Diagram.SnapConstraints.SnapToVerticalLines };

//enable snap to both horizontal and vertical gridlines constraint
snapSettings = { snapConstraints: ej.datavisualization.Diagram.SnapConstraints.SnapToLines}

{% endhighlight %}

**SnapInterval**

You can customize the position to which a diagram object snaps by changing the value of the **snapInterval** property of grid lines.

**snapInterval** is a double collection that determines the space between patterns of gridlines.

{% highlight js %}

//set snap interval
var snapSettings = { horizontalGridlines: { snapInterval: [20] }, verticalGridlines: { snapInterval: [20] }};

{% endhighlight %}

**SnapToObject**

The **snap-to-object** feature provides visual cues to assist with aligning and spacing diagram nodes. You can snap a node with its neighboring objects based on its size and position. Such alignments are visually represented as guidelines.

{% include image.html url="/js/Diagram/Concepts-and-Features/Interaction_images/Interaction_img4.png" Caption="Snap to Object"%}

**Enabling and Disabling snapping to objects**

**snapSettings.enableSnapToObject** determines whether nodes are snapped to object.

{% highlight js %}

//enable snap to object behavior
$("#Diagram").ejDiagram({ snapSettings: { enableSnapToObject: true }});

{% endhighlight %}

**SnapAngle**

You can rotate the Node with multiples of **snapAngle**.

{% highlight js %}

//set snap angle
$("#Diagram").ejDiagram({ snapSettings: { snapAngle: 5 }});

{% endhighlight %}

**Events**

_Events_

<table>
<tr>
<td>
<b>Events</b></td><td>
<b>Arguments</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
mouseLeave</td><td>
{cancel, element, model, type}<br/>
cancel: boolean<br/>
element: object(node/connector)<br/>
model: object(diagram’s model)<br/>
type: string(event name “mouseLeave”)</td><td>
This event is raised when themouse pointer leaves from the node/connector during runtime.</td></tr>
<tr>
<td>
mouseEnter</td><td>
{cancel, element, model, type}<br/>
cancel: boolean<br/>
element: object(node/connector)<br/>
model: object(diagram’s model)<br/>
type: string(event name “mouseEnter”)</td><td>
This event is raised when the mouse pointer enters on the node/connector during runtime.</td></tr>
<tr>
<td>
mouseHover</td><td>
{ cancel, diagram, model, type }<br/>
cancel: boolean<br/>
diagram: object(node/connector)<br/>
model: object(diagram’s model)<br/>
type: string(event name “mouseHover”)</td><td>
This event is raised when mouse pointer hovers on the node/connector during runtime.</td></tr>
<tr>
<td>
click</td><td>
{cancel, element, model, type}<br/>
cancel: boolean<br/>
element: object(node/connector)<br/>
model: object(diagram’s model)<br/>
type: string(event name “click”)</td><td>
This event is raised when you click on the node/connector during runtime.</td></tr>
<tr>
<td>
doubleClick</td><td>
{cancel, element, model, type}<br/>
cancel: boolean<br/>
element: object(node/connector)<br/>
model: object(diagram’s model)<br/>
type: string(event name “doubleClick”)</td><td>
This event when you Double-click on the node/connector during runtime.</td></tr>
</table>
