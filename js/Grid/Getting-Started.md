---
layout: post
title: Getting started with JavaScript Grid Control | Syncfusion
description: Learn here about getting started with Syncfusion Essential Studio JavaScript Grid control, its elements, and more.
platform: JS
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# Getting started with Javascript Grid

## Preparing HTML document

The grid control has the following list of external JavaScript dependencies. 

* [jQuery](http://jquery.com/) 1.7.1 and later versions
* [jsRender](https://github.com/borismoore/jsrender) - to render the templates

Refer to the internal dependencies in the following table.

<table>
<tr>
<th>
File                          </th><th>
Description/Usage</th></tr>
<tr>
<td>
ej.core.min.js</td><td>
It is referred always before using all the JS controls.</td></tr>
<tr>
<td>
ej.data.min.js</td><td>
Used to handle data operation and is used while binding data to the JS controls.</td></tr>
<tr>
<td>
ej.touch.min.js</td><td>
Used to handle touch operations in touch-enabled devices.</td></tr>
<tr>
<td>
ej.print.min.js</td><td>
Used to handle print operation in JS controls.</td></tr>
<tr>
<td>
ej.globalize.min.js</td><td>
It is referred when using localization in Grid.</td></tr>
<tr>
<td>
ej.draggable.min.js</td><td>
Used for drag and drop an element in JS controls.</td></tr>
<tr>
<td>
ej.grid.min.js</td><td>
The grid's main file.</td></tr>
<tr>
<td>
ej.pager.min.js</td><td>
It is referred when paging is used in the Grid.  </td></tr>
<tr>
<td>
ej.scroller.min.js</td><td>
It is referred when scrolling is used in the Grid.  </td></tr>
<tr>
<td>
ej.waitingpopup.min.js</td><td>
It is referred when the remote data binding is used in the Grid. The waiting popup shows while requesting the server for data.</td></tr>
<tr>
<td>
ej.dropdownlist.min.js</td><td rowspan = "8">
These files are used while enable the Editing and Filtering feature in the Grid.</td></tr>
<tr>
<td>
ej.dialog.min.js</td></tr>
<tr>
<td>
ej.button.min.js</td></tr>
<tr>
<td>
ej.autocomplete.min.js</td></tr>
<tr>
<td>
ej.datepicker.min.js</td></tr>
<tr>
<td>
ej.timepicker.min.js</td></tr>
<tr>
<td>
ej.datetimepicker.min.js</td></tr>
<tr>
<td>
ej.checkbox.min.js</td></tr>
<tr>
<td>
ej.editor.min.js</td></tr>
<tr>
<td>
ej.tooltip.js</td><td rowspan = "2">
It is referred when toolbar is enabled in Grid.</td></tr>
<tr>
<td>
ej.toolbar.min.js</td></tr>
<tr>
<td>
ej.menu.js</td><td>
It is referred when excel like filter menu or context menu is enabled.</td></tr>
<tr>
<td>
ej.radiobutton.js</td><td>
It is referred when filtering is enabled.</td></tr>
<tr>
<td>
ej.excelfilter.js</td><td>
It is referred when excel like filter menu is enabled.</td></tr>
</table>


To get started, you can use the `ej.web.all.min.js` file that encapsulates all the `ej` controls and frameworks in one single file. So, the complete boilerplate code is.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Essential Studio for JavaScript">
    <meta name="author" content="Syncfusion">
    <title></title>
    <!-- Essential Studio for JavaScript  theme reference -->
    <link rel="stylesheet" href="http://cdn.syncfusion.com/13.2.0.29/js/web/flat-azure/ej.web.all.min.css" />

    <!-- Essential Studio for JavaScript  script references -->
    <script src="https://code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.2.0.29/js/web/ej.web.all.min.js"> </script>

    <!-- Add your custom scripts here -->

</head>
<body>

</body>
</html>
{% endhighlight %}



N> In production, we highly recommend you to use our [custom script generator](https://help.syncfusion.com/js/custom-script-generator)  to create custom script file with required controls and its dependencies only. Also, to reduce the file size further please use [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) in your server.

For themes, you can use the `ej.web.all.min.css` CDN link from the code example given. To add the themes in your application, please refer to [this link](https://help.syncfusion.com/js/theming-in-essential-javascript-components).

## Create a Grid

The grid can be created from a HTML `DIV` element with the HTML `id` attribute set to it. To create the grid, you should call the `ejGrid` jQuery plug-in function with the options as parameter. Refer to the following code example.

{% highlight html %}

<div id='Grid'></div>

<script>

    $(function () {
        $('#Grid').ejGrid({
            dataSource: shipDetails
        });
    });

    var shipDetails = [
          { Name: 'Hanari Carnes', City: 'Brazil' },
          { Name: 'Split Rail Beer & Ale', City: 'USA' },
          { Name: 'Ricardo Adocicados', City: 'Brazil' }
    ];

</script>


{% endhighlight %}


![Getting started](Getting-started_images/Getting-started_img1.png)
{:.image }


## Data binding

[`Data binding`](https://help.syncfusion.com/js/grid/data-binding) in the grid is achieved by assigning an array of JavaScript objects to the [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:columns-datasource) property.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
    $(function () {// Document is ready.
        $("#Grid").ejGrid({
        //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
        });
    });
</script>

{% endhighlight %}

![Data binding](Getting-started_images/Getting-started_img2.png)
{:.image }



## Enable Paging

[Paging](https://help.syncfusion.com/js/grid/paging) can be enabled by setting the [`allowPaging`](https://help.syncfusion.com/api/js/ejgrid#members:allowpaging) to true.  This adds the pager in the bottom of the grid and page size can be customized by using the [`pageSettings.pageSize`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-pagesize) property.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
   $(function () {
        $("#Grid").ejGrid({
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window.gridData,
            allowPaging: true,
            pageSettings: { pageSize: 8 },
            columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
       });
   });
</script>
{% endhighlight %}

N> Pager settings can be customized by using the [`pageSettings.pageSize`](https://help.syncfusion.com/api/js/ejgrid#members:pagesettings-pagesize) property. When it is not given by default the values for `pageSize` and `pageCount` are 12 and 8 respectively.


![Paging](Getting-started_images/Getting-started_img3.png)
{:.image }


## Enable Filtering

[`Filtering`](/js/grid/filter) can be enabled by setting the `allowFiltering` as `true`. By default, the filter bar row is displayed to perform filtering, you can change the filter type by using the [`filterSetting.filterType`](https://help.syncfusion.com/api/js/ejgrid#members:filtersettings) property.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
    
    $(function () {
        //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
        $("#Grid").ejGrid({
             dataSource: window.gridData,
             allowPaging: true,
             pageSettings: { pageSize: 8 },
             allowFiltering: true,
             columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
         });
    });
    </script>
{% endhighlight %}

![Filtering](Getting-started_images/Getting-started_img4.png)
{:.image }


## Enable Grouping

[`Grouping`](/js/grid/grouping) can be enabled by setting the [`allowGrouping`](https://help.syncfusion.com/api/js/ejgrid#members:allowgrouping) to `true`.  Columns can be grouped dynamically by drag and drop the grid column header to the group drop area. The initial grouping can be done by adding required column names in the [`groupSettings.groupedColumns`](https://help.syncfusion.com/api/js/ejgrid#members:groupsettings-groupedcolumns) property. 
{% highlight html %}

<div id="Grid"></div>

<script type="text/javascript">
    $(function () {
        //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
        $("#Grid").ejGrid({
            dataSource: window.gridData,
            allowPaging: true,
            pageSettings: { pageSize: 8 },
            allowGrouping: true,
            columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
        });
    });
</script>
{% endhighlight %}

![Grouping](Getting-started_images/Getting-started_img5.png)
{:.image }


Refer to the following code example for initial grouping.
{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
    
    $(function () {
        $("#Grid").ejGrid({
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window.gridData,
            allowPaging: true,
            pageSettings: { pageSize: 8 },
            allowGrouping: true,
            groupSettings: { groupedColumns: ["ShipCountry", "CustomerID"] },
            columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
         });
    });

</script>
{% endhighlight %}

![Initial Grouping](Getting-started_images/Getting-started_img6.png)
{:.image }


## Add Summaries

[`Summaries`](https://help.syncfusion.com/js/grid/summary) can be added by setting the [`showSummary`](https://help.syncfusion.com/api/js/ejgrid#members:showsummary) to true and adding required summary rows and columns in the [`summaryRows`](https://help.syncfusion.com/api/js/ejgrid#members:summaryrows) property. For demonstration, Stock column's sum value is displayed as summary.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
    $(function () {
        $("#Grid").ejGrid({
            //The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
            dataSource: window.gridData,
            allowPaging: true,
            pageSettings: { pageSize: 8 },
            allowGrouping: true,
            groupSettings: { groupedColumns: ["CustomerID"] },
            showSummary: true,
            summaryRows: [
                {
                  	title: "Sum",
                  	summaryColumns: [
                    { summaryType: ej.Grid.SummaryType.Sum, displayColumn: "Freight", dataMember: "Freight" }
              	  ]
              }
           ],
           columns : ["OrderID", "EmployeeID", "CustomerID", "ShipCountry", "Freight"]
        });
    })

</script>
{% endhighlight %}

![Summaries](Getting-started_images/Getting-started_img7.png)
{:.image }




