---
layout: post
title: Data binding in DropDownList widget for Syncfusion Essential JS
description: Describes about the data binding in DropDownList widget for Syncfusion Essential JS
platform: js
control: DropDownList
documentation: ug
keywords: DropDownList, dropdown, data binding, REStFul Binding, WebAPI, Web Method, OData, OData4
api: /api/js/ejdropdownlist
---

# Data Binding

To populate data in the DropDownList widget, define [dataSource](https://help.syncfusion.com/api/js/ejdropdownlist#members:datasource) property with associated fields. In DropDownList, can bind either local array or OData, WebApi and other [RESTful](https://en.wikipedia.org/wiki/Representational_state_transfer) services.

## Fields

The below listed fields are the data collection fields which maps fields for the data items of the DropDownList. 

<table>
    <tr>
        <th>
            Properties
            <br/>
        </th>
        <th>
            Description
            <br/>
        </th>
    </tr>
    <tr>
        <td>
            [dataSource](https://help.syncfusion.com/api/js/ejdropdownlist#members:datasource)
            <br/>
        </td>
        <td>
            The data source contains the list of data for generating the popup list items.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [query](https://help.syncfusion.com/api/js/ejdropdownlist#members:query)
            <br/>
        </td>
        <td>
            It specifies the query to retrieve the data from the online server.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [fields](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields)
            <br/>
        </td>
        <td>
            It specifies the mapping fields for the data items of the DropDownList widget.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [id](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-id)
            <br/>
        </td>
        <td>
            It specifies the ID of the tag.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [text](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-text)
            <br/>
        </td>
        <td>
            It specifies the text content of the tag.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [value](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-value)
            <br/>
        </td>
        <td>
            It specifies the value of the tag.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [groupBy](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-groupby)
            <br/>
        </td>
        <td>
            It is used to categorize the items based on a specific field.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [imageUrl](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-imageurl)
            <br/>
        </td>
        <td>
            It defines the image location.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [imageAttributes](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-imageattributes)
            <br/>
        </td>
        <td>
            It defines the image attributes such as height, width, styles, etc.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [spriteCssClass](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-spritecssclass)
            <br/>
        </td>
        <td>
            It defines the sprite CSS for the image tag.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [htmlAttributes](https://help.syncfusion.com/api/js/ejdropdownlist#members:htmlattributes)
            <br/>
        </td>
        <td>
            It defines the HTML attributes such as class and styles for an item.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [selected](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-selected)
            <br/>
        </td>
        <td>
            This field defines the tag value to be selected initially. Corresponding field mapped has Boolean values to select the list items on control creation. The data with value true in this field is selected automatically when the control is initialized with checkbox.
            <br/>
        </td>
    </tr>
    <tr>
        <td>
            [tableName](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields-tablename)
            <br/>
        </td>
        <td>
            It defines the table name for the tag value or displays text while rendering remote data.
            <br/>
        </td>
    </tr>
</table>

## Local Data

Define a JSON array and initialize the widget with [dataSource](https://help.syncfusion.com/api/js/ejdropdownlist#members:datasource) property. Specify the column names in the [fields](#Fields) property.

N> The columns are bounded automatically when the fields are specified with the default names like id, text, etc...

{% highlight html %}

	<input type="text" id="dropdown1" />
    
{% endhighlight %}

{% highlight css %}

    	.imgId {
        	margin: 0;
        	padding: 3px 10px 3px 3px;
        	border: 0 none;
        	width: 60px;
        	height: 60px;
        	float: none;
    	}

{% endhighlight %}

{% highlight javascript %}
	
    $(function() {
        var List = [{
            text: "Erik Linden",
            role: "Representative",
            country: "England",
            img: "images/Employee/3.png",
            attr: {
                class: "imgId"
            }
        }, {
            text: "John Linden",
            role: "Representative",
            country: "Norway",
            img: "images/Employee/6.png",
            attr: {
                class: "imgId"
            }
        }, {
            text: "Louis",
            role: "Representative",
            country: "Australia",
            img: "images/Employee/7.png",
            attr: {
                class: "imgId"
            }
        }, {
            text: "Lawrence",
            role: "Representative",
            country: "India",
            img: "images/Employee/8.png",
            attr: {
                class: "imgId"
            }
        }];
        $('#dropdown1').ejDropDownList({
            dataSource: List,
            fields: {
                text: "text",
                value: "country",
                groupBy: "role",
                imageUrl: "img",
                imageAttributes: "attr"
            },
            width: "200px"
        });
    });	

{% endhighlight %}

![](DataBinding_images/DataBinding_img1.jpeg)

N> Images for this sample are available in (installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\samples\web\themes\images<br/>
I> htmlAttributes and imageAttributes should have JSON type value and sample for spriteCSSClass field is available in [here](http://jsplayground.syncfusion.com/Sync_px3jew3i) 
	
The JSON array to the [dataSource](https://help.syncfusion.com/api/js/ejdropdownlist#members:datasource) property can also be provided as an instance of the [ej.DataManager](https://help.syncfusion.com/api/js/ejdatamanager). When the JSON array is passed as an instance of [ej.DataManager](https://help.syncfusion.com/api/js/ejdatamanager), the [ej.JsonAdaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#json-adaptor) will be used to manipulate the DropDownList data source. The following code explains this behavior,

{% highlight html %}

	<input type="text" id="dropdown1" />
	
{% endhighlight %}

{% highlight javascript %}	
  
    $(function() {
        var items = [{
            text: "ListItem 1",
            value: "item1"
        }, {
            text: "ListItem 2",
            value: "item2"
        }, {
            text: "ListItem 3",
            value: "item3"
        }, {
            text: "ListItem 4",
            value: "item4"
        }, {
            text: "ListItem 5",
            value: "item5"
        }];
  
        //Passing as instance to the DataManager 
        $('#dropdown1').ejDropDownList({
            dataSource: ej.DataManager(items)
        });
  
    });

{% endhighlight %}


## Binding Remote Data Service

To bind remote data to the DropDownList, assign a service data as an instance of `ejDataManager` to the `dataSource` property.

### OData

OData is a standardized protocol for creating and consuming data. Provide the [OData service](http://www.odata.org/) URL directly to the "ej.DataManager" class and then you can assign it to DropDownList "dataSource".

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}

    $(function() {
        var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders");
        $('#dropdown1').ejDropDownList({
            dataSource: dataManager,
            fields: {
                text: "ShipCountry",
                value: "OrderID"
            }
        });
    });       

{% endhighlight %}
           
          
## OData Version 4
The OData v4 is an improved version of OData protocols and the Data Manager can also retrieve and consume data from [ODatav4](http://www.odata.org/) services.

By using URL property of “ej.DataManager” bind OData Version 4 Service link and specify adaptor as ej.ODataV4Adaptor.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}

    $(function() {
        var dataManager = ej.DataManager({
            url: "http://services.odata.org/V4/Northwind/Northwind.svc/Regions/",
            adaptor: new ej.ODataV4Adaptor()
        });
        $('#dropdown1').ejDropDownList({
            dataSource: dataManager,
            fields: {
                text: "RegionDescription",
                value: "RegionID"
            }
        });
    });
  
{% endhighlight %}
           
           
![](DataBinding_images/DataBinding_img2.jpeg)

N> Events associated with remote data bind is listed [here](https://help.syncfusion.com/api/js/ejdropdownlist#events). 

## WebAPI Binding

Using [ej.WebApiAdaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#webapi-adaptor), bind WebApi service’s data to DropDownList. The data from WebApi service must be returned as an object that has property “Items” with its value as data source and another property “Count” with its value as dataSource’s total records count.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}

    $(function() {
        $("#dropdown1").ejDropDownList({
            dataSource: ej.DataManager({
                url: "/api/Orders",
                adaptor: new ej.WebApiAdaptor()
            }),
            fields: {
                text: "Name",
                value: "EmployeeID"
            }
        });
    });

{% endhighlight %}

{% highlight c# %}

    public class OrdersController : ApiController
    {
        NorthwindDataContext db = new NorthwindDataContext();
        
        // GET API/<controller>       
        public PageResult<EmployeePhoto> Get(ODataQueryOptions opts)
        {
            List<EmployeePhoto> photo = db.EmployeePhotos.ToList();            

            return new PageResult<EmployeePhoto>(photo as IEnumerable<EmployeePhoto>, null, photo.Count);
        }
    } 

{% endhighlight %}

![](DataBinding_images/DataBinding_img3.jpeg)

## ASP.NET Web Method Binding

The data can retrieve data from ASP.NET Web methods by making use of the WebMethod Adaptor of ejDataManager.

The WebMethod Adaptor is used to bind data source from remote services and code behind methods. 
By using “[WebMethodAdaptor](https://help.syncfusion.com/js/datamanager/getting-started)” we can bind data from WebService to the DropDownList control and also we need to include “ScriptService” Attribute to WebService in order to enable request from client-side.

{% highlight html %}

    <span> Please select... </span>
    <input type="text" id="myList" />
    
{% endhighlight %}

{% highlight c# %}

    [System.Web.Script.Services.ScriptService]
    public class WebService1 : System.Web.Services.WebService
    {

        [WebMethod]
        public object Get()
        {

            List<Employee> Data = new List<Employee>();
            Data.Add(new Employee
            {
                Name = "Erik Linden",
                Role = "Executive"
                
            });
            Data.Add(new Employee
            {
                Name = "John Linden",
                Role = "Representative"
                
            });
            Data.Add(new Employee
            {
                Name = "Louis",
                Role = "Representative"
                
            });
            Data.Add(new Employee
            {
                Name = "Lawrence",
                Role = "Executive"
                
            });
            dynamic count = Data.Count;
            return new
            {
                result = Data,
                count = count
            };

        }
        public class Employee
        {
            public string Name { get; set; }
            public string Role { get; set; }
            
        }
    }
    
{% endhighlight %}

{% highlight javascript %}

    <script type="text/javascript">
        var data = ej.DataManager({
            url: "WebService1.asmx/Get",
            adaptor: new ej.WebMethodAdaptor()
        });
        var query = ej.Query().requiresCount();
        $("#myList").ejDropDownList({
            dataSource: data,
            query: query,
            fields : {text :"Name", value :"Country"}
        });
    </script>
    
{% endhighlight %}

Use the above code example to use WebMethod adaptor and bind the data to the DropDownList with the help of [query](https://help.syncfusion.com/api/js/ejdropdownlist#members:query) property.

## MVC controller Action Binding

The data can retrieve from MVC controller. This can be achieved by using the UrlAdaptor of ej.DataManager.

Defines the List of Employee Data and converted into JSON object. 

{% highlight c# %}

    using System.Web.Script.Serialization;
    public partial class DropdownlistController: Controller
    {
        public ActionResult DropdownlistFeatures()
        {
            return View();
         } 
        public class Employee
        {
            public string Name { get; set; }
            public string Role { get; set; }
        }
        public JsonResult getData()
        {
            List<Employee> Data = new List<Employee>();
            Data.Add(new Employee
            {
                Name = "Erik Linden",
                Role = "Executive"
            });
            Data.Add(new Employee
            {
                Name = "John Linden",
                Role = "Representative"
            });
            Data.Add(new Employee
            {
                Name = "Louis",
                Role = "Representative"
            });
            Data.Add(new Employee
            {
                Name = "Lawrence",
                Role = "Executive"
            });
            var jsonSerializer = new JavaScriptSerializer();
            return Json(jsonSerializer.Serialize(Data));
        }
    }
    
{% endhighlight %}

In client side, specify the URL of Data to url property and specify the type of Adaptor in adaptor property of DataManager and initialize the DropDownList with [dataSource](https://help.syncfusion.com/api/js/ejdropdownlist#members:datasource) property. Specify the column names in the [fields](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields) property.

{% highlight javascript %}

    <div class="ctrl-label"> Select an Employee</div>
    <input id="List"/>
    
    <script>
        $(function() {
        
            var dataManager = ej.DataManager({
                url: "/Dropdownlist/getData",
                adaptor: new ej.UrlAdaptor()
            });
        
            $("#List").ejDropDownList({
            
                dataSource: dataManager,
                fields: { text: "Name", value: "Role" }
            });
        
        });
    </script>

{% endhighlight %}

## Other Restful web services

The [Custom Adaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#custom-adaptor) concept of "ej.DataManager" allows to customize or generate your own adaptor which is used to process "query" and "result" data. 
When using remote data binding, the adaptor of "ej.DataManager" plays vital role in processing queries to make them suitable to sends along with data request and also process the response data from the server.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}
  
    $(function() {
        //custom adaptor

        var customAdaptor = new ej.Adaptor().extend({
            insert: function(dataObj, data) {
                return dataObj.dataSource.json.push(data);
            },
            processQuery: ej.JsonAdaptor.prototype.processQuery
                // reused process query from JSON adaptor
        });
  
        window.dropdownData = [{
            FirstName: "John",
            LastName: "Abraham"
        }, {
            FirstName: "Ben",
            LastName: "Nick"
        }, {
            FirstName: "Andrew",
            LastName: "Clarke"
        }];
  
        var dataManager = new ej.DataManager(window.dropdownData);
  
        // assigning custom adaptor to datamanager
        dataManager.adaptor = new customAdaptor(); 
  
  		// insert from custom adaptor usage
        dataManager.insert({
            FirstName: "Joel",
            LastName: "Nick"
        });
  
        $('#dropdown1').ejDropDownList({
            dataSource: dataManager,
            fields: {
                text: "FirstName",
                value: "LastName"
            }
        });
  
    });

{% endhighlight %}

![](DataBinding_images/DataBinding_img4.jpeg)


## Virtual Scrolling 

To improve the performance when displaying large data set, you can use [allowVirtualScrolling](https://help.syncfusion.com/api/js/ejdropdownlist#members:allowvirtualscrolling) and [virtualScrollMode](https://help.syncfusion.com/api/js/ejdropdownlist#members:virtualscrollmode) property. This retrieves only a fixed amount of list items and loads remaining data on scrolling. The items will be fetched via AJAX request.

This supports two modes of virtualization. They are,

* Normal Mode
* Continuous Mode

I> 1. Sorting and Grouping is not supported with Virtual Scrolling
I> 2. “virtualScrollMode” property accepts both the string and ej.VirtualScrollMode enum value.

### Normal Mode

It loads the data on scrolling the list of items. This can be achieved by setting [normal](https://help.syncfusion.com/api/js/ejdropdownlist#members:virtualscrollmode) value to the "virtualScrollMode" property.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}
  
        $(function() { 
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders"
            });
            
        $('#dropdown1').ejDropDownList({
            dataSource: dataManager,
            fields: {
                text: "ShipName",
                value: "ShipCountry"
            },
            allowVirtualScrolling: true,
            virtualScrollMode: ej.VirtualScrollMode.Normal,
            itemsCount: 7
        });
    });

{% endhighlight %}

### Continuous Mode

It loads the set of items when the scroller reaches at the end. This behaves like infinity scrolling. So when scroll reaches the end, it will fetch the remaining set of items and bind with your DropDownList. This can be achieved by setting [continuous](https://help.syncfusion.com/api/js/ejdropdownlist#members:virtualscrollmode) value to the "virtualScrollMode" property.

N> In both modes, set of items will be fetched based on the count specified in the [itemsCount](https://help.syncfusion.com/api/js/ejdropdownlist#members:itemscount) property and next set of items will be loaded on scrolling.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}
    
       $(function() {        
        var dataManager = ej.DataManager({
            url: "http://mvc.syncfusion.com/services/Northwnd.svc/Orders"
       });
        
        $('#dropdown1').ejDropDownList({
            dataSource: dataManager,
            fields: {
                text: "ShipName",
                value: "ShipCountry"
            },
            allowVirtualScrolling: true,
            virtualScrollMode: ej.VirtualScrollMode.Continuous,
            itemsCount: 7
            });
        });
     

{% endhighlight %}
