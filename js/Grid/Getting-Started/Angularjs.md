---
layout: post
title: Getting started with Grid widget for Syncfusion Essential AngularJS
description: How to create the Grid, data bind, enable paging, grouping, filtering and add summaries
platform: JS
control: Grid
documentation: ug
---
# Getting started

Before we start with the Grid, please refer [this page] ([http://help.syncfusion.com/js/angularjs](http://help.syncfusion.com/js/angularjs# "")) for general information regarding integrating Syncfusion widget's.

## Preparing HTML document

The Grid control has the following list of external JavaScript dependencies.

* [jQuery]([http://jquery.com/](http://jquery.com/# "")) 1.7.1 and later versions

* [jsRender]([https://github.com/borismoore/jsrender](https://github.com/borismoore/jsrender# "")) - to render the templates

* [jQuery.easing]([http://gsgd.co.uk/sandbox/jquery/easing/](http://gsgd.co.uk/sandbox/jquery/easing/# "")) - to support animation effects in the                        components

To get started, you can use the `ej.web.all.min.js` file that encapsulates all the `ej` controls and frameworks in one single file. Also use the `ej.widget.angular.min.js` script file that encapsulates the angular directives for our controls. So the complete boilerplate code is

<table>
<tr>
<td>
<!DOCTYPE html><br/><br/><html><br/><br/><head><br/><br/><meta name="viewport" content="width=device-width, initial-scale=1.0"><br/><br/><meta name="description" content="Essential Studio for JavaScript"><br/><br/><meta name="author" content="Syncfusion"><br/><br/><title></title><br/><br/><!-- Essential Studio for JavaScript  theme reference --><br/><br/><link rel="stylesheet" href="http://cdn.syncfusion.com/13.4.0.53/js/web/flat-azure/ej.web.all.min.css" /><br/><br/><!-- Essential Studio for JavaScript  script references --><br/><br/><script src="https://code.jquery.com/jquery-1.10.2.min.js"></script><br/><br/><script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script><br/><br/>src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script><br/><br/><script src="http://cdn.syncfusion.com/13.4.0.53/js/web/ej.web.all.min.js"> </script><br/><br/><script src="http://cdn.syncfusion.com/13.4.0.53/js/web/ej.widget.angular.min.js"> </script><br/><br/><!-- Add your custom scripts here --><br/><br/></head><br/><br/><body><br/><br/></body><br/><br/></html><br/><br/></td></tr>
</table>
N> In production, we highly recommend you to use our [custom script generator]([http://helpjs.syncfusion.com/js/include-only-the-needed-widgets](http://helpjs.syncfusion.com/js/include-only-the-needed-widgets# ""))  to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip compression]([https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en# "")) in your server.

For themes, you can use the `ej.web.all.min.css` CDN link from the code example given. To add the themes in your application, please refer to [this link]([http://help.syncfusion.com/js/theming-in-essential-javascript-components](http://help.syncfusion.com/js/theming-in-essential-javascript-components# "")).

## Create a Grid

All the Essential JavaScript directives have been encapsulated into a single module called `ejangular` so the first step would be to declare dependency for this module within your AngularJS application. 

The grid can be created using `ej-grid` angular directive and its properties can be defined using `e-` prefix followed by the property name. 

The code example for defining controls in AngularJS is as follows,

<table>
<tr>
<td>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" ng-app="listCtrl"><br/><br/><head><br/><br/><title>Essential Studio for AngularJS: Flat Grid</title><br/><br/></head><br/><br/><body ng-controller="GridCreationCtrl"><br/><br/><div id="Grid" ej-grid e-datasource="shipdetails" ><br/><br/></div><br/><br/><script><br/><br/>angular.module('listCtrl', ['ejangular'])<br/><br/>.controller('GridCreationCtrl', function ($scope) {<br/><br/>$scope.shipdetails = [<br/><br/>{ Name: 'Hanari Carnes', City: 'Brazil' },<br/><br/>{ Name: 'Split Rail Beer & Ale', City: 'USA' },<br/><br/>{ Name: 'Ricardo Adocicados', City: 'Brazil' }<br/><br/>];<br/><br/>});<br/><br/></script><br/><br/></body><br/><br/></html><br/><br/><br/><br/></td></tr>
</table>

![](Getting-started_images/Angularimages/Getting-started_img1.png)
{:.image }

In the above code snippet, `ej-grid` denotes the control directive for the Syncfusion’s Grid angular widget and all its properties are prefixed with the letter `e-` (For example, e-datasource).

## Data Binding

`Data binding` in the grid is achieved by using the [`ej.DataManager`] ([http://helpjs.syncfusion.com/js/datamanager/overview](http://helpjs.syncfusion.com/js/datamanager/overview# "")) that supports both RESTful JSON data services binding and local JSON array binding.  To set the data source to the grid, the `e-datasource` property is assigned with the instance of the `ej.DataManger`. For demonstration purpose, [Northwind OData service]([http://mvc.syncfusion.com/Services/Northwnd.svc/](http://mvc.syncfusion.com/Services/Northwnd.svc/# "")) is used in this tutorial. Refer to the following code example.

<table>
<tr>
<td>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" ng-app="listCtrl"><br/><br/><head><br/><br/><title>Essential Studio for AngularJS: Flat Grid</title><br/><br/></head><br/><br/><body ng-controller="DataBindingCtrl"><br/><br/><div id="Grid" ej-grid e-datasource="data" e-allowpaging="true"><br/><br/></div><br/><br/><script><br/><br/>angular.module('listCtrl', ['ejangular'])<br/><br/>.controller('DataBindingCtrl', function ($scope) {<br/><br/>$scope.data = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");<br/><br/>});<br/><br/></script><br/><br/></body><br/><br/></html><br/><br/><br/><br/></td></tr>
</table>

![](Getting-started_images/Angularimages/Getting-started_img2.png)
{:.image }


N> ODataAdaptor is the default adaptor for the DataManager. On binding to other web services, proper [data adaptor]([http://helpjs.syncfusion.com/js/datamanager/data-adaptors](http://helpjs.syncfusion.com/js/datamanager/data-adaptors# "")) needs to be set on `adaptor` option of the DataManager.

## Enable Paging

`Paging` can be enabled by setting the `e-allowpaging` to `true`. This adds the pager in the bottom of the grid and page size can be customized by using the `e-pagesettings-pagesize` attribute.

<table>
<tr>
<td>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" ng-app="listCtrl"><br/><br/><head><br/><br/><title>Essential Studio for AngularJS: Flat Grid</title><br/><br/></head><br/><br/><body ng-controller="PagingCtrl"><br/><br/><div id="Grid" ej-grid e-datasource="data" e-allowpaging="true" e-pagesettings="pageset"><br/><br/></div><br/><br/><script><br/><br/>angular.module('listCtrl', ['ejangular'])<br/><br/>.controller('PagingCtrl', function ($scope) {<br/><br/>$scope.data = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");;<br/><br/>$scope.pageset = { pageSize: 8 };<br/><br/>});<br/><br/></script><br/><br/></body><br/><br/></html><br/><br/><br/><br/></td></tr>
</table>
N> _1.Pager settings can be customized by using the `e-pagesettings-pagesize` property. When it is not given the default values for `pageSize` and `pageCount` are 12 and 8 respectively.

2. The array properties of Syncfusion widget's in angularjs has to be defined by using the scope variable.



![](Getting-started_images/Angularimages/Getting-started_img3.png)
{:.image }



## Enable Filtering

`Filtering` can be enabled by setting the `e-allowfiltering` to `true`. By default, the filter bar row is displayed to perform filtering, you can change the filter type by using the `e-filtersettings-filterType` attribute.

<table>
<tr>
<td>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" ng-app="listCtrl"><br/><br/><head><br/><br/><title>Essential Studio for AngularJS: Flat Grid</title><br/><br/></head><br/><br/><body ng-controller="FilteringCtrl"><br/><br/><div id="Grid" ej-grid e-datasource="data" e-allowpaging="true" e-pagesettings-pagesize="8" e-allowfiltering="true" }><br/><br/></div><br/><br/><script><br/><br/>angular.module('listCtrl', ['ejangular'])<br/><br/>.controller('FilteringCtrl', function ($scope) {<br/><br/>$scope.data = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");<br/><br/>});<br/><br/></script><br/><br/></body><br/><br/></html><br/><br/></td></tr>
</table>
![](Getting-started_images/Angularimages/Getting-started_img4.png)
{:.image }

## Enable Grouping

`Grouping` can be enabled by setting the `e-allowgrouping` to `true`. Columns can be grouped dynamically by drag and drop the grid column header to the group drop area. The initial grouping can be done by adding required column names in the `e-groupsettings-groupedcolumns` attribute. 

<table>
<tr>
<td>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" ng-app="listCtrl"><br/><br/><head><br/><br/><title>Essential Studio for AngularJS: Flat Grid</title><br/><br/></head><br/><br/><body ng-controller="GroupingCtrl"><br/><br/><div id="Grid" ej-grid e-datasource="data" e-allowpaging="true" e-pagesettings-pagesize="8" e-allowgrouping="true" }><br/><br/></div><br/><br/><script><br/><br/>angular.module('listCtrl', ['ejangular'])<br/><br/>.controller('GroupingCtrl', function ($scope) {<br/><br/>$scope.data = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");<br/><br/>});<br/><br/></script><br/><br/></body><br/><br/></html><br/><br/><br/><br/></td></tr>
</table>
![](Getting-started_images/Angularimages/Getting-started_img5.png)
{:.image }

Refer to the following code example for initial grouping.

<table>
<tr>
<td>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" ng-app="listCtrl"><br/><br/><head><br/><br/><title>Essential Studio for AngularJS: Flat Grid</title><br/><br/></head><br/><br/><body ng-controller="GroupingCtrl"><br/><br/><div id="Grid" ej-grid e-datasource="data" e-allowpaging="true" e-pagesettings-pagesize="8" e-allowgrouping="true" e-groupsettings="grouping"><br/><br/></div><br/><br/><script><br/><br/>angular.module('listCtrl', ['ejangular'])<br/><br/>.controller('GroupingCtrl', function ($scope) {<br/><br/>$scope.data = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");<br/><br/>$scope.grouping = { groupedColumns: ["ItemType"] };<br/><br/>});<br/><br/></script><br/><br/></body><br/><br/></html><br/><br/><br/><br/></td></tr>
</table>
![](Getting-started_images/Angularimages/Getting-started_img6.png)
{:.image }

## Add Summaries

`Summaries` can be added by setting the `e-showsummary` to true and adding required summary rows and columns in the `e-summaryrows` property. We can set value for `e-summaryrows` and that value can be accessed through $scope variable. For demonstration, Stock column's sum value is displayed as summary.

<table>
<tr>
<td>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" ng-app="listCtrl"><br/><br/><head><br/><br/><title>Essential Studio for AngularJS: Flat Grid</title><br/><br/></head><br/><br/><body ng-controller="SummaryCtrl"><br/><br/><div id="Grid" ej-grid e-datasource="data" e-allowpaging="true" e-pagesettings-pagesize="8" e-allowgrouping="true" e-groupsettings="grouping" e-showsummary="true" e-summaryrows="summaryRows"><br/><br/></div><br/><br/><script><br/><br/>angular.module('listCtrl', ['ejangular'])<br/><br/>.controller('SummaryCtrl', function ($scope) {<br/><br/>$scope.data = new ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Foods");;<br/><br/>$scope.grouping = { groupedColumns: ["ItemType"] };<br/><br/>$scope.summaryRows = [<br/><br/>{ title: "Sum", summaryColumns: [{ summaryType: ej.Grid.SummaryType.Sum, displayColumn: "Stock", dataMember: "Stock" }] },<br/><br/>];<br/><br/>});<br/><br/></script><br/><br/></body><br/><br/></html><br/><br/><br/><br/></td></tr>
</table>
![](Getting-started_images/Angularimages/Getting-started_img7.png)
{:.image }


