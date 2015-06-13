---
layout: post
title: Keyboard-Interaction
description: keyboard interaction	
platform: js
control: Dialog
documentation: ug
---

# Keyboard Interaction	

The **Dialog** provides you to interact with the keyboard actions instead of mouse actions. All the **Dialog** actions can be achieved by using **Keyboard** shortcuts.

_Key shortcuts for Dialog_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Alt + j	</td><td>
Focus the Dialog control</td></tr>
<tr>
<td>
Up</td><td>
Dialog moves up direction</td></tr>
<tr>
<td>
Down</td><td>
Dialog moves down direction</td></tr>
<tr>
<td>
Right</td><td>
Dialog moves right direction</td></tr>
<tr>
<td>
Left</td><td>
Dialog moves left direction</td></tr>
<tr>
<td>
Esc</td><td>
Dialog window close</td></tr>
</table>

## Configure Keyboard Interaction

The following steps explains you to enable keyboard interaction for **Dialog** control.

1. In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 

{% highlight html %}

**[HTML]**

      <div id="keyboardDialog" title="WinRT">
        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications <span>including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more.</span>
        It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
        </div>

{% endhighlight %}

{% highlight js %}

**[JavaScript]**

// Set the width and define the Dialog function
    <script type="text/javascript">
        $("#keyboardDialog").ejDialog({
            width: 550            
        });
        //Control focus key
        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) { // j- key code.
                $("#keyboardDialog").focus();
            }	
        });
     </script>

{% endhighlight %}

2. Run the sample and press Alt + j key to focus the **Dialog** control. You can perform the specified option using keyboard shortcuts.

