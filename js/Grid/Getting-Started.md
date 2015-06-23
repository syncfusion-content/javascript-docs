---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Grid
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Grid** in your application with **JavaScript**.

## Initializing Grid

The **Grid** can be easily configured to the DOM element, such as &lt;div&gt;. You can create a **Grid** with a highly customizable look and feel. You can use the **Grid control** to generate complex **Grid** based reports with rich formatting. In the following example, you can take a look at how the transaction of a product is managed, analysis of a particular sale using filtering and grouping feature. This section explains you about adding group, filter and paging of sales products.

{% include image.html url="/js/Grid/Getting-Started_images/Getting-Started_img1.png"%}


   Create an **HTML** file and add the following references to the required libraries.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta charset="utf-8" />
    <link href="http://cdn.syncfusion.com{{site.releaseversion}}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.js"></script>
    <script src="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>

<body>
</body>

</html>


{% endhighlight %}



 Add a **&lt;div&gt;** element. It is a container for **ejGrid**.

{% highlight html %}


<body>
    <div id="Grid"></div>   
</body>


{% endhighlight %}



 Create the **ejGrid** widget as follows. In Columns definition, the **textAlign** property allows you to align text of the columns, the **width** property allows you to define the width of the columns and **format** property allows you to format the particular columns value.

{% highlight html %}


<head>
  <script type="text/javascript">
    $(function () {
        $("#Grid").ejGrid({            
            columns: [
                { field: "Order", headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
                { field: "CustomerID", headerText: "Customer ID", width: 80 },
                { field: "ShipName", headerText: "Ship Name", width: 100 },
                { field: "ShipCity", headerText: "Ship City", width: 100 },
                { field: "Freight", width: 80, format: "{0:C3}", textAlign: ej.TextAlign.Right }
            ]
        });
    });
  </script>
</head>



{% endhighlight %}



 You can execute the above code example to render an empty **ejGrid** with specified column headers, where the data is specified.

{% include image.html url="/js/Grid/Getting-Started_images/Getting-Started_img2.png"%}

##Set Sales Data

You can pass the data to the **Grid**  either  locally or remotly. Assign the web service **URL** link to the **url** property of the **ejDataManager.** The **crossDomain** property **is enabled to retrieve data from another domain** and **offline** property allows you to load data on time from server.

{% highlight html %}

<head>
  <script type="text/javascript">
    $(function () {
        window.dataManager = ej.DataManager({
        url: "http://mvc.syncfusion.com/UGService/api/Orders",
        crossDomain: true,
        offline:true
    });
    
    $("#Grid").ejGrid({
      dataSource: window.dataManager,
        columns: [
                { field: "OrderID", headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
                { field: "CustomerID", headerText: "Customer ID", width: 80 },
                { field: "ShipName", headerText: "Ship Name", width: 100 },
                { field: "ShipCity", headerText: "Ship City", width: 100 },
                { field: "Freight", width: 80, format: "{0:C3}", textAlign: ej.TextAlign.Right }
        ]
    });
    });
  </script>
</head>

{% endhighlight %}



The following screenshot illustrates a **Grid** with sales data.

{% include image.html url="/js/Grid/Getting-Started_images/Getting-Started_img3.png"%}

##Enable Paging

**Paging** feature in **Grid** provides complete navigation support to easily switch between the pages, using the page bar available at the bottom of the **Grid** control. To enable **paging**, use **allowPaging** property of **Grid** as follows.

{% highlight html %}


<head>
  <script type="text/javascript">
    $(function () {
        window.dataManager = ej.DataManager({
            url: "http://mvc.syncfusion.com/UGService/api/Orders",
            crossDomain: true,
            offline:true
        }); 
    
        $("#Grid").ejGrid({
            dataSource: window.dataManager,
            allowPaging: true,
            columns: [
                    { field: "OrderID", headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
                    { field: "CustomerID", headerText: "Customer ID", width: 80 },
                    { field: "ShipName", headerText: "Ship Name", width: 100 },
                    { field: "ShipCity", headerText: "Ship City", width: 100 },
                    { field: "Freight", width: 80, format: "{0:C3}", textAlign: ej.TextAlign.Right }
           ]
        });
    });
  </script>
</head>

{% endhighlight %}



Use **allowPaging** to switch between pages.

{% include image.html url="/js/Grid/Getting-Started_images/Getting-Started_img4.png"%}

##Enable Filtering

**Filtering** feature in **Grid** is used**to facilitate the extraction of a subset of records that meets certain criteria**. You can apply **Filter** to one or more columns. This feature is used to filter particular sales data to review details.

To enable filtering, use **allowFiltering** property of **Grid** as follows.

{% highlight html %}

<head>
  <script type="text/javascript">
    $(function () {
        window.dataManager = ej.DataManager({
            url: "http://mvc.syncfusion.com/UGService/api/Orders",
            crossDomain: true,
            offline:true
        }); 
    
        $("#Grid").ejGrid({
            dataSource: window.dataManager,
            allowPaging: true,
            allowFiltering: true,
            columns: [
                    { field: "OrderID", headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
                    { field: "CustomerID", headerText: "Customer ID", width: 80 },
                    { field: "ShipName", headerText: "Ship Name", width: 100 },
                    { field: "ShipCity", headerText: "Ship City", width: 100 },
                    { field: "Freight", width: 80, format: "{0:C3}", textAlign: ej.TextAlign.Right }
           ]
        });
    });
  </script>
</head>

{% endhighlight %}



The following screenshot illustrates how to filter the sales data.

{% include image.html url="/js/Grid/Getting-Started_images/Getting-Started_img5.png"%}

##Enable Grouping

The **Grouping** feature in **Grid** is used to consolidate **Grid** data into groups. **Grouping** allows the categorization of records based on specified columns. You can easily group a particular column by simply dragging the column to the upper portion of the **Grid**. The **Grid** data is automatically grouped when you drop a particular column.  In this example, **Grouping** feature is used to analyze the shipment details of products.

To enable grouping, use **allowGrouping** property of **Grid** as follows.

{% highlight html %}

<head>
<script type="text/javascript">
$(function () {
    window.dataManager = ej.DataManager({
        url: "http://mvc.syncfusion.com/UGService/api/Orders",
        crossDomain: true,
        offline:true
    }); 

    $("#Grid").ejGrid({
        dataSource: window.dataManager,
        allowPaging: true,
        allowFiltering: true,
        allowGrouping: true,
        groupSettings: { groupedColumns: ["ShipName"] },
        columns: [
                { field: "OrderID", headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
                { field: "CustomerID", headerText: "Customer ID", width: 80 },
                { field: "ShipName", headerText: "Ship Name", width: 100 },
                { field: "ShipCity", headerText: "Ship City", width: 100 },
                { field: "Freight", width: 80, format: "{0:C3}", textAlign: ej.TextAlign.Right }
       ]
    });
});
</script>
</head>

{% endhighlight %}



The following screenshot shows the analysis of sales data by grouping unit stock.

{% include image.html url="/js/Grid/Getting-Started_images/Getting-Started_img6.png"%}

##Enable Group Summary

**Enable Group Summary** property allows you to summarize the **Grid** data into groups. **Grouping** allows the categorization of records based on specified columns. **Group summary** summarizes the data present in the group. In this example, Group summary is used to summarize freight data of grouped ship name category.

The following code example shows the option to enable group summary.

{% highlight html %}

<head>
<head>
  <script type="text/javascript">
    $(function () {
        window.dataManager = ej.DataManager({
            url: "http://mvc.syncfusion.com/UGService/api/Orders",
            crossDomain: true,
            offline: true
        });
    
        $("#Grid").ejGrid({
            dataSource: window.dataManager,
            allowPaging: true,
            allowFiltering: true,
            allowGrouping: true,
            groupSettings: { groupedColumns: ["ShipName"] },
            showSummary: true,
            columns: [
                    { field: "OrderID", headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
                    { field: "CustomerID", headerText: "Customer ID", width: 80 },
                    { field: "ShipName", headerText: "Ship Name", width: 100 },
                    { field: "ShipCity", headerText: "Ship City", width: 100 },
                    { field: "Freight", width: 80, format: "{0:C3}", textAlign: ej.TextAlign.Right }
            ],
            summaryRows: [{
                showTotalSummary: false,
                summaryColumns: [{
                    summaryType: ej.Grid.SummaryType.Sum,
                    displayColumn: "Freight",
                    prefix: "Sum =",
                    dataMember: "Freight",
                    format: "{0:C3}"
                }]
            }]
        });
    });
  </script>
</head>

{% endhighlight %}



The following screenshot shows the group summary.

{% include image.html url="/js/Grid/Getting-Started_images/Getting-Started_img7.png"%}

