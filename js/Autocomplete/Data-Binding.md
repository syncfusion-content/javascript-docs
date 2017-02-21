---
layout: post
title: Databinding in AutoComplete widget for Essential JS
description: How to populate data for the suggestion list.
platform: js
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, js autocomplete, jquery autocomplete, web autocomplete, ej autocomplete, essential javascript autocomplete,
---

# Data Binding

In order to render the AutoComplete control, the data needs to be bound to it in a proper way. The below sections explains about how to bind either the local or remote data to the AutoComplete widget. 

## Fields

The AutoComplete widget has a field property (object) which holds the properties to map with datasource fields. For example, the field object has a text property which is necessary to map with specific field in the datasource to render the suggestion items in the AutoComplete widget.

The field object contains the following properties.

* [text](https://help.syncfusion.com/api/js/ejautocomplete)

* [key](https://help.syncfusion.com/api/js/ejautocomplete)

* [groupBy](https://help.syncfusion.com/api/js/ejautocomplete)

* [htmlAttributes](https://help.syncfusion.com/api/js/ejautocomplete)



### Local data

The local data can be an array of JSON objects which is assigned for the Autocomplete widget’s datasource property. Refer the below example.

Here the name and index fields are mapped with text and key properties of the field object respectively.

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

[OData](https://help.syncfusion.com/js/datamanager/data-binding) is a standardized protocol for creating and consuming the data. You can retrieve data from OData service by using [ej.DataManager](https://help.syncfusion.com/js/datamanager/getting-started).

Here the ContactName and SupplierID fields are mapped with text and key properties respectively, of the field object. The queries can be created using [ej.Query()](https://help.syncfusion.com/js/datamanager/query).

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



N> In the above data manager configuration, “crossDomain” must be set to true to access the data from Web API. [Cross domain](https://help.syncfusion.com/js/grid/data-binding) requests can be possible using ej.DataManager.

![AutoComplete-APIData](webapi_images\webapi_img1.png)




#### Handling errors

 In remote binding, the server might not return data sometimes due to various reasons. In such cases we need to handle the error properly. We can handle this using the “[actionFailure](https://help.syncfusion.com/api/js/ejautocomplete)” event. 

{%seealso%} 
* [actionComplete](https://help.syncfusion.com/api/js/ejautocomplete) event

* [actionSuccess](https://help.syncfusion.com/api/js/ejautocomplete) event
{%endseealso%}

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



