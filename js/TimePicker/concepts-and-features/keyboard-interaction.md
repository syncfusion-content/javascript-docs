---
layout: post
title: keyboard-interaction
description: keyboard interaction
platform: js
control: TimePicker
documentation: ug
---

# Keyboard Interaction

You can use **Keyboard** shortcut keys as an alternative to the mouse on using **TimePicker** widget. **TimePicker** widget allows you to perform all kinds of actions using keyboard shortcuts.

_Table_ _1__: List of keyboard shortcuts_

<table>
<tr>
<td>
Shortcut Key</td><td>
Description</td></tr>
<tr>
<td>
<a href=http://en.wikipedia.org/wiki/Access_key>Access key</a> + j</td><td>
Focuses into Timepicker widget</td></tr>
<tr>
<td>
Alt + Down</td><td>
Opens/Hides the popup</td></tr>
<tr>
<td>
Right/Left</td><td>
Moves to adjacent part</td></tr>
<tr>
<td>
Up</td><td>
Increments the value</td></tr>
<tr>
<td>
Down</td><td>
Decrements the value</td></tr>
</table>


**When popup is open**

_Table_ _2__: List of keyboard shortcuts_

<table>
<tr>
<td>
Shortcut Key</td><td>
Description</td></tr>
<tr>
<td>
Up</td><td>
Selects the previous time </td></tr>
<tr>
<td>
Down </td><td>
Selects the next time.</td></tr>
<tr>
<td>
Home/End</td><td>
Moves to the first / last item</td></tr>
<tr>
<td>
Esc</td><td>
Closes the popup</td></tr>
</table>
### Configure Keyboard Interaction

The following steps explains you on how to enable keyboard interaction for the **TimePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget and enable keyboard interaction by setting the **access key** property.





<table>
<tr>
<td>
<b>[HTML]</b>        &lt;input type="text" id="time" accesskey="j"/&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// You can render the TimePicker control using the following code.</b>   &lt;script type="text/javascript"&gt;    $(function () {         $('#time').ejTimePicker();            //Control focus key            $(document).on("keydown", function (e) {                if (e.altKey && e.keyCode === 74) { // j- key code.                    $("#time ").focus();                }            });        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[_cshtml]</b><b>// Add the following code in your view page to render TimePicker.</b>        @Html.EJ().TimePicker("time")</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Render the TimePicker control.</b>&lt;script type="text/javascript"&gt;$(function () {      $(document).on("keydown", function (e) {           if (e.altKey && e.keyCode === 74) { // j- key code.                 $("#time").<b>focus()</b>;     }});    });  &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[_aspx]</b>// Add the code in ASPX page to render TimePicker&lt;ej:TimePicker ID="time" runat="server"&gt;&lt;/ej:TimePicker&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Render the TimePicker control &lt;script type="text/javascript"&gt;$(function () {      $(document).on("keydown", function (e) {           if (e.altKey && e.keyCode === 74) { // j- key code.                 $("#time").<b>focus()</b>;     }});    });  &lt;/script&gt;</td></tr>
</table>


Run the code sample, press [Access key](http://en.wikipedia.org/wiki/Access_key)**Alt** **+ J** to focus in the **TimePicker** widget that enables it and you can navigate using arrow keys and Esc key to close the popup.



![](keyboard-interaction_images\keyboard-interaction_img1.png)![](keyboard-interaction_images\keyboard-interaction_img2.png)

_Figure_ _22__35__:_ _TimePicker_ _focused with keyboard shortcut_





