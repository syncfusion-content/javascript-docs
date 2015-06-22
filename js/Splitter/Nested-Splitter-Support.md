---
layout: post
title: Nested-Splitter-Support
description: nested splitter support
platform: js
control: Splitter
documentation: ug
---

# Nested Splitter Support

The **Splitter** provides nested pane support that allows you to add a pane between two pane elements.

## Configure Nested Splitter

The following steps explain the implementation of the “**nestedsplitter**” option.

In the **HTML** page set the corresponding **&lt;div&gt;** elements for outer and inner **Splitter** control. 

{% highlight html %}

    <div id="outersplitter">
        <div>
            <div style="padding: 0px 15px;">
                <h3 class="h3">ASP.NET MVC </h3>
            </div>
        </div>
        <div id="innersplitter">
            <div>
                <div style="padding: 0px 15px;">
                    <h3 class="h3">Tools </h3>
                    Essential Tools is an collection of user interface components used to create interactive
                                ASP.NET MVC applications.
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
                    Essential Mvc Grid offers full featured a Grid control with extensive support for
                                Grouping and the display of hierarchical data.
                </div>
            </div>
        </div>
    </div>

{% endhighlight %}

{% highlight js %}


    $("#outersplitter").ejSplitter({
        height: 280, width: 600,
        orientation: ej.Orientation.Vertical,
        properties: [{ paneSize: 60 }]
    });

    $("#innersplitter").ejSplitter({
        width: 600,
        properties: [{ paneSize: 200 }, { paneSize: 170 }]
    });


{% endhighlight %}

The output for **nested Splitter**.



{% include image.html url="/js/Splitter/Nested-Splitter-Support_images/Nested-Splitter-Support_img1.png" Caption="Nested Splitter"%}

