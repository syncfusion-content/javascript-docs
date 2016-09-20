---
layout: post
title: Getting started with Grid widget for Syncfusion Essential JS
description: How to create the Grid, data bind, enable paging, grouping, filtering and add summaries
platform: JS
control: Grid
documentation: ug
---
# Getting started

## Adding JavaScript and CSS references

The grid control has the following list of external JavaScript dependencies. 

* [jQuery](http://jquery.com/) 1.7.1 and later versions
* [jsRender](https://github.com/borismoore/jsrender) - to render the templates
* [jQuery.easing](http://gsgd.co.uk/sandbox/jquery/easing/) - to support animation effects in the components

To get started, you can use the `ej.web.all.min.js` file that encapsulates all the `ej` controls and frameworks in one single file. So the complete boilerplate code is

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



N> In production, we highly recommend you to use our [custom script generator](http://helpjs.syncfusion.com/js/custom-script-generator)  to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) in your server.

For themes, you can use the `ej.web.all.min.css` CDN link from the code example given. To add the themes in your application, please refer to [this link](http://help.syncfusion.com/js/theming-in-essential-javascript-components).

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


![](../Getting-started_images/Getting-started_img1.png)
{:.image }


## Data Binding

[`Data Binding`](http://helpjs.syncfusion.com/js/grid/data-binding) in the grid is achieved by using the [`ej.DataManager`](http://helpjs.syncfusion.com/js/datamanager/overview) that supports both RESTful JSON data services binding and local JSON array binding.  To set the data source to the grid, the [`dataSource`](http://help.syncfusion.com/js/api/ejgrid#members:columns-datasource) property is assigned with the instance of the `ej.DataManger`. For demonstration purpose, [Northwind OData service](http://mvc.syncfusion.com/Services/Northwnd.svc/) is used in this tutorial. Refer to the following code example.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
    $(function () {// Document is ready.
        //oData Adaptor with DataManager
        var dataManager = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");
        $("#Grid").ejGrid({
            dataSource: dataManager
        });
    });
</script>

{% endhighlight %}

![](../Getting-started_images/Getting-started_img2.png)
{:.image }


N> ODataAdaptor is the default adaptor for the DataManager. On binding to other web services, proper_ [data adaptor](http://helpjs.syncfusion.com/js/datamanager/data-adaptors) needs _to be set on `adaptor` option of the DataManager.


## Enable Paging

[Paging](http://helpjs.syncfusion.com/js/grid/paging) can be enabled by setting the [`allowPaging`](http://help.syncfusion.com/js/api/ejgrid#members:allowpaging) to true.  This adds the pager in the bottom of the grid and page size can be customized by using the [`pageSettings.pageSize`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-pagesize) property

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
   $(function () {
        var dataManager = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");
        $("#Grid").ejGrid({
            dataSource: dataManager,
            allowPaging: true,
            pageSettings: { pageSize: 8 }
       });
   });
</script>
{% endhighlight %}

N> Pager settings can be customized by using the [`pageSettings.pageSize`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-pagesize) property. When it is not given the default values for `pageSize` and `pageCount` are 12 and 8 respectively.


![](../Getting-started_images/Getting-started_img3.png)
{:.image }


## Enable Filtering

[`Filtering`](/js/grid/filter) can be enabled by setting the `allowFiltering` to `true`. By default, the filter bar row is displayed to perform filtering, you can change the filter type by using the [`filterSetting.filterType`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings) property.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
    
    $(function () {
        var dataManager = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");
        $("#Grid").ejGrid({
             dataSource: dataManager,
             allowPaging: true,
             pageSettings: { pageSize: 8 },
             allowFiltering: true
         });
    });
    </script>
{% endhighlight %}

![](../Getting-started_images/Getting-started_img4.png)
{:.image }


## Enable Grouping

[`Grouping`](/js/grid/grouping) can be enabled by setting the [`allowGrouping`](http://help.syncfusion.com/js/api/ejgrid#members:allowgrouping) to `true`.  Columns can be grouped dynamically by drag and drop the grid column header to the group drop area. The initial grouping can be done by adding required column names in the [`groupSettings.groupedColumns`](http://help.syncfusion.com/js/api/ejgrid#members:groupsettings-groupedcolumns) property. 
{% highlight html %}

<div id="Grid"></div>

<script type="text/javascript">
    $(function () {
        var dataManager = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");
        $("#Grid").ejGrid({
            dataSource: dataManager,
            allowPaging: true,
            pageSettings: { pageSize: 8 },
            allowGrouping: true
        });
    });
</script>
{% endhighlight %}

![](../Getting-started_images/Getting-started_img5.png)
{:.image }


Refer to the following code example for initial grouping.
{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
    
    $(function () {
      var dataManager = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");
        $("#Grid").ejGrid({
            dataSource: dataManager,
            allowPaging: true,
            pageSettings: { pageSize: 8 },
            allowGrouping: true,
            groupSettings: { groupedColumns: ["ItemType"] }
         });
    });

</script>
{% endhighlight %}

![](../Getting-started_images/Getting-started_img6.png)
{:.image }


## Add Summaries

[`Summaries`](http://helpjs.syncfusion.com/js/grid/summary) can be added by setting the [`showSummary`](http://help.syncfusion.com/js/api/ejgrid#members:showsummary) to true and adding required summary rows and columns in the [`summaryRows`](http://help.syncfusion.com/js/api/ejgrid#members:summaryrows) property. For demonstration, Stock column's sum value is displayed as summary.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
    $(function () {
        var dataManager = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");
        $("#Grid").ejGrid({
            dataSource: dataManager,
            allowPaging: true,
            pageSettings: { pageSize: 8 },
            allowGrouping: true,
            groupSettings: { groupedColumns: ["ItemType"] },
            showSummary: true,
            summaryRows: [
                {
                  	title: "Sum",
                  	summaryColumns: [
                    { summaryType: ej.Grid.SummaryType.Sum, displayColumn: "Stock", dataMember: "Stock" }
              	  ]
              }
           ]
        });
    })

</script>
{% endhighlight %}

![](../Getting-started_images/Getting-started_img7.png)
{:.image }

## Internal Dependency Scripts

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
ej.gridresize.min.js</td><td>
It is referred when resizing is used in the Grid.</td></tr>
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
ej.datetimepicker.min.js</td></tr>
<tr>
<td>
ej.checkbox.min.js</td></tr>
<tr>
<td>
ej.editor.min.js</td></tr>
<tr>
<td>
ej.excelfilter.js</td><td>
It is referred when excel like filter menu is enabled.</td></tr>
<tr>
<td>
ej.globalize.min.js</td><td>
It is referred when using localization in Grid.</td></tr>
</table>


