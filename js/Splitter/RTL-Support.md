---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: Splitter
documentation: ug
api: /api/js/ejsplitter
---

# RTL Support

The **Splitter** provides you with **RTL** (**Right-To-Left**) support. The alignment of **Splitter** can be changed from **Left-To-Right** to **Right-To-Left**.

## Enable RTL

The following steps explain enabling the right-to-left property for **Splitter** widget.

In the **HTML** page set the corresponding **&lt;div&gt;** elements for outer and inner **Splitter** control.

{% highlight html %}

<div id="outerSplitter">
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3"> JavaScript </h3>
        </div>
    </div>
    <div id="innerSplitter">
        <div>
            <div style="padding: 0px 15px;">
                <h3 class="h3">Tools </h3>
                Essential Tools is an collection of user interface components used to create interactive
                            JavaScript applications.
            </div>
        </div>
        <div>
            <div style="padding: 0px 15px;">
                <h3 class="h3">Chart </h3>
                Essential Chart is a business-oriented charting component.
            </div>
        </div>
        <div>
            <div style="padding: 0px 15px;">
                <h3 class="h3">Grid </h3>
                Essential JavaScript Grid offers full featured a Grid control with extensive support for
                            Grouping and the display of hierarchical data.
            </div>
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

    $("#outerSplitter").ejSplitter({
        height: 250, width: 600,
        orientation: ej.Orientation.Vertical,
        enableRTL: true,
        properties: [{ paneSize: 60 }]
    });
    
    $("#innerSplitter").ejSplitter({
        width: 600,
        properties: [{ paneSize: 200 }, { paneSize: 170 }]
    });

{% endhighlight %}

The output for **Splitter** when [enableRTL](https://help.syncfusion.com/api/js/ejsplitter#members:enablertl) is “**true**”.

![](/js/Splitter/RTL-Support_images/RTL-Support_img1.png) 









