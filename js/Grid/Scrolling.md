---
layout: post
title: Scrolling
description: scrolling
platform: js
control: Grid
documentation: ug
---

# Scrolling

## Default Scrolling

Scrolling is an important feature in **ejGrid**. It makes **Grid** more compatible with layout and design. The **allowScrolling** property is used to enable scrolling functionality to the **ejGrid**. The default value for **allowScrolling** is **false**.

In this following code example, **scrollSettings** property is used to adjust the **Grid** width and height. 

{% highlight html %}


<div id ="Grid">
</div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: ej.DataManager(window.gridData).executeLocal(ej.Query().take(30)),
          allowScrolling: true,
          scrollSettings: { width: 886, height: 300 },
          columns: [
                       { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 100 },
                       { field: "CustomerID", headerText: "Customer ID", width: 100 },
                       { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 100 },
                       { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 100, format: "{0:C}" },
                       { field: "ShipCity", headerText: "Ship City", width: 100 },
                       { field: "ShipName", headerText: "Ship Name", width: 100 },
                       { field: "OrderDate", headerText: "Order Date", textAlign: ej.TextAlign.Right, format: "{0:MM/dd/yyyy}", width: 100 },
                       { field: "ShipCountry", headerText: "Ship Country", width: 100 },
                       { field: "ShipPostalCode", headerText: "Postal Code", textAlign: ej.TextAlign.Right, width: 100 },
                       { field: "Verified", headerText: "Verified", width: 100 }
          ]
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Scrolling_images/Scrolling_img1.png" Caption="Scrolling"%}

## Scroll Settings

The **scrollSettings** contains the properties to enable scrolling related functionalities in the **ejGrid**.

### To Enable Vertical Scrolling

The **height** property in the **scrollSettings** is used to enable the vertical scroll bar in the Grid. The scroll height should be less than the Grid content height. That is, total rows height for enabling vertical scroll bar.

The **height** property can support percentage, pixel and auto values in **scrollSettings**. The default value for height in **scrollSettings** is 0.

The following code example illustrates how to enable vertical scrolling in the **Grid**. 

{% highlight html %}

  
<div id ="Grid">
</div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: ej.DataManager(window.gridData).executeLocal(ej.Query().take(30)),
          allowScrolling: true,
          scrollSettings: { height: 300 },
          columns: [
                       { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 100 },
                       { field: "CustomerID", headerText: "Customer ID", width: 100 },
                       { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 100 },
                       { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 100, format: "{0:C}" },
                       { field: "ShipCity", headerText: "Ship City", width: 100 },
                       { field: "ShipName", headerText: "Ship Name", width: 100 },
                       { field: "OrderDate", headerText: "Order Date", textAlign: ej.TextAlign.Right, format: "{0:MM/dd/yyyy}", width: 100 },
                       { field: "ShipCountry", headerText: "Ship Country", width: 100 },
                       { field: "ShipPostalCode", headerText: "Postal Code", textAlign: ej.TextAlign.Right, width: 100 },
                       { field: "Verified", headerText: "Verified", width: 100 }
          ]
      });
  });
</script>

