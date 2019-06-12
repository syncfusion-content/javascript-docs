---
layout: post
title: Databinding in Syncfusion AutoComplete widget for Essential JS
description: How to populate data for the suggestion list.
platform: js
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, js autocomplete, jquery autocomplete, web autocomplete, ej autocomplete, essential javascript autocomplete,
api: /api/js/ejautocomplete
---

# Data Binding

In order to render the Autocomplete widget, the data needs to be bound to it in a proper way. The below sections explain about binding local or remote data to the Autocomplete widget.

## Fields

The Autocomplete widget has a field property (object) which holds the properties to map with dataSource fields. Whenever we bind a data to Autocomplete, corresponding fields must be mapped using this property.

The field object contains the following properties.

<table>
<tr>
<th>Fields property</th>
<th>Description</th>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-text">text</a> </td>
<td>Maps the display text in the suggestion list </td>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-key">key</a> </td>
<td>Maps to the unique key field in the data source</td>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-groupBy">groupBy</a> </td>
<td>Allows to enable grouping based on the assigned field</td>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-htmlAttributes">htmlAttributes</a> </td>
<td>Maps to set the HTML attribute for the list items</td>
</tr>
</table>



### Local data

The local data must be an array of JSON objects which is assigned for the Autocomplete widget [dataSource](https://help.syncfusion.com/api/js/ejautocomplete#members:datasource) property. 

In the below example name and index fields are mapped with text and key properties of the field object respectively.

{% highlight html %}

        
        <input type="text" id="autocomplete" />
        
        <script type="text/javascript">
        
                var countriesField = [
                { name: "Austria", index: "C1" },
                { name: "Australia", index: "C2" }, { name: "Antarctica", index: "C3" },
                { name: "Bangladesh", index: "C4" }, { name: "Belgium", index: "C5" },
                { name: "Brazil", index: "C6" },
                { name: "Canada", index: "C7" }, { name: "China", index: "C8" },
                { name: "Cuba", index: "C9" },
                { name: "Denmark", index: "C10" }, { name: "Dominica", index: "C11" },
                { name: "Europe", index: "C12" }, { name: "Egypt", index: "C13" },
                { name: "England", index: "C14" },
                { name: "India", index: "C15" }, { name: "Indonesia", index: "C16" }
                ];
        
                $('#autocomplete').ejAutocomplete({ dataSource: countriesField, fields: { key: "index", text: "name" }, width: 205 });
        
        </script>



{% endhighlight %}

![AutoComplete-LocalData](local-data_images\local-data_img1.png)



### Remote data

#### OData

[OData](https://help.syncfusion.com/js/datamanager/data-binding) is a standardized protocol for creating and consuming the data. You can retrieve data from OData service by using [ej.DataManager](https://help.syncfusion.com/js/datamanager/getting-started) and the queries can be added using [ej.Query()](https://help.syncfusion.com/js/datamanager/query).

Here ContactName and SupplierID fields are mapped with text and key [fields](https://help.syncfusion.com/api/js/ejautocomplete#members:fields) properties are respective to the field object.

{% highlight html %}

        <input type="text" id="autocomplete" />
        
        <script type="text/javascript">
        
                /* Create DataManager */
                var dataManger = ej.DataManager({
                /* OData service */
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
                });
                /* Create Query */
                var query = ej.Query().from("Suppliers").select("SupplierID", "ContactName");
        
                $('#autocomplete').ejAutocomplete({ dataSource: dataManger, query: query, fields: { text: "ContactName", key: "SupplierID" }, width: 205 });
        
        </script>
        


{% endhighlight %}



![AutoComplete-OData](odata_images\odata_img1.png)



#### WebAPI



[ASP.NET Web API](https://msdn.microsoft.com/en-us/library/hh833994(v=vs.108).aspx) is a Framework for building HTTP services. You can retrieve data from ASP.NET Web API by using [ej.DataManager](https://help.syncfusion.com/js/datamanager/getting-started).

Here the ContactName field is mapped with text property of the field object. 

{% highlight html %}
        
        <input type="text" id="autocomplete" />
        
        <script type="text/javascript">
        
                /* Creating DataManager */
                var dataManger = ej.DataManager({
                /* ASP.NET Web API */
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Suppliers",
                crossDomain: true
                });        
                $('#autocomplete').ejAutocomplete({ dataSource: dataManger, fields: { text: "ContactName" }, width: 205 });
        
        </script>
        


{% endhighlight %}



N> In the above data manager configuration, “crossDomain” must be set to true to access the data from Web API. Cross origin requests can be possible using ej.DataManager.

![AutoComplete-APIData](webapi_images\webapi_img1.png)

#### URL Adaptor

URL Adaptor of **DataManager** can be used when you are required to use remote service to retrieve data. It interacts with server-side for all **DataManager** Queries and **CRUD** operations.

Now, in the following code example the data is retrieved from **MVC****Controller**.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}



{% highlight js %}

   var dataManager = ej.DataManager({ url: "Home/Data", adaptor: new ej.UrlAdaptor() });
        var query = ej.Query().take(10);

    $(function () {
            $("#autocomplete").ejAutocomplete({
        dataSource: dataManager,
        fields: { "text": "text","key":"uniqueKey " },
        query: query,
        }); 


{% endhighlight %}



**Controller:**

{% highlight c# %}


public partial class AutocompleteController : Controller
    {

        public JsonResult DataSource()
        {

            IEnumerable Data = setListSource();
            return Json(Data, JsonRequestBehavior.AllowGet);
        }

        public static List<CarsList> setListSource()
        {
            List<CarsList> cars = new List<CarsList>();

            cars.Add(new CarsList { uniqueKey = 1, text = "Audi S6", company = "Audi" });
            cars.Add(new CarsList { uniqueKey = 2, text = "Austin-žHealey", company = "Austin" });
            cars.Add(new CarsList { uniqueKey = 3, text = "BMW š7", company = "BMW" });
            cars.Add(new CarsList { uniqueKey = 4, text = "Chevrolet Camarož", company = "Chevrolet" });
            cars.Add(new CarsList { uniqueKey = 6, text = "Ferrari š360", company = "Ferrari" });
            cars.Add(new CarsList { uniqueKey = 7, text = "Honda S2000", company = "Honda" });
            cars.Add(new CarsList { uniqueKey = 8, text = "Hyundai Santroš", company = "Hyundai" });
            cars.Add(new CarsList { uniqueKey = 9, text = "Isuzu Swift", company = "Isuzu" });
            cars.Add(new CarsList { uniqueKey = 10, text = "Jaguar XJS", company = "Jaguar" });
            cars.Add(new CarsList { uniqueKey = 11, text = "iLotus Esprit", company = "Lotus" });
            cars.Add(new CarsList { uniqueKey = 12, text = "Mercedes-Benz", company = "Mercedes" });
            cars.Add(new CarsList { uniqueKey = 13, text = "Toyota ž2000GT", company = "Toyota" });
            cars.Add(new CarsList { uniqueKey = 14, text = "Volvo P1800", company = "Volvo" });
            ViewBag.datasource = cars;
            return View();
        }




{% endhighlight %}

![AutoComplete-Url](odata_images\url_img.png)


#### Handling errors

 In remote binding, the server actions can be handled for adding client side purpose. 
 
<table>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-actionFailure">actionFailure</a> </td>
<td>Event get triggered when remote server does not return data. We can handle the error properly in client side in this event</td>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-actionComplete">actionComplete</a> </td>
<td>Event gets triggered when the server action is completed, whether it may be success or failure</td>
</tr>
<tr>
<td> <a href="https://help.syncfusion.com/api/js/ejautocomplete#members:fields-actionSuccess">actionSuccess</a> </td>
<td>Event gets triggered when the remote server action returns data successfully</td>
</tr>
</table> 


{% highlight html %}

        <input type="text" id="autocomplete" />
        
        <script type="text/javascript">
        
                /* Creating DataManager */
                var dataManger = ej.DataManager({
                /* Web service host */
                url: "http://mvc.syncfusion.com/Services/"
                });
                /* Query creation */
                var query = ej.Query().from("Suppliers").select("SupplierID", "ContactName");
        
                $('#autocomplete').ejAutocomplete({ dataSource: dataManger, query: query, fields: { text: "ContactName", key: "SupplierID" }, width: 205, actionFailure: onRequestFailure });
        
                function onRequestFailure(args) {
                //Error handler
                }
        
        </script>



{% endhighlight %}



