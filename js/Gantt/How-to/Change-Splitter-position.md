---
layout: post
title: Change splitter position in JavaScript Gantt | Syncfusion
description: Learn hera all about change splitter position Syncfusion Essential JavaScript Gantt control, its elements and more details.
platform: js
control: Gantt
documentation: ug
---

# Change splitter position at load in JavaScript Gantt

In Gantt control, Splitter separates the TreeGrid section from the Chart section and is possible to change the position of the Splitter while loading the Gantt by using the [`splitterSettings`](/api/js/ejgantt#members:splittersettings "splitterSettings") property, thereby varying the width of the TreeGrid and Chart sections in the control. [`splitterSettings.position`](/api/js/ejgantt#members:splittersettings-position "splitterSettings.position") property denotes the percentage of the TreeGrid section’s width to be rendered and this property supports both pixels and percentage values.
And also we can define the splitter position as column index value by using [`splitterSettings.index`](/api/js/ejgantt#members:splittersettings-index "splitterSettings.index") property.

The following code example explains how to define the [`splitterSettings.position`](/api/js/ejgantt#members:splittersettings-position "splitterSettings.position") property in the Gantt.

{% highlight javascript %}

    $("#gantt").ejGantt({

        // ...     
        splitterSettings: {
            position: "50%",
        },

        //also you can define with pixel value as 
        //‘ splitterSettings: { position: "650" } (or) ‘ splitterSettings: { position: "650px" } ’
        //you can define splitter index value as below
            //splitterSettings: {
            //    index: 3,
            //},

    });

{% endhighlight %}

![Change splitter position in JavaScript Gantt.](/js/gantt/how-to/change-splitter-position_images/javascript-gantt-splitter-position.png)

Gantt with 30% splitter position
{:.caption}

![Change splitter 30% position in JavaScript Gantt.](/js/gantt/how-to/change-splitter-position_images/javascript-gantt-thirty-percent-position.png)

Gantt with 50% splitter position
{:.caption}

![Change splitter 50% position in JavaScript Gantt.](/js/gantt/how-to/change-splitter-position_images/javascript-gantt-fifty-percent-position.png)

Gantt with 600px splitter position
{:.caption}

![JavaScript Gantt with 600px splitter position.](/js/gantt/how-to/change-splitter-position_images/javascript-gantt-px-position.png)

Gantt splitter positioned on third indexed column.
{:.caption}

N> We can define the splitter position value by using [`splitterPosition`](/api/js/ejgantt#members:splitterposition) property also, but this property was deprecated with [`splitterSettings.position`](/api/js/ejgantt#members:splittersettings-position "splitterSettings.position") property.

## Change splitter position dynamically

In Gantt, we can change the splitter position dynamically by using [`setSplitterPosition`](/api/js/ejgantt#methods:setsplitterposition) and [`setSplitterIndex`](/api/js/ejgantt#methods:setsplitterindex) methods. The following code example shows how to use this methods.

{% highlight javascript %}

    $("#gantt").ejGantt({
        // ...     
        splitterSettings: {
            position: "50%",
        },
    });

$("#set_position").click(function () {
    $("#gantt").ejGantt("setSplitterPosition", "400");
});

$("#set_index").click(function () {
    $("#gantt").ejGantt("setSplitterIndex", 3);
});

{% endhighlight %}

You can find the JS playground sample for this methods [here](https://jsplayground.syncfusion.com/Sync_qxj4bcda "Demo Link").