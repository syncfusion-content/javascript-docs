---
layout: post
title: Searching
description: searching
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---
# Searching

The Gantt control for JavaScript has in-built support for searching any content in Gantt.

### Searching for content columns

In Gantt, we can search the content using the JavaScript method [`searchItem`](/api/js/ejgantt#methods:searchitem "searchItem(searchString)") with search key as parameter. Also, we can integrate the search text box in Gantt toolbar by adding search toolbar item in [`toolbarItems`](/api/js/ejgantt#members:toolbarsettings-toolbaritems) property.

The following code example shows you how to add search option in Gantt toolbar.

{% highlight javascript %}
 $("#GanttContainer").ejGantt({
            //...
            toolbarSettings: {
                showToolbar: true,
                toolbarItems: [
                ej.Gantt.ToolbarItems.Search, //TO FIND THE TASK
                ],
            }
        });
{% endhighlight %}

The following screenshot shows the output of searching for string in Gantt control.

![](/js/Gantt/Searching_images/Searching_img1.png)