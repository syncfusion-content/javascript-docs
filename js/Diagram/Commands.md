---
layout: post
title: Commands
description: commands
platform: js
control: Diagram
documentation: ug
---

# Commands

There are several commands available in diagram. They are listed as follows.

* Alignment
* Spacing
* Sizing
* Clipboard
* Grouping
* Z-Order
* Zoom
* Nudge
* FitToPage
* Undo/Redo

## Alignment Command

**Alignment command** are used to align selected nodes/connectors on the Diagram page. The alignment is based on the selection boundary. The alignment command is as follows.

<table>
<tr>
<th>
Command</th><th>
Parameter</th><th>
Description</th></tr>
<tr>
<td>
align</td><td>
<b>direction</b> (string)<br/>
Values accepted-(“left”, “right”, “center”, “top”, “bottom” or “middle”)</td><td>
Align all the nodes/connectors in the selection list to the left, right, center, top, bottom, middle of the selection boundary</td></tr>
</table>


### Vertical Alignment command

The node is aligned vertically to left, right and center using alignment command. The following code illustrates how to execute the vertical alignment command.

{% highlight js %}

//align left
diagram.align("left");

//align right
diagram.align("right");

//align center
diagram.align("center");

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img1.png" %}

### Horizontal Alignment command

The node is aligned horizontally to top, bottom, and middle using alignment commands. The following code illustrates how to execute the horizontal alignment command.

{% highlight js %}

//align top
diagram.align("top");

//align bottom
diagram.align("bottom");

//align middle
diagram.align("middle");

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img2.png" %}

## Spacing Command

**Spacing command** are used to place selected nodes on the diagram at equal intervals from each other. The objects are spaced within the bounds of the first and last objects in the selection.

<table>
<tr>
<th>
Command</th><th>
Description</th></tr>
<tr>
<td>
spaceAcross</td><td>
Align the nodes/connectors in the selection list with equal horizontal distance between them.</td></tr>
<tr>
<td>
spaceDown</td><td>
Align the nodes/connectors in the selection list with equal vertical distance between them.</td></tr>
</table>


### spaceAcross Command

The `spaceAcross` command spaces selected nodes with equal horizontal distance between them. The following code illustrates how to execute spaceAcross command.

{% highlight js %}

//SpaceAcross
diagram.spaceAcross();

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img3.png" %}

### spaceDown Command

The `spaceDown` command spaces selected nodes with equal vertical distance between them. The following code illustrate how to execute spaceDown command.

{% highlight js %}

//space down
diagram.spaceDown();

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img4.png" %}

## Sizing Command

**Sizing command** are used to size the selected nodes on the Diagram. The following are the sizing commands.

<table>
<tr>
<th>
Command</th><th>
Description</th></tr>
<tr>
<td>
sameSize</td><td>
Size of the nodes in the selection list is resized to size of first node in the selection list.</td></tr>
<tr>
<td>
sameHeight</td><td>
Height of the nodes in the selection list is resized to height of first node in the selection list.</td></tr>
<tr>
<td>
sameWidth</td><td>
Width of the nodes in the selection list is resized to width of first node in the selection list.</td></tr>
</table>


The following code illustrate how to execute Sizing command

{% highlight js %}

//same size
diagram.sameSize();

//same height
diagram.sameHeight();

//same width
diagram.sameWidth();

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img5.png" %}

## Clipboard command

**Clipboard command** are used to cut, copy, and paste the selected elements on Diagram. The following are the Clipboard command.

* cut
* copy
* paste

### Cut

`cut` the selected elements from the Diagram to the `Diagram`'s clipboard. The following code illustrates how to execute Cut command.

{% highlight js %}

//cut the selected nodes/connectors
diagram.cut();

{% endhighlight %}

### Copy

`copy` the selected elements from the Diagram to the `Diagram`'s clipboard. The following code illustrates how to execute Copy command.

{% highlight js %}

//copy the nodes/connectors
diagram.copy();

{% endhighlight %}

### Paste

`paste` the `Diagram`'s clipboard data (nodes/connectors) into the Diagram. The following code illustrates how to execute Paste command.

{% highlight js %}

//paste the cut/copied nodes/connectors on diagram
diagram.paste();

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img6.png"%}

## Grouping Command

**Grouping command** are used to group/ungroup the selected elements on Diagram.

### Group

The following code illustrates how to Group the selected elements on Diagram.

{% highlight js %}

//group the selected nodes/connectors
diagram.group();

{% endhighlight %}

### Ungroup

The following code illustrates how to Ungroup the selected group on diagram.

{% highlight js %}

//ungroup the selected group 
diagram.ungroup();

{% endhighlight %}

## Z-Order Command

**Z-order command** are used to move the selected elements to the front of other elements. To send it back of other elements, move it one step (z-index) forward and move it one step (z-index) backward.
These commands provide support to control overlapping objects.

* bringToFront
* sendToBack
* moveForward
* sendBackward

### bringToFront Command

The `bringToFront` command moves the selected element over other elements by increasing the selected element's z-index to Diagram element's maximum value. The following code illustrates how to execute the BringToFront command.

