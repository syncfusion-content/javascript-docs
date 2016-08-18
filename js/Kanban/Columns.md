---
layout: post
title:  Columns
description: Columns
documentation: ug
platform: js
keywords: columns,kanban columns
---

# Columns 

Column fields are present in the [`dataSource`](https://help.syncfusion.com/js/api/ejkanban#members:datasource) schema and it is rendering cards based its mapping column values.

## Key Mapping

To render Kanban with simple cards, you need to map the `dataSource` fields to Kanban cards and [`columns`](https://help.syncfusion.com/js/api/ejkanban#members:columns). The required mapping field are listed as follows

<table>
<tr>
<th>
Mapping Fields</th><th>
Description</th></tr>
<tr>
<td>
{{ '[keyField](https://help.syncfusion.com/js/api/ejkanban#members:keyField)' | markdownify }} </td><td>
Map the column name to use as {{ '[key](https://help.syncfusion.com/js/api/ejkanban#members:columns-key)'| markdownify }} values to columns.</td></tr>
<tr>
<td>
{{ '[columns.key](https://help.syncfusion.com/js/api/ejkanban#members:columns-key)' | markdownify }} </td><td>
Map the corresponding `key` values of `keyField` column to each columns.</td></tr>
<tr>
<td>
{{ '[columns.headerText](https://help.syncfusion.com/js/api/ejkanban#members:columns-headertext)' | markdownify }} </td><td>
 It represents the title for particular column</td></tr>
<tr>
<td>
{{ '[fields.content](https://help.syncfusion.com/js/api/ejkanban#members:fields-content)' | markdownify }} </td><td>
Map the column name to use as content to cards.</td></tr>
</table>

N> 1. If the column with `keyField` is not in the dataSource and `key` values specified will not available in column values, then the cards will not be rendered.
N> 2. If the `fields.content` is not in the dataSource, then empty cards will be rendered.

The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(30));
    
        $("#Kanban").ejKanban({    
            dataSource: data,
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

![](Columns_images/column_img.png)


## Headers

### Header Template

The template design that applies on for the column header. To render template, set [`headerTemplate`](https://help.syncfusion.com/js/api/ejkanban#members:columns-headertemplate) property of the [`columns`](https://help.syncfusion.com/js/api/ejkanban#members:columns).

You can use JsRender syntax in the template. For more information about JsRender syntax, please refer the [`link`](https://www.jsviews.com/).

The following code example describes the above behavior.

{% highlight html %}

        <!—Column Template -->
        <script id="column1" type="text/x-jsrender">
            <span class="e-backlog e-icon"></span> Backlog
        </script>
        <div id="column4">
            <span class="e-done e-icon"></span> Done
        </div>
    <div id='Kanban'></div> 

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(30));
    
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                { headerText: "Backlog", key: "Open", headerTemplate: "#column1" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close", headerTemplate: "#column4" }    
            ],
                keyField: "Status",
                fields: {
                    content: "Summary"
                }
            });
    });

{% endhighlight %}

{% highlight css %}

    /*CSS for Header template icon*/
    .e-backlog,.e-done {
        font-size: 16px;
        padding-right: 5px;
        display: inline-block;
        }    
    .e-backlog:before {
        content: "\e807";
        }    
    .e-done:before {
        content: "\e80a";
        }

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Columns_images/column_img1.png)

## Width

You can specify the width for particular column by setting [`width`](https://help.syncfusion.com/js/api/ejkanban#members:columns-width) property of [`columns`](https://help.syncfusion.com/js/api/ejkanban#members:columns) as in pixel (ex: 100) or in percentage (ex: 40%).

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
                    { headerText: "Backlog", key: "Open", width: "5%" },
                    { headerText: "In Progress", key: "InProgress", width: "12%" },
                    { headerText: "Testing", key: "Testing", width: 100 },
                    { headerText: "Done", key: "Close", width: 100 }
                ],
                keyField: "Status",
                fields: {
                    content: "Summary"
                }
            });
    });


{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Columns_images/column_img2.png)

## Visibility 

You can hide particular column in Kanban by setting [`visible`](https://help.syncfusion.com/js/api/ejkanban#members:columns-visible) property of it as false.

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
                    { headerText: "Testing", key: "Testing", visible: false },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    content: "Summary"
                }
            });
    });


{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Columns_images/column_img3.png)

## Toggle 

You can set particular column collapsed state in Kanban by setting [`isCollapsed`](https://help.syncfusion.com/js/api/ejkanban#members:columns-iscollapsed) property of it as true. You need to set [`allowToggleColumn`](https://help.syncfusion.com/js/api/ejkanban#members:allowtogglecolumn) as true to use “Expand/Collapse” Column.

The following code example describes the above behavior.

{% highlight html %}

    <div id='Kanban'></div>

{% endhighlight %}

{% highlight javascript %}

    $(function() {
        var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(30));
        
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                allowToggleColumn:true,
                columns: [
                    { headerText: "Backlog", key: "Open",isCollapsed:true },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],                                                           			
                keyField: "Status",
                fields: {
                content: "Summary",
                primaryKey: "Id"
            },
            });
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Columns_images/column_img4.png)
