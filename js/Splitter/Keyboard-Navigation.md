---
layout: post
title: Keyboard-Navigation
description: keyboard navigation
platform: js
control: Splitter
documentation: ug
---

# Keyboard Navigation

With the keyboard navigation enabled in the **Splitter** control, it is possible to control the actions of the **Splitter** with the provided shortcut keys. Almost all the **Splitter** actions that are done by mouse can be controlled with shortcut keys.

The various keyboard shortcuts available within the **Splitter** control are discussed in the following table.

Keyboard Shortcuts

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

In the **HTML** page set the corresponding **&lt;div&gt;** element for rendering **Splitter** control. 

{% highlight html %}

        <div id="spliter">
            <div>
                <div class="cont">Pane 1 </div>
            </div>
            <div>
                <div class="cont">Pane 2 </div>
            </div>
        </div>

{% endhighlight %}

{% highlight js %}


    $("#spliter").ejSplitter({
        height: 250, width: 400,
        properties: [{}, { paneSize: 80 }]
    });

    //Control focus key
    $(document).on("keydown", function (e) {
        if (e.altKey && e.keyCode === 74) { // j- key code.
            $("#spliter .e-splitbar")[0].focus();
        }
    });


{% endhighlight %}

Run the sample and press **Alt + J** to focus the **Splitter** widget. Perform provided functionality by using keyboard shortcuts.



{% include image.html url="/js/Splitter/Keyboard-Navigation_images/Keyboard-Navigation_img1.png" Caption="Splitter focused with keyboard shortcut"%}

