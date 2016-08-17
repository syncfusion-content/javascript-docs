---
layout: post
title:  Cards
description: Cards
documentation: ug
platform: js
keywords: cards,kanban cards
---

# Cards

## Customization

Cards can be customized with appropriate mapping fields from the database. The customizable mapping properties are listed as follows 

<table>
<tr>
<th>
Mapping Fields</th><th>
Description</th></tr>
<tr>
<td>
[`content`](https://help.syncfusion.com/js/api/ejkanban#members:fields-content)</td><td> Map the column name to use as content to cards.</td></tr>
<tr>
<td>
[`tag`](https://help.syncfusion.com/js/api/ejkanban#members:fields-tag) </td><td>
Map the column name to use as tag. Multiple tags can be given with comma separated.  Eg. “API”,”Sql,Database”.</td></tr>
<tr>
<td>
[`color`](https://help.syncfusion.com/js/api/ejkanban#members:fields-color) </td><td>
 Map the column name to use as colors to highlight cards left border.</td></tr>
<tr>
<td>
[`colorMapping`](https://help.syncfusion.com/js/api/ejkanban#members:cardsettings.colormapping)</td><td>
Map the colors to use with column values which is mapped with `fields.color`.</td></tr>
<tr>
<td>
[`imageUrl`](https://help.syncfusion.com/js/api/ejkanban#members:fields-imgurl)</td><td>
Map the column name to use as image to cards.</td></tr>
<tr>
<td>
[`primaryKey`](https://help.syncfusion.com/js/api/ejkanban#members:fields-primarykey)</td><td>
Map the column name to use as primary key to cards.</td></tr>
<tr>
<td>
[`priorityKey`](https://help.syncfusion.com/js/api/ejkanban#members:fields-prioritykey)</td><td>
Map the column name to use as priority key to cards.</td></tr>
<tr>
<td>
[`title`](https://help.syncfusion.com/js/api/ejkanban#members:fields-title)</td><td>
Map the column name to use as title to cards. Default title is  `primaryKey`.</td></tr>
<tr>
<td>
[`allowTitle`](https://help.syncfusion.com/js/api/ejkanban#members:allowtitle)</td><td>
Set as true to enable title for card.</td></tr>
</table>

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
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                allowTitle:true,
                fields: {
                    content: "Summary",
                    primaryKey: "Id",
                    priorityKey: "RankId",
                    tag: "Tags",
                    color: "Type",
                    imageUrl: "ImgUrl"
                },
                cardSettings: {
                    colorMapping: {
                        "#cb2027": "Bug,Story",
                        "#67ab47": "Improvement",
                        "#fbae19": "Epic",
                        "#6a5da8": "Others"
                    }
                }
            });
    });


{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cards_images/cards_img1.png)

## Template

Templates are used to create custom card layout as per the user convenient. Html templates can be specified in the [`template`](https://help.syncfusion.com/js/api/ejkanban#members:cardSettings-template) property of the [`cardSettings`](https://help.syncfusion.com/js/api/ejkanban#members:cardsettings) as an ID of the template’s HTML element.

You can use JsRender syntax in the template. For more information about JsRender syntax, please refer this [`link`](https://www.jsviews.com/).

The following code example describes the above behavior.


{% highlight html %}

    <div id='Kanban'></div>
    <script id="cardtemplate" type="text/x-jsrender">        
            <table>
            <tr>
                <td class="photo">
                    <img src="{{:Priority}}.png">
                </td>            
                <td class="details">
                    <table>
                        <colgroup>
                            <col width="30%">
                            <col width="70%">
                        </colgroup>
                        <tbody>
                            <tr>
                                <td class="CardHeader">   Name: </td>
                                <td>{{:Assignee}}</td>
                            </tr>
                            <tr>
                                <td class="CardHeader">   Task: </td>
                                <td>{{:Type}}</td>
                            </tr>
                        </tbody>
                    </table>
                </td>
            </tr>
            </table> 
        </script>
            
{% endhighlight %}

{% highlight javascript %}

    $(function () {
        var data = new ej.DataManager(window.kanbanData).executeLocal(new ej.Query().take(20));
    
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open"},
                { headerText: "In Progress", key: "InProgress"},
                { headerText: "Done", key: "Close"}
            ],
            keyField: "Status",
        fields: {
            primaryKey: "Id",
            color: "Type",
        },
            cardSettings: {
                template: "#cardtemplate",                    
                colorMapping: {
                    "#cb2027": "Bug,Story",
                    "#67ab47": "Improvement",
                    "#fbae19": "Epic",
                    "#6a5da8": "Others"
                }
            }
        });
    });

{% endhighlight %}

{% highlight css %}

    <!--CSS for card template-->
        <style>
            .e-templatetable {
                width: 100%;
            }

            .details > table {
                margin-left: 2px;
                border-collapse: separate;
                border-spacing: 2px;
                width: 100%;
            }

            .details td {
                vertical-align: top;
            }

            .details {
                padding: 8px 8px 10px 0;
            }

            .photo {
                padding: 8px 6px 10px 6px;
                text-align: center;
            }

            .CardHeader {
                font-weight: bolder;
                padding-right: 10px;
            }
        </style>

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](Cards_images/cards_img2.png)

## Tooltip

You can enable HTML tooltip for Kanban card elements by setting [`enable`](https://help.syncfusion.com/js/api/ejkanban#members:tooltipsettings-enable) property as true in [`tooltipSettings`](https://help.syncfusion.com/js/api/ejkanban#members:tooltipsettings).

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
                tooltipSettings: {
                    enable: true
                },
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
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

![](Cards_images/cards_img3.png)

### Template

By making use of template feature with tooltip, all the field names that are mapped from the `dataSource` can be accessed to define the [`template`](https://help.syncfusion.com/js/api/ejkanban#members:tooltipsettings-template) tooltip for card. The [`tooltipSettings.enable`](https://help.syncfusion.com/js/api/ejschedule#members:tooltipsettings.enable) must be enabled first.

The following code example describes the tooltip template.

{% highlight html %}

    <div id='Kanban'></div>
    <script id="tooltipTemp" type="text/x-jsrender">
            <div class='e-kanbantooltiptemplate'>
                <table>
                    <tr>
                        <td class="photo">
                            <img src="{{:ImgUrl}}">
                        </td>
                        <td class="details">
                            <table>
                                <colgroup>
                                    <col width="30%">
                                    <col width="70%">
                                </colgroup>
                                <tbody>
                                    <tr>
                                        <td class="CardHeader">Assignee:</td>
                                        <td>{{:Assignee}}</td>
                                    </tr>
                                    <tr>
                                        <td class="CardHeader">Type:</td>
                                        <td>{{:Type}}</td>
                                    </tr>                                
                                    <tr>
                                        <td class="CardHeader">Estimate:</td>
                                        <td>{{:Estimate}}</td>
                                    </tr>                                
                                    <tr>
                                        <td class="CardHeader">Summary:</td>
                                        <td>{{:Summary}}</td>
                                    </tr>
                                </tbody>
                            </table>
                        </td>
                    </tr>
                </table>
            </div>
    </script>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
    var data = ej.DataManager(window.kanbanData).executeLocal(ej.Query().take(20));
    
    $("#Kanban").ejKanban(
        {
            dataSource: data,
            tooltipSettings: {
                enable: true,
                template: "#tooltipTemp"
            },
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Done", key: "Close" }
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

{% highlight css %}

    <!--toolTip template releated css -->
    <style> 
        .details >table {
            width: 100%;
            margin-left:2px;           
            border-collapse: separate;
            border-spacing: 1px;
        }
        .e-kanbantooltiptemplate {
            width: 250px;
            padding: 3px;
        }
        .e-kanbantooltiptemplate > table {
            width: 100%;
        }
        .e-kanbantooltiptemplate td {
            vertical-align: top;
        }
        td.details {
            padding-left: 10px;
        }
        .CardHeader {
            font-weight: bolder;
        }
    </style>

{% endhighlight %}

 
The following output is displayed as a result of the above code example.

![](Cards_images/cards_img4.png)