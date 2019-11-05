---
layout: post
title: Syncfusion Kanban Stacked Headers
description: This section explains how to define the stacked headers in the Syncfusion JavaScript ejKanban component.
documentation: ug
platform: js
keywords: stacked headers,kanban stacked headers
api : /api/js/ejkanban
---
# Stacked Headers

The stacked headers helps you to group the logical columns in Kanban. It can be shown by setting `showStackedHeader` as true and by defining [`stackedHeaderRows`](https://help.syncfusion.com/api/js/ejkanban#members:stackedheaderrows).

## Adding Stacked header columns

To stack columns in stacked header, you need to define [`column`](https://help.syncfusion.com/api/js/ejkanban#members:stackedheaderrows-stackedheadercolumns-column) property in [`stackedHeaderColumns`](https://help.syncfusion.com/api/js/ejkanban#members:stackedheaderrows-stackedheadercolumns) with field names of visible columns.

The following code example describes the above behavior.


{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    <script>
            $(function () {
                var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(20));

                $("#Kanban").ejKanban(
                    {
                        dataSource: data,
                        columns: [
                            { headerText: "Backlog", key: "Open" },
                            { headerText: "In Progress", key: "InProgress" },
                            { headerText: "Testing", key: "Testing" }
                        ],
                        keyField: "Status", 
                        fields: {
                        primaryKey: "Id",
                        content: "Summary",
                        },
                        stackedHeaderRows: [{
                        stackedHeaderColumns: [{
                            headerText: "Unresolved",
                            column: "Backlog,In Progress"
                        }, {
                            headerText: "Resolved",
                            column: "Testing,Done"
                        }]
                    }]

                    });
            });
        </script>


{% endhighlight %}

The following output is displayed as a result of the above code example.

![Adding Stacked header columns](Stacked_Headers_images/stacked_header_img1.png)