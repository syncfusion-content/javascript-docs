---
layout: post
title: Data-Binding
description: data binding
platform: js
control: Grid
documentation: ug
---

# Data Binding
Grid supports different kinds of databinding methods such as 

1. Local data
2. Remote data
3. HTML table

## Local data

Grid can bind to local data source. To bind local data, directly assign the JSON array to grid's `dataSource` property. 

{% highlight html %}



<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      // Data for grid.
      window.gridData = [
        { firstName: "John", lastName: "Beckett", email: "john@syncfusion.com" },
        { firstName: "Ben", lastName: "Beckett", email: "ben@syncfusion.com" },
        { firstName: "Andrew", lastName: "Beckett", email: "andrew@syncfusion.com" }
      ];
      $("#Grid").ejGrid({
          dataSource:window.gridData,
          columns: [
                   { field: "firstName",headerText:"First Name" },
                   { field: "lastName", headerText: "Last Name" },
                   { field: "email", headerText: "Email" }
          ]
      });
  });
  
</script>



{% endhighlight %}



Result of the above code example.

{% include image.html url="/js/Grid/Data-Binding_images/Data-Binding_img1.png"%}

## Remote data

### oData Binding	

**oData** is a standardized protocol for creating and consuming the data. You can retrieve data from oData service by using `ej.DataManager`. The following code is a simple example of remote data binding by using oData service.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      //oData Adaptor with DataManager
      var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Products");
  
      $("#Grid").ejGrid({
          dataSource: dataManager,
          columns: ["ProductID", "ProductName", "SupplierID", "UnitPrice"]
      });
  });
</script>


{% endhighlight %}



The following output is the result of the above code example.

{% include image.html url="/js/Grid/Data-Binding_images/Data-Binding_img2.png"%}

> _**Note**: For information about DataManager with Grid check DataAdaptors concept._

### Load at once

Through this **load at once** technique, you can load all data from the server to browser and process records in client-side. This can be enabled by setting `offline` property as true in `ej.DataManager`. The following code example shows **load at once** with Grid. 

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      //oData Adaptor with DataManager
      var dataManager = ej.DataManager({
          url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Products",
          offline: true
      });
  
      $("#Grid").ejGrid({
          dataSource: dataManager,
          allowPaging: true,
          columns: ["ProductID", "ProductName", "SupplierID", "UnitPrice"]
      });
  });
  
</script>

{% endhighlight %}



The following output is the result of the above code example.

{% include image.html url="/js/Grid/Data-Binding_images/Data-Binding_img3.png"%}

### Load on demand

**Load on demand** is a technique used to reduce bandwidth size of consuming the data. This feature is enabled by default, when remote data is bound to Grid. In the following example, oData service is used. At load time, it retrieves required data from service, only for the visible page. When you move to another page, it loads for current page. The following code example shows you how load on demand works with remote data.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      //oData Adaptor with DataManager
      var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Products");
  
      $("#Grid").ejGrid({
          dataSource: dataManager,
          allowPaging: true,
          columns: ["ProductID", "ProductName", "SupplierID", "UnitPrice"]
      });
  });
</script>


{% endhighlight %}



The following screenshot is the result of the above code example.

{% include image.html url="/js/Grid/Data-Binding_images/Data-Binding_img4.png"%}

If you have developer tools, you can capture network transfer to check **Grid** consumed data. The following screenshot shows demanded data being loaded in **Grid**.

{% include image.html url="/js/Grid/Data-Binding_images/Data-Binding_img5.png"%}

### Cross domain

Cross domain data requests can be possible using `ej.DataManager`. This can be enabled using the property `crossDomain` in `ej.DataManager` options. This property is for configuring the client-side to make the cross domain request however you need configure the server as well, to retrieve data from server. For server configuration, you can refer this link ([https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS)). The following code example shows you how to use or retrieve cross domain data from Grid.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      //DataManger
      var dataManager = ej.DataManager({
          url: "http://mvc.syncfusion.com/UGService/api/Orders",
          crossDomain: true,
          offline: true
      });
      $("#Grid").ejGrid({
          allowPaging: true,
          dataSource: dataManager,
          columns: ["OrderID", "CustomerID", "EmployeeID", "ShipCity"]
      });
  });
  
</script>


{% endhighlight %}



The following screenshot is the result of the above code example.

{% include image.html url="/js/Grid/Data-Binding_images/Data-Binding_img6.png"%}

### HTTP additional parameters

In this section, you can learn how to customize or add an extra parameter for `HTTP` request. You can add additional parameter to web service using the grid's `query` property and DataManager Query's `addParams` functions. Query value will be passed to `ej.DataManager` internally in Grid.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      //oData Adaptor with DataManager
      var dataManager = ej.DataManager({
          url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Products"
      });
  
      $("#Grid").ejGrid({
          dataSource: dataManager,
          allowPaging: true,
          query: new ej.Query().addParams("$filter", "ProductID gt 50"), //extra parameter
          columns: ["ProductID", "ProductName", "SupplierID", "CategoryID"]
      });
  });
  
</script>


{% endhighlight %}



The following screenshot is the result of the above code example.

{% include image.html url="/js/Grid/Data-Binding_images/Data-Binding_img7.png"%}

### Supported DataTypes

ejGrid supports various data types in JavaScript such as string, number, datetime and Boolean. By default, data types will be read from first row of `dataSource`. You can also manually set the data type to a column through `type` property.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          columns: [
                   { field: "firstName", type: "string" },
                   { field: "lastName", type: "string" },
                   { field: "email" }
          ]
      });
  });
</script>



{% endhighlight %}

## HTML table

Grid can be created from HTML table using DataManager. Please refer the following code snippet to achieve it.

{% highlight html %}

<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
        dataSource: ej.DataManager($("#Table1")), // binds table to grid
          columns: [
                   { field: "Laptop", headerText: "Laptop Brands"},
                   { field: "Model", headerText: "Model" },
                   { field: "Price", headerText: "Price", width: 90, textAlign: ej.TextAlign.Right, format: " ${0:c}" },
                   { field: "OS", headerText: "Operating System" },
                   { field: "RAM", headerText: "RAM", width: 120, textAlign: ej.TextAlign.Right },
                   { field: "ScreenSize", headerText: "Screen Size", textAlign: ej.TextAlign.Right, width: 100, format: "{0:N1} inch" }
          ]
      });
  });
</script>

<div id="Grid"></div>
<table id="Table1">
  <thead>
    <tr>
      <th>
        Laptop
      </th>
      <th>
        Model
      </th>
      <th>
        Price
      </th>
      <th>
        OS
      </th>
      <th>
        RAM
      </th>
      <th>
        ScreenSize
      </th>
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



The following screenshot is the result of the above code example.

{% include image.html url="/js/Grid/Data-Binding_images/Data-Binding_img8.png"%}

