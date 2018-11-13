---
layout: post
title: DataBinding with Grid widget for Syncfusion Essential JS
description: How to bind in-memory JSON and remote web services in Grid
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
--- 
# Data binding

The Grid control uses [`ej.DataManager`](https://help.syncfusion.com/js/datamanager/overview# "ej.DataManager") which supports both RESTful JSON data services binding and local JSON array binding.  The [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property can be assigned either with the instance of [`ej.DataManger`](https://help.syncfusion.com/api/js/ejdatamanager# "ej.DataManager") or JSON data array collection. It supports different kinds of data binding methods such as.

1. Local data
2. Remote data
3. HTML table

N> 1. To update the dataSource after Grid rendered, use `dataSource` method of Grid. Refer to this [link](https://help.syncfusion.com/api/js/ejgrid#members:datasource) for more information.
N> 2. DateTime values, retrieved from server-end or database, will be converted based on the local time zone. To avoid the local time zone conversion, refer this knowledge base [link](https://www.syncfusion.com/kb/8613/how-to-convert-dates-to-utc-format).

## Local Data


To bind local data to the Grid, you can assign a JSON array to the [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>

{% endhighlight %}


{% highlight javascript %}
	$(function () {

		$("#Grid").ejGrid({
		
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
			dataSource: window.gridData,
			allowPaging: true,
			columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
			});
		});



{% endhighlight %}

The JSON array to the [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property can also be provided as an instance of the [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager"). When the JSON array is passed as an instance of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager"), the `ej.JsonAdaptor` will be used to manipulate the grid datasource. 

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
	$(function () {

			$("#Grid").ejGrid({
			// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
				dataSource: ej.DataManager(window.gridData),
				allowPaging: true,
				columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
		});

	});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Bind local data to Grid.](dataBinding_images/dataBinding_img1.png)


N> 1. There is no in-built support to bind the XML data to the grid. But you can achieve this requirement with the help of [custom adaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#custom-adaptor) concept. 
N> 2. Refer this [Knowledge Base link](http://www.syncfusion.com/kb/3377/how-to-process-xml-data-from-server-using-datamanager-and-bound-to-grid#) for bounding XML data to grid using custom adaptor. 
N> 3. To update the dataSource after Grid rendered, use [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#methods:datasource) method of grid. Either JSON or DataManager can be passed to [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#methods:datasource) method.

## Remote Data

To bind remote data to Grid Control, you can assign a service data as an instance of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager") to the [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property.

### OData

OData is a standardized protocol for creating and consuming data. You can provide the [OData service](http://www.odata.org/#) URL directly to the [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager") class and then you can assign it to Grid [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "datasource").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>

{% endhighlight %}

{% highlight javascript %}
	$(function () {

		var dataManager =ej.DataManager("http://js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Orders/");
		$("#Grid").ejGrid({
			dataSource: dataManager,
			allowPaging:true,
			columns: ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
		});
		
	});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Bind remote data to Grid](dataBinding_images/dataBinding_img2.png)


#### OData Version 4

For OData Version 4 support, ej.ODataV4Adaptor should be used. By using `url` property of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager") you can bind OData Version 4 Service link and specify  `adaptor` as `ej.ODataV4Adaptor`.

I> You can provide adaptor value either as `string` value ("ODataAdaptor") or by creating a new instance (new `ej.ODataV4Adaptor`).

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
	$(function () {

		var dataManager = ej.DataManager({
			url:["http://services.odata.org/V4/Northwind/Northwind.svc/Regions/"](http://services.odata.org/V4/Northwind/Northwind.svc/Regions/#),
			adaptor: new ej.ODataV4Adaptor()
		});

		$("#Grid").ejGrid({
			dataSource: dataManager,
			allowPaging:true
		});
	});

{% endhighlight %}

{% seealso %}For further details about OData service please refer to [this link](http://www.odata.org/#). {% endseealso %}

### WebAPI

Using `ej.WebApiAdaptor`, you can bind WebApi service data to Grid. The data from WebApi service must be returned as object that has property `Items` with its value as datasource and another property `Count` with its value as dataSource's total records count.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>

{% endhighlight %}

{% highlight javascript %}
	$(function () {
		var dataManager = ej.DataManager({
			url:"/api/Orders",
			adaptor: new ej.WebApiAdaptor()
		});

		$("#Grid").ejGrid({
			dataSource: dataManager,
			allowPaging:true,
			columns: ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
		});
	});

{% endhighlight %}

{% highlight cs %}
using EJGrid.Models;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Linq.Expressions;
using System.Net;
using System.Net.Http;
using System.Web;
using System.Web.Http;

namespace EJGrid.Controllers
{

	public class OrdersController: ApiController
	{

		// GET: api/Orders
		NORTHWNDEntities db = new NORTHWNDEntities();

		public object Get()
		{
			var queryString = HttpContext.Current.Request.QueryString;
			int skip = Convert.ToInt32(queryString["$skip"]);
			int take = Convert.ToInt32(queryString["$top"]);
			var data = db.Orders.Skip(skip).Take(take).ToList();
			return new {
				Items = data.Skip(skip).Take(take), Count = data.Count()
			};
		}
	}
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Bind data from WEBAPI service](dataBinding_images/dataBinding_img3.png)


### Other RESTful web services

The [Custom Adaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#custom-adaptor "CustomAdaptor") concept of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager") allows to customize or generate your own adaptor which is used to process the `query` and `result` data. 

When using remote data binding, the adaptor of the [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager") plays vital role in processing queries to make them suitable to sends along with the data request and also in processing the response data from the server.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>

{% endhighlight %}

{% highlight javascript %}
$(function() {

	var customAdaptor = new ej.Adaptor().extend({
		insert: function(dataManager, data) {
			//Auto-increment `id` field value on insert
			data["id"] = dataManager.dataSource.json[dataManager.dataSource.json.length - parseInt(1, 10)].id + 1;
			return dataManager.dataSource.json.push(data);
		},
		processQuery: ej.JsonAdaptor.prototype.processQuery //Reusing JsonAdaptor`s processQuery
	});

	window.gridData = [
	{
		id: 1,
		firstName: "John",
		lastName: "Beckett",
		email: "john@syncfusion.com"
	},
	{
		id: 2,
		firstName: "Ben",
		lastName: "Beckett",
		email: "ben@syncfusion.com"
	},
	{
		id: 3,
		firstName: "Andrew",
		lastName: "Beckett",
		email: "andrew@syncfusion.com"
	}];

	var dataManager = new ej.DataManager(window.gridData);
	// assigning custom adaptor to datamanager
	dataManager.adaptor = new customAdaptor();

	// insert from custom adaptor usage
	dataManager.insert({
		firstName: "Joel",
		lastName: "Beckett",
		email: "joel@syncfusion.com"
	});

	$("#Grid").ejGrid({
		dataSource: dataManager,
		columns: ["firstName", "lastName", "email"]
	});
});

{% endhighlight %}

The following output is displayed as a result of the above code example.

![Bind data from other restful service](dataBinding_images/dataBinding_img4.png)


### Load At Once

On remote data binding, by default all the Grid actions will be processed on server-side such as paging, sorting, editing, grouping and filtering etc. To avoid post back to server on every action, you can set the grid to load all the data on initialization time and make the actions client-side. To enable this, you can use `offline` property of the [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function() {

	var dataManager = ej.DataManager({
		url: "http://js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Orders/",
		adaptor: new ej.ODataAdaptor(),
		offline: true
	});

	$("#Grid").ejGrid({
		dataSource: dataManager,
		allowPaging: true,
		columns: ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
	});

});

{% endhighlight %}

Please refer to this [link](https://help.syncfusion.com/js/datamanager/adavancedfunctionalities#offline-support "offline") for further reference on `offline` property

The following output is displayed as a result of the above code example.

![load data at once fro service](dataBinding_images/dataBinding_img5.png)


### Data Caching

Date caching will help you prevent the request to server for already visited pages in Grid using the `enableCaching` property of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager"). Also using `cachingPageSize` and `timeTillExpiration` properties of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager"), you can control the number of pages to be cached and duration it should be cached respectively.

N> The cached data will be stored in browser's HTML5 `localStorage`. 

The following code example describes the above behavior.

{% highlight html %}
<div id="CacheGrid"></div>

{% endhighlight %}

{% highlight javascript %}

$(function() {

	var dataManger = ej.DataManager({
		url: "http://js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Orders/",
		enableCaching: true,
		cachingPageSize: 10,
		timeTillExpiration: 120000
	});

	$("#CacheGrid").ejGrid({
		dataSource: dataManger,
		allowPaging: true,
		columns: ["OrderID", "CustomerID", "EmployeeID", "Freight", "ShipCity"]
	});

});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Bind data with data caching](dataBinding_images/dataBinding_img6.png)


### Custom request parameters and HTTP Header


#### Adding request parameters

You can use the [`addParams`](https://help.syncfusion.com/api/js/ejquery#methods:addparams "addparams") method of [`ej.Query`](https://help.syncfusion.com/api/js/ejquery# "ejquery") class, to add custom parameter to the data request. The Grid has [`query`](https://help.syncfusion.com/api/js/ejgrid#members:query "query") property, which accepts instance of [`ej.Query`](https://help.syncfusion.com/api/js/ejquery# "ejQuery").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function() {
	$("#Grid").ejGrid({
		dataSource: ej.DataManager({
			url: "http://js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Orders/"
		}),
		allowPaging: true,
		query: new ej.Query().addParams("Syncfusion", true),
		columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
	});
});

{% endhighlight %}

The custom parameter will be passed along with the data request of the grid as follows.

![send custom parameter along with request](dataBinding_images/dataBinding_img7.png)

#### Adding custom header to server using datamanager

You can pass any values in the Headers of ejDataManager and retrieve them at the server-side using the Request object of the HttpRequestMessage. This can be added to the headers either in the [`load`](https://help.syncfusion.com/api/js/ejgrid#events:load "load") event of ejGrid or while performing any server-side operations like editing/adding and retrieve them at the server-side as follows.

{% highlight html %}
 <div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function() {
$("#Grid").ejGrid({
        dataSource: ej.DataManager({ url: "/Home/DataSource", adaptor: new ej.UrlAdaptor() }),
        allowScrolling: true,
        allowFiltering: true,
        allowPaging: true,
        load: function(args){
            this.model.dataSource.dataSource.headers = [];//So define them as array
            this.model.dataSource.dataSource.headers.push({ "field": "OrderID"});//pushing Some JSON Object
            this.model.dataSource.dataSource.headers.push({ "IsValid": true });//pushing Some JSON Object
  
        },
        columns: [
  
                { field: "OrderID" },
                { field: "ShipCountry" },
                { field: "CustomerID" },
                { field: "EmployeeID" },
                { field: "ShipCity" }
        ]
    });
});

{% endhighlight %}

The custom header will be passed along with the data request of the grid as follows.

![send custom header along with request using dataManager](dataBinding_images/dataBinding_img11.png)

#### Handling HTTP Errors

During server interaction from the Grid, there may occur some server-side exceptions and you can acquire those error messages or exception details in client-side using the [`actionFailure`](https://help.syncfusion.com/api/js/ejgrid#events:actionfailure "actionFailure") event of Grid Control.

The argument passed to the [`actionFailure`](https://help.syncfusion.com/api/js/ejgrid#events:actionfailure "actionFailure") Grid event contains the Error details returned from server. Please refer to the following table for some error details that would be acquired in client-side event arguments.

 <table>
        <tr>
            <th>
                Parameter
            </th>
            <th>
                Description
            </th>
        </tr>
        <tr>
            <td>
                argument.error.status
            </td>
            <td>
                It returns the response error code.
            </td>
        </tr>
        <tr>
            <td>
                argument.error.statusText
            </td>
            <td>
                It returns the error message.
            </td>
        </tr>
    </table>


The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight javascript %}
$(function() {
	var dataManger = ej.DataManager({
		url: "http://js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Orders/",
		adaptor: "ODataAdaptor"
	});

	$("#Grid").ejGrid({
		dataSource: dataManger,
		allowPaging: true,
		columns: ["OrderID", "CustomerID", "EmployeeID", "Freight", "ShipCity"],
		actionFailure: function(args) {
			alert(args.error.status + " : " + args.error.statusText);
		}
	});
});

{% endhighlight %}

The following output is displayed as a result of the above code example.

![how to handle the HTTP error](dataBinding_images/dataBinding_img8.png)


## HTML Table 

A HTML Table element can also be used as the datasource of Grid. To use HTML Table as datasource, the table element should be passed to [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource "dataSource") property of Grid as an instance of the [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager# "DataManager").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight html %}
<table id="Table1">
   <thead>
      <tr>
         <th>Laptop</th>
         <th>Model</th>
         <th>Price</th>
         <th>OS</th>
         <th>RAM</th>
         <th>ScreenSize</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>Dell Vostro</td>
         <td>2520</td>
         <td>39990</td>
         <td>Windows 8</td>
         <td>4GB</td>
         <td>15.6</td>
      </tr>
      <tr>
         <td>HP Pavilion Sleekbook</td>
         <td>14-B104AU</td>
         <td>22800</td>
         <td>Windows 8</td>
         <td>2GB</td>
         <td>14</td>
      </tr>
      <tr>
         <td>Sony Vaio</td>
         <td>E14A15</td>
         <td>42500</td>
         <td>Windows 7 Home Premium</td>
         <td>4GB DDR3 RAM</td>
         <td>14</td>
      </tr>
      <tr>
         <td>Lenovo</td>
         <td>Yoga 13</td>
         <td>57000</td>
         <td>Windows 8 RT</td>
         <td>2GB DDR3 RAM</td>
         <td>11.6</td>
      </tr>
      <tr>
         <td>Toshiba</td>
         <td>L850-Y3110</td>
         <td>57700</td>
         <td>Windows 8 SL</td>
         <td>8GB DDR3 RAM</td>
         <td>15.6</td>
      </tr>
   </tbody>
</table>

{% endhighlight %}

{% highlight javascript %}
$(function() {
	$("#Grid").ejGrid({
		dataSource: ej.DataManager($("#Table1")),
		columns: ["Laptop", "Model", "Price", "RAM", "ScreenSize"]
	});
});

{% endhighlight %}

The following output is displayed as a result of the above code example.

![Bind HTML data to grid](dataBinding_images/dataBinding_img9.png)


I> The HTML Table element is the only valid element when using HTML Table binding. Using other elements will throws an exception.


#### Miscellaneous

To update/refresh the Grid datasource and collect the details related to the current view data of the Grid from external actions, Grid provides following methods. 


1. [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#methods:datasource "dataSource")
2. [`getCurrentViewData`](https://help.syncfusion.com/api/js/ejgrid#methods:getcurrentviewdata "getCurrentViewData")
3. [`refreshContent`](https://help.syncfusion.com/api/js/ejgrid#methods:refreshcontent "refreshContent")

{% highlight html %}

	<label>Refresh Template</label><input id="check" type="checkbox">
	
	<label>Methods</label><select id="columnName" class="e-ddl" data-bind="value: field">
		<option value="dataSource" selected="selected">dataSource</option>
		<option value="getCurrentViewData">getCurrentViewData</option>
		<option value="refreshContent">refreshContent</option>
	</select>
	<label>Current View Data</label> <textarea id="cols"></textarea>
    <div id="Grid"></div>

{% endhighlight %}

{% highlight javascript %}
		$("#columnName").ejDropDownList({
			watermarkText: "Select Methods",
			width: "100%",
			change: function(args){
				if(args.selectedText == "dataSource") $("#Grid").ejGrid("dataSource", window.gridData.slice(0,5));
				else if(args.selectedText == "refreshContent") { 
					var obj = $("#Grid").ejGrid("instance")
					obj.model.columns.splice(3,1)
					//if the argument is set to true, it will refresh all the templates
					obj.refreshContent($("#check").is(":checked"));
				}
				else $("#cols").val(JSON.stringify($("#Grid").ejGrid("getCurrentViewData")));
			}
		});
        $(function () {
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                allowPaging:true,
				columns: [
					 { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right },
					 { field: "CustomerID", headerText: "Customer ID"},
					 { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, format: "{0:C}" },
					 { field: "ShipCity", headerText: "Ship City" },
					 { field: "ShipName", headerText: "Ship Name" }
                ]
            });
		  });
{% endhighlight %}

N> If the argument is set to true in the refreshContent([argument]]), it will refresh the Grid content along with the template else only grid content is refreshed. To refresh the template alone,  [`refreshTemplate`](https://help.syncfusion.com/api/js/ejgrid#methods:refreshtemplate "refreshTemplate") can be used.

The following output is displayed as a result of the above code example.

![update the Grid dataSource upon dropdownlist selection](dataBinding_images/dataBinding_img10.png)