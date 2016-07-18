---
title: Data binding with Spreadsheet widget for Syncfusion Essential JS
description: How to perform Data Binding and configure its properties like dataSource, query etc.
platform: js
control: Spreadsheet
documentation: ug
---
# Data Binding

Spreadsheet can be populated with external datasource using [`dataSource`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-datasource "dataSource") property. The [`dataSource`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-datasource "dataSource") property can be assigned either with the instance of [`ej.DataManager`](http://help.syncfusion.com/js/api/ejdatamanager# "ej.DataManager") or JSON data array collection. Spreadsheet supports three different kinds of Data binding.

* Local Data

* Remote Data

* HTML Table Data

## Local Data


To bind local data to the Spreadsheet, you can assign a JSON array to the [`dataSource`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-datasource "dataSource") property. The following code illustrates how to bind local data to the Spreadsheet

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
$("#Spreadsheet").ejSpreadsheet({                                
sheets: [{
dataSource: window.filterData // JSON
}]
});
});

</script>

{% endhighlight %}

The following output is displayed as a result of the above code snippets.
![](Data-Binding_images/Data-Binding_img1.png)

##  Remote Data

To bind remote data to the Spreadsheet, you can assign a service data as an instance of [`ej.DataManager`](http://help.syncfusion.com/js/api/ejdatamanager# "ej.DataManager") to the [`dataSource`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-datasource "dataSource") property. The following code illustrates how to bind remote data to the Spreadsheet

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
$("#Spreadsheet").ejSpreadsheet({                
sheets: [{
dataSource: ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/"),
query: ej.Query().take(50).select(["OrderID", "CustomerID", "EmployeeID", "ShipName", "ShipAddress"]),                    
primaryKey: "OrderID"
}]
});
});

</script>

{% endhighlight %}

The following output is displayed as a result of the above code snippets.
![](Data-Binding_images/Data-Binding_img2.png)

## HTML Table Data

A HTML Table element can also be used as the data source of Spreadsheet. To use HTML Table as data source, the table element should be passed to [`dataSource`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-datasource "dataSource") property of Spreadsheet as an instance of the [`ej.DataManager`](http://help.syncfusion.com/js/api/ejdatamanager# "ej.DataManager"). The following code illustrates how to bind HTML Table data to the Spreadsheet

{% highlight html %}

<div id="Spreadsheet"></div>
<table id="Table1">
<thead>
<tr>
<th>Laptop</th>
<th>Model</th>
<th>Price</th>
<th>OS</th>
<th>RAM</th>
<th>ScreenSize</th>
</tr>
</thead>
<tbody>
<tr>
<td>Dell Vostro</td>
<td>2520</td>
<td>39990</td>
<td>Windows 8</td>
<td>4GB</td>
<td>15.6</td>
</tr>
<tr>
<td>HP Pavilion Sleekbook</td>
<td>14-B104AU</td>
<td>22800</td>
<td>Windows 8</td>
<td>2GB</td>
<td>14</td>
</tr>
<tr>
<td>Sony Vaio</td>
<td>E14A15</td>
<td>42500</td>
<td>Windows 7 Home Premium</td>
<td>4GB DDR3 RAM</td>
<td>14</td>
</tr>
<tr>
<td>Lenovo</td>
<td>Yoga 13</td>
<td>57000</td>
<td>Windows 8 RT</td>
<td>2GB DDR3 RAM</td>
<td>11.6</td>
</tr>
<tr>
<td>Toshiba</td>
<td>L850-Y3110</td>
<td>57700</td>
<td>Windows 8 SL</td>
<td>8GB DDR3 RAM</td>
<td>15.6</td>
</tr>
</tbody>
</table>

<script>
$(function () {
$("#Spreadsheet").ejSpreadsheet({                
sheets: [{
dataSource: ej.DataManager($("#Table1"))
}]
});
});
</script>

{% endhighlight %}

The following output is displayed as a result of the above code snippets.
![](Data-Binding_images/Data-Binding_img3.png)

## Ways to bind data in Spreadsheet

You can bind data in Spreadsheet with following ways,

* Cell binding

* Range binding 

* Sheet binding 

## Cell Binding

Spreadsheet can bind data for individual cells in a sheet. The data may contain value, style, format, comment and hyperlink. The individual cell properties are listed below,
<table>
<tr>
<td colspan=1 rowspan=1>
Properties<br/></td><td colspan=1 rowspan=1>
Description<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
index<br/></td><td colspan=1 rowspan=1>
To specify particular cell<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
value<br/></td><td colspan=1 rowspan=1>
To specify value. It may be string, integer, formula etc.<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
style<br/></td><td colspan=1 rowspan=1>
To specify style in a cell<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
format<br/></td><td colspan=1 rowspan=1>
To specify number format in a cell<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
comment<br/></td><td colspan=1 rowspan=1>
To specify comment in a cell<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
hyperlink<br/></td><td colspan=1 rowspan=1>
to specify hyperlink in a cell<br/></td></tr>
</table>
The individual row properties are listed below,
<table>
<tr>
<td colspan=1 rowspan=1>
Properties<br/></td><td colspan=1 rowspan=1>
Description<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
index<br/></td><td colspan=1 rowspan=1>
To specify particular row<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
height<br/></td><td colspan=1 rowspan=1>
To specify row height<br/></td></tr>
</table>

You can specify particular row with index property and its height with height property in rows property collection. The following code illustrates cell binding in Spreadsheet

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
$("#Spreadsheet").ejSpreadsheet({               
sheets: [{
rows: [{
height: 30,
cells: [
{ value: "Item Name", style: { "font-weight": "bold", "color": "#FFFFFF", "background-color": "#428bca" } },
{ value: "Quantity", style: { "font-weight": "bold", "color": "#FFFFFF", "background-color": "#428bca" } },
{ value: "Price", style: { "font-weight": "bold", "color": "#FFFFFF", "background-color": "#428bca" } },
{ value: "Amount", style: { "font-weight": "bold", "color": "#FFFFFF", "background-color": "#428bca" } },
{ value: "Stock Detail", style: { "font-weight": "bold", "color": "#FFFFFF", "background-color": "#428bca" } },
{ value: "Website", style: { "font-weight": "bold", "color": "#FFFFFF", "background-color": "#428bca" } }
]
},
{
cells: [
{ value: "Casual Shoes", comment: { value: "Casual Footwears with wide variety of colors." } },                                
{ value: "20", index: 2, format: { type: "currency" } },
{ value: "=B2*C2" },
{ value: "OUT OF STOCK" },
{ value: "Amazon", hyperlink: { webAddr: "www.amazon.com" } }
]
},
{
cells: [
{ value: "Sports Shoes", style: { "background-color": "#E5F3FF" } },
{ value: "20", style: { "background-color": "#E5F3FF" } },
{ value: "30", format: { type: "currency" }, style: { "background-color": "#E5F3FF" } },
{ value: "=B3*C3", style: { "background-color": "#E5F3FF" } },
{ value: "IN STOCK", style: { "background-color": "#E5F3FF" } },
{ value: "AliExpress", hyperlink: { webAddr: "www.aliexpress.com" }, style: { "background-color": "#E5F3FF" } }
]
},
{
cells: [
{ value: "Formal Shoes", comment: { value: "Formal Footwears with wide range of sizes." } },
{ value: "20" },
{ value: "15", format: { type: "currency" } },
{ value: "=B4*C4" },
{ value: "IN STOCK" },
{ value: "Amazon", hyperlink: { webAddr: "www.amazon.com" } }
]
},                    
{
height: 30,
index: 5,
cells: [
{ style: { "background-color": "#428bca" } },
{ style: { "background-color": "#428bca" } },
{ value: "Total Amount", index: 2, style: { "font-weight": "bold", "color": "#FFFFFF", "background-color": "#428bca" } },
{ value: "=Sum(D2:D4)", style: { "font-weight": "bold", "color": "#FFFFFF", "background-color": "#428bca" } },
{ style: { "background-color": "#428bca" } },
{ style: { "background-color": "#428bca" } }
]
}]                            
}]
});
});
</script>

