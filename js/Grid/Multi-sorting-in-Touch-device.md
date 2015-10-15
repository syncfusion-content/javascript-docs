---
layout: post
title: Multi-sorting-in-Touch-device
description: multi sorting in touch device
platform: js
control: Grid
documentation: ug
---

# Multi sorting in Touch device

While using **Grid** in a touch device environment, you have the option of multi sorting. If you click **Grid** header it shows a popup to enable or disable single click on **Grid** header as multi sorting or simple sorting. If you want to enable multi sorting with a single click then click the sorting symbol in popup.

The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Multi-sorting-in-Touch-device_images/Multi-sorting-in-Touch-device_img1.png"%}

## Multi sorting key configs

In the normal way of sorting, if you want to sort any column, you can click the header cell of that column. For multi sorting, you need to press **ctrl key** plus **mouse left click.**

If you want to clear sorting for a column then you need to use **shift** plus **mouse left click.**

## Clear sorting using API

In **ejGrid**, you have an **API** to clear sorted columns. Through this **API**, you can clear sorting at any stage.

{% highlight html %}

<input type="button" id="clearsorting" name="sorting" value="clear sorting" />
<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          allowMultiSorting: true,
          sortSettings: { sortedColumns: [{ field: "CustomerID", direction: ej.sortOrder.Ascending }, { field: "EmployeeID", direction: ej.sortOrder.Ascending }] },
          allowPaging: true
      });
      $("#clearsorting").ejButton({
          click: function (args) {
              $("#Grid").ejGrid("clearSorting");
          }
      });
  });
  
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Multi-sorting-in-Touch-device_images/Multi-sorting-in-Touch-device_img2.png"%}

{% include image.html url="/js/Grid/Multi-sorting-in-Touch-device_images/Multi-sorting-in-Touch-device_img3.png"%}

## Merge Sort

In the normal way of sorting, first preference is given to capital letters and then small letters. When you do not want discrimination between small and capital letters, you can set `enableLocalizedSort` API as true to sort both small and capital letters.

{% highlight html %}

<!--Sorting with Merge Sort-->

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      ej.support.enableLocalizedSort = true
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          sortSettings: { sortedColumns: [{ field: "CustomerID", direction: ej.sortOrder.Ascending }]},
          allowPaging: true,
          columns: [
                { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 100 },
                { field: "CustomerID", headerText: "Customer ID", width: 130 },
                { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 100, format: "{0:C}" },
                { field: "ShipCountry", headerText: "ShipCountry", width: 100 }
          ]
      });
  });
</script>


<!--MultiSorting with Merge Sort-->

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      ej.support.enableLocalizedSort = true
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          allowMultiSorting: true,
          sortSettings: { sortedColumns: [{ field: "CustomerID", direction: ej.sortOrder.Ascending }] },
          allowPaging: true,
          columns: [
                { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 100 },
                { field: "CustomerID", headerText: "Customer ID", width: 130 },
                { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 100, format: "{0:C}" },
                { field: "ShipCountry", headerText: "ShipCountry", width: 100 }
          ]
      });
  });
  
</script>

{% endhighlight %}



 The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Multi-sorting-in-Touch-device_images/Multi-sorting-in-Touch-device_img4.png"%}

