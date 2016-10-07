---
layout: post
title:  Items Count
description: Items Count
documentation: ug
platform: js
keywords: Items Count,Kanban Items Count
---

#Items Count

You can show total cards count in each column's header using the property `enableTotalCount` and the default value is `false`.

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
				enableTotalCount:true,
                columns: [
                    { headerText: "Backlog", key: "Open"},
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    content: "Summary",
                    primaryKey: "Id"
                }
            });
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Items_count_images/Items_count_img1.png)


## Customize Items count text

You can customize the Items count text using the property `totalCount.text`.

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
				enableTotalCount:true,
                columns: [
                    { headerText: "Backlog", key: "Open",totalCount:{text:"Backlog Count"}},
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    content: "Summary",
                    primaryKey: "Id"
                }
            });
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Drag_and_Drop_images/Items_count_img2.png)