{% highlight js %}

//bring to front
diagram.bringToFront();

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img7.png" %}

### sendToBack Command

The `sendToBack` command moves the selected element behind all other elements by setting the selected element's z-index to zero. The following code illustrates how to execute sendToBack command.

{% highlight js %}

//send to back
diagram.sendToBack();

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img8.png" %}

### moveForward Command

The `moveForward` command increases the z-index value of the selected element by 1. The following code illustrates how to execute moveForward Command.

{% highlight js %}

//move forward
diagram.moveForward();

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img9.png" %}

### sendBackward Command

The `sendBackward` command decreases the z-index value of the selected element by 1. The following code illustrates how to execute sendBackward command.

{% highlight js %}

//send backward
diagram.sendBackward();

{% endhighlight %}

{% include image.html url="/js/Diagram/Commands_images/Commands_img10.png" %}

## Zoom Command

Zoom feature is used to zoom-in and zoom-out the Diagram view and the zooming performed based on the center of current Diagram view. The following code illustrates how to zoom-in the Diagram.

{% highlight js %}

//ZoomIn
function ZoomIn() {
   var diagram = $("#diagram").ejDiagram("instance");
   var zoom = {
      zoomFactor: 0.2,
      zoomCommand: ej.datavisualization.Diagram.ZoomCommand.ZoomIn
   };
   diagram.zoomTo(zoom);
}  

{% endhighlight %}

The following code illustrates how to zoom-out the Diagram.

{% highlight js %}

//ZoomOut       
function ZoomOut() {
   var diagram = $("#diagram").ejDiagram("instance");
   var zoom = {
      zoomFactor: 0.2,
      zoomCommand: ej.datavisualization.Diagram.ZoomCommand.ZoomOut
   };
   diagram.zoomTo(zoom);
}
{% endhighlight %}

## Nudge Command

`nudge` command move selected elements on the Diagram toward up, down, left or right by 1 pixel. The Nudge command is as follows.

<table>
<tr>
<th>
Command</th><th>
Parameter</th><th>
Description</th></tr>
<tr>
<td>
nudge</td><td>
direction (string)<br/>
Value accepted- (“up”/“down”/“left”/“right”)<br/>
delta(integer)</td><td>
Nudge command moves the selected elements towards up/ down/ left/ right by the number of pixels specified by the parameter delta. When delta is not specified, by default it is considered as 1 pixel.</td></tr>
</table>


The following code illustrates how to execute Nudge command.

{% highlight js %}

//nudge up
diagram.nudge("up", 5);

{% endhighlight %}

**Nudge by using Arrow Keys**

The corresponding arrow keys are used to move the selected elements to up, down, left or right by 1 pixel.

{% include image.html url="/js/Diagram/Commands_images/Commands_img11.png" %}

`nudge` command are particularly useful for accurate placement of elements on the Diagram as it allows you to move by 1 pixel each time.

## FitToPage command

`fitToPage` command helps to fit the Diagram content into the view with respect to either width, height or at the whole.

<table>
<tr>
<th>
Command</th><th>
Parameter</th><th>
Description</th></tr>
<tr>
<td>
fitToPage</td><td>
<b>mode</b> (string)<br/>
Value accepted: ej.datavisualization.Diagram.FitMode<br/><br/>
<b>region</b> (string)<br/>
Value accepted-ej.datavisualization.Diagram.Region<br/><br/>
<b>margin</b> (object) </td><td>
<b>FitToPage</b> command fits the <b>Diagram</b> into the view. The area/bounds to be fit into a view is specified through the parameters.<br/>
<b>mode</b> – To specify whether to fit the <b>Diagram</b> into view either in terms of width, height or entire page.<br/>
<b>region</b> – To specify whether to fit the content based on the <b>Diagram</b> elements or page settings.<br/>
<b>margin</b> – Space that is to be left in between the content and viewport.</td></tr>
</table>


The following code illustrates how to execute FitToPage command.

{% highlight js %}

//fit to page – fit diagram based on elements
diagram.fitToPage("page", "content", {
   left: 25,
   top: 25,
   right: 25,
   bottom: 25
});
{% endhighlight %}

### FitToMode

`Mode` is to specify whether the Diagram content can be fit into view with respect to width, height or entire bounds of diagram.

<table>
<tr>
<th>
Mode</th><th>
Description</th></tr>
<tr>
<td>
Page</td><td>
Fits the entire <b>Diagram</b> content into view</td></tr>
<tr>
<td>
Width</td><td>
Fits the width of <b>Diagram</b> content into view </td></tr>
<tr>
<td>
Height</td><td>
Fits the height of <b>Diagram</b> content into view</td></tr>
</table>


### Region

`Region` is to specify the region/bounds of Diagram content to fit into view.

<table>
<tr>
<th>
Region</th><th>
Description</th></tr>
<tr>
<td>
Content</td><td>
Specifies the region covered by the <b>Diagram</b> elements </td></tr>
<tr>
<td>
PageSettings</td><td>
Specifies the region based on page settings</td></tr>
</table>


