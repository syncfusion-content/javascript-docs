---
layout: post
title: Data-Binding
description: data binding
platform: js
control: DataManager
documentation: ug
---

# Data Binding

##JSON

A data source can be bound to a table through **JavaScript**. The **DataManager** supports **JSON** array binding. It is useful to bind records in client side using **JSON** data that is very helpful in Single Page Application (SPA) and in feature rich web application. To achieve this, you can refer the following code example.

{% highlight html %}
<body>
   <div class="datatable" style="padding:10px">
      <table id="table1" class="table table-striped table-bordered" style="width:700px">
         <thead>
            <tr>
               <th>Order ID</th>
               <th>Customer ID</th>
               <th>Employee ID</th>
               <th>Frieght</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script type="text/javascript">
      $(function () {
          window.data = [{ OrderID: 10248, CustomerID: "VINET", EmployeeID: 2, Freight: 32.38 },
                          { OrderID: 10249, CustomerID: "AANAR", EmployeeID: 9, Freight: 11.61 },
                          { OrderID: 10250, CustomerID: "VICTE", EmployeeID: 2, Freight: 65.83 },
                          { OrderID: 10251, CustomerID: "TOMSP", EmployeeID: 7, Freight: 70.63 },
                          { OrderID: 10252, CustomerID: "SUPRD", EmployeeID: 9, Freight: 45.45 },
                          ];
          var dataManager = ej.DataManager(data);
          var query = ej.Query();
          var promise = dataManager.executeLocal(query);
          $("#table1 tbody").html($("#tableTemplate").render(promise));
      });
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>OrderID}}</td>
          <td>{{>CustomerID}}</td>
          <td>{{>EmployeeID}}</td>
          <td>{{>Freight}}</td>
      </tr>       
   </script>
</body>

{% endhighlight %}



The result of the above code example is illustrated as follows.



![](/js/DataManager/Data-Binding_images/Data-Binding_img1.png) 

##REST Services

###OData binding

**OData** is standardized protocol for creating and consuming data. You can retrieve data from OData service using **DataManager.** You can refer to the following code example of remote Data binding using OData service.



{% highlight html %}

<body>
   <div class="datatable">
      <table id="table1">
         <thead>
            <tr>
               <th>Item ID</th>
               <th>Item Name</th>
               <th>Item Type</th>
               <th>Price</th>
               <th>Stock</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script type="text/javascript">
      var dataManger = ej.DataManager(
                           "http://mvc.syncfusion.com/Services/Northwnd.svc"
                       );
      
      // Query creation
      var query = ej.Query()
          .from("Foods")
          .select("ItemID", "ItemName", "ItemType", "Price", "Stock").take(7)
      var execute = dataManger.executeQuery(query) // executing query
             .done(function (e) {
                 $("#table1 tbody").html($("#tableTemplate").render(e.result));
             });
      
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>ItemID}}</td>
          <td>{{>ItemName}}</td>
          <td>{{>ItemType)}}</td>
          <td>{{>Price}}</td>
          <td>{{>Stock}}</td>         
      </tr>
   </script>
</body>

{% endhighlight %}



The result of the above code example is illustrated as follows.

![](/js/DataManager/Data-Binding_images/Data-Binding_img2.png) 

##OData V4

