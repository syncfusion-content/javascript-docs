---
layout: post
title: Data-Adaptors
description: data adaptors
platform: js
control: Grid
documentation: ug
---

# Data Adaptors

**DataManager** consists of three concepts, commonly called as **adaptors** that are used to manipulate data. There are four types of adaptors in **DataManager**. They are

* **JSON Adaptor**

* **OData Adaptor**

* **Custom Adaptor**

* **Cache Adaptor**

## JSON Adaptor

**JSON adaptor** is a powerful way to define **JSON data** to **Grid**.  Using this technique, you can use **DataManager** features to **JSON** before binding it to **Grid**.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      window.gridData = [
           { firstName: "John", lastName: "Beckett", email: "john@syncfusion.com" },
           { firstName: "Ben", lastName: "Beckett", email: "ben@syncfusion.com" },
           { firstName: "Andrew", lastName: "Beckett", email: "andrew@syncfusion.com" }
      ];
      //JSON adaptor with DataManager.
      var dataManager = ej.DataManager(window.gridData);
      dataManager.insert({firstName: "Joel", lastName:"Beckett", email:"joel@syncfusion.com"});
  
      $("#Grid").ejGrid({
          dataSource: dataManager,
      });
  });
  
</script>


{% endhighlight %}



The following screenshot is the result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Data-Adaptors_images/Data-Adaptors_img1.png" Caption="JSON Adaptor"%}

## OData Adaptor

Nowadays **oData** is a very useful technique in consuming data. You can use **oData** protocol through **DataManager**’s **ODataAdaptor**. The following code example demonstrates how you can use **oDataAdaptor** with **Grid**.

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



The following screenshot is the result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Data-Adaptors_images/Data-Adaptors_img2.png" Caption="OData Adaptor"%}

## Custom Adaptor

**CustomAdaptor** is a technique used to customize adaptors in **ej.DataManager**. It helps you to make your own adaptor. Normally **ej.Adaptor** is used as the base class for all adaptors, so you must first inherit **ej.Adaptor** to develop a customized one.Then you can override functionality in **customAdaptor** with base class. The following code example shows you how to create **customAdaptor** and use it with **Grid**.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      //new custom adaptor implmentation
      //able to implement more option in custom adaptor other than insert
      var customAdaptor = new ej.Adaptor().extend({
          insert: function (dm, data) {
              data["id"] = dm.dataSource.json[dm.dataSource.json.length - parseInt(1,10)].id + 1;// id auto increment
              return dm.dataSource.json.push(data);
              },
     processQuery:ej.JsonAdaptor.prototype.processQuery // resused process query from json adaptor
  });
      window.gridData = [
          { id: 1 , firstName: "John", lastName: "Beckett", email: "john@syncfusion.com" },
          { id: 2, firstName: "Ben", lastName: "Beckett", email: "ben@syncfusion.com" },
          { id: 3, firstName: "Andrew", lastName: "Beckett", email: "andrew@syncfusion.com" }
      ];
  
      var dataManager = new ej.DataManager(window.gridData);
      // assigning custom adaptor to datamanager
      dataManager.adaptor = new customAdaptor();
      // insert from custom adaptor usage
     dataManager.insert({ firstName: "Joel", lastName: "Beckett", email: "joel@syncfusion.com" });
  
      $("#Grid").ejGrid({
          dataSource: dataManager,
          columns: [
              { field: "firstName", headerText: "First Name" },
              { field: "lastName", headerText: "Last Name" },
              { field: "email", headerText: "Email" }
          ]
      });
  });
</script>

{% endhighlight %}



The following screenshot is the result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Data-Adaptors_images/Data-Adaptors_img3.png" Caption="Custom adaptor"%}

## Cache Adaptor

Cache Adaptor is a technique used to cache multiple page data by using the property enableCaching. You can provide the number of pages that is required to cache in single request using **cachingPageSize** property. It enables you to reduce multiple request to server. You can use any type of adaptor with multiple page caching by using cache adaptor. The following code illustrates how to create cache adaptor and use it with grid.

{% highlight html %}

 <div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      var dataManger = ej.DataManager({
          url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/",
          enableCaching: true,
          cachingPageSize: 10,
          timeTillExpiration: 120000
      });
      $("#Grid").ejGrid({
          dataSource: dataManger,
          columns: ["OrderID ", " CustomerID ", " EmployeeID ", " Freight", " ShipCity"]
      });
  });
</script>


{% endhighlight %}



The following screenshot is the result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Data-Adaptors_images/Data-Adaptors_img4.png" Caption=""%}

_Cache Adaptor_

