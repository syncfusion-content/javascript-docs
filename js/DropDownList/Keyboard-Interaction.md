---
layout: post
title: Keyboard-Interaction
description: keyboard interaction
platform: js
control: DropDownList
documentation: ug
---

# Keyboard Interaction

You can use **Keyboard** shortcut keys as an alternative to the mouse on using **Dropdown** widget. **Dropdown** Widget allows you to perform all kind of actions using keyboard shortcuts.

Keyboard Shortcut Keys

<table>
<tr>
<th>Shortcut Key</th><th>Description</th></tr>
<tr>
<td>
<a href="http://en.wikipedia.org/wiki/Access_key">Access key</a> + j	</td><td>
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

## Configure Keyboard Interaction

The following steps explains you to enable keyboard interaction for a dropdown textbox.

In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget and enable keyboard interaction by setting the **accesskey** property

{% highlight html %}

<input type="text" id="dropdowmlist" accesskey="j"/>
<div id="list">
   <ul>
     <li>Art</li>
     <li>Architecture</li>
     <li>Biography</li>
     <li>comics</li>
     <li>Sports</li>
     <li>Science</li>
   </ul>
</div>

{% endhighlight %}

{% highlight js %}

    // Render Dropdownlist control
    $('#dropdownlist').ejDropDownList({
                width: 200,
                targetID: "list"
    });

{% endhighlight %}

Run the sample, press Alt + J to focus in the **DropdownList** widget that enables it and you can navigate using arrow keys and Esc key to close the popup.

{% include image.html url="/js/DropDownList/Keyboard-Interaction_images/Keyboard-Interaction_img1.png" %}
