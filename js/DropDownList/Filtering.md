---
layout: post
title: Searching in the DropDownList widget for Syncfusion Essential JS
description: Description about searching in the DropDownList widget for Syncfusion Essential JS
platform: js
control: DropDownList
documentation: ug
keywords: DropDownList, dropdown, Search, Incremental Search, Filter Search, Server Filtering
api: /api/js/ejdropdownlist
---

# Search

Items are searched based on the keyed in values to the textbox. There are two types of searches,

* Incremental Search
* Filter Search

## Incremental Search

Selects the item in the popup list based on the keyed in value. If the time taken to type exceeds 1000 milliseconds then filtered items will be reset based on the current input value.For this search, [enableIncrementalSearch](https://help.syncfusion.com/api/js/ejdropdownlist#members:enableincrementalsearch) property must be enabled. By default this mode of search is enabled. Incremental search can be case sensitive or case insensitive. To make case sensitive, you can use [caseSensitiveSearch](https://help.syncfusion.com/api/js/ejdropdownlist#members:casesensitivesearch) property.

{% highlight html %}

    <input type="text" id="dropdown1" />
                
{% endhighlight %}

{% highlight javascript %}

     $(function() {
        var items = [{
            text: "Adams",
            value: "emp1"
        }, {
            text: "James",
            value: "emp2"
        }, {
            text: "Maria",
            value: "emp3"
        }, {
            text: "Jessica",
            value: "emp4"
        }, {
            text: "Jenneth",
            value: "emp5"
        }];
        $('#dropdown1').ejDropDownList({
            dataSource: items,
            fields: {
                text: "text",
                value: "value"
            },
            enableIncrementalSearch: true,
            caseSensitiveSearch: true
        });
    });
	
{% endhighlight %}

![](Functionalities_images/Functionalities_img8.jpeg)

## Filter search

You can quickly locate specific item within a large data source by filtering matches with a search box. A text box appears in the popup list for searching when [enableFilterSearch](https://help.syncfusion.com/api/js/ejdropdownlist#members:enablefiltersearch) property is enabled. By default, filtering returns the matched items list based on text in search textbox. 
You can configure the search filter by using [filterType](https://help.syncfusion.com/api/js/ejdropdownlist#members:filtertype) property. There is two types of filter options,

* Starts With 
* Contains

N> Items are filtered based on “contains” filter type by default.

{% highlight html %}

    <input type="text" id="dropdown1" />
                
{% endhighlight %}

{% highlight javascript %}

    $(function() {
        var items = [{
            text: "Adams",
            value: "emp1"
        }, {
            text: "James",
            value: "emp2"
        }, {
            text: "Maria",
            value: "emp3"
        }, {
            text: "Jessica",
            value: "emp4"
        }, {
            text: "Jenneth",
            value: "emp5"
        }];
        $('#dropdown1').ejDropDownList({
            dataSource: items,
            fields: {
                text: "text",
                value: "value"
            },
            enableFilterSearch: true,
            filterType: "startsWith"
        });
    });
    
{% endhighlight %}

![](Functionalities_images/Functionalities_img9.jpeg)

## Server Filtering

Server filtering for displaying only a fixed amount of dataset from the whole dataset. In general, DropDownList displays just the data returned from the server. This feature is convenient for you to apply when the user does not want to see the whole dataset in the popup wrapper.
[enableServerFiltering](https://help.syncfusion.com/api/js/ejdropdownlist#members:enableServerFiltering) If set to true, the filtering operations performed in the remote service and returns the result.

{% highlight html %}

    <div class="control">
        <div class="ctrllabel">Select a Customer Name</div>
        <input type="text" id="customerList" />
    </div>
    <script type="text/javascript">
	
        var customerList = ej.DataManager({url:"http://js.syncfusion.com/ejServices/Wcf/Northwind.svc/Customers", crossDomain: true});
		
        var controlProperty = 
        {
            dataSource: customerList , 
            fields : { text: "ContactName", value: 'ContactName'  }, 
            itemsCount : 10 , 
            popupHeight: "200px",
            width: "250px",
            enableFilterSearch: true,
            enableServerFiltering: true
        };
	
        $(function () 
		{
			$('#customerList').ejDropDownList(controlProperty);
			 
		});

    </script>

{% endhighlight %}

![](ServerFiltering_images/ServerFiltering_image2.png)

This sample raises the query on Customer service. Returns ContactName records for customers with ContactName containing the string “d”.

![](ServerFiltering_images/ServerFiltering_image1.png)

