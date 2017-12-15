---
layout: post
title: Keyboard-Navigation
description: keyboard navigation
platform: js
control: Splitter
documentation: ug
api: /api/js/ejsplitter
---

# Keyboard Navigation

With the [allowKeyboardNavigation](https://help.syncfusion.com/api/js/ejsplitter#members:allowkeyboardnavigation) enabled in the **Splitter** control, it is possible to control the actions of the **Splitter** with the provided shortcut keys. Almost all the **Splitter** actions that are done by mouse can be controlled with shortcut keys.

The various keyboard shortcuts available within the **Splitter** control are discussed in the following table.

Keyboard Shortcuts

<table>
<tr>
<th>
Shortcut Key</th><th>
Description</th></tr>
<tr>
<td>
Left</td><td>
Moves the Split bar left. </td></tr>
<tr>
<td>
Right</td><td>
Moves the Split bar right. </td></tr>
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
Moves the Split bar up.</td></tr>
<tr>
<td>
Down</td><td>
Moves the Split bar down.</td></tr>
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
Resize the pane to the current Split bar position.</td></tr>
<tr>
<td>
Esc</td><td>
Focuses out from the Split bar.</td></tr>
</table>

## Configuring Keyboard Navigation

The following steps explain to enable keyboard interaction for **Splitter** widget.

In the **HTML** page set the corresponding **&lt;div&gt;** element for rendering **Splitter** control. 

{% highlight html %}

<div id="splitter">
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Tools </h3>
            Essential Tools is an collection of user interface components used to create interactive
            ASP.NET MVC applications.
        </div>
    </div>
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Grid </h3>
            Essential MVC Grid offers full featured a Grid control with extensive support for
            Grouping and the display of hierarchical data.
        </div>
    </div>
</div> 

{% endhighlight %}

{% highlight javascript %}


    $("#splitter").ejSplitter({
        height: 280, 
        width: 600
    });
    
    //Control focus key
    $(document).on("keydown", function (e) {
        if (e.altKey && e.keyCode === 74) { // j- key code.
            $("#splitter .e-splitbar")[0].focus();
        }
    });


{% endhighlight %}

Run the sample and press **Alt + J** to focus the **Splitter** widget. Perform provided functionality by using keyboard shortcuts.

![](/js/Splitter/Keyboard-Navigation_images/Keyboard-Navigation_img1.png) 

