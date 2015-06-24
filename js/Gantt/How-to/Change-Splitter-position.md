---
layout: post
title: Change-Splitter-position
description: change splitter position
platform: js
control: Gantt
documentation: ug
---

# Change Splitter position

In Gantt control, Splitter separates the Treegrid section from the Chart section,and is possible to change the position of the Splitter while loading the Gantt by using the `splitterPosition` property, thereby varying the width of the Treegrid and Chart sections in the control.  `SplitterPosition` property denotes the percentage of the Treegrid section’s width to be rendered and this property supports both pixels and percentage values.

The following code example explains how to define the `splitterPosition` property in the Gantt.

{% highlight js %}

    $("#gantt").ejGantt({

        // ...     

        splitterPosition: "50%",

        //also you can define with pixel value as 
        //‘ splitterPosition:”650” ’ (or) ‘ splitterPosition:“650px” ’

    });

{% endhighlight %}

{% include image.html url="/js/Gantt/How-to/Change-Splitter-position_images/Change-Splitter-position_img2.png" Caption="Gantt with 30 % splitter position"%}

{% include image.html url="/js/Gantt/How-to/Change-Splitter-position_images/Change-Splitter-position_img3.png" Caption="Gantt with 50% splitter position"%}

{% include image.html url="/js/Gantt/How-to/Change-Splitter-position_images/Change-Splitter-position_img4.png" Caption="Gantt with 600px splitter position"%}

