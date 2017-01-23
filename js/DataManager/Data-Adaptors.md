---
layout: post
title: Data-Adaptors
description: data adaptors
platform: js
control: DataManager
documentation: ug
---

# Data Adaptors

**DataManger** uses adaptors to process data. There are three types of adaptors in **DataManger**. They are

* JSON Adaptor

* URL Adaptor

* OData Adaptor

Here, you can learn when and how each adaptor is used.

## JSON Adaptor

**JSONAdaptor** is used to process **JSON** data. It contains methods to process the given **JSON** data based on the queries. The following code example illustrates on how to use **JSONAdaptor**.


{% highlight html %}

<body>
   <div class="datatable">
      <table id="table1" class="table table-striped table-bordered" style="width:700px">
         <thead>
            <tr>
               <th>Order ID</th>
               <th>Customer ID</th>
               <th>Employee ID</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script type="text/javascript">
      $(function () {
      
          var data = [{ OrderID: 10248, CustomerID: "VINET", EmployeeID: 5 },
      { OrderID: 10249, CustomerID: "AANAR", EmployeeID: 9 },
      { OrderID: 10250, CustomerID: "VICTE", EmployeeID: 2 },
      { OrderID: 10251, CustomerID: "TOMSP", EmployeeID: 7 },
      { OrderID: 10252, CustomerID: "SUPRD", EmployeeID: 6 }];
      
          var dataManager = ej.DataManager(data);
          $("#table1 tbody").html($("#tableTemplate")
                     .render(dataManager.executeLocal(new ej.Query().take(3))));
      });
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>OrderID}}</td>
          <td>{{>CustomerID}}</td>
          <td>{{>EmployeeID)}}</td>
      </tr>
   </script>
</body>

{% endhighlight %}


The result of above code example is illustrated as follows.


![](/js/DataManager/Data-Adaptors_images/Data-Adaptors_img1.png) 

## URL Adaptor

URL Adaptor of **DataManager** can be used when you are required to use remote service to retrieve data. It interacts with server-side for all **DataManager** Queries and **CRUD** operations. Now, in the following code example the data is retrieved data from **MVC** **Controller**. 

{% highlight html %}

<body>
   <div class="datatable">
      <table id="table1" class="table table-striped table-bordered" style="width:700px">
         <thead>
            <tr>
               <th>Order ID</th>
               <th>Customer ID</th>
               <th>Employee ID</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script type="text/javascript">
      $(function () {
          var dataManager = ej.DataManager({ url: "Home/Data", adaptor: new ej.UrlAdaptor() });
          var query = ej.Query().take(3);
          var execute = dataManager.executeQuery(query) // executing query
                 .done(function (e) {
                     $("#table1 tbody").html($("#tableTemplate").render(e.result));
                 });
      });
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>OrderID}}</td>
          <td>{{>CustomerID}}</td>
          <td>{{>EmployeeID)}}</td>
      </tr>
   </script>
</body>

{% endhighlight %}



{% highlight c# %}

  public class HomeController : Controller
    {
       public JsonResult Data(DataManager dm)
        {
            List<Object> data = new List<object>();
            for (int i = 1; i <= 10; i++)
            {
                data.Add(new { OrderID = 10240 + i, CustomerID = "Customer" + i, EmployeeID = i });
            }
            var records = data.Take(dm.Take); // take query of Data Manager

            return Json(records, JsonRequestBehavior.AllowGet);
        }
    }

{% endhighlight %}


The result of the above code example is illustrated as follows.


![](/js/DataManager/Data-Adaptors_images/Data-Adaptors_img2.png) 

## OData Adaptor

**OData** Adaptor that is extended from URL Adaptor, is used for consuming data through OData Service. You can use the following code example to use **OData** adaptor.


{% highlight html %}

<body>
   <div class="datatable">
      <table id="table1" class="table table-striped table-bordered" style="width:700px">
         <thead>
            <tr>
               <th>Order ID</th>
               <th>Customer ID</th>
               <th>Employee ID</th>
               <th>Freight</th>
               <th>Ship Country</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script type="text/javascript">
      $(function () {// Document is ready.
          //oData Adaptor with DataManager
          var dataManager = ej.DataManager({
              url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders",
              crossDomain: true,
              offline: true
          });
          var query = ej.Query()
              .select("OrderID", "CustomerID", "EmployeeID", "Freight", "ShipCountry").take(10)
          var execute = dataManager.executeQuery(query) // executing query
                 .done(function (e) {
                     $("#table1 tbody").html($("#tableTemplate").render(e.result));
                 });
      });
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>OrderID}}</td>
          <td>{{>CustomerID}}</td>
          <td>{{>EmployeeID)}}</td>
          <td>{{>Freight}}</td>
          <td>{{>ShipCountry}}</td>
      </tr>
   </script>
</body>

{% endhighlight %}


The result of the above code example is illustrated as follows.



![](/js/DataManager/Data-Adaptors_images/Data-Adaptors_img3.png) 

## WebAPI Adaptor

