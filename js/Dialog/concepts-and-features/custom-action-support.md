---
layout: post
title: custom-action-support
description: custom action support
platform: js
control: Dialog
documentation: ug
---

# Custom Action Support

The **Dialog** provides custom action buttons such as close, collapsible, maximize, minimize and pin. You can set the action buttons as per your requirement in the **Dialog**.

## Configure Custom Action

The following steps explains you the implementation of custom action. 

* In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="customAction" title="Audi-R8"&gt;        &lt;img src="Content/images/r8-coupe.png" /&gt;        The Audi R8 was initially equipped with a 4.2 litre V8 engine. Specifically, it is an all-aluminum alloy 32-valve (four valves per cylinder) petrol engine, utilising Fuel Stratified Injection (FSI), and has a displacement of 4,163 cubic centimetres (254.0 cu in).    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>actionButtons</b> property in the <b>Dialog</b> function. The default value of <b>actionButtons</b> is <b>[“close”]</b>    &lt;script type="text/javascript"&gt;        $("#customAction").ejDialog({            width: 300,            <b>actionButtons: ["close", "collapsible", "maximize", "minimize", "pin"]                               </b>        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and assign the ActionButtons value.** 



@{List<string> icon = new List<string>() { "close", "collapsible", "maximize", "minimize", "pin" };}



@{Html.EJ().Dialog("customaction").Title("Audi-R8").ContentTemplate(@&lt;div&gt;

   &lt;img src="@Url.Content("~/Content/images/r8-coupe.png")" /&gt;

       The Audi R8 was initially equipped with a 4.2 litre V8 engine. Specifically, it is an all-aluminum alloy 32-valve (four valves per cylinder) petrol engine, utilising Fuel Stratified Injection (FSI), and has a displacement of 4,163 cubic centimetres (254.0 cu in).&lt;/div&gt;).Width(300).**ActionButtons(icon)**.Render();}





**[ASPX]**

**// In the ASPX page add the Dialog widget and assign the ActionButtons value.**



    &lt;ej:Dialog ID="customaction" runat="server" Width="300" Title="Audi-R8" ActionButtons="close,collapsible,maximize,minimize,pin"&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                &lt;img src="images/r8-coupe.png" /&gt;

                The Audi R8 was initially equipped with a 4.2 litre V8 engine. Specifically, it is an all-aluminum alloy 32-valve (four valves per cylinder) petrol engine, utilising Fuel Stratified Injection (FSI), and has a displacement of 4,163 cubic centimetres (254.0 cu in).

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt; 



* The output of **actionButtons** in **Dialog** widget is as follows.

![C:\Users\ApoorvahR\Desktop\14.png](custom-action-support_images\custom-action-support_img1.png)

_Figure_ _29__19__: Dialog with “actionButtons_____

