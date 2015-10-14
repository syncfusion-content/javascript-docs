---
layout: post
title: Hierarchical-Query
description: hierarchical query
platform: js
control: DataManager
documentation: ug
---

# Hierarchical Query

The **DataManager** contains support to manage the hierarchical query. The hierarchical queries are commonly required when you use foreign key binding. The hierarchical query can be provided using the **hierarchical** function. This method accepts two parameters such as the query and the selector function. 

##foreignKey

The **foreignkey** method of **ej.Query** can be used to refer another table fields. The foreignkey method accepts one parameter that is the foreign key value. 

The following code example illustrates the hierarchical query and foreignkey method. 


{% highlight html %}

<body>
   <div class="datatable" style="padding:10px">
      <table id="table1" class="table table-striped table-bordered" style="width:700px">
         <thead>
            <tr>
               <th>Order ID</th>
               <th>Customer ID</th>
               <th>Employee ID</th>
               <th>First Name</th>
            </tr>
         </thead>
         <tbody></tbody>
      </table>
   </div>
   <script type="text/javascript">
      $(function () {
      var dataManager = ej.DataManager({ url:"http://mvc.syncfusion.com/Services/Northwnd.svc/" });
          var query = ej.Query()
                 .from("Orders")
                 .search("TM", ["CustomerID", "Employee.FirstName"])
                 .page(1, 4)
                 .hierarchy(
                     ej.Query()
                         .foreignKey("OrderID")
                         .from("Order_Details")
                         .sortBy("Quantity"),
                     function () {
                         // Selective loading of child elements
                         return [10410, 10492, 10949, 10742, 10975]
                     })
                 .select("OrderID", "CustomerID", "EmployeeID", "Employee.FirstName")
                 .expand("Employee");
          var promise = dataManager.executeQuery(query);
          promise.done(function (e) {
              $("#table1 tbody").html($("#tableTemplate").render(e.result));
          });                      
      });
   </script>
   <script id="hierTemplate" type="text/x-jsrender">
      <tr>
          <td class="e-rowcell">{{>ProductID}}</td>
          <td class="e-rowcell">{{>Quantity}}</td>
          <td class="e-rowcell">{{>UnitPrice}}</td>
      </tr>
   </script>
   <script id="tableTemplate" type="text/x-jsrender">
      <tr>
          <td>{{>OrderID}}</td>
          <td>{{>CustomerID}}</td>
          <td>{{>EmployeeID}}</td>
          <td>{{>Employee.FirstName}}</td>
      </tr>
      {{if Order_Details && Order_Details.length}}
      <tr>
          <td colspan="4">
              <table class="table table-striped table-bordered">
                  <caption class="alert-info">Child Table</caption>
                  <thead>
                      <tr>
                          <th>ProductID</th>
                          <th>Quantity</th>
                          <th>Unit Price</th>                            
                      </tr>
                  </thead>
                  <tbody>
                      {{for Order_Details tmpl="#hierTemplate"/}}
                  </tbody>
              </table>
          </td></tr>
              {{/if}}
   </script>
</body>


{% endhighlight %}



The result for the above code example is illustrated as follows.

![]("/js/DataManager/Hierarchical-Query_images/Hierarchical-Query_img1.png") 



