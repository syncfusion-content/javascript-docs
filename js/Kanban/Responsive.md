---
layout: post
title:  Responsive
description: Responsive
documentation: ug
platform: js
keywords: responsive,kanban responsive
---

# Responsive

The Kanban control has support for responsive behavior based on client browser’s width and height. To enable responsive, [`isResponsive`](https://help.syncfusion.com/js/api/ejkanban#members:isresponsive) property should be true. 

## Width

By default, the Kanban is adaptable to its parent container. It can adjust its width of columns based on parent container width. You can also assign width of [`columns`](https://help.syncfusion.com/js/api/ejkanban#members:columns) in percentage. 

The following code example describes the above behavior.


{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    $(function() {
        var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(20));
        
    $("#Kanban").ejKanban(
        {
            dataSource: data,
            isResponsive: true,
            columns: [
                { headerText: "Backlog", key: "Open",width:"10%" },
                { headerText: "In Progress", key: "InProgress", width: "10%" },
                { headerText: "Done", key: "Close", width: "10%" }
            ],
            keyField: "Status",
            fields: {
            primaryKey: "Id",
            content: "Summary",
            tag: "Tags"
        }           
        });
    });


{% endhighlight %}

N> `allowScrolling` should be false while defining width in percentage.

## Min Width

Min Width is used to maintain minimum width for the Kanban. If the Kanban width is less than [`minWidth`](https://help.syncfusion.com/js/api/ejkanban#members:minwidth) then the scrollbar will be displayed to maintain minimum width.

The following code example describes the above behavior.


{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(20));
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            minWidth: 700,
            isResponsive: true,
            columns: [
                { headerText: "Backlog", key: "Open", width: 120 },
                { headerText: "In Progress", key: "InProgress", width: 110 },
                { headerText: "Done", key: "Close", width: 110 }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
                tag: "Tags"
            }        
        });
    });


{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Responsive_images/responsive_img1.png)
