---
layout: post
title: keyboard-interaction
description: keyboard interaction
platform: js
control: DropDownList
documentation: ug
---

# Keyboard Interaction

You can use **Keyboard** shortcut keys as an alternative to the mouse on using **Dropdown** widget. **Dropdown** Widget allows you to perform all kind of actions using keyboard shortcuts.

_Table_ _3__: Keyboard Shortcut K__eys_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
<a href=http://en.wikipedia.org/wiki/Access_key>Access key</a> + j	</td><td>
Focuses into the Dropdown text box</td></tr>
<tr>
<td>
Up</td><td>
Moves to previous item in pop up</td></tr>
<tr>
<td>
Down</td><td>
Moves to next item in pop up</td></tr>
<tr>
<td>
Enter</td><td>
Selects the focused item</td></tr>
<tr>
<td>
Esc</td><td>
Closes the popup window</td></tr>
<tr>
<td>
Left </td><td>
Moves to previous item in pop up</td></tr>
<tr>
<td>
Right </td><td>
Moves to next item in pop up</td></tr>
<tr>
<td>
Home</td><td>
Navigates to the starting item </td></tr>
<tr>
<td>
End</td><td>
Navigates to the end item </td></tr>
<tr>
<td>
Alt + Up</td><td>
Close the popup window</td></tr>
<tr>
<td>
Alt +down </td><td>
Opens the popup window </td></tr>
</table>
**Configure Keyboard Interaction**

The following steps explains you to enable keyboard interaction for a dropdown textbox.

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget and enable keyboard interaction by setting the **accesskey** property



<table>
<tr>
<td>
<b>[HTML]</b>           &lt;input type="text" id="dropdowmlist" accesskey="j"/&gt;           &lt;div id="list"&gt;               &lt;ul&gt;                 <li>Art</li>                 <li>Architecture</li>                 <li>Biography</li>                 <li>comics</li>                 <li>Sports</li>                 <li>Science</li>            &lt;/ul&gt;           &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Render <b>Dropdownlist</b> control    $('#dropdownlist”).ejDropDownList({                width: 200,                targetID: "list",            });</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b>// Add a DropDownList element using the helper class in CSHTML@Html.EJ().DropDownList("dropdownlist").TargetID("list")           &lt;div id="list"&gt;    &lt;ul&gt;        <li>Art</li>        <li>Architecture</li>        <li>Biography</li>        <li>Comics</li>        <li>Sports</li>        <li>Science</li>    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JavaScript]// Render Dropdown list control     &lt;script type="text/javascript"&gt;        $(function () {            //Control focus key            $(document).on("keydown", function (e) {                if (e.altKey && e.keyCode === 74) { // j- key code.                    $("#dropdownlist_wrapper").focus();                }            });                    });    &lt;/script&gt; </td></tr>
</table>


**[ASPX]**

// Add Dropdown list widget in ASPX page



&lt;div class="control"&gt;

      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Width="200px" AccessKey="j"  runat="server"&gt;

      &lt;/ej:DropDownList&gt;

     &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

             &lt;/ul&gt;

     &lt;/div&gt;

&lt;/div&gt;



Run the sample, press Alt + J to focus in the **DropdownList****Dropdownlist** widget that enables it and you can navigate using arrow keys and Esc key to close the popup.


![](keyboard-interaction_images\keyboard-interaction_img1.png)

_Figure_ _59__33__:_ _DropdownList____Dropdown list_ _focused_ _and moved with Keyboard shortcut_



