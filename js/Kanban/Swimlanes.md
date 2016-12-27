---
layout: post
title:  Swimlanes
description: Swimlanes
documentation: ug
platform: js
keywords: swimlanes,kanban swimlanes
---

# Swim lanes

Swim lanes are a horizontal categorization of issues in the Kanban control which brings transparency to the workflow. This can be enabled by mapping the [`swimlaneKey`](https://help.syncfusion.com/api/js/ejkanban#members:swimlaneKey) to appropriate column name in the [`dataSource`](https://help.syncfusion.com/api/js/ejkanban#members:datasource).

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

# Drag And Drop between swim lanes

You can set ['allowDragAndDrop'](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-allowdraganddrop) property of ['swimlaneSettings'](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings) as true to enable Drag and Drop between the swim lanes.

If a card is to be dragged in the same swim lane, only a droppable target cell is added to the dotted line border. If a card is dragged from one swim lane to another, all the Kanban cells will be added to the dotted line borders, except the dragged card cell.

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
                },
                swimlaneSettings:{
                    allowDragAndDrop: true,
                },
            });
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Swimlane_images/swimlane_img2.png)

# Unassigned swim lane group

Kanban cards which have null,undefined, empty string("") swimlane key values or user specified swimlane key values in the `keys(swimlaneSettings.unassignedGroup.keys)` collection will be grouped under the Unassigned swimlane group.You can enable and disble this behavior using the property `enable(swimlaneSettings.unassignedGroup.enable)` and the default value is `true`.
  
Default values in the `keys(swimlaneSettings.unassignedGroup.keys)` collection are null,undefined,empty string("").You can also add your own(user-defined) swim-lane key values in the `keys(swimlaneSettings.unassignedGroup.keys)` collection.
  
## Unassigned swim lane group with default values

Kanban cards which have null,undefined, empty string("") swimlane key values will be grouped under the Unassigned swimlane group when Unassigned swim lane group is enabled.(set `true` to `enable(swimlaneSettings.unassignedGroup.enable)` property and the default value is `true`).

Default values in the `keys(swimlaneSettings.unassignedGroup.keys)` collection are null,undefined,empty string("").

The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    var imagePath = window.sample ? "content" : "../content";
    window.kanbanData = [{ Id: 1, Status: "Open", Summary: "Analyze the new requirements gathered from the customer.", Type: "Story", Priority: "Low", Tags: "Analyze,Customer", Estimate: 3.5, Assignee: "Andrew Fuller", ImgUrl: imagePath + "/images/kanban/2.png", RankId: 1 }, { Id: 2, Status: "InProgress", Summary: "Improve application performance", Type: "Improvement", Priority: "Normal", Tags: "Improvement", Estimate: 6, Assignee: "Andrew Fuller", ImgUrl: imagePath + "/images/kanban/2.png", RankId: 1 }, { Id: 3, Status: "Open", Summary: "Arrange a web meeting with the customer to get new requirements.", Type: "Others", Priority: "Critical", Tags: "Meeting", Estimate: 5.5, Assignee: undefined, RankId: 2 }, { Id: 4, Status: "InProgress", Summary: "Fix the issues reported in the IE browser.", Type: "Bug", Priority: "Release Breaker", Tags: "IE", Estimate: 2.5, Assignee: null, RankId: 2 }, { Id: 5, Status: "Close", Summary: "Fix the issues reported by the customer.", Type: "Bug", Priority: "Low", Tags: "Customer", Estimate: "3.5", Assignee: "", RankId: 1 }];
    $(function () {
    var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(5));
    $("#Kanban").ejKanban(
                {
                    dataSource: data,
                    columns: [
                        { headerText: "Backlog", key: "Open" },
                        { headerText: "In Progress", key: "InProgress" },
                        { headerText: "Done", key: "Close" }
                    ],
                    keyField: "Status",
                    allowTitle: true,
                    fields: {
                        content: "Summary",
                        primaryKey: "Id",
                        swimlaneKey: "Assignee",
                        imageUrl: "ImgUrl"
                    },
                    allowSelection: false
                });
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Swimlane_images/swimlane_img3.png)

## Unassigned swim lane group with user specified values

User specified swimlane key values in the `keys(swimlaneSettings.unassignedGroup.keys)` collection will be grouped under the Unassigned swimlane group when Unassigned swim lane group is enabled.(set `true` to `enable(swimlaneSettings.unassignedGroup.enable)` propertyproperty and the default value is `true`).

The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    var imagePath = window.sample ? "content" : "../content";
    window.kanbanData = [{ Id: 1, Status: "Open", Summary: "Analyze the new requirements gathered from the customer.", Type: "Story", Priority: "Low", Tags: "Analyze,Customer", Estimate: 3.5, Assignee: "Nancy Davloio", ImgUrl: imagePath + "/images/kanban/1.png", RankId: 1 }, { Id: 2, Status: "InProgress", Summary: "Improve application performance", Type: "Improvement", Priority: "Normal", Tags: "Improvement", Estimate: 6, Assignee: "Andrew Fuller", ImgUrl: imagePath + "/images/kanban/2.png", RankId: 1 }, { Id: 3, Status: "Open", Summary: "Arrange a web meeting with the customer to get new requirements.", Type: "Others", Priority: "Critical", Tags: "Meeting", Estimate: 5.5, Assignee: "", RankId: 2 }, { Id: 4, Status: "InProgress", Summary: "Fix the issues reported in the IE browser.", Type: "Bug", Priority: "Release Breaker", Tags: "IE", Estimate: 2.5, Assignee: null, RankId: 2 }, { Id: 5, Status: "Close", Summary: "Fix the issues reported by the customer.", Type: "Bug", Priority: "Low", Tags: "Customer", Estimate: "3.5", Assignee: "", RankId: 1 }];
    $(function () {
    var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(5));
            $("#Kanban").ejKanban(
                {
                    dataSource: data,
                    columns: [
                        { headerText: "Backlog", key: "Open" },
                        { headerText: "In Progress", key: "InProgress" },
                        { headerText: "Done", key: "Close" }
                    ],
                    keyField: "Status",
                    allowTitle: true,
                    fields: {
                        content: "Summary",
                        primaryKey: "Id",
                        swimlaneKey: "Assignee",
                        imageUrl: "ImgUrl"
                    },
                    swimlaneSettings: {
                        unassignedGroup: {
                            keys: ["Andrew Fuller", "", "null"]
                        }
                    },
                    allowSelection: false
                });
    });
{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Swimlane_images/swimlane_img4.png)

## Enable/Disable unassigned swim lane group

You can enable and disble the unassigned swim lane group using the property `enable(swimlaneSettings.unassignedGroup.enable)` and the default value is `true`.

The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    var imagePath = window.sample ? "content" : "../content";
    window.kanbanData = [{ Id: 1, Status: "Open", Summary: "Analyze the new requirements gathered from the customer.", Type: "Story", Priority: "Low", Tags: "Analyze,Customer", Estimate: 3.5, Assignee: "Andrew Fuller", ImgUrl: imagePath + "/images/kanban/2.png", RankId: 1 }, { Id: 2, Status: "InProgress", Summary: "Improve application performance", Type: "Improvement", Priority: "Normal", Tags: "Improvement", Estimate: 6, Assignee: "Andrew Fuller", ImgUrl: imagePath + "/images/kanban/2.png", RankId: 1 }, { Id: 3, Status: "Open", Summary: "Arrange a web meeting with the customer to get new requirements.", Type: "Others", Priority: "Critical", Tags: "Meeting", Estimate: 5.5, Assignee: null, RankId: 2 }, { Id: 4, Status: "InProgress", Summary: "Fix the issues reported in the IE browser.", Type: "Bug", Priority: "Release Breaker", Tags: "IE", Estimate: 2.5, Assignee: null, RankId: 2 }, { Id: 5, Status: "Close", Summary: "Fix the issues reported by the customer.", Type: "Bug", Priority: "Low", Tags: "Customer", Estimate: "3.5", Assignee: null, RankId: 1 }];
    $(function () {
    var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(5));
            $("#Kanban").ejKanban(
                {
                    dataSource: data,
                    columns: [
                        { headerText: "Backlog", key: "Open" },
                        { headerText: "In Progress", key: "InProgress" },
                        { headerText: "Done", key: "Close" }
                    ],
                    keyField: "Status",
                    allowTitle: true,
                    fields: {
                        content: "Summary",
                        primaryKey: "Id",
                        swimlaneKey: "Assignee",
                        imageUrl: "ImgUrl"
                    },
                    swimlaneSettings: {
                        unassignedGroup: {
                            enable: false
                        }
                    },
                    allowSelection: false
                });
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Swimlane_images/swimlane_img5.png)