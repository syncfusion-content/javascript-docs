---
layout: post
title: Getting started | Grid | JavaScript | Syncfusion
description: getting started
platform: JS
control: Grid
documentation: ug
---

# Getting started

##Preparing HTML document

The grid control has the following list of external JavaScript dependencies. 

* [jQuery](http://jquery.com/) 1.7.1 and later versions
* [jsRender](https://github.com/borismoore/jsrender) - to render the templates
* [jQuery.easing](http://gsgd.co.uk/sandbox/jquery/easing/) - to support animation effects in the components
* [jQuery.Globalize](https://github.com/jquery/globalize/tree/v0.1.1) v0.1.1 - to support globalization

And the internal dependencies are tabulated below.

<table>
<tr>
<td>
File                          </td><td>
Description/Usage</td></tr>
<tr>
<td>
ej.core.min.js</td><td>
Must be referred always before using all the JS controls.</td></tr>
<tr>
<td>
ej.data.min.js</td><td>
Used to handle data operation and should be used while binding data to JS controls.</td></tr>
<tr>
<td>
ej.grid.min.js</td><td>
The grid’s main file</td></tr>
<tr>
<td>
ej.pager.min.js</td><td>
Should be referred when using paging in grid.  </td></tr>
<tr>
<td>
ej.scroller.min.js</td><td>
Should be referred when using scrolling in grid.  </td></tr>
<tr>
<td>
ej.waitingpopup.min.js</td><td>
Should be referred when using the remote databinding in grid. The waiting popup will show while requesting the server for data.</td></tr>
<tr>
<td>
ej.gridresize.min.js</td><td>
Should be referred when using the resizing in grid.</td></tr>
<tr>
<td>
ej.dropdownlist.min.js</td><td rowspan = "8">
These files are used while enable Editing and Filtering feature in grid.</td></tr>
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
Should be referred when excel like filter menu is enabled</td></tr>
</table>


For getting started you can use the `ej.web.all.min.js` file, which encapsulates all the `ej` controls and frameworks in one single file. So the complete boilerplate code is

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

    <!-- Add custom scripts here -->

</head>

<body>

</body>

</html>



N> _In production, we highly recommend you to use our_ [custom script generator](http://helpjs.syncfusion.com/js/include-only-the-needed-widgets) _to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use_ [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) in your server_._ 

For themes, you can use the `ej.web.all.min.css` CDN link from the snippet given. To add the themes in your application, please refer [this link](http://help.syncfusion.com/js/theming-in-essential-javascript-components).

## Creating Grid

The grid can be created from a HTML `DIV` element with the HTML `id` attribute set to it. To create the grid, you should call the `ejGrid` jQuery plug-in function with the options as parameter. Code snippet for this is follows.

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





![](Getting-started_images/Getting-started_img1.png)
{:.image }


## Data binding

[`Data binding`](http://helpjs.syncfusion.com/js/grid/data-binding) in grid is achieved using [`ej.DataManager`](http://helpjs.syncfusion.com/js/datamanager/overview) which has support for both RESTful JSON data services binding and local JSON array binding.  To set the data source to grid, the [`dataSource`](http://help.syncfusion.com/js/api/ejgrid#members:columns-datasource) property should be assigned with the instance of `ej.DataManger`. For demonstration purpose [Northwind OData service](http://mvc.syncfusion.com/Services/Northwnd.svc/) is used in this tutorial. The code snippet for this is

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



N> _ ODataAdaptor is the default adaptor for DataManager. On binding to other web services, proper_ [data adaptor](http://helpjs.syncfusion.com/js/datamanager/data-adaptors) needs _to be set on `adaptor` option of DataManager._ 

![](Getting-started_images/Getting-started_img2.png)
{:.image }


## Enable Paging

[Paging](http://helpjs.syncfusion.com/js/grid/paging) can be enabled by setting [`allowPaging`](http://help.syncfusion.com/js/api/ejgrid#members:allowpaging) as true.  This will add the pager in bottom of grid and page size can be customized using [`pageSettings.pageSize`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-pagesize) property

$(function () {

    var dataManager = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");



    $("#Grid").ejGrid({

        dataSource: dataManager,

        allowPaging: true,

        pageSettings: { pageSize: 8 }

    });

});

N> _: Pager settings can be customized using [`pageSettings.pageSize`](http://help.syncfusion.com/js/api/ejgrid#members:pagesettings-pagesize) property. When it is not given the default values for pageSize and pageCount are 12 and 8 respectively.
_![](Getting-started_images/Getting-started_img3.png)
{:.image }


## Enable Filtering

[Filtering](http://helpjs.syncfusion.com/js/grid/filtering) can be enabled by setting `allowFiltering` as `true`. By default filter bar row will be displayed to perform filtering, you can change the filter type using [`filterSetting.filterType`](http://help.syncfusion.com/js/api/ejgrid#members:filtersettings) property.

$(function () {

    var dataManager = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");



    $("#Grid").ejGrid({

        dataSource: dataManager,

        allowPaging: true,

        pageSettings: { pageSize: 8 },

        allowFiltering: true

    });

});

![](Getting-started_images/Getting-started_img4.png)
{:.image }


## Enable Grouping

[`Grouping`](http://helpjs.syncfusion.com/js/grid/grouping) can be enabled by setting [`allowGrouping`](http://help.syncfusion.com/js/api/ejgrid#members:allowgrouping) as `true`.  Columns can be grouped dynamically by drag and drop the grid column header to the group drop area and also initial grouping can be done by adding required column names in [`groupSettings.groupedColumns`](http://help.syncfusion.com/js/api/ejgrid#members:groupsettings-groupedcolumns) property. 

$(function () {

    var dataManager = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");



    $("#Grid").ejGrid({

        dataSource: dataManager,

        allowPaging: true,

        pageSettings: { pageSize: 8 },

        allowGrouping: true

    });

});

![](Getting-started_images/Getting-started_img5.png)
{:.image }


Code Snippet for initial grouping is

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





![](Getting-started_images/Getting-started_img6.png)
{:.image }


## Adding Summaries

[`Summaries`](http://helpjs.syncfusion.com/js/grid/summary) can be added by setting [`showSummary`](http://help.syncfusion.com/js/api/ejgrid#members:showsummary) as true and adding required summary rows and columns in [`summaryRows`](http://help.syncfusion.com/js/api/ejgrid#members:summaryrows) property. For demonstration, Stock column’s `sum` value is display as summary.

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



![](Getting-started_images/Getting-started_img7.png)
{:.image }




