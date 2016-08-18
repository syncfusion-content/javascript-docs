---
layout: post
title:  Swimlanes
description: Swimlanes
documentation: ug
platform: js
keywords: swimlanes,kanban swimlanes
---

# Swim lanes

Swim lanes are a horizontal categorization of issues in the Kanban control which brings transparency to the workflow. This can be enabled by mapping the [`swimlaneKey`](https://help.syncfusion.com/js/api/ejkanban#members:swimlaneKey) to appropriate column name in the [`dataSource`](https://help.syncfusion.com/js/api/ejkanban#members:datasource).

The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(30));
        
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    content: "Summary",
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    imageUrl: "ImgUrl"
                }
            });
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Swimlane_images/swimlane_img1.png)