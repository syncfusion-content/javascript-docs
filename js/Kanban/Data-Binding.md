---
layout: post
title:  Data Binding 
description: Data Binding 
documentation: ug
platform: js
keywords: data binding ,kanban data binding
---

# Data Binding  

The Kanban control uses [`ej.DataManager`](https://help.syncfusion.com/js/datamanager/overview) which supports both RESTful JSON data services binding and local JSON array binding. The [`dataSource`](https://help.syncfusion.com/api/js/ejkanban#members:datasource) property can be assigned either with the instance of [`ej.DataManager`](https://help.syncfusion.com/js/datamanager/overview) or JSON data array collection. It supports different kinds of data binding methods such as

1.	Local data
2.	Remote data

## Local Data

To bind local data to the Kanban, you can assign a JSON array to the [`dataSource`](https://help.syncfusion.com/api/js/ejkanban#members:datasource) property.

The JSON array to the [`dataSource`](https://help.syncfusion.com/api/js/ejkanban#members:datasource) property can also be provided as an instance of the [`ej.DataManager`](https://help.syncfusion.com/js/datamanager/overview). When the JSON array is passed as an instance of [`ej.DataManager`](https://help.syncfusion.com/js/datamanager/overview), the `ej.JsonAdaptor` will be used to manipulate the Kanban data source.

The following code example describes the above behavior.


{% highlight html %}

    <div id='Kanban'></div> 

{% endhighlight %}

{% highlight javascript %}

    var kanbanData = [
        { Id: 1, Status: "Open", Summary: "Analyze the new requirements gathered from the customer.", Assignee: "Nancy Davloio" },
        { Id: 2, Status: "InProgress", Summary: "Improve application performance", Assignee: "Andrew Fuller" },
        { Id: 3, Status: "Open", Summary: "Arrange a web meeting with the customer to get new requirements.", Assignee: "Janet Leverling" },
        { Id: 4, Status: "InProgress", Summary: "Fix the issues reported in the IE browser.", Assignee: "Janet Leverling" },
        { Id: 5, Status: "Testing", Summary: "Fix the issues reported by the customer.", Assignee: "Steven walker" }
    ];

    $("#Kanban").ejKanban(
    {
        dataSource: kanbanData,
        columns: [
            { headerText: "Backlog", key: "Open" },
            { headerText: "In Progress", key: "InProgress" },
            { headerText: "Testing", key: "Testing" }
        ],
        keyField: "Status",
        fields: {
            content: "Summary"
        }
    });


{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data_Binding_images/Data_Bind_img1.png)

## Remote Data

To bind remote data to Kanban Control, you can assign a service data as an instance of [`ej.DataManager`](https://help.syncfusion.com/js/datamanager/overview) to the [`dataSource`](https://help.syncfusion.com/api/js/ejkanban#members:datasource) property.

### OData

OData is a standardized protocol for creating and consuming data. You can provide the [`OData service`](http://www.odata.org/) URL directly to the [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager) class and then you can assign it to Kanban [`dataSource`](https://help.syncfusion.com/api/js/ejkanban#members:datasource).

The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        var data = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Tasks");

        $("#Kanban").ejKanban(
        {
            dataSource: kanbanData,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" }
            ],
            keyField: "Status",
            fields: {
                content: "Summary"
            }
        });
    });


{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Data_Binding_images/Data_Bind_img2.png)


### WebAPI

Using `ej.WebApiAdaptor`, you can bind WebApi service data to Kanban. The data from WebApi service must be returned as object that has property `Items` with its value as `dataSource` and another property `Count` with its value as dataSource’s total cards count.

The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
    var dataManager = ej.DataManager({
        url: "/api/Tasks", adaptor: new ej.WebApiAdaptor()
    });

    $("#Kanban").ejKanban(
    {
        dataSource: dataManager,
        columns: [
            { headerText: "Backlog", key: "Open" },
            { headerText: "In Progress", key: "InProgress" },
            { headerText: "Testing", key: "Testing" },
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

Please refer the following link for common WebAPI creation.

http://www.asp.net/web-api/overview/getting-started-with-aspnet-web-api/tutorial-your-first-web-api


{% highlight c# %}

    using EJKanban.Models;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Linq.Expressions;
    using System.Net;
    using System.Net.Http;
    using System.Web;
    using System.Web.Http;

    namespace EJKanban.Controllers
    {

        public class TasksController: ApiController
        {

            // GET: api/Tasks
            NORTHWNDEntities db = new NORTHWNDEntities();

            public object Get()
            {
                var data = db.Tasks.Take(30).ToList();
                return new {
                    Items = data, Count = data.Count()
                };
            }
        }
    }

{% endhighlight %} 

The following output is displayed as a result of the above code example.

![](Data_Binding_images/Data_Bind_img3.png)
