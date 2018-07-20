---
layout: post
title: Get column collection in resource view
description: Get column collection in resource view
platform: js
control: Gantt
documentation: ug
---

# Get column collection in resource view

In Gantt resource view it is possible to get all the columns in a variable by using [`getResourceViewEditColumns`](/api/js/ejgantt#methods:getresourcevieweditcolumns) public method. By using this we can add custom columns to gantt which can be editable in add/edit dialog.
The following code example shows this.

{% highlight javascript %}

    $("#resourceGantt").ejGantt({
        load: function () {

            var columns = this.getResourceViewEditColumns();
            var editColumn = {
                field: "customColumn",
                mappingName: "CustomColumn",
                headerText: "Custom Column",
            }
            columns.push(editColumn);
        }
    });
            
{% endhighlight %}

The following screen shot shows the custom column in add dialog.

![](/js/Gantt/How-to/Get-resource-view-column_images/image-1.png)
