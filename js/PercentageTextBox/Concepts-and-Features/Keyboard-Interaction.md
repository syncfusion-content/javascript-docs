---
layout: post
title: Keyboard-Interaction
description: keyboard interaction
platform: js
control: PercentageTextBox 
documentation: ug
---

# Keyboard Interaction

With the keyboard navigation enabled in the **PercentageTextBox** control, it is possible to control the actions of the **PercentageTextBox** with the provided shortcut keys. Almost all the **PercentageTextBox** actions that are done through mouse can be controlled with shortcut keys.

The various keyboard shortcuts available within the **PercentageTextBox** control are discussed in the following table. 

_Table_ _1__: Keyboard Shortcuts_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
<a href="http://en.wikipedia.org/wiki/Access_key">Access key</a><b> + j</b></td><td>
Focuses the PercentageTextBox<b> </b>control</td></tr>
<tr>
<td>
Up</td><td>
Increments the value</td></tr>
<tr>
<td>
Down</td><td>
Decrements the value</td></tr>
</table>
## Configuring Keyboard Navigation

The following steps explain the implementation of keyboard interaction in **PercentageTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. Set the **accesskey** property to the **PercentageTextBox** control for focusing the control while key is pressed.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" accesskey="j" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 22                    });    &lt;/script&gt;</td></tr>
</table>


Run the above example and press [Access key](http://en.wikipedia.org/wiki/Access_key) **+ j** key to focus the **PercentageTextB****ox******widget. Perform provided functionality by using keyboard shortcuts.



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Keyboard-Interaction_images/Keyboard-Interaction_img1.png" Caption="Figure 31: PercentageTextBox focused with keyboard shortcut"%}





