{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Scrolling_images/Scrolling_img2.png" Caption="Vertical scrolling Grid"%}

### To Enable Horizontal Scrolling

The **width** property in the **scrollSettings** is used to enable the horizontal scroll bar in the **Grid**. The scroll width should be less than the Grid content width. That is, total columns width for enabling horizontal scroll bar.

The **width** property can support percentage, pixel and auto values in **scrollSettings**. The default value for width in **scrollSettings** is **auto**. The default Grid content width is 100%, when you don’t specify the width to the columns it takes its width value from the Grid content.

When you set **width** as **auto,** it renders **Grid** with browser calculate value.

The following code example illustrates how to enable horizontal scrolling in the **Grid**. 

{% highlight html %}

  
 <div id="Grid">
</div>
<script type="text/javascript">
  $(function () {
      $("#Grid").ejGrid({
          // the datasource "window.gridData" is referred from jsondata.min.js
          dataSource: ej.DataManager(window.gridData).executeLocal(ej.Query().take(30)),
          allowScrolling: true,
          scrollSettings: { width: 800 },
          columns: [
                       { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 100 },
                       { field: "CustomerID", headerText: "Customer ID", width: 100 },
                       { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 100 },
                       { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 100, format: "{0:C}" },
                       { field: "ShipCity", headerText: "Ship City", width: 100 },
                       { field: "ShipName", headerText: "Ship Name", width: 100 },
                       { field: "OrderDate", headerText: "Order Date", textAlign: ej.TextAlign.Right, format: "{0:MM/dd/yyyy}", width: 100 },
                       { field: "ShipCountry", headerText: "Ship Country", width: 100 },
                       { field: "ShipPostalCode", headerText: "Postal Code", textAlign: ej.TextAlign.Right, width: 100 },
                       { field: "Verified", headerText: "Verified", width: 100 }
          ]
      });
  });
</script>

{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Scrolling_images/Scrolling_img3.png" Caption="Horizontal scrolling Grid"%}

## Virtual scrolling on demand

Virtual scrolling is powerful technique in **ejGrid**. It makes **Grid** more compatible with layout and its loading record performance is high. The **allowVirtualScrolling** property in **scrollSettings** is used to enable virtual scroll functionality in the **Grid**. The default value for **allowVirtualScrolling** is false.

**Essential JavaScript Grid** supports two mode of virtualization. They are,

* Normal Mode

* Continuous Mode

### Normal Mode

This feature allows you to load the **Grid** with data while scrolling. The following code example illustrates how to set **virtualScrollMode** as Normal.

{% highlight html %}

<div id ="Grid">
</div>
<script>
  $(function () {
      $("#Grid").ejGrid({
          dataSource: ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders"),
          allowScrolling: true,
          scrollSettings: { width: 0, height: 300, allowVirtualScrolling: true, virtualScrollMode: ej.Grid.VirtualScrollMode.Normal },
          columns: [
          { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right },
          { field: "CustomerID", headerText: "Customer ID" },
          { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right },
          { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, format: "{0:C}" },
          { field: "ShipCity", headerText: "Ship City" },
          { field: "ShipName", headerText: "Ship Name" }
          ]
      });
  })
</script>


{% endhighlight %}



The following screenshot displays the Grid while scrolling. The request is sent to the server to fetch data.

{% include image.html url="/js/Grid/Concepts-and-Features/Scrolling_images/Scrolling_img4.png" Caption="Normal mode virtual Scrolling"%}

The following screenshot displays the **Grid** after it is loaded with data.

{% include image.html url="/js/Grid/Concepts-and-Features/Scrolling_images/Scrolling_img5.png" Caption="Grid after loaded with data"%}

### Continuous Mode

You can enable the continuous mode by setting the **virtualScrollMode** property as Continuous. In Continuous mode, the data is loaded in **Grid** when the scrollbar reaches the end. The following code example illustrates how to set the continuous mode in virtualization.

{% highlight html %}


<div id ="Grid">
</div>
<script>
  $(function () {
      $("#Grid").ejGrid({
          dataSource: ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders"),
          allowScrolling: true,
          scrollSettings: { width: 0, height: 300, allowVirtualScrolling: true, virtualScrollMode: ej.Grid.VirtualScrollMode.Continuous },
          columns: [
          { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right },
          { field: "CustomerID", headerText: "Customer ID" },
          { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right },
          { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, format: "{0:C}" },
          { field: "ShipCity", headerText: "Ship City" },
          { field: "ShipName", headerText: "Ship Name" }
          ]
      });
  })
</script>


{% endhighlight %}



The following screenshot illustrates the request made to fetch the data after the **Grid** scrollbar touches the end.

{% include image.html url="/js/Grid/Concepts-and-Features/Scrolling_images/Scrolling_img6.png" Caption="Continuous mode virtual scrolling"%}

The following screenshot illustrates the **Grid** after the data is loaded.

{% include image.html url="/js/Grid/Concepts-and-Features/Scrolling_images/Scrolling_img7.png" Caption="Grid after loaded with data"%}