The OData v4 is an improved version of OData protocols and the **DataManager** can also retrieve and consume OData v4 services.  For more details on OData v4 Services, refer the [odata documentation](http://www.odata.org/documentation/).

You can refer to the following code example for consuming OData v4 services and bind the result to the simple **HTML** table. In the the following code, `crossDomain` is enabled to make cross domain request.

{% highlight html %}

<body>
   <div class="datatable" style="padding:10px">
      <table id="table1" class="table table-striped table-bordered" style="width:700px" >
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
          var dataManager = ej.DataManager({ url: "http://services.odata.org/V4/Northwind/Northwind.svc/", crossDomain: true });
          var query = new ej.Query().from("Orders").select("OrderID", "CustomerID", "EmployeeID").take(5);
          var promise = dataManager.executeQuery(query);
          promise.done(function (e) {
              $("#table1 tbody").html($("#tableTemplate").render(e.result.value));
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



The request and response to the service from the **DataManager** is illustrated as follows.



![](/js/DataManager/Data-Binding_images/Data-Binding_img3.png) 

 _OData v4 request and response_

The result of the above code example is illustrated as follows.



![](/js/DataManager/Data-Binding_images/Data-Binding_img4.png) 

 _OData v4 binding_

##WebAPI binding

The Web API is a programmatic interface to define the request and response messages system that is mostly exposed in **JSON** or **XML**. The **DataManager** contains default adaptor to handle the Web API request and responses. The **WebApiAdaptor** is discussed briefly in the Adaptor section.

Refer to the following code example for consuming Web API data using ej.DataManager.



{% highlight html %}

<body>
   <div class="datatable" style="padding:10px">
      <table id="table1" class="table table-striped table-bordered" style="width:700px" >
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
          var dataManager = ej.DataManager({ url: "http://mvc.syncfusion.com/UGService/api/Orders", crossDomain: true, adaptor:new ej.WebApiAdaptor() });
          var query = new ej.Query().take(5);
          var promise = dataManager.executeQuery(query);
          promise.done(function (e) {
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



The request to the Web API and response is illustrated as follows.

![](/js/DataManager/Data-Binding_images/Data-Binding_img5.png) 

_Web API adaptor request and response_

The result for the above code example is illustrated as follows.



![](/js/DataManager/Data-Binding_images/Data-Binding_img6.png) 

_Web API data binding_

##Other Web Services binding

The ejDataManager can also retrieve data from **ASP.Net Web** methods and **ASP.Net MVC** Controller`s action. You can achieve this by using the UrlAdaptor of ej.DataManager. The UrlAdaptor is discussed briefly in the adaptor section.  By default, the UrlAdaptor is used when accessing remote data. 

Refer to the following code example to know how the **DataManager** can be used to consume data from the web method.



{% highlight html %}

<asp:Content runat="server" ID="BodyContent" ContentPlaceHolderID="MainContent">
   <div class="datatable" style="padding:10px">
      <table id="table1" class="table table-striped table-bordered" style="width:700px" >
         <thead>
            <tr>
               <th>University Code</th>
               <th>Title</th>
               <th>Course Fees</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
</asp:Content>

<asp:Content runat="server" ID="ScriptContent" ContentPlaceHolderID="ScriptContent">
   <script type="text/javascript">
      $(function () {
          var dataManager = ej.DataManager({ url: "WebService1.asmx/getData" });
          var promise = dataManager.executeQuery(new ej.Query());
          promise.done(function (e) {
              $("#table1 tbody").append($("#tableTemplate").render(e.result));
          });
      });
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>UniversityCode}}</td>
          <td>{{>Title}}</td>
          <td>{{>CourseFees)}}</td>
      </tr>
   </script>
</asp:Content>

{% endhighlight %}


![](/js/DataManager/Data-Binding_images/Data-Binding_img7.png) 

Consuming data from the MVC controller`s action is as follows. Now the data from the action is handled by the UrlAdaptor.



{% highlight html %}

<body>
   <div class=”datatable”>
      <table id=”table1” class=”table table-striped table-bordered” style=”width:700px”>
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
   <script type=”text/javascript”>
      $(function () {
          var dataManager = ej.DataManager({ url: “Home/Data”, adaptor: new ej.UrlAdaptor() });
          var query = ej.Query().take(3);
          var execute = dataManager.executeQuery(query) // executing query
                 .done(function I {
                     $(“#table1 tbody”).html($(“#tableTemplate”).render(e.result));
                 });
      });
   </script>
   <script id=”tableTemplate” type=”text/x-jsrender”>
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
                data.Add(new { OrderID = 10240 + i, CustomerID = “Customer” + i, EmployeeID = i });
            }
            var records = data.Take(dm.Take); // take query of Data Manager
            return Json(records, JsonRequestBehavior.AllowGet);
        }
    }
{% endhighlight %}



The result and the request-response to the controller is illustrated as follows.

![](/js/DataManager/Data-Binding_images/Data-Binding_img8.png) 

##Offline Mode

The offline mode is one of the useful feature of **DataManager** that can be enabled by setting `offline` property of the data manager as **true.** With offline as true, the **DataManager** requests the server only once and further data manipulation operation can be done at client side itself.

In the following code example, the `offline` property of the **DataManager** is set as true.


{% highlight html %}

<div class="datatable">
   <table id="table1" class="table table-striped table-bordered" style="width:700px" >
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
   $(function () {// Document is ready.
       //oData Adaptor with DataManager
       var dataManager = ej.DataManager({
           url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders",
   offline: true
       });
   
       var query = ej.Query().select("OrderID", "CustomerID", "EmployeeID").take(5)
   
       var execute = dataManger.executeQuery(query) // executing query
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

{% endhighlight %}



The result of the above code example is illustrated as follows.



![](/js/DataManager/Data-Binding_images/Data-Binding_img9.png) 

##Load on demand

Load on demand is powerful technique to reduce band width size of consuming data. It allow you to retrieve the required range of data alone from the server and this feature helps you when the server contains large amount of data.

You can use the following code example for implementing load on demand using **DataManager**.


{% highlight html %}

<body>
   <div class="datatable" style="padding:10px">
      <div class="row">
         <div class="col-md-7">
            <table id="table1" class="table table-striped table-bordered" style="width:700px">
               <thead>
                  <tr>
                     <th>OrderID</th>
                     <th>CustomerID</th>
                     <th>EmployeeID</th>
                     <th>Freight</th>
                  </tr>
               </thead>
               <tbody></tbody>
            </table>
         </div>
         <div class="col-md-5">
            <form class="form-horizontal" role="form">
               <div class="form-group">
                  <label class="col-sm-4 control-label">Page Index:</label>
                  <div class="col-sm-8">
                     <input type="text" class="form-control" id="from">
                  </div>
               </div>
               <div class="form-group">
                  <label class="col-sm-4 control-label">Page Size:</label>
                  <div class="col-sm-8">
                     <input type="text" class="form-control" id="to">
                  </div>
               </div>
               <div class="form-group">
                  <div class="col-sm-offset-4 col-sm-4">
                     <button type="button" id="formsubmit" class="btn btn-default">Load data on demand</button>
                  </div>
               </div>
            </form>
         </div>
      </div>
   </div>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>OrderID}}</td>
          <td>{{>CustomerID}}</td>
          <td>{{>EmployeeID}}</td>
          <td>{{>Freight}}</td>
      </tr>
   </script>
   <script>
      $(function () {
          var dataManager = ej.DataManager({ url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders",crossDomain:true });
          var query = ej.Query().page(1, 5), tempQuery;
          var promise = dataManager.executeQuery(query);
          promise.done(function(e) {
              $("#table1 tbody").html($("#tableTemplate").render(e.result));
          });
          $("#formsubmit").click(function (e) {
              var from = parseInt($("#from").val());
              var to = parseInt($("#to").val());
              tempQuery = new ej.Query();
              tempQuery.page(from, to);
              dataManager.executeQuery(tempQuery).done(function (e1) {
                  $("#table1 tbody").html($("#tableTemplate").render(e1.result));
              });
          });
      });
   </script>
</body>

{% endhighlight %}



The result of the above code example is illustrated as follows.

![](/js/DataManager/Data-Binding_images/Data-Binding_img10.png) 

 _Load on demand_

The request and the response for the above code is send as follows.



![](/js/DataManager/Data-Binding_images/Data-Binding_img11.png) 

 _Demanded data_	
 		

##Custom Request Headers

You can add custom request headers using **DataManager** and the headers can be added to the request headers in two ways that is illustrated in the following code example.

You can add custom request headers to every request made by the **DataManager** using the `headers` property. Refer to the following code example for setting the custom request headers using the `headers` property.



{% highlight html %}

<body>
   <div class="datatable" style="padding:10px">
      <table id="table1" class="table table-striped table-bordered" style="width:700px" >
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
          var dataManager = ej.DataManager({ url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders", 
      headers: [{"DataServiceVersion":"1.0","MaxDataServiceVersion":"1.0"}] });
          var query = new ej.Query().take(5);
          var promise = dataManager.executeQuery(query);
          promise.done(function (e) {
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


You can set the custom headers using pre-request callback **beforeSend** as follows. The **setRequestHeader** method can be used to modify the **XMLHTTPRequest**.

{% highlight html %}

<body>
   <div class="datatable" style="padding:10px">
      <table id="table1" class="table table-striped table-bordered" style="width:700px" >
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
          var dataManager = ej.DataManager({ url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders",
              beforeSend: function (dm, request, settings) {
              // some services do not support custom header on crossDomain (CORS) request
                  if (!dm.dataSource.crossDomain) {
                      request.setRequestHeader("DataServiceVersion", "1.0");
                      request.setRequestHeader("MaxDataServiceVersion", "1.0");
                  }
              }});
      
          var query = new ej.Query().take(5);
          var promise = dataManager.executeQuery(query);
          promise.done(function (e) {
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



The above method generates the request header with custom header as follows.

![](/js/DataManager/Data-Binding_images/Data-Binding_img12.png) 

##Cross domain & JSONP

The **DataManager** contains support for creating cross domain request, you can achieve this by using `crossDomain` and `jsonp` property of the **DataManager**. The following code example illustrate on how to create cross domain request. 


{% highlight html %}

<body>
   <div class="datatable" style="padding:10px">
      <table id="table1" class="table table-striped table-bordered" style="width:700px">
         <thead>
            <tr>
               <th>OrderID</th>
               <th>CustomerID</th>
               <th>EmployeeID</th>
               <th>Freight</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>OrderID}}</td>
          <td>{{>CustomerID}}</td>
          <td>{{>EmployeeID}}</td>
          <td>{{>Freight}}</td>
      </tr>
   </script>
   <script>
      $(function () {
          var dataManager = ej.DataManager({ url: "http://services.odata.org/V4/Northwind/Northwind.svc/Orders", crossDomain:true });
          var query = ej.Query().page(1, 5), tempQuery;
          var promise = dataManager.executeQuery(query);
          promise.done(function (e) {
              $("#table1 tbody").html($("#tableTemplate").render(e.result.value));
          });
      
      });
   </script>
</body>

{% endhighlight %}



Result of above code example is illustrated as follows.



![](/js/DataManager/Data-Binding_images/Data-Binding_img13.png) 

##HTML Table

Other than **JSON** and **Remote** datasource, the **DataManager** can also fetch and use data from **HTML** element. You can achieve this by using the **table** property of the **DataManager**. The **DataManager** can fetch data from the **HTML** table element.

Refer to the following code example for the **HTML** element binding using **DataManager**.


{% highlight html %}

<body>
   <div class="datatable" style="padding:10px">
      <table id="datasource" style="display:none">
         <thead>
            <tr>
               <th>OrderID</th>
               <th>EmployeeID</th>
               <th>CustomerID</th>
            </tr>
         </thead>
         <tbody>
            <tr>
               <td>10248</td>
               <td>VINET</td>
               <td>5</td>
            </tr>
            <tr>
               <td>10249</td>
               <td>TOMSP</td>
               <td>6</td>
            </tr>
            <tr>
               <td>10250</td>
               <td>HANAR</td>
               <td>4</td>
            </tr>
            <tr>
               <td>10251</td>
               <td>VICTE</td>
               <td>3</td>
            </tr>
            <tr>
               <td>10252</td>
               <td>SUPRD</td>
               <td>4</td>
            </tr>
         </tbody>
      </table>
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
          var dataManager = ej.DataManager({ table:$("#datasource") });
          var query = new ej.Query();
          var promise = dataManager.executeQuery(query);
          promise.done(function (e) {
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



The result of the above code example is illustrated as follows.


![](/js/DataManager/Data-Binding_images/Data-Binding_img14.png) 
