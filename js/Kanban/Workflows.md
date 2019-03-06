---
layout: post
title: Syncfusion Kanban Workflows
description: This section explains the flow of cards between the Kanban columns in the Syncfusion JavaScript Kanban component.
documentation: ug
platform: js
keywords: Workflows,kanban Workflows
api : /api/js/ejkanban
---

# Workflows 

Workflows can be defined to set the flow of card moving between the Kanban column statuses and it is applicable to drag and drop and context menu features.

You can set [`workflows`](https://help.syncfusion.com/api/js/ejkanban#members:workflows) as array of Objects which consists of [`key`](https://help.syncfusion.com/api/js/ejkanban#members:workflows-key) and [`allowedTransitions`](https://help.syncfusion.com/api/js/ejkanban#members:workflows-allowedtransitions) properties. The `allowedTransitions` accepts more than one transition of the specific column key mentioned in `key` property.

If a card is to be dragged to not allowed transition columns , then not supported warning symbol will be displayed for denoting the error.
        
The following code example describes the above Workflow functionality.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(30));
    
        $("#Kanban").ejKanban({    
            dataSource: data,
            workflows:[                
				     { key:"Open",allowedTransitions:"InProgress"},
                     { key:"InProgress",allowedTransitions:"Testing,Close"}
				   ],
            columns: [
                { headerText: "Backlog", key: "Open"},
                { headerText: "In Progress", key: "InProgress"},
                { headerText: "Testing", key: "Testing"},
                { headerText: "Done", key: "Close"}    
            ],        
            keyField: "Status",
            fields: {
                content: "Summary"
            }
        });
    }); 

{% endhighlight %}

The following output is displayed as a result of the above code example.

![Workflows](WorkFlows_images/workflows1.png)