---
layout: post
title: Properties,Methods and Events of Essential JS ejDataManager Widget
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejDataManager
<ts  isFrameWork="true" />

Communicates with data source and returns the desired result based on the Query provided.


#### Syntax

{% highlight javascript %}

var dataManager = new ej.DataManager(datasource, query, adaptor)

{% endhighlight %}

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">datasource</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Sets the data source to create the Data Manager.</td>
</tr>
<tr>
<td class="name">query</td>
<td class="type"><span class="param-type">ej.Query</span></td>
<td class="description last">Sets the default query for the data source.</td>
</tr>
<tr>
<td class="name">adaptor</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Configures the adaptor based on the data source type of the Data Manager.</td>
</tr>
</tbody>
</table>

#### Example
{:.example}

{% highlight html %}
<style>
.table,tr,td{ border:1px solid; padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dataManger = ej.DataManager(window.gridData);
var tbody = ""; 
for(var i=0;i<5;i++){ row="dataManger.dataSource.json[0];;" tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td><td>{3}</td><td>{4}</td></tr>"," row.orderid,="" row.customerid,="" row.employeeid,="" row.shipcity,="" row.freight);="" $(".table="" tbody").html(tbody);};=""></5;i++){>{% endhighlight %}
 

## Methods


### executeLocal<span class="signature">(query)</span>
{:#methods:executelocal}

This method does not execute more than one operation at a time; it waits for one operation to complete, and then executes the next operation.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">query</td>
<td class="type"><span class="param-type">ej.Query</span></td>
<td class="description last">Sets the default query for the data source.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Array

#### Example
{:.example}

{% highlight html %}
<style>
.table,tr,td{ border:1px solid; padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().select(["OrderID", "CustomerID", "Freight"]).take(3));
var tbody="";
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].orderid,="" dm[i].customerid,="" dm[i].freight);="" $(".table="" tbody").html(tbody);};=""></3;i++){>{% endhighlight %}


### executeQuery<span class="signature">(query)</span>
{:#methods:executequery}

The executeQuery property is used to process the data based on the query on URL Binding.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">query</td>
<td class="type"><span class="param-type">ej.Query</span></td>
<td class="description last">Sets the default query for the data source.</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

JQueryPromise

#### Example
{:.example}

{% highlight html %}
<script>
var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/");
var query =  ej.Query().select(["OrderID", "CustomerID", "ShipName"]).from("Orders").take(3);
var promise = dataManager.executeQuery(query);
promise.done(function(e){});
promise.fail(function(e){});
</script>{% endhighlight %}


### insert<span class="signature">(data, tableName)</span>
{:#methods:insert}

It is a method used to inserts a new record in the table.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">JSON data or JSON array</td>
</tr>
<tr>
<td class="name">tableName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the table</td>
</tr>
</tbody>
</table>
 
#### Returns:
{:#methods:returns:}

Object
 
#### Example
{:.example}

{% highlight html %}
<div id="before"></div>
<style>
.table,tr,td{ border:1px solid; padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<div id="after"></div>
<table class="table1" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.employeeData);
var local = dm.executeLocal(ej.Query().select(["EmployeeID", "LastName", "FirstName", "Country"]).where("EmployeeID","equal","5"));
$("#before").text("before insert:");
var tbody="";
for(var i=0;i<3;i++){ var="" j="dm.dataSource.json[i];" tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," j.employeeid,="" j.firstname,="" j.lastname,="" j.country);="" $(".table="" tbody").html(tbody);};="" dm.insert(local.shift());="" $("#after").text("after="" insert:");="" tbody="" ;="" for(var="" i=""></3;i++){><4;i++){ var="" j="dm.dataSource.json[i];" tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," j.employeeid,="" j.firstname,="" j.lastname,="" j.country);="" $(".table1="" tbody").html(tbody);};="" </script>=""></4;i++){>{% endhighlight %}
 
 
### remove<span class="signature">(keyField, value, tableName)</span>
{:#methods:remove}

It is used to remove the data from the dataSource.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">keyField</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">keyColumn to find the data</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">specified value for the keyField</td>
</tr>
<tr>
<td class="name">tableName </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the source table</td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Object

#### Example
{:.example}

{% highlight html %}
<div id="before"></div>
<style>
.table,tr,td{ border:1px solid; padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<div id="after"></div>
<table class="table1" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.employeeData);
var local = dm.executeLocal(ej.Query().select(["EmployeeID", "LastName", "FirstName", "Country"]).where("EmployeeID","equal","2"));
$("#before").text("before remove:");
var tbody="";
for(var i=0;i<3;i++){ var="" j="dm.dataSource.json[i];" tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," j.employeeid,="" j.firstname,="" j.lastname,="" j.country);="" $(".table="" tbody").html(tbody);};="" dm.remove("employeeid",local.shift().employeeid);="" $("#after").text("after="" insert:");="" tbody="" ;="" for(var="" i=""></3;i++){><2;i++){ var="" j="dm.dataSource.json[i];" tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," j.employeeid,="" j.firstname,="" j.lastname,="" j.country);="" $(".table1="" tbody").html(tbody);};="" </script>=""></2;i++){>{% endhighlight %}


### saveChanges<span class="signature">(changes, key, tableName)</span>
{:#methods:savechanges}

This method is used to save the changes to the corresponding table. You can add a new record, edit an existing record, or delete a record by using this method.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">changes</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
<tr>
<td class="name">key</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
<tr>
<td class="name">tableName</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Object

#### Example
{:.example}

{% highlight html %}
<style>
.table,tr,td{ border:1px solid; padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var newData = { "added": [{ OrderID: 10248, CustomerID: "VINET", EmployeeID: 25 }], "deleted": {} , "changed":{} };
var data = [{ OrderID: 10249, CustomerID: "AANAR", EmployeeID: 5 },
{ OrderID: 10250, CustomerID: "VINET", EmployeeID: 5 },
{ OrderID: 10251, CustomerID: "SDDER", EmployeeID: 1 }];
var dm = ej.DataManager(window.gridData).saveChanges(newData);
$(function (){});
</script>{% endhighlight %}

 
### update<span class="signature">(keyField, value, tableName)</span>
{:#methods:update}

Updates existing record and saves the changes to the table.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">keyField</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
<tr>
<td class="name">tableName</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>

#### Returns:
{:#methods:returns:}

Object

#### Example
{:.example}

{% highlight html %}
<style>
.table,tr,td{ border:1px solid; padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var first = [{ OrderID: 10248, CustomerID: "VINET", EmployeeID: 2 },
{ OrderID: 10249, CustomerID: "AANAR", EmployeeID: 9 }];
var updateData = {OrderID: 10249, CustomerID: "Test", EmployeeID: 0 };
ej.DataManager(first).update("OrderID", updateData, first);
$(function (){});
</script>{% endhighlight %}