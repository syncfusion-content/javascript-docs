---
layout: post
title: behavior-settings-
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

* In an **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable resize in the <b>Dialog</b> function by setting <b>enableResize </b>property as true. By default, value for <b>enableResize</b> is <b>true</b>     &lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#Dialog").ejDialog({                height: 200,                width: 300,                enableResize: true            });        });    &lt;/script&gt;&lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,            <b>enableResize: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add the Dialog widget using helpers and set EnableResize to ‘true’.** 



@{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").ContentTemplate(@<div>The Syncfusion Dialog control is rendered.&lt;/div&gt;).Width(300).Height("200").

**EnableResize(true)**.Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and set EnableResize as true.** 



&lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" EnableResize="true" Title="Syncfusion Dialog"&gt;

    &lt;DialogContent&gt;       

        &lt;div&gt;

            The Syncfusion Dialog control is rendered.

        &lt;/div&gt;

    &lt;/DialogContent&gt;

&lt;/ej:Dialog&gt;





* The output for **Dialog** control when “**enableResize**” is “**true”** is as follows.

![C:\Users\ApoorvahR\Desktop\1.png](behavior-settings-_images\behavior-settings-_img1.png)

_Figure_ _16__6__: Dialog with “enableResize”_                                                                                 

## Drag Support

The **Dialog** control supports the drag functionality. You can click the **Dialog** header and drag the control anywhere in the web page.

### Allow Drag Option

The following steps explains you the implementation of drag option in the **Dialog** control. 

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Allow drag in the <b>Dialog</b> function by setting <b>allowDraggable</b> property as <b>true</b>. The default value for <b>allowDraggable</b> is <b>true</b> in the <b>Dialog</b> control    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            allowDraggable: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set AllowDraggable to ‘true’.**



@{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").ContentTemplate(@<div>The Syncfusion Dialog control is rendered.&lt;/div&gt;).Width(300).Height("200").

**AllowDraggable(true)**.Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and set AllowDraggable as true.** 



&lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" AllowDraggable="true" Title="Syncfusion Dialog"&gt;

    &lt;DialogContent&gt;       

        &lt;div&gt;

            The Syncfusion Dialog control is rendered.

        &lt;/div&gt;

    &lt;/DialogContent&gt;

&lt;/ej:Dialog&gt;





* The output for **Dialog** control when “**allowDraggable”** is “**true**” is as follows.

![C:\Users\ApoorvahR\Desktop\2.png](behavior-settings-_images\behavior-settings-_img2.png)

_Figure_ _17__7__: Dialog with "allowDraggable"___

## Close Icon ToolTip Support

* You can change the close icon tooltip in the **Dialog** control by using **closeIconTooltip** property. The default value for **cCloseIconTooltip** is **close** in the **Dialog** control.

### Define Close Icon ToolTip

The following steps explains you the implementation of close icon tooltip option in the **Dialog** control. 

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 


<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>closeIconTooltip</b> value in the <b>Dialog</b> function using the following codes. The default value for <b>closeIconTooltip</b> is <b>close</b> in the <b>Dialog</b> control    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,            <b>closeIconTooltip: "close"</b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and assign the CloseIconTooltip property as close.**



    @{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").Items(data =>

      {

          data.ContentTemplate(@<div>The Syncfusion Dialog control is rendered.&lt;/div&gt;);

      }).Width(300).Height("200").**CloseIconTooltip("close")**.Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and set the CloseIconTooltip value as close.**



&lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" CloseIconTooltip="close" Title="Syncfusion Dialog"&gt;

    &lt;DialogContent&gt;       

        &lt;div&gt;

            The Syncfusion Dialog control is rendered.

        &lt;/div&gt;

    &lt;/DialogContent&gt;

&lt;/ej:Dialog&gt;





* The output for **Dialog** control when “**closeIconTooltip**” is “**close**” is as follows.

![C:\Users\ApoorvahR\Desktop\3.png](behavior-settings-_images\behavior-settings-_img3.png)

_Figure_ _18__8__: Dialog with "closeIconTooltip___

## Persistence Support

The **Dialog** control supports the state maintenance where you can maintain the state of the **Dialog** control in the web page. The default value for **eEnablePersistence** is **false** in the **Dialog** control.

### Enable Persistence Option

The following steps explains the implementation of persistence support in the **Dialog** control. 

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable the persistence to the <b>Dialog</b> function by setting <b>enablePersistence</b> property as true. The default value for <b>enablePersistence</b> is <b>false</b> in the <b>Dialog</b> control    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            enablePersistence: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set EnablePersistence to ‘true’.**



    @{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").Items(data =>

      {

          data.ContentTemplate(@<div>The Syncfusion Dialog control is rendered.&lt;/div&gt;);

      }).Width(300).Height("200").**EnablePersistence(true)**.Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and set EnablePersistence as true.**

&lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" EnablePersistence="true" Title="Syncfusion Dialog"&gt;

    &lt;DialogContent&gt;       

        &lt;div&gt;

            The Syncfusion Dialog control is rendered.

        &lt;/div&gt;

    &lt;/DialogContent&gt;

&lt;/ej:Dialog&gt;




Make resize and reload the web page. The state is maintained in the **Dialog** control. The output for **Dialog** control when “**enablePersistence**” is “**true**” is as follows. 

![C:\Users\ApoorvahR\Desktop\4.png](behavior-settings-_images\behavior-settings-_img4.png)

_Figure_ _19__9__: Dialog with “enablePersistence"_

## Enabled or Disabled

The **Dialog** control supports the enabled or disabled option that allows you to enable or disable the **Dialog** control in the web page.

### Enable Dialog Control

The following steps explains the implementation of enable option in the **Dialog** control. 

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable the <b>Dialog</b> in the <b>Dialog</b> function by setting <b>enabled</b> property as true. The default value for <b>enabled</b> is <b>true</b> in the <b>Dialog</b> control    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            enabled: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set Enabled to ‘true’.** 



@{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").ContentTemplate(@<div>The Syncfusion Dialog control is rendered..&lt;/div&gt;).Width(300).Height("200").

**Enabled(true).**Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and set Enabled as true.**



&lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" Enabled="true" Title="Syncfusion Dialog"&gt;

    &lt;DialogContent&gt;       

        &lt;div&gt;

            The Syncfusion Dialog control is rendered.

        &lt;/div&gt;

    &lt;/DialogContent&gt;

&lt;/ej:Dialog&gt;



* The output for **Dialog** control when “enabled” is “**true**” is as follows.          

![C:\Users\ApoorvahR\Desktop\5.png](behavior-settings-_images\behavior-settings-_img5.png)

_Figure_ _20__10__: Dialog with “enabled" as “true”_

## Disable Dialog Control

The following steps explains you the implementation of disable option in the **Dialog** control. 

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Disable the <b>Dialog</b> in the <b>ejDialog</b> function by setting <b>enabled</b> as false    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            enabled: false</b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set Enabled to ‘false’.**



    @{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").Items(data =>

      {

          data.ContentTemplate(@<div>The Syncfusion Dialog control is rendered.&lt;/div&gt;);

      }).Width(300).Height("200").**Enabled(false)**.Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and set Enabled as false.**

&lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" Enabled="false" Title="Syncfusion Dialog"&gt;

    &lt;DialogContent&gt;       

        &lt;div&gt;

            The Syncfusion Dialog control is rendered.

        &lt;/div&gt;

    &lt;/DialogContent&gt;

&lt;/ej:Dialog&gt;



* The output for **Dialog** control when **enabled** is “**false**” is as follows.

![C:\Users\ApoorvahR\Desktop\6.png](behavior-settings-_images\behavior-settings-_img6.png)

_Figure_ _21__11__: Dialog with “enabled" as “false”___

## Dialog Position

The **Dialog** provides the option to place the control based upon its X-axis and Y-axis position in the web page. The following steps explains you the implementation of dialog position option.

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.&lt;br /&gt;        Position &lt;br /&gt;        X-Axis : 20 &lt;br /&gt;        Y-Axis : 26    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the X and Y position to the <b>Dialog</b> function by setting <b>Position</b> property    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            position: { X: 20, Y: 26 }</b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set the Position values.**



@{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").ContentTemplate(@&lt;div&gt;

            The Syncfusion Dialog control is rendered.&lt;br /&gt;

            Position

            &lt;br /&gt;

            X-Axis : 20

            &lt;br /&gt;

            Y-Axis : 26

        &lt;/div&gt;).Width(300).Height("200").**Position(p => p.XValue("20").YValue("26"))**.

Render();}







**[ASPX]**

**// In the ASPX page add the Dialog widget and set Position values.**



    &lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" Title="Syncfusion Dialog"&gt;

**&lt;Position XValue="20" YValue="26" /&gt;**

        &lt;DialogContent&gt;

            &lt;div&gt;

                The Syncfusion Dialog control is rendered.&lt;br /&gt;

                Position

              &lt;br /&gt;

                X-Axis : 20

              &lt;br /&gt;

                Y-Axis : 26

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt;





* The output for **Dialog** control after setting X-axis and Y-axis value.

![C:\Users\ApoorvahR\Desktop\7.png](behavior-settings-_images\behavior-settings-_img7.png)

_Figure_ _22__12__: Dialog with “Position"_

## Header Option

You can show or hide the **Dialog** header by setting **showHeader** property. The following steps explains you the implementation of **Dialog** header option.

**Show Header**

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 

<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.            &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showHeader</b> property as true in the <b>Dialog</b> function    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            showHeader: </b>true        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set the ShowHeader as true.** 



@{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").ContentTemplate(@<div>The Syncfusion Dialog control is rendered.&lt;/div&gt;).Width(300).Height("200").

**ShowHeader(true).**Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and set ShowHeader as true.**



    &lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" ShowHeader="true" Title="Syncfusion Dialog"&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                The Syncfusion Dialog control is rendered.               

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt;



* The output for **Dialog** control when **showHeader** is “**true**” is as follows.

![C:\Users\ApoorvahR\Desktop\8.png](behavior-settings-_images\behavior-settings-_img8.png)

_Figure_ _23__13__: Dialog with “showHeader" as “true”___

## Hide Header

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.           &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showHeader</b> property as false in the <b>Dialog</b> function    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            showHeader: </b>false        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set the ShowHeader to ‘false’.** 



@{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").ContentTemplate(@<div>The Syncfusion Dialog control is rendered.&lt;/div&gt;).Width(300).Height("200").

**ShowHeader(false).**Render();}







**[ASPX]**

**// In the ASPX page add the Dialog widget and set ShowHeader as false.**



    &lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" ShowHeader="false" Title="Syncfusion Dialog"&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                The Syncfusion Dialog control is rendered.               

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt;





* The output for **Dialog** control when **showHeader** is “**false**” is as follows.

![C:\Users\ApoorvahR\Desktop\9.png](behavior-settings-_images\behavior-settings-_img9.png)

_Figure_ _24__14__: Dialog with “showHeader" as “false”___

## Show at Initial

The **Dialog** control contains an option to be visible or hidden at initialization. The default value for **showOnInit** is **true**. Setting false to the **showOnInit** hides the **Dialog** control at initialization.

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 

<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.           &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showOnInit</b> property as true in the <b>Dialog</b> function    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            showOnInit: true</b> /* false hides the dialog at initialization */           });                           &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set the ShowOnInit to ‘true’.**

@{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").ContentTemplate(@<div>The Syncfusion Dialog control is rendered.&lt;/div&gt;).Width(300).Height("200").

**ShowOnInit(true)**.Render();}



**[ASPX]**

**// In the ASPX page add the Dialog widget and set ShowOnInit as true.**



    &lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" ShowOnInit="true" Title="Syncfusion Dialog"&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                The Syncfusion Dialog control is rendered.               

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt;





* The output for **Dialog** control when **showOnInit** is “**true**” is as follows.

![C:\Users\ApoorvahR\Desktop\10.png](behavior-settings-_images\behavior-settings-_img10.png)

_Figure_ _25__15__: Dialog with “showOnInit"___

## Rounded Corner Support

The **Dialog** can support with rounded corner appearance, the default value for **showRoundedCorner** is **false**. 

* In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div id="Dialog" title="Syncfusion Dialog"&gt;        The Syncfusion Dialog control is rendered.           &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showRoundedCorner</b> property as true in the <b>Dialog</b> function    &lt;script type="text/javascript"&gt;        $("#Dialog").ejDialog({            height: 200,            width: 300,<b>            showRoundedCorner: true </b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set ShowRoundedCorner to ‘true’.**



@{Html.EJ().Dialog("dialog").Title("Syncfusion Dialog").ContentTemplate(@<div>The Syncfusion Dialog control is rendered.&lt;/div&gt;).Width(300).Height("200").

**ShowRoundedCorner(true).**Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and set ShowRoundedCorner as true.**



    &lt;ej:Dialog ID="dialog" runat="server" Width="300" Height="200" ShowRoundedCorner="true" Title="Syncfusion Dialog"&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                The Syncfusion Dialog control is rendered.               

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt;





* The output for **Dialog** control when **showRoundedCorner** is “**true**” is as follows.

![C:\Users\ApoorvahR\Desktop\11.png](behavior-settings-_images\behavior-settings-_img11.png)

_Figure_ _26__16__: Dialog with “showRoundedCorner"_

