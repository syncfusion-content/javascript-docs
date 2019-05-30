---
layout: post
title:  Essential EJ1 Syncfusion Kanban Prioritization of cards
description: The priority property is used to reorder the cards position in any desired place by dropping the card in Syncfusion JavaScript Kanban component.
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

![Card Priority](Card_Priority_images/card_priority_img1.png)

N> For Drag and Drop event handling, please refer this [API](https://help.syncfusion.com/api/js/ejkanban#events:carddrag).

N> If the [`priority`](https://help.syncfusion.com/api/js/ejkanban#members:fields-priority) property is not set in the Kanban fields, the cards are dropped based on the specifying JSON data orders in a particular column.  If not set, drop the card in a particular position based on the previous card `priority` value and the next card’s `priority` values will change dynamically.