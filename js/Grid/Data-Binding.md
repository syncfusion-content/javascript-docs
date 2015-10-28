---
layout: post
title: DataBinding
description: data binding
platform: js
control: Grid
documentation: ug
--- 

# Data binding

Grid uses [`ej.DataManager`](http://helpjs.syncfusion.com/js/datamanager/overview# "ej.DataManager") which supports both RESTful JSON data services binding and local JSON array binding.  The [`dataSource`](http://help.syncfusion.com/js/api/ejgrid#members:datasource "dataSource") property can be assigned either with the instance of [`ej.DataManger`](http://help.syncfusion.com/js/api/ejdatamanager# "ej.DataManager") or JSON data array collection. It supports different kinds of databinding methods such as

1. Local data
2. Remote data
3. HTML table
## Local Data


To bind local data to the grid, you can assign a JSON array to the [`dataSource`](http://help.syncfusion.com/js/api/ejgrid#members:datasource "") property.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight js %}
	$(function () {

		$("#Grid").ejGrid({
		
		// the datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
			dataSource: window.gridData,
			allowPaging: true,
			columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]
			});
		});



{% endhighlight %}

The JSON array to the [`dataSource`](http://help.syncfusion.com/js/api/ejgrid#members:datasource "") property can also be provided as an instance of the [`ej.DataManager`](http://help.syncfusion.com/js/api/ejdatamanager# ""). When the JSON array is passed as an instance of [`ej.DataManager`](http://help.syncfusion.com/js/api/ejdatamanager# ""), the `ej.JsonAdaptor` will be used to manipulate the grid datasource. 

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight js %}
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

![](trial_images/trial_img1.png)


I>[ There is no in-built support to bind the XML data to the grid. But you can achieve this requirement with the help of custom adaptor concept.] 

Refer this [Knowledge Base link](http://www.syncfusion.com/kb/3377/how-to-process-xml-data-from-server-using-datamanager-and-bound-to-grid# "") for bounding XML data to grid using custom adaptor.

## Remote Data

To bind remote data to the grid, you can assign a service data as an instance of [`ej.DataManager`](http://help.syncfusion.com/js/api/ejdatamanager# "") to the [`dataSource`](http://help.syncfusion.com/js/api/ejgrid#members:datasource "") property.

### OData

OData is a standardized protocol for creating and consuming data. You can provide the [OData service](http://www.odata.org/# "") URL directly to the [`ej.DataManager`](http://help.syncfusion.com/js/api/ejdatamanager# "") class and then you can assign it to Grid [`dataSource`](http://help.syncfusion.com/js/api/ejgrid#members:datasource "")`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight js %}
		$(function () {

			var dm =ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders”);

				$("#Grid").ejGrid({

					dataSource: dm,

					allowPaging:true,

					columns: ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]

					});

			});



{% endhighlight %}

The following output is displayed as a result of the above code example.

![](trial_images/trial_img2.png)


#### OData Version 4

For OData Version 4 support ej.ODataV4Adaptor should be used. By using `url` property of [`ej.DataManager`](http://help.syncfusion.com/js/api/ejdatamanager# "") you can bind OData Version 4 Service link and specify  `adaptor` as `ej.ODataV4Adaptor`.

I>[ You can provide adaptor value either as `string` value (“ODataAdaptor”) or by creating a new instance (new `ej.ODataAdaptor`).] 

{%seealso}For further details about OData service please refer [the link](http://www.odata.org/# ""). {% endseealso %}

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight js %}
	$(function () {

		var dataManager = ej.DataManager({

			url:"[http://services.odata.org/V4/Northwind/Northwind.svc/Regions/](http://services.odata.org/V4/Northwind/Northwind.svc/Regions/# "")",

			adaptor: new ej.ODataV4Adaptor()

			});

		$("#Grid").ejGrid({

			dataSource: dataManager,

			allowPaging:true

			});

	});



{% endhighlight %}

### WebAPI

Using `ej.WebApiAdaptor`, you can bind WebApi service data to Grid. The data from WebApi service must be returned as object that has property “Items” with its value as datasource and another property “Count” with its value as dataSource’s total records count.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight js %}
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



{% endhighlight %}

The following output is displayed as a result of the above code example.

![](trial_images/trial_img3.png)


### Other Restful web services

The [Custom Adaptor](http://helpjs.syncfusion.com/js/datamanager/data-adaptors#custom-adaptor "") concept of `[ej.DataManager](http://help.syncfusion.com/js/api/ejdatamanager# "")` allows to customize or generate your own adaptor which is used to process `query` and `result` data. 

When using remote data binding, the adaptor of `[ej.DataManager](http://help.syncfusion.com/js/api/ejdatamanager# "")` plays vital role in processing queries to make them suitable to sends along with data request and also process the response data from the server.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight js %}
$(function() {

	var customAdaptor = new ej.Adaptor().extend({

		insert: function(dm, data) {

			//Auto-increment `id` field value on insert

			data["id"] = dm.dataSource.json[dm.dataSource.json.length - parseInt(1, 10)].id + 1;

			return dm.dataSource.json.push(data);

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
	}

	];

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

![](trial_images/trial_img4.png)


### Load At Once

On remote data binding, by default all the grid actions will be processed on server-side such as paging, sorting, editing, grouping and filtering etc. To avoid post back to server on every action, you can set the grid to load all the data on initialization time and make the actions client-side. To enable this, you can use `offline` property of `[ej.DataManager](http://help.syncfusion.com/js/api/ejdatamanager# "")`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight js %}
$(function() {

	var dataManager = ej.DataManager({

		url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/",

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

Please refer [the link](http://help.syncfusion.com/js/datamanager/data-binding#offline-mode "") for further reference on `offline` property

The following output is displayed as a result of the above code example.

![](trial_images/trial_img5.png)


### Data Caching

Date caching will help you can prevent the request to server for already visited pages in Grid using `enableCaching` property of `[ej.DataManager](http://help.syncfusion.com/js/api/ejdatamanager# "")`. Also the grid options to control the number of pages to be cached and duration it should be cached. The properties for these are `cachingPageSize` and `timeTillExpiration` respectively.

I> [: The cached data will be stored in browser’s HTML5 `localStorage`]. 

The following code example describes the above behavior.

{% highlight html %}
<div id="CacheGrid"></div>



{% endhighlight %}

{% highlight js %}
$(function() {

	var dataManger = ej.DataManager({

		url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/",

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

![](trial_images/trial_img6.png)


### Custom request parameters and HTTP Header

#### Adding request parameters

You can use the `[addParams](http://help.syncfusion.com/js/api/ejquery#methods:addparams "")` method of `[ej.Query](http://help.syncfusion.com/js/api/ejquery# "")` class, to add custom parameter to the data request. The Grid has `[query](http://help.syncfusion.com/js/api/ejgrid#members:query "")` property, which accepts instance of `[ej.Query](http://help.syncfusion.com/js/api/ejquery# "")`, to add custom parameters to the data request.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight js %}
$(function() {

	$("#Grid").ejGrid({

		dataSource: ej.DataManager({

			url: [http: //mvc.syncfusion.com/Services/Northwnd.svc/Orders](http://mvc.syncfusion.com/Services/Northwnd.svc/Orders# "")

			}),

		allowPaging: true,

		query: new ej.Query().addParams("Syncfusion", true),

		columns: ["OrderID", "EmployeeID", "ShipCity", "ShipCountry", "Freight"]

		});

	});



{% endhighlight %}

The custom parameter added will be passed along with the data request of the grid as follows.

![](trial_images/trial_img7.png)


#### Handling Http Errors

During server interaction from the Grid, there may occur some server-side exceptions and you can acquire those error messages or exception details in client-side using grid's `[actionFailure](http://help.syncfusion.com/js/api/ejgrid#events:actionfailure "")` event.

The argument passed to the `[actionFailure](http://help.syncfusion.com/js/api/ejgrid#events:actionfailure "")` Grid event contains the Error details returned from server. Please refer the following table for some error details acquired in client-side event arguments.

<table>
<tr>
<td colspan=1 rowspan=1>
Parameter<br/><br/></td><td colspan=1 rowspan=1>
JSON Properties<br/><br/></td><td colspan=1 rowspan=1>
Description<br/><br/></td></tr>
<tr>
<td colspan=1 rowspan=2>
argument<br/><br/></td><td colspan=1 rowspan=1>
argument.error.status<br/><br/></td><td colspan=1 rowspan=1>
It returns the response error code<br/><br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
argument.error.statusText<br/><br/></td><td colspan=1 rowspan=1>
It returns the error message<br/><br/></td></tr>
</table>
The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>



{% endhighlight %}

{% highlight js %}
$(function() {

	var dataManger = ej.DataManager({

		url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Order",

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

![](trial_images/trial_img8.png)


## HTML Table 

A HTML Table element can also be used as the datasource of grid. To use HTML Table as datasource, the table element should be passed to instance of the `[ej.DataManager](http://help.syncfusion.com/js/api/ejdatamanager# "")` to grid's `[dataSource](http://help.syncfusion.com/js/api/ejgrid#members:datasource "")` property.

The following code example describes the above behavior.

{% highlight html %}
<div id=”Grid”></div>



{% endhighlight %}

{% highlight html %}
<table id="Table1">
   <thead>
      <tr>
         <th> Laptop </th>
         <th> Model </th>
         <th> Price </th>
         <th> OS </th>
         <th> RAM </th>
         <th> ScreenSize </th>
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

{% highlight js %}
$(function() {

	$("#Grid").ejGrid({

		dataSource: ej.DataManager($("#Table1")),

		columns: ["Laptop", "Model", "Price", "RAM", "ScreenSize"]

	});

});



{% endhighlight %}

The following output is displayed as a result of the above code example.

![](trial_images/trial_img9.png)


I>[ The HTML Table element is the only valid element when using HTML Table binding, using other elements will throw exception.

