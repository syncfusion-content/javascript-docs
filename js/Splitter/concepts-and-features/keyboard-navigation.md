---
layout: post
title: keyboard-navigation
description: keyboard navigation
platform: js
control: Splitter
documentation: ug
---

# Keyboard Navigation

With the keyboard navigation enabled in the **Splitter** control, it is possible to control the actions of the **Splitter** with the provided shortcut keys. Almost all the **Splitter** actions that are done by mouse can be controlled with shortcut keys.

The various keyboard shortcuts available within the **Splitter** control are discussed in the following table.

_Table_ _1__: Keyboard Shortcuts_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Left</td><td>
Moves the Splitbar left. </td></tr>
<tr>
<td>
Right</td><td>
Moves the Splitbar right. </td></tr>
<tr>
<td>
Ctrl + Left</td><td>
Collapses the left pane.</td></tr>
<tr>
<td>
Ctrl + Right</td><td>
Collapses the right pane.</td></tr>
<tr>
<td>
Up</td><td>
Moves the Splitbar up.</td></tr>
<tr>
<td>
Down</td><td>
Moves the Splitbar down.</td></tr>
<tr>
<td>
Ctrl + Up</td><td>
Collapses the top pane.</td></tr>
<tr>
<td>
Ctrl + Down</td><td>
Collapses the bottom pane.</td></tr>
<tr>
<td>
Enter</td><td>
Resize the pane to the current Splitbar position.</td></tr>
<tr>
<td>
Esc</td><td>
Focuses out from the Splitbar.</td></tr>
</table>
## Configuring Keyboard Navigation

The following steps explain to enable keyboard interaction for **Splitter** widget.

* In the **HTML** page set the corresponding **&lt;div&gt;** element for rendering **Splitter** control. 



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="spliter"&gt;            &lt;div&gt;                <div class="cont">Pane 1 &lt;/div&gt;            &lt;/div&gt;            &lt;div&gt;                <div class="cont">Pane 2 &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>Splitter</b> properties and focus key function in the script.    &lt;script type="text/javascript"&gt;            $("#spliter").ejSplitter({                height: 250, width: 400,                properties: [{}, { paneSize: 80 }]            });        });        <b>//Control focus key</b>        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) { // j- key code.                $("#spliter .e-splitbar")[0].focus();            }        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b>@{Html.EJ().Splitter("Splitter").Height("250").Width("400").PaneProperties(    p =>    {        p.Add().ContentTemplate(            @&lt;div&gt;                 <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>            &lt;/div&gt;);        p.Add().ContentTemplate(            @&lt;div&gt;                 <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>            &lt;/div&gt;).PaneSize("80");    }).Render();}</td></tr>
<tr>
<td>
[JavaScript]    &lt;script type="text/javascript"&gt;                    <b>//Control focus key</b>        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) { // j- key code.                $("#spliter .e-splitbar")[0].focus();            }        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>&lt;div id="spliter"&gt;&lt;ej:Splitter ID="splitter" Height="250" Width="400" runat="server"&gt;                &lt;ej:SplitPane&gt;               &lt;div&gt;                <div class="cont">Pane 1 &lt;/div&gt;            &lt;/div&gt;           &lt;/ej:SplitPane&gt;              &lt;ej:SplitPane PaneSize="80"&gt;             &lt;div&gt;                <div class="cont">Pane 2 &lt;/div&gt;            &lt;/div&gt;           &lt;/ej:SplitPane&gt;          &lt;/ej:Splitter&gt;   &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>        <b>//Control focus key</b>        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) { // j- key code.                $("#spliter .e-splitbar")[0].focus();            }        });    &lt;/script&gt;</td></tr>
</table>


* Run the sample and press **Alt + J** to focus the **Splitter** widget. Perform provided functionality by using keyboard shortcuts.



{% include image.html url="\js\Splitter\concepts-and-features\keyboard-navigation_images\keyboard-navigation_img1.png" Caption="Figure 2218: Splitter focused with keyboard shortcut"%}