## Undo/Redo Command

Refer the Link for [Undo/Redo Commands](/js/Diagram/Undo-and-Redo).

## Command Manager

Diagram provides support to map/bind command execution with desired combination of key gestures. By default, diagram maps some commands with a set of key gestures and they are illustrated in the following table.

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Command</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Ctrl + A</td><td>
selectAll</td><td>
Select all nodes/connectors in diagram</td></tr>
<tr>
<td>
Ctrl + C</td><td>
copy</td><td>
Copy the diagram selected elements</td></tr>
<tr>
<td>
Ctrl + V</td><td>
paste</td><td>
Paste the copied elements</td></tr>
<tr>
<td>
Ctrl + X</td><td>
cut</td><td>
Cut the selected elements</td></tr>
<tr>
<td>
Ctrl + Z</td><td>
undo</td><td>
Undo(Reverse the last editing action performed on diagram)</td></tr>
<tr>
<td>
Ctrl + Y</td><td>
redo</td><td>
Redo(Restores the last editing action if no other actions have occurred since the last undo on diagram)</td></tr>
<tr>
<td>
Delete</td><td>
delete</td><td>
Delete the selected elements </td></tr>
<tr>
<td>
F2</td><td>
startEdit</td><td>
Sets the selected element's label mode as “edit” </td></tr>
<tr>
<td>
Esc</td><td>
endEdit</td><td>
Sets the selected element's label mode as “view” </td></tr>
<tr>
<td>
Ctrl /Shift+ Click on object</td><td>
</td><td>
Multiple selection(Selector binds all selected nodes/connectors)</td></tr>
<tr>
<td>
Up Arrow</td><td>
nudge(“up”)</td><td>
nudgeUp(move the selected elements towards up by one pixel)</td></tr>
<tr>
<td>
Down Arrow</td><td>
nudge(“down”)</td><td>
nudgeDown(move the selected elements towards down by one pixel)</td></tr>
<tr>
<td>
Left Arrow</td><td>
nudge(“left”)</td><td>
nudgeLeft(move the selected elements towards left by one pixel)</td></tr>
<tr>
<td>
Right Arrow</td><td>
nudge(“right”)</td><td>
nudgeRight(move the selected elements towards right by one pixel)</td></tr>
<tr>
<td>
Ctrl + MouseScroll</td><td>
zoom</td><td>
Zoom(Zoom in/Zoom out the diagram)</td></tr>
<tr>
<td>
Ctrl+MouseScroll</td><td>
zoom</td><td>
Zoom(Zoom in/Zoom out the diagram)</td></tr>
</table>

_In built commands_

Command Manager provides support to map custom commands with the set of desired key combinations. The defined custom commands will be executed when the specified key gesture is recognized.

### Custom command

A custom command has to be defined with a set of predefined fields as follows.

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Type</b></td><td>
<b>Default</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
gesture</td><td>
Object</td><td>
Null</td><td>
Combination of keys and key modifiers to recognize when to execute the command</td></tr>
<tr>
<td>
canExecute</td><td>
Object</td><td>
A method that returns true.</td><td>
The method to define whether the command is executable at the current moment or not.It will be called when the specified key gesture is recognized.</td></tr>
<tr>
<td>
execute</td><td>
Object</td><td>
Null</td><td>
The execute method acts as the command handler and will be called when the canExecute method returns true.</td></tr>
<tr>
<td>
parameter</td><td>
Object</td><td>
Null</td><td>
parameter is an object. If specified, the parameter will be passed to the handler on command execution.</td></tr>
</table>

_Custom Command_

The following code snippet illustrates how to define a custom command.

{% highlight js %}

$("#DiagramContent").ejDiagram({
    commandManager: {
        commands:{
            //command to clone the selected item
            "clone": {
                //Method to define whether the command can be executed at the current moment
                canExecute: function (args) {
                    //Defines that the clone command can be executed, if and only if the selection list is not empty.
                    if (args.model.selectedItems.length) return true;
                },
                //Command handler
                execute: function (args) {
                    //Logic to clone the selected element
                    diagram.copy();
                    diagram.paste();
                },
                //Defines that the clone command has to be executed on the recognition of Shift+C key press.
                gesture: { key: ej.datavisualization.Diagram.Keys.C, keyModifiers: ej.datavisualization.Diagram.KeyModifiers.Shift }
            }
        }
    }
});

{% endhighlight %}

### Modify the existing command

By default, diagram maps certain commands with relevant key combination. If those commands are not desired for the specified keys, they can be disabled. If the functionality of a specific command has to be changed, the command can be completely rewritten. Following code snippet illustrates how to disable a command.

{% highlight js %}

$("#DiagramContent").ejDiagram({
    //disable the nudging commands
    commandManager: {
        commands:{
        //Assigning null value to an existing command, disables its execution
        "nudgeUp": null,
        "nudgeDown": null,
        "nudgeRight": null,
        "nudgeLeft": null
        }
  }
});

{% endhighlight %}
