---
layout: post
title: Keyboard-Interaction
description: keyboard interaction
platform: js
control: NumericTextbox
documentation: ug
---

# Keyboard Interaction

With the keyboard navigation enabled in the **NumericTextBox** control, it is possible to control the actions of the **NumericTextBox** with the provided shortcut keys. Almost all the **NumericTextBox** actions that are done through mouse can be controlled with shortcut keys.

The various keyboard shortcuts available within the **NumericTextBox** control are discussed in the following table. 

_Keyboard Shortcuts_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
<a href=http://en.wikipedia.org/wiki/Access_key>Access key</a><b> + j</b></td><td>
Focuses the control</td></tr>
<tr>
<td>
Up</td><td>
Increments the value</td></tr>
<tr>
<td>
Down</td><td>
Decrements the value</td></tr>
<tr>
<td>
Tab</td><td>
Focus the next element</td></tr>
</table>
## Configuring Keyboard Navigation

The following steps explain the implementation of keyboard interaction in **NumericTextBox** .

1. In the HTML page set the corresponding &lt;input&gt; elements for rendering NumericTextBox controls. Set the accesskey property to the NumericTextBox control for focusing the control while key is pressed.



<table>
<tr>
<td>
<b>[HTML]</b>      &lt;input id="numeric" type="text" accesskey="j"/&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 11                    });    &lt;/script&gt;</td></tr>
</table>


2. Run the above example and press [Access key](http://en.wikipedia.org/wiki/Access_key) **+ j** key to focus the **NumericTextBox**widget. Perform provided functionality by using keyboard shortcuts.



{% include image.html url="/js/NumericTextBox/Concepts-and-Features/Keyboard-Interaction_images/Keyboard-Interaction_img1.png" Caption=""%}

_NumericTextBox focused with keyboard shortcut_

