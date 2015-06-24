---
layout: post
title: Selection
description: selection
platform: js
control: Grid
documentation: ug
---

# Selection

The Selection property is used to highlight a row that you select. 

## Types of selection

 There are two types of Selections. 

* Single
* Multiple

Single selection is used to select a single row, cell or column in Grid. In Multiple selection you can select more than one row, cell or column. Refer to the following code examples of Selection types.

### Single Selection

By default, the selection type is “**Single**”.

#### Selection Modes

**Row**

By default, the selection mode of the grid is “**Row**”. This enables you to select the row in the grid. Refer to the following code example. Using `selectionMode` property in `selectionSettings` property to enable row selection.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowSelection: true,
          selectionSettings: { selectionMode: [ej.Grid.SelectionMode.Row] },
          columns: [
                  { field: "OrderID", headerText: "Order ID", width: 75 },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75 },
                  { field: "Freight", width: 75, format: "{0:C}" },
                  { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:dd/MM/yyyy}" },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
          ]
      });
  });
</script>


{% endhighlight %}



The following screenshot displays the result of the above code.

{% include image.html url="/js/Grid/Selection_images/Selection_img1.png"%}

**Cell**

Cell selection can be enabled using the `selectionMode` property. This enables you to select a cell in the grid. Refer to the following code example.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowSelection: true,
          selectionSettings: { selectionMode: [ej.Grid.SelectionMode.Cell] },
          columns: [
                  { field: "OrderID", headerText: "Order ID", width: 75 },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75 },
                  { field: "Freight", width: 75, format: "{0:C}" },
                  { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:dd/MM/yyyy}" },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
          ]
      });
  });
</script>


{% endhighlight %}



The following screenshot displays the result of the above code.

{% include image.html url="/js/Grid/Selection_images/Selection_img2.png"%}

**Column**

Column selection can be enabled using the `selectionMode` property. This enables you to select a particular column in the grid. Refer to the following code example.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowSelection: true,
          selectionSettings: { selectionMode: [ej.Grid.SelectionMode.Column] },
          columns: [
                  { field: "OrderID", headerText: "Order ID", width: 75 },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75 },
                  { field: "Freight", width: 75, format: "{0:C}" },
                  { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:dd/MM/yyyy}" },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
          ]
      });
  });
</script>


{% endhighlight %}



The following screenshot displays the result of the above code.

{% include image.html url="/js/Grid/Selection_images/Selection_img3.png"%}

### Multiple Selection

Multiple selection can be enabled using `selectionType` property. This allows you to select more than one row, cell and column at a time.

#### Selection Modes

**Row**

By default, the selection mode of the grid is “**Row**”. This enable you to select the row in the grid. Refer to the following code example.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowSelection: true,
          //select the multiple records in the grid.
          selectionType: "multiple",   // you can also enable to select single record{selectionType:"single"}
          selectionSettings: { selectionMode: [ej.Grid.SelectionMode.Row] },
          columns: [
                  { field: "OrderID", headerText: "Order ID", width: 75 },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75 },
                  { field: "Freight", width: 75, format: "{0:C}" },
                  { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:dd/MM/yyyy}" },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
          ]
      });
  });
</script>



{% endhighlight %}



The following screenshot displays the result of the above code.

{% include image.html url="/js/Grid/Selection_images/Selection_img4.png"%}

**Cell**

Cell selection can be enabled using the `selectionMode` property. This enables you to select a cell in the grid. Refer to the following code example.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowSelection: true,
          //select the multiple records in the grid.
          selectionType: "multiple",   // you can also enable to select single record{selectionType:"single"}
          selectionSettings: { selectionMode: [ej.Grid.SelectionMode.Cell] },
          columns: [
                  { field: "OrderID", headerText: "Order ID", width: 75 },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75 },
                  { field: "Freight", width: 75, format: "{0:C}" },
                  { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:dd/MM/yyyy}" },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
          ]
      });
  });
</script>



{% endhighlight %}



The following screenshot displays the result of the above code.

{% include image.html url="/js/Grid/Selection_images/Selection_img5.png"%}

**Column**

Column selection can be enabled using the `selectionMode` property. This enables you to select a particular column in the grid. Refer to the following code example.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowSelection: true,
          //select the multiple records in the grid.
          selectionType: "multiple",   // you can also enable to select single record{selectionType:"single"}
          selectionSettings: { selectionMode: [ej.Grid.SelectionMode.Column] },
          columns: [
                  { field: "OrderID", headerText: "Order ID", width: 75 },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75 },
                  { field: "Freight", width: 75, format: "{0:C}" },
                  { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:dd/MM/yyyy}" },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
          ]
      });
  });
</script>



{% endhighlight %}



The following screenshot displays the result of the above code.

{% include image.html url="/js/Grid/Selection_images/Selection_img6.png"%}

## Enable All Modes of selection

You can also enable all the three modes of selection using `selectionMode` property. Refer to the following code example.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowSelection: true,
          selectionSettings: { selectionMode: [ej.Grid.SelectionMode.Row, ej.Grid.SelectionMode.Cell, ej.Grid.SelectionMode.Column] },
          columns: [
                  { field: "OrderID", headerText: "Order ID", width: 75 },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75 },
                  { field: "Freight", width: 75, format: "{0:C}" },
                  { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:dd/MM/yyyy}" },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
          ]
      });
  });
</script>



{% endhighlight %}



The following screenshot displays the result of the above code.

{% include image.html url="/js/Grid/Selection_images/Selection_img7.png"%}

## Enable toggle

You can toggle the selection using the `enableToggle` property. This provides support to toggle selection based on the Boolean value specified to the property. By default the `enableToggle` property is set to disabled. Refer to the following code example.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: window.gridData,
          allowPaging: true,
          allowSelection: true,
          selectionSettings: { selectionMode: [ej.Grid.SelectionMode.Row], enableToggle: true },
          columns: [
                  { field: "OrderID", headerText: "Order ID", width: 75 },
                  { field: "CustomerID", headerText: "Customer ID", width: 80 },
                  { field: "EmployeeID", headerText: "Employee ID", width: 75 },
                  { field: "Freight", width: 75, format: "{0:C}" },
                  { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:dd/MM/yyyy}" },
                  { field: "ShipCity", headerText: "Ship City", width: 110 }
          ]
      });
  });
</script>

{% endhighlight %}



The following screenshot displays the result of the above code.

{%include image.html url="/js/Grid/Selection_images/Selection_img8.png" Caption="select Row"%}

{%include image.html url="/js/Grid/Selection_images/Selection_img9.png" Caption="Unselect Row"%}

## Customize Selection Color

In this section, you can learn how to customize or override selection background color through css. The following code example is for Selection color customization.

{% highlight html %}

<head>
  <style type="text/css">
    .e-grid td.e-active {
    background-color: lightseagreen !important;
    }
  </style>
</head>
<body>
  <div id="Grid"></div>
  <script type="text/javascript">
    $(function () {
        $("#Grid").ejGrid({
            // the datasource "window.gridData" is referred from jsondata.min.js
            dataSource: window.gridData,
            //select the multiple records in the grid.
            selectionType: "multiple",  // you can also enable to select single
            allowPaging: true,
            pageSettings: { pageSize: 8 }
        });
    });
  </script>
</body>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Selection_images/Selection_img10.png"%}

## Get selected record data

In this section, you can learn how to get selected records from one **Grid** and how this selected record is used to update datasource of another **Grid**. 

{% highlight html %}


  <div class="label1">Master Grid </div>
<div id="MasterGrid"></div>
<div class="label1">Detail Grid</div>
<div id="DetailGrid"></div>
<script type="text/javascript">
  $(function () {
      $("#MasterGrid").ejGrid({
          // the datasource "window.employeeData" is referred from templatelocaldata.js
          dataSource: ej.DataManager(window.employeeData).executeLocal(ej.Query().take(5)),
          rowSelected: function (args) {
              var employeeID = args.data.EmployeeID;
              var detaildata = ej.DataManager(window.gridData).executeLocal(ej.Query().where("EmployeeID", ej.FilterOperators.equal, employeeID, false).take(10));
              var gridObj = $("#DetailGrid").ejGrid("instance");
              gridObj.model.dataSource = ej.DataManager(detaildata.slice(0, 5));
              $("#DetailGrid").ejGrid("refreshContent");
          },
      });
  
      $("#DetailGrid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: ej.DataManager(window.gridData).executeLocal(ej.Query().take(10)),
          allowPaging: false
      });
  
      $("#MasterGrid").ejGrid("selectRows", 0);
  
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Selection_images/Selection_img11.png"%}

