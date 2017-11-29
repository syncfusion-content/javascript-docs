---
layout: post
title: Server Filtering in the DropDownList widget for Syncfusion Essential JS
description: Description about server filtering in the DropDownList widget for Syncfusion Essential JS
platform: js
control: DropDownList
documentation: ug
keywords: DropDownList, dropdown, Selection, Grouping, Sorting
api: /api/js/ejdropdownlist
---
# Server Filtering

Server filtering for displaying only a fixed amount of dataset from the whole dataset. In general, DropDownList displays just the data returned from the server. This feature is convenient for you to apply when the user does not want to see the whole dataset in the popup wrapper.
enableServerFiltering If set to true, the filtering operations performed in the remote service and returns the result.

{% highlight html %}

    <div class="control">
        <div class="ctrllabel">Select a Company Name</div>
        <input type="text" id="CompanyNames" />
    </div>
    <script type="text/javascript">
	
        var companyList = ej.DataManager({url:"http://js.syncfusion.com/ejServices/Wcf/Northwind.svc/Customers", crossDomain: true});
		
        var controlProperty = 
        {
            dataSource: companyList , 
            fields : { text: "ContactName", value: 'ContactName'  }, 
            itemsCount : 10 , 
            popupHeight: "200px",
            width: "250px",
            enableFilterSearch: true,
            enableServerFiltering: true
        };
	
        $(function () 
		{
			$('#CompanyNames').ejDropDownList(controlProperty);
			 
		});

    </script>

{% endhighlight %}

![](ServerFiltering_images/ServerFiltering_image2.png)

This sample raises the query on Customer service. Returns ContactName records for customers with ContactName containing the string “d”.

![](ServerFiltering_images/ServerFiltering_image1.png)

