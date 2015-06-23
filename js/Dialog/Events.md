---
layout: post
title: Events
description: events
platform: js
control: Dialog
documentation: ug
---

# Events

 The **Dialog** widget provides the following events,

Events of Dialog

<table>
<tr>
<th>Event</th><th>Description</th></tr>
<tr>
<td>
beforeClose</td><td>
Triggered when the control before close</td></tr>
<tr>
<td>
close</td><td>
Triggered when the control is close</td></tr>
<tr>
<td>
beforeOpen</td><td>
Triggered when the control before open</td></tr>
<tr>
<td>
open</td><td>
Triggered when the control is open</td></tr>
<tr>
<td>
drag</td><td>
Triggered when the control is drag</td></tr>
<tr>
<td>
dragStart</td><td>
Triggered when the control drag start </td></tr>
<tr>
<td>
dragStop</td><td>
Triggered when the control drag stop</td></tr>
<tr>
<td>
resize</td><td>
Triggered when the control is resize</td></tr>
<tr>
<td>
resizeStart</td><td>
Triggered when the control resize start</td></tr>
<tr>
<td>
resizeStop</td><td>
Triggered when the control resize stop</td></tr>
</table>

## Configure Events

The following steps describes you on how the events are added to the **Dialog** control.

In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control.



{% highlight html %}

<div id="eventDialog" title="WinRT">
   Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications <span>including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more.</span>
   It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
</div>


{% endhighlight %}



Define the client side events for **Dialog** control.



{% highlight js %}

        $("#eventDialog").ejDialog({
            create: "onCreate",
            beforeClose: "onBeforeClose",
            close: "onClose",
            beforeOpen: "onBeforeOpen",
            open: "onOpen",
            drag: "onDrag",
            dragStart: "onDragStart",
            dragStop: "onDragStop",
            resize: "onResize",
            resizeStart: "onResizeStart",
            resizeStop: "onResizeStop"
        });


{% endhighlight %}



Define the script for handling **Dialog** events.



{% highlight js %}

        function onCreate(args) {
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             alert("Event triggered is " + args.type);
         }
        
         function onBeforeClose(args) {
             // {Object} argument.event - returns the close icon click event args    
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             alert("Event triggered is " + args.type);
         }
        
         function onClose(args) {
             // {Object} argument.event - returns the close icon click event args    
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             alert("Event triggered is " + args.type);
         }
        
         function onBeforeOpen(args) {
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             alert("Event triggered is " + args.type);
         }
        
         function onOpen(args) {
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             alert("Event triggered is " + args.type);
         }
        
         function onDrag(args) {
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             // {Object} argument.event - returns the mouse move event args
             alert("Event triggered is " + args.type);
         }
        
         function onDragStart(args) {
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             // {Object} argument.event - returns the mouse down event args
             alert("Event triggered is " + args.type);
         }
        
         function onDragStop(args) {
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             // {Object} argument.event - returns the mouse down event args
             alert("Event triggered is " + args.type);
         }
        
         function onResize(args) {
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             // {Object} argument.event - returns the mouse move event args
             alert("Event triggered is " + args.type);
         }
        
         function onResizeStart(args) {
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             // {Object} argument.event - returns the mouse down event args
             alert("Event triggered is " + args.type);
         }
        
         function onResizeStop(args) {
             // {boolean} argument.cancel - returns the cancel option value
             // {object} argument.model - returns the dialog model
             // {string} argument.type - returns the name of the event
             // {Object} argument.event - returns the mouse leave event args
             alert("Event triggered is " + args.type);
         }

{% endhighlight %}



