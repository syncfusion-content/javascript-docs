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



Output of **Dialog** widget when the events trigger is as follows.


<table>
     <tr>
        <td>
            <img src="Events_images\Events_img1.png" alt="C:\Users\ApoorvahR\Desktop\1.png" width="223pt" height="150pt"/></td>
        <td>
            <img src="Events_images\Events_img2.png" alt="C:\Users\ApoorvahR\Desktop\2.png" width="214pt" height="141pt"/></td>
     </tr>
</table>

_Dialog triggered create and beforeOpen event_               


<table>
<tr>
<td>
<img src="Events_images\Events_img3.png" alt="C:\Users\ApoorvahR\Desktop\3.png" width="332pt" height="226pt"</td><td>
<img src="Events_images\Events_img4.png" alt="C:\Users\ApoorvahR\Desktop\4.png" width="339pt" height="236pt"</td></tr>
</table>

_Dialog triggered open and before close event_  


<table>
<tr>
<td>
<img src="Events_images\Events_img5.png" alt="C:\Users\ApoorvahR\Desktop\5.png" width="214pt" height="157pt"</td><td>
<img src="Events_images\Events_img6.png" alt="C:\Users\ApoorvahR\Desktop\6.png" width="347pt" height="242pt"</td></tr>
</table>

_Dialog triggered close and drag event_


<table>
<tr>
<td>
<img src="Events_images\Events_img7.png" alt="C:\Users\ApoorvahR\Desktop\7.png" width="329pt" height="222pt"</td><td>
<img src="Events_images\Events_img8.png" alt="C:\Users\ApoorvahR\Desktop\8.png" width="322pt" height="158pt"</td></tr>
</table>

_Dialog triggered dragStart and dragStop event_


<table>
<tr>
<td>
<img src="Events_images\Events_img9.png" alt="C:\Users\ApoorvahR\Desktop\9.png" width="323pt" height="214pt"</td><td>
<img src="Events_images\Events_img10.png" alt="C:\Users\ApoorvahR\Desktop\10.png" width="320pt" height="212pt"</td></tr>
</table>

_Dialog triggered resize and resizeStart event_


{% include image.html url="/js/Dialog/Events_images/Events_img11.png" Caption="Dialog triggered resizeStop event"%}