{% endhighlight %}

The following output is displayed as a result of the above code snippets.
![](Data-Binding_images/Data-Binding_img4.png)

## Range Binding

Spreadsheet can bind data for one or more range in a sheet using [`rangeSettings`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-rangesettings "rangeSettings"). The individual range properties are listed below,

<table>
<tr>
<td colspan=1 rowspan=1>
Properties<br/></td><td colspan=1 rowspan=1>
Description<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`dataSource`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-rangesettings-datasource"dataSource")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To specify JSON or ejDataManager<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`query`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-rangesettings-query"query")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To specify query for ejDataManager<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`startCell`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-rangesettings-startcell"startCell")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To specify start cell of a range<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`primarykey`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-rangesettings-primarykey"primarykey")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To specify data source primary key<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`showHeader`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-rangesettings-showheader"showHeader")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To show data source header<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`headerStyles`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-rangesettings-headerstyles"headerStyles")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
to specify header styles<br/></td></tr>
</table>
The following code illustrates range binding in Spreadsheet

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
$("#Spreadsheet").ejSpreadsheet({               
sheets: [{
rangeSettings: [{
dataSource: window.markList, // JSON
startCell: "C2",
showHeader: true,
headerStyles: { "font-weight": "bold" }
}]
}]
});
});
</script>

{% endhighlight %}

The following output is displayed as a result of the above code snippets.
![](Data-Binding_images/Data-Binding_img5.png)

## Sheet Binding

Spreadsheet can bind data for a sheet. The individual sheet properties are listed below,

<table>
<tr>
<td colspan=1 rowspan=1>
Properties<br/></td><td colspan=1 rowspan=1>
Description<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`dataSource`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-datasource"dataSource")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To specify JSON or ejDataManager<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`query`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-query"query")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To specify query for ejDataManager<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`startCell`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-startcell"startCell")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To specify start cell of a range<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`primarykey`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-primarykey"primarykey")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To specify data source primary key<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`showHeader`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-showheader"showHeader")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To show data source header<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`headerStyles`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-headerstyles"headerStyles")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
to specify header styles<br/></td></tr>
<tr>
<td colspan=1 rowspan=1>
{{'[`fieldAsColumnHeader`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-fieldascolumnheader"fieldAsColumnHeader")'| markdownify }}<br/></td><td colspan=1 rowspan=1>
To show data source fields in column header<br/></td></tr>
</table>
The following code illustrates sheet binding in Spreadsheet

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
$("#Spreadsheet").ejSpreadsheet({                
sheets: [{
dataSource: ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/"),
query: ej.Query().take(50).select(["OrderID", "CustomerID", "EmployeeID", "ShipName", "ShipAddress"]),
fieldAsColumnHeader: true,
primaryKey: "OrderID"
}]
});
});
</script>

{% endhighlight %}

The following output is displayed as a result of the above code snippets. 
![](Data-Binding_images/Data-Binding_img6.png)

