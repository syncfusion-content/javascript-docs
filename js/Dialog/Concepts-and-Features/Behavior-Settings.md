---
layout: post
title: Behavior-Settings
description: behavior settings 
platform: js
control: Dialog
documentation: ug
---

# Behavior Settings 

## Resize Support

The **Dialog** control can be resized using this feature. You can resize the **Dialog** by dragging the bottom right corner area.

### Enable Resize Option

The following steps explains you the implementation of resize option in the **Dialog** control. 

1. In an HTML page set a &lt;div&gt; element with dialog content for rendering the Dialog control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable resize in the <b>Dialog</b> function by setting <b>enableResize </b>property as true. By default, value for <b>enableResize</b> is <b>true</b>     &lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#Dialog").ejDialog({                height: 200,                width: 300,                enableResize: true            });        });    &lt;/script&gt;</td></tr>
</table>


2. The output for Dialog control when “enableResize” is “true” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img1.png" Caption="Dialog with enableResize"%}

## Drag Support

The **Dialog** control supports the drag functionality. You can click the **Dialog** header and drag the control anywhere in the web page.

### Allow Drag Option

The following steps explains you the implementation of drag option in the **Dialog** control. 

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Allow drag in the <b>Dialog</b> function by setting <b>allowDraggable</b> property as <b>true</b>. The default value for <b>allowDraggable</b> is <b>true</b> in the <b>Dialog</b> control    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            allowDraggable: true</b>        });    &lt;/script&gt;</td></tr>
</table>


2. The output for Dialog control when “allowDraggable” is “true” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img2.png" Caption="Dialog with allowDraggable"%}

## Close Icon ToolTip Support

You can change the close icon tooltip in the **Dialog** control by using **closeIconTooltip** property. The default value for **closeIconTooltip** is **close** in the **Dialog** control.

### Define Close Icon ToolTip

The following steps explains you the implementation of close icon tooltip option in the **Dialog** control. 

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 


<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>closeIconTooltip</b> value in the <b>Dialog</b> function using the following codes. The default value for <b>closeIconTooltip</b> is <b>close</b> in the <b>Dialog</b> control    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,            <b>closeIconTooltip: "close"</b>        });    &lt;/script&gt;</td></tr>
</table>


2. The output for Dialog control when “closeIconTooltip” is “close” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img3.png" Caption="Dialog with  closeIconTooltip"%}

## Persistence Support

The **Dialog** control supports the state maintenance where you can maintain the state of the **Dialog** control in the web page. The default value for **enablePersistence** is **false** in the **Dialog** control.

### Enable Persistence Option

The following steps explains the implementation of persistence support in the **Dialog** control. 

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable the persistence to the <b>Dialog</b> function by setting <b>enablePersistence</b> property as true. The default value for <b>enablePersistence</b> is <b>false</b> in the <b>Dialog</b> control    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            enablePersistence: true</b>        });    &lt;/script&gt;</td></tr>
</table>

Make resize and reload the web page. The state is maintained in the **Dialog** control. The output for **Dialog** control when “**enablePersistence**” is “**true**” is as follows. 

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img4.png" Caption="Dialog with enablePersistence"%}

## Enabled or Disabled

The **Dialog** control supports the enabled or disabled option that allows you to enable or disable the **Dialog** control in the web page.

### Enable Dialog Control

The following steps explains the implementation of enable option in the **Dialog** control. 

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable the <b>Dialog</b> in the <b>Dialog</b> function by setting <b>enabled</b> property as true. The default value for <b>enabled</b> is <b>true</b> in the <b>Dialog</b> control    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            enabled: true</b>        });    &lt;/script&gt;</td></tr>
</table>


2. The output for Dialog control when “enabled” is “true” is as follows.          

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img5.png" Caption="Dialog with enabled  as true"%}

## Disable Dialog Control

The following steps explains you the implementation of disable option in the **Dialog** control. 

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Disable the <b>Dialog</b> in the <b>ejDialog</b> function by setting <b>enabled</b> as false    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            enabled: false</b>        });    &lt;/script&gt;</td></tr>
</table>
2. The output for Dialog control when enabled is “false” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img6.png" Caption="Dialog with enabled  as false"%}

## Dialog Position

The **Dialog** provides the option to place the control based upon its X-axis and Y-axis position in the web page. The following steps explains you the implementation of dialog position option.

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 



<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.&lt;br /&gt;        Position &lt;br /&gt;        X-Axis : 20 &lt;br /&gt;        Y-Axis : 26    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the X and Y position to the <b>Dialog</b> function by setting <b>Position</b> property    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            position: { X: 20, Y: 26 }</b>        });    &lt;/script&gt;</td></tr>
</table>


2. The output for Dialog control after setting X-axis and Y-axis value.

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img7.png" Caption="Dialog with Position "%}

## Header Option

You can show or hide the **Dialog** header by setting **showHeader** property. The following steps explains you the implementation of **Dialog** header option.

**Show Header**

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.            &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showHeader</b> property as true in the <b>Dialog</b> function    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            showHeader: </b>true        });    &lt;/script&gt;</td></tr>
</table>


2. The output for Dialog control when showHeader is “true” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img8.png" Caption="Dialog with showHeader  as true"%}

## Hide Header

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 



<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.           &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showHeader</b> property as false in the <b>Dialog</b> function    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            showHeader: </b>false        });    &lt;/script&gt;</td></tr>
</table>


2. The output for Dialog control when showHeader is “false” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img9.png" Caption="Dialog with showHeader  as false"%}

## Show at Initial

The **Dialog** control contains an option to be visible or hidden at initialization. The default value for **showOnInit** is **true**. Setting false to the **showOnInit** hides the **Dialog** control at initialization.

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.           &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showOnInit</b> property as true in the <b>Dialog</b> function    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            showOnInit: true</b> /* false hides the dialog at initialization */           });                           &lt;/script&gt;</td></tr>
</table>


2. The output for Dialog control when showOnInit is “true” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img10.png" Caption="Dialog with showOnInit"%}

## Rounded Corner Support

The **Dialog** can support with rounded corner appearance, the default value for **showRoundedCorner** is **false**. 

1. In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 



<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.           &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showRoundedCorner</b> property as true in the <b>Dialog</b> function    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            showRoundedCorner: true </b>        });    &lt;/script&gt;</td></tr>
</table>


2. The output for **Dialog** control when **showRoundedCorner** is “**true**” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img11.png" Caption="Dialog with showRoundedCorner "%}