**WebApi** Adaptor, extended from UrlAdaptor, of **DataManager** is used for retrieving data from WebApi service. Refer to the following code example.


{% highlight html %}

<body>
   <div class="datatable">
      <table id="table1" class="table table-striped table-bordered" style="width:700px">
         <thead>
            <tr>
               <th>Order ID</th>
               <th>Customer ID</th>
               <th>Employee ID</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script type="text/javascript">
      $(function () {
          var dataManager = ej.DataManager({ url: "http://mvc.syncfusion.com/UGService/api/Orders", crossDomain: true, adaptor: new ej.WebApiAdaptor() });
          var query = ej.Query()
              .select("OrderID", "CustomerID", "EmployeeID").take(5)
          var execute = dataManager.executeQuery(query) // executing query
                 .done(function (e) {
                     $("#table1 tbody").html($("#tableTemplate").render(e.result));
                 });
      
          $("#table1 tbody").html($("#tableTemplate")
                     .render(dataManager.executeQuery(new ej.Query().take(3))));
      });
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>OrderID}}</td>
          <td>{{>CustomerID}}</td>
          <td>{{>EmployeeID)}}</td>
      </tr>
   </script>
</body>

{% endhighlight %}



Result of the above code example is illustrated as follows.



![](/js/DataManager/Data-Adaptors_images/Data-Adaptors_img4.png) 

## RemoteSave Adaptor

**RemoteSaveAdaptor**, extended from **JsonAdaptor** of **DataManager**, is used for binding local data and performs all **DataManager** queries in client-side. It interacts with server-side only for **CRUD** operations to pass the modified records. Refer to the following code example.


{% highlight html %}

<body>
   <div>
      <div class="row">
         <div class="col-md-3">
            OrderID
         </div>
         <div class="col-md-3">
            <input id="OrderID" class="e-ejinputtext" type="text" value="" />
         </div>
      </div>
      <div class="row">
         <div class="col-md-3">
            Customer ID
         </div>
         <div class="col-md-3">
            <input id="CustomerID" class="e-ejinputtext" type="text" value="" />
         </div>
      </div>
      <div class="row">
         <div class="col-md-3">
            Employee ID
         </div>
         <div class="col-md-3">
            <input id="EmployeeID" class="e-ejinputtext" type="text" value="" />
         </div>
      </div>
      <div class="row">
         <div class="col-md-3">
            <input type="button" value="Change" />
            <input type="button" value="Add" />
            <input type="button" value="Remove" />
         </div>
      </div>
   </div>
   <div class="datatable">
      <table id="table1" class="table table-striped table-bordered" style="width:700px">
         <thead>
            <tr>
               <th>Order ID</th>
               <th>Customer ID</th>
               <th>Employee ID</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script type="text/javascript">
      $(function () {
          var records = [{ OrderID: 10248, CustomerID: "Customer1", EmployeeID: 1 },
                    { OrderID: 10249, CustomerID: "Customer2", EmployeeID: 2 },
                    { OrderID: 10250, CustomerID: "Customer3", EmployeeID: 3 },
                    { OrderID: 10251, CustomerID: "Customer4", EmployeeID: 4 },
                    { OrderID: 10252, CustomerID: "Customer5", EmployeeID: 5 }];
          window.DataManager = ej.DataManager({ json: records, adaptor: new ej.remoteSaveAdaptor(), updateUrl: "Home/Update",insertUrl:"Home/Insert",removeUrl: "Home/Remove", offline:false });
      
          $("#table1 tbody").html($("#tableTemplate").render(window.DataManager.dataSource.json));
      
          $("input:button").ejButton({
              click: function (args) {
                  if (document.activeElement.value == "Change") {
                     var data = window.DataManager.executeLocal(new ej.Query().where("OrderID", ej.FilterOperators.equal, $("#OrderID").val(), 10));
                      if (data.length) {
                          data[0].OrderID = $("#OrderID").val();
                          data[0].CustomerID = $("#CustomerID").val();
                          data[0].EmployeeID = $("#EmployeeID").val();
                          window.DataManager.update("OrderID", data[0]).done(function (e) {
                              $("#table1").find("tbody").empty().html($("#tableTemplate").render(e));
                              window.DataManager.dataSource.json = e;
                              window.changes = null;
                              $(".e-ejinputtext").val("");
                          })
                      }
                  }
                  if (document.activeElement.value == "Add") {
                      var data = {OrderID: $("#OrderID").val(), CustomerID:$("#CustomerID").val(), EmployeeID: $("#EmployeeID").val()};
                          window.DataManager.insert(data).done(function (e) {
                              $("#table1").find("tbody").empty().html($("#tableTemplate").render(e.record));
                              window.DataManager.dataSource.json = e.record;
                              window.changes = null;
                              $(".e-ejinputtext").val("");
                          })
                  }
                  if (document.activeElement.value == "Remove") {
                      var data = $("#OrderID").val();
                      if (data.length) {
                          window.DataManager.remove("OrderID", data).done(function (e) {
                              $("#table1").find("tbody").empty().html($("#tableTemplate").render(e));
                              window.DataManager.dataSource.json = e;
                              window.changes = null;
                              $(".e-ejinputtext").val("");
                          })
                      }       
                  }
              }
          });
      });
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>OrderID}}</td>
          <td>{{>CustomerID}}</td>
          <td>{{>EmployeeID)}}</td>
      </tr>
   </script>
</body>

{% endhighlight %}



{% highlight c# %}

 public class HomeController : Controller
    {
            public static IList<EditableOrder> Data()
            {
                IList<EditableOrder> records = (IList<EditableOrder>)System.Web.HttpContext.Current.Session["Orders"];

                if (records == null)
                {
                    List<EditableOrder> temp = new List<EditableOrder>();
                    for (int i = 1; i <= 5; i++)
                    {
                        var order = new EditableOrder() { OrderID = 10247 + i, CustomerID = "Customer" + i, EmployeeID = i };
                        temp.Add(order);
                    }
                    System.Web.HttpContext.Current.Session["Orders"] = records = temp;
                }
                return records;
            }
       public JsonResult Update(EditableOrder value)
       {

           var record = Data().Where(o => o.OrderID == value.OrderID).FirstOrDefault();
           if (record != null)
           {
               record.OrderID = value.OrderID;
               record.CustomerID = value.CustomerID;
               record.EmployeeID = value.EmployeeID;
           }
           return Json(Data(), JsonRequestBehavior.AllowGet);
       }
        public JsonResult Insert(EditableOrder value)
       {
           Data().Insert(0, value);
           return Json(Data(), JsonRequestBehavior.AllowGet);
       }
        public JsonResult Remove(int key)
        {
            var record = Data().Where(o => o.OrderID == key).FirstOrDefault();
            Data().Remove(record);
            return Json(Data(), JsonRequestBehavior.AllowGet);
        }
    }


{% endhighlight %}



Result of the above code example is illustrated as follows.



![](/js/DataManager/Data-Adaptors_images/Data-Adaptors_img5.png) 



## Custom Adaptor

Custom adaptor is a key technique to customize adaptors in **DataManager**. It is useful to write own adaptor. Normally **ej.Adaptor** is base class for all adaptors. Therefore you first inherit **ej.Adaptor** to develop customized one and then you override functionality in custom adaptor with base class. The following code example illustrates you on how to create custom adaptor.

{% highlight html %}

<body>
   <div class="datatable">
      <table id="table1" class="table table-striped table-bordered" style="width:700px">
         <thead>
            <tr>
               <th>FirstName</th>
               <th>LastName</th>
               <th>Email</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script type="text/javascript">
      $(function () {// Document is ready.
      
          //new custom adaptor implementation
      
          //able to implement more option in custom adaptor other than insert
      
          var customAdaptor = new ej.Adaptor().extend({
      
              insert: function (dm, data) {
      
                  return dm.dataSource.json.push(data);
      
              },
      
              processQuery: ej.JsonAdaptor.prototype.processQuery // reused process query from json adaptor
      
          });
      
          window.gridData = [
      
              { FirstName: "john", LastName: "beckett", Email: "john@syncfusion.com" },
              { FirstName: "ben", LastName: "beckett", Email: "ben@syncfusion.com" },
              { FirstName: "andrew", LastName: "beckett", Email: "andrew@syncfusion.com" }
          ];
      
          var dataManager = new ej.DataManager(window.gridData);
          // assigning custom adaptor to datamanager
      
          dataManager.adaptor = new customAdaptor();
      
          // insert from custom adaptor usage
      
          dataManager.insert({ FirstName: "joel", LastName: "beckett", Email: "joel@syncfusion.com" });
          
      $("#table1 tbody").html($("#tableTemplate")
             .render(dataManager.executeLocal(new ej.Query())));
      });
      
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>FirstName}}</td>
          <td>{{>LastName}}</td>
          <td>{{>Email)}}</td>
      </tr>
   </script>
</body>

{% endhighlight %}

Result of above code example is as follows.

![](/js/DataManager/Data-Adaptors_images/Data-Adaptors_img6.png) 

## Cache Adaptor

Cache Adaptor is used to cache the data of the visited pages. It prevents new requests for the previously visited pages. It can be enabled by using the `enableCaching` property. You can configure cache page size and duration of caching by using `cachingPageSize` and `timeTillExpiration` properties of the [`ej.DataManager`](http://help.syncfusion.com/api/js/ejdatamanager# "DataManager"). 

{% highlight html %}
<div id="CacheGrid"></div

{% endhighlight %}

{% highlight javascript %}
$(function() {

var dataManger = ej.DataManager({ url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/",

enableCaching: true, 

cachingPageSize: 10, 

timeTillExpiration: 120000 }); 

$("#CacheGrid").ejGrid({

dataSource: dataManger, 

allowPaging: true, 

columns: ["OrderID", "CustomerID", "EmployeeID", "Freight", "ShipCity"] }); });

{% endhighlight %}

![](Data-Adaptors_images/Data-Adaptors_img7.png)

N> The unit for timeTillExpiration is in milliseconds <BR>
1000 ms = 1 second.
