---
layout: post
title:  Prioritization of cards
description: Prioritization of cards
documentation: ug
platform: js
keywords: card priority
api : /api/js/ejkanban
---

# Prioritization of cards

Prioritizing cards is easy with drag-and-drop re-ordering that helps you to categorize most important work at the top.  Cards can be categorized with priority by mapping specific database field into [`priority`](https://help.syncfusion.com/api/js/ejkanban#members:fields-priority) property.

`RankId` defined in the dataSource which is consist priority of cards. The `RankId` will be changed while card ordering changes through `Drag and Drop` and `Editing`.

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
                    priority: "RankId"
                }
        });
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Card_Priority_images/card_priority_img1.png)

N> For Drag and Drop event handling, please refer this [API](https://help.syncfusion.com/api/js/ejkanban#events:carddrag).

N> If you are not set [`priority`](https://help.syncfusion.com/api/js/ejkanban#members:fields-priority) property in the fields of Kanban, cards are dropped based on specifying JSON data orders in a particular column.  If you are set [`priority`](https://help.syncfusion.com/api/js/ejkanban#members:fields-priority) property, you can drop the card at a particular position based on previous card `priority` value and also dynamically changed on next cards `priority` values.