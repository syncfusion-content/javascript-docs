---
layout: post
title: Syncfusion Kanban Swimlanes
description: This section explains the horizontal categorization of issues in the Syncfusion JavaScript Kanban component.
documentation: ug
platform: js
keywords: swimlanes,kanban swimlanes
api : /api/js/ejkanban
---

# Swim lanes

Swim lanes are a horizontal categorization of issues in the Kanban control which brings transparency to the workflow. This can be enabled by mapping the [swimlaneKey](https://help.syncfusion.com/api/js/ejkanban#members:fields-swimlanekey) to appropriate column name in the [`dataSource`](https://help.syncfusion.com/api/js/ejkanban#members:datasource).

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

![Swim lanes](Swimlane_images/swimlane_img1.png)

## Customized swimlane header text

You can change the swimlane row header text using the swimlane [`headers`](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-headers) property.  In this property, the text is changed using the [`text`](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-headers-text) property and the corresponding value is mapped into the [`key`](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-headers-key) property based on [`swimlaneKey`](https://help.syncfusion.com/api/js/ejkanban#members:fields-swimlanekey) datasource mapping.

Refer to the following code example.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    var kanbanData = [
        { Id: 6, Status: "Close", Summary: "Arrange a web meeting with the customer to get the login page requirements.", Type: "Others", Priority: "Low", Tags: "Meeting", Estimate: 2, Assignee: "Janet", ImgUrl: "/images/kanban/6.png", RankId: 1 },
        { Id: 7, Status: "Validate", Summary: "Validate new requirements", Type: "Improvement", Priority: "Low", Tags: "Validation", Estimate: 1.5, Assignee: "Janet", ImgUrl: "/images/kanban/7.png", RankId: 1 },
        { Id: 8, Status: "Close", Summary: "Login page validation", Type: "Story", Priority: "Release Breaker", Tags: "Validation,Fix", Estimate: 2.5, Assignee: "Andrew Fuller", ImgUrl: "/images/kanban/8.png", RankId: 2 },
        { Id: 9, Status: "Testing", Summary: "Fix the issues reported in Safari browser.", Type: "Bug", Priority: "Release Breaker", Tags: "Fix,Safari", Estimate: 1.5, Assignee: "Janet", ImgUrl: "/images/kanban/1.png", RankId: 2 },
        { Id: 10, Status: "InProgress", Summary: "Test the application in the IE browser.", Type: "Story", Priority: "Low", Tags: "Testing,IE", Estimate: 5.5, Assignee: "Andrew Fuller", ImgUrl: "/images/kanban/4.png", RankId: 3 }];
    $("#Kanban").ejKanban({
        dataSource: kanbanData,
        columns: [
            { headerText: "Backlog", key: "Open" },
            { headerText: "InProgress", key: "InProgress" },
            { headerText: "Done", key: "Close" }
        ],
        keyField: "Status",
        allowTitle: true,
        fields: {
            content: "Summary",
            primaryKey: "Id",
            swimlaneKey: "Assignee",
        },
        swimlaneSettings: {
            headers: [{ text: 'Andrew', key: 'Andrew Fuller' },
            { text: 'Janet', key: 'Janet' }]
        },
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![Customized swimlane header text](Swimlane_images/swimlane_img6.png)

## Empty swimlane row on Kanban board

You can create an empty swimlane row by enabling the [`showEmptySwimlane`](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-showemptyswimlane) property based on swimlane headers [`key`](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-headers-key) value mapping.  If no data is present, then the empty swimlane row is rendered on the Kanban board based on the specified swimlane headers [`key`](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-headers-key).

Refer to the following code.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}
 
    var kanbanData = [
        { Id: 8, Status: "Close", Summary: "Login page validation", Type: "Story", Priority: "Release Breaker", Tags: "Validation,Fix", Estimate: 2.5, Assignee: "Andrew Fuller", ImgUrl: "/images/kanban/8.png", RankId: 2 },
        { Id: 9, Status: "Testing", Summary: "Fix the issues reported in Safari browser.", Type: "Bug", Priority: "Release Breaker", Tags: "Fix,Safari", Estimate: 1.5, Assignee: "Janet", ImgUrl: "/images/kanban/1.png", RankId: 2 },
        { Id: 10, Status: "InProgress", Summary: "Test the application in the IE browser.", Type: "Story", Priority: "Low", Tags: "Testing,IE", Estimate: 5.5, Assignee: "Andrew Fuller", ImgUrl: "/images/kanban/4.png", RankId: 3 }];
    $("#Kanban").ejKanban({
        dataSource: kanbanData,
        columns: [
            { headerText: "Backlog", key: "Open" },
            { headerText: "InProgress", key: "InProgress" },
            { headerText: "Done", key: "Close" }
        ],
        keyField: "Status",
        allowTitle: true,
        fields: {
            content: "Summary",
            primaryKey: "Id",
            swimlaneKey: "Assignee",
        },
        swimlaneSettings: {
            showEmptySwimlane: true,
            headers: [{ text: 'Andrew', key: 'Andrew Fuller' },
                { text: 'Janet', key: 'Janet Leverling' }]
            },
        });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![Empty swimlane row on Kanban board](Swimlane_images/swimlane_img7.png)

## Drag And Drop between swim lanes

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

![Drag And Drop between swim lanes](Swimlane_images/swimlane_img2.png)

## Unassigned swim lane group

Unassigned swim lane feature provides option to group some common swim lane key values as separate swim lane group. You can enable and disable this behavior using the property [enable](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-unassignedgroup-enable).
User can use default common key values or user defined key values. 

    •	Using default values
    •	Using user defined values

N> By default, given common keys are grouped under the swim lane name “Unassigned”, user can customize the name using localization.

### Using default values

By default, the swim lane keys of card which is having null, undefined, empty string ("") values will be grouped as unassigned category when [enable](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-unassignedgroup-enable) property is set as true on [unassignedGroup](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-unassignedgroup).

The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    window.kanbanData = [{ Id: 1, Status: "Open", Summary: "Analyze the new requirements gathered from the customer.", Type: "Story", Priority: "Low", Tags: "Analyze, Customer", Estimate: 3.5, Assignee: "Andrew Fuller", ImgUrl: "../content/images/kanban/2.png", RankId: 1 }, { Id: 2, Status: "InProgress", Summary: "Improve application performance", Type: "Improvement", Priority: "Normal", Tags: "Improvement", Estimate: 6, Assignee: "Andrew Fuller", ImgUrl: "../content/images/kanban/2.png", RankId: 1 }, { Id: 3, Status: "Open", Summary: "Arrange a web meeting with the customer to get new requirements.", Type: "Others", Priority: "Critical", Tags: "Meeting", Estimate: 5.5, Assignee: undefined, RankId: 2 }, { Id: 4, Status: "InProgress", Summary: "Fix the issues reported in the IE browser.", Type: "Bug", Priority: "Release Breaker", Tags: "IE", Estimate: 2.5, Assignee: null, RankId: 2 }, { Id: 5, Status: "Close", Summary: "Fix the issues reported by the customer.", Type: "Bug", Priority: "Low", Tags: "Customer", Estimate: "3.5", Assignee: "", RankId: 1 }];
    
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

The output of the above code example.

![Unassigned swim lane group](Swimlane_images/swimlane_img3.png)

### Using user defined values

You can override default values for unassigned swim lane group using the property [keys](https://help.syncfusion.com/api/js/ejkanban#members:swimlanesettings-unassignedgroup-keys).
The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

 window.kanbanData = [
            { Id: 1, Status: "Open", Summary: "Analyze the new requirements gathered from the customer.", Type: "Story", Priority: "Low", Tags: "Analyze,Customer", Estimate: 3.5, Assignee: "Nancy", ImgUrl: "../content /images/kanban/1.png", RankId: 1 },
            { Id: 2, Status: "InProgress", Summary: "Improve application performance", Type: "Improvement", Priority: "Normal", Tags: "Improvement", Estimate: 6, Assignee: "Andrew", ImgUrl: "../content/images/kanban/2.png", RankId: 1 }, 
            { Id: 3, Status: "Open", Summary: "Arrange a web meeting with the customer to get new requirements.", Type: "Others", Priority: "Critical", Tags: "Meeting", Estimate: 5.5, Assignee: "", RankId: 2 }, 
            { Id: 4, Status: "InProgress", Summary: "Fix the issues reported in the IE browser.", Type: "Bug", Priority: "Release Breaker", Tags: "IE", Estimate: 2.5, Assignee: null, RankId: 2 },
            { Id: 5, Status: "Close", Summary: "Fix the issues reported by the customer.", Type: "Bug", Priority: "Low", Tags: "Customer", Estimate: "3.5", Assignee: "", RankId: 1 }];
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

The output of the above code example.
![Using user defined values](Swimlane_images/swimlane_img4.png)
