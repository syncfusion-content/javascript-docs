---
layout: post
title: Columns
description: columns
platform: js
control: Grid
documentation: ug
---

# Columns

Columns are a key feature in **Grid** to define schema in a control based on a datasource. It is useful to map field to datasource values.

## Formatting

**Formatting** is used to convert data values to human readable formats by using specific culture settings. In **ejGrid**, you have an option to format a particular column through the `format` property. For more details about **globalize.js**, refer to the link ([https://github.com/jquery/globalize](https://github.com/jquery/globalize)). The following code example shows you how to use formatting in **Grid**.

{% highlight html %}

 <div id="Grid"></div>
 <script type="text/javascript">
  $(function () {// Document is ready.
      window.data = [];
      for (i = 1; i < 6; i++) {
          window.data.push({ Number: 100 / i, Currency: 100 / i, Date: new Date() });
      }
      $("#Grid").ejGrid({
          // the datasource gets data
          dataSource: window.data,
          columns: [
                  // the formatting columns
              { field: "Number", headerText: "Number", textAlign: ej.TextAlign.Right, format: "{0:n2}", width: 70 },
              { field: "Currency", headerText: "Currency", textAlign: ej.TextAlign.Right, format: "{0:c2}", width: 70 },
              { field: "Date", headerText: "Date", textAlign: ej.TextAlign.Right, format: "{0:MM/dd/yyyy}", width: 70 }
          ],
      });
  
  });
</script>


{% endhighlight %}



The following is the result of column formatting.

{% include image.html url="/js/Grid/Columns_images/Columns_img1.png" %}

## Template

A **template** is used to render a specific template to a particular column using `Template` and `templateID` property. These columns are not bound to **Grid**.

{% highlight html %}


<script type="text/x-jsrender" id="columnTemplate">
  <!--jsrender script-->
  <img style="width:130px;height:100px" src="http://js.syncfusion.com/demos/web/themes/images/Employees//{{:EmployeeID}}.png" alt="{{:EmployeeID}}" />
</script>
<script type="text/javascript">
  $(function () {//Document is ready
      $("#Grid").ejGrid({
          // the datasource "window.employeeView" is referred from jsondata.min.js
          dataSource: window.employeeView,
          allowPaging: true,
          pageSettings: { pageSize: 4 },
          columns: [
          //to enable the Template and templateId loads own template
          { headerText: "EmployeePhoto", template: true, templateID: "#columnTemplate", width: 25, textAlign: ej.TextAlign.Center },
          { field: "EmployeeID", headerText: "EmployeeID", textAlign: ej.TextAlign.Right, width: 20 },
          { field: "FirstName", headerText: "FirstName", textAlign: ej.TextAlign.Left, width: 30 },
          { field: "BirthDate", headerText: "BirthDate", textAlign: ej.TextAlign.Right, width: 30, format: "{0:dd/MM/yy}" }
          ],
      });
  });
</script>

{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Columns_images/Columns_img2.png"%}

## Custom Attribute

**Custom attribute** is a powerful feature of **Columns**. This is used to modify the styles and appearance of a particular column. 

{% highlight html %}

<style>
  .e-rowcell[employeeid = "5"] {
  color: red;
  }
</style>
<div id="Grid"></div>
<script type="text/javascript">
  $(function () {   // Document is ready.
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          pageSettings: { pageSize: 7 },
          columns: [
                        { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 75 },
                        { field: "CustomerID", headerText: "Customer ID", textAlign: ej.TextAlign.Left, width: 90, },
                        { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 90, customAttributes: { "employeeid": "{{:EmployeeID}}" } }, // jsrender syntax usage in custom Attribute
                        { field: "OrderDate", headerText: "Order Date", textAlign: ej.TextAlign.Right, width: 100, format: "{0:MM/dd/yyyy}" },
                        { field: "ShipCountry", headerText: "Ship Country", textAlign: ej.TextAlign.Left, width: 110 }
          ],
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Columns_images/Columns_img3.png"%}

## Read only

`allowEditing` enables you to edit a column, but it prevents the fields from showing it as editable. When you want to make a column as **read-only** then set `allowEditing` as **False for** that column. The following code example shows **Essential JavaScript** column as **read-only**.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {   // Document is ready.
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          pageSettings: { pageSize: 5 },
          editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },
          columns:
              [
                  { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 60 },
          // column read only at while editing
                  { field: "CustomerID", headerText: "Customer ID", textAlign: ej.TextAlign.Left, width: 80, allowEditing: false },
                  { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 60 },
                  { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 60 }
              ]
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Columns_images/Columns_img4.png"%}

## Controlling Grid actions

In **ejGrid**, you can control **Grid** actions through `allowSorting, allowGrouping, allowFiltering`. The following code example shows you how to disable a particular column. The following example has controlled grouping action in **CustomerID** column, filtering in **EmployeeID** column and sorting in **Freight** column.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {  // Document is ready.
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          pageSettings: { pageSize: 5 },
          allowSorting: true,
          allowMultiSorting: true,
          allowFiltering: true,
          allowGrouping: true,
          groupSettings: { groupedColumns: ["OrderID"] },
          columns:
      [
          { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 60 },
          { field: "CustomerID", headerText: "Customer ID", allowGrouping: false, textAlign: ej.TextAlign.Left, width: 80 },
          { field: "EmployeeID", headerText: "Employee ID", allowFiltering: false, textAlign: ej.TextAlign.Right, width: 60 },
          { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Left, allowSorting: false, width: 60 }
      ],
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Columns_images/Columns_img5.png"%}

## Auto-generate column

The columns are automatically generated from the datasource and you do not need specific column declarations. The following code example shows auto-generate column behavior with **Grid**.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          pageSettings: { pageSize: 5 },
  
      });
  });
</script>

{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Columns_images/Columns_img6.png"%}

## Foreign key columns

Foreign key is a field in relational table. It matches the specific key columns of another table. 

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      // the datasource "window.gridData" is referred from jsondata.min.js
      var data = window.gridData;
      $("#Grid").ejGrid({
          dataSource: data,
          allowPaging: true,
          columns: [
                  { field: "OrderID", width: 80, isPrimaryKey: true, textAlign:ej.TextAlign.Right,  },
                  { field: "EmployeeID", foreignKeyField: "EmployeeID", foreignKeyValue: "FirstName", dataSource: window.employeeView, width: 75, headerText: "First Name" ,textAlign:ej.TextAlign.Left} ,
                  { field: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                  { field: "ShipCity", headerText: "Ship City", width: 75 ,  textAlign:ej.TextAlign.Left}
  
          ],
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Columns_images/Columns_img7.png"%}

## Cell Merging

Cell merging feature enables to merge cells based on your requirement. The following code example illustrates Cell Merging. `allowCellMerging` property allowed to enable cell merging feature.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      // Data for grid.
      var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders");
      $("#Grid").ejGrid({
          dataSource:dataManager,
          allowPaging: true,
          allowScrolling: true,
          allowCellMerging: true,
          columns: [ "OrderID", "EmployeeID", "ShipCity", "ShipName", "Freight" ],
          mergeCellInfo: function (args) {
              if (args.column.field == "EmployeeID" && args.data.OrderID == 10248) {
                 args.rowMerge(3);
             }
             else if (args.column.field == "ShipCity" && args.data.OrderID == 10252) {
                 args.colMerge(3);
             }
             else if (args.column.field == "ShipCity" && args.data.OrderID == 10255) {
                 args.merge(0, 3);
             }
         },
      });
  });
</script>

{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/Grid/Columns_images/Columns_img8.png"%}

_Cell Merging_

## AutoWrap Column Cells

AutoWrap feature allows you to wrap cell content to next line when the content exceeds the boundary of the Column cells. Use the following code example for Auto wrap in column cells. `allowTextWrap` property allowed to enable auto wrap feature.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      // Data for grid.
     var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders");
          $("#Grid").ejGrid({
          dataSource:dataManager,
          allowPaging: true,
          allowScrolling: true,
          allowTextWrap: true,
          columns: [ "OrderID", "EmployeeID", "ShipCity", "ShipName", "Freight" ]
      });
  });
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/Grid/Columns_images/Columns_img9.png"%}

## Column Chooser

**Column Chooser** is used to view or hide particular column. To enable column chooser set `showColumnChooser` property as true. Use the following code example to enable column Chooser.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {   
      $("#Grid").ejGrid({
         showColumnChooser: true,
         columns: [ "OrderID","CustomerID", "EmployeeID","Freight","OrderDate" ]
      });
  });
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/Grid/Columns_images/Columns_img10.png"%}

## DisableHtmlEncode

`disableHtmlEncode` property helps you show the encoded **HTML** view of **Grid** content and header elements. 

The following code example shows you how to set `disableHtmlEncode`:

{% highlight html %}

 <div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          allowPaging: true,
          columns: [
             {field:"OrderID", isPrimarykey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right },
             {field:"CustomerID", headerText: "<div>Customer ID</div>", disableHtmlEncode: true },
             {field:"EmployeeID",headerText:"<div>Employee ID</div>" ,textAlign:ej.TextAlign.Right,disableHtmlEncode:true},
             {field:"Freight",headerText:"Freight", textAlign:ej.TextAlign.Right },
             {field:"ShipCountry", headerText: "Ship Country" },
          ]
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Columns_images/Columns_img11.png"%}

## Stacked Header

The **Stacked Header** feature allows additional header rows that span across the grid columns. Columns can be grouped under such headers. You can effectively group extensive data with the help of multilevel **Stacked Headers** as well. Enable the **Stacked Header** by setting the `showStackedHeader` property to **true** and set the stacked header row by using the `stakedHeaderRows` property. The **Stacked Header** feature also supports all other grid features including Grouping, Sorting, Filtering, Reordering, etc. 

{% highlight html %}

<script type="text/javascript">
  $(function () {
      var data = ej.DataManager(window.gridData).executeLocal(ej.Query().take(50));
      $("#Grid").ejGrid({
          dataSource: data,
          allowPaging: true,
          showStackedHeader: true,
          allowReordering: true,
          allowResizing: true,
          stackedHeaderRows: [{
              stackedHeaderColumns: [{ headerText: "Order Details", column: "OrderID,OrderDate,Freight" }
              , { headerText: "Ship Details", column: "ShipCity,ShipCountry" }
              ]
          }
          ],
          columns: ["OrderID", "OrderDate", "Freight", "ShipCity", "ShipCountry"]
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Columns_images/Columns_img12.png" Caption="Stacked Header" % }

{% include image.html url="/js/Grid/Columns_images/Columns_img13.png" Caption="Stacked Header with Grouping support"%}

