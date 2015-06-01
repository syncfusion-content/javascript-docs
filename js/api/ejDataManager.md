---
layout: post
title: ejDataManager
documentation: API
platform: js
metaname: 
metacontent: 
---

Communicates with data source and returns the desired result based on the Query provided.










#### $(element).ejDataManager<span class="signature">(datasource, query, adaptor)</span>







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
<td class="name"><code>datasource</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Sets the data source to create the Data Manager.</td>
</tr>
<tr>
<td class="name"><code>query</code></td>
<td class="type"><span class="param-type">ej.Query</span></td>
<td class="description last">Sets the default query for the data source.</td>
</tr>
<tr>
<td class="name"><code>adaptor</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Configures the adaptor based on the data source type of the Data Manager.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;style&gt;
.table,tr,td{ border:1px solid; padding:3px;}
&lt;/style&gt;
&lt;table class="table" style="border-collapse:collapse"&gt;
&lt;tbody&gt;&lt;/tbody&gt;
&lt;/table&gt;
&lt;script&gt;
var dataManger = ej.DataManager(window.gridData);
var tbody = ""; 
for(var i=0;i&lt;5;i++){ row="dataManger.dataSource.json[0];;" tbody="" +="String.format("&lt;tr&gt;&lt;td&gt;{0}&lt;/td&gt;&lt;td&gt;{1}&lt;/td&gt;&lt;td&gt;{2}&lt;/td&gt;&lt;td&gt;{3}&lt;/td&gt;&lt;td&gt;{4}&lt;/td&gt;&lt;/tr&gt;"," row.orderid,="" row.customerid,="" row.employeeid,="" row.shipcity,="" row.freight);="" $(".table="" tbody").html(tbody);};=""&gt;&lt;/5;i++){&gt;</code>
</pre>






### Methods








#### excuteLocal<span class="signature">(query)</span>








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
<td class="name"><code>query</code></td>
<td class="type"><span class="param-type">ej.Query</span></td>
<td class="description last">Sets the default query for the data source.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;style&gt;
.table,tr,td{ border:1px solid; padding:3px;}
&lt;/style&gt;
&lt;table class="table" style="border-collapse:collapse"&gt;
&lt;tbody&gt;&lt;/tbody&gt;
&lt;/table&gt;
&lt;script&gt;
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().select(["OrderID", "CustomerID", "Freight"]).take(3));
var tbody="";
for(var i=0;i&lt;3;i++){ tbody="" +="String.format("&lt;tr&gt;&lt;td&gt;{0}&lt;/td&gt;&lt;td&gt;{1}&lt;/td&gt;&lt;td&gt;{2}&lt;/td&gt;&lt;/tr&gt;"," dm[i].orderid,="" dm[i].customerid,="" dm[i].freight);="" $(".table="" tbody").html(tbody);};=""&gt;&lt;/3;i++){&gt;</code>
</pre>






#### excuteQuery<span class="signature">(query)</span>








The executeQuery property is used to process the data based on the query on Url Binding.

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
<td class="name"><code>query</code></td>
<td class="type"><span class="param-type">ej.Query</span></td>
<td class="description last">Sets the default query for the data source.</td>
</tr>
</tbody>
</table>




##### Returns:

result of each operation will be handled once the result is available.


##### Example

<pre class="prettyprint">
<code>&lt;script&gt;
var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/");
var query =  ej.Query().select(["OrderID", "CustomerID", "ShipName"]).from("Orders").take(3);
var promise = dataManager.executeQuery(query);
promise.done(function(e){}); 
&lt;/script&gt;</code>
</pre>






#### insert<span class="signature">(data, tableName)</span>








It is a method used to inserts a new record in the table..

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
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">json data or json array</td>
</tr>
<tr>
<td class="name"><code>tableName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the table</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="before"&gt;&lt;/div&gt;
&lt;style&gt;
.table,tr,td{ border:1px solid; padding:3px;}
&lt;/style&gt;
&lt;table class="table" style="border-collapse:collapse"&gt;
&lt;tbody&gt;&lt;/tbody&gt;
&lt;/table&gt;
&lt;div id="after"&gt;&lt;/div&gt;
&lt;table class="table1" style="border-collapse:collapse"&gt;
&lt;tbody&gt;&lt;/tbody&gt;
&lt;/table&gt;
&lt;script&gt;
var dm = ej.DataManager(window.employeeData);
var local = dm.executeLocal(ej.Query().select(["EmployeeID", "LastName", "FirstName", "Country"]).where("EmployeeID","equal","5"));
$("#before").text("before insert:");
var tbody="";
for(var i=0;i&lt;3;i++){ var="" j="dm.dataSource.json[i];" tbody="" +="String.format("&lt;tr&gt;&lt;td&gt;{0}&lt;/td&gt;&lt;td&gt;{1}&lt;/td&gt;&lt;td&gt;{2}&lt;/td&gt;&lt;/tr&gt;"," j.employeeid,="" j.firstname,="" j.lastname,="" j.country);="" $(".table="" tbody").html(tbody);};="" dm.insert(local.shift());="" $("#after").text("after="" insert:");="" tbody="" ;="" for(var="" i=""&gt;&lt;/3;i++){&gt;&lt;4;i++){ var="" j="dm.dataSource.json[i];" tbody="" +="String.format("&lt;tr&gt;&lt;td&gt;{0}&lt;/td&gt;&lt;td&gt;{1}&lt;/td&gt;&lt;td&gt;{2}&lt;/td&gt;&lt;/tr&gt;"," j.employeeid,="" j.firstname,="" j.lastname,="" j.country);="" $(".table1="" tbody").html(tbody);};="" &lt;/script&gt;=""&gt;&lt;/4;i++){&gt;</code>
</pre>






#### remove<span class="signature">(keyField, value, tableName)</span>








It is used to remove the data from the dataSource

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
<td class="name"><code>keyField</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">keyColumn to find the data</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">specified value for the keyField</td>
</tr>
<tr>
<td class="name"><code>tableName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the source table</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="before"&gt;&lt;/div&gt;
&lt;style&gt;
.table,tr,td{ border:1px solid; padding:3px;}
&lt;/style&gt;
&lt;table class="table" style="border-collapse:collapse"&gt;
&lt;tbody&gt;&lt;/tbody&gt;
&lt;/table&gt;
&lt;div id="after"&gt;&lt;/div&gt;
&lt;table class="table1" style="border-collapse:collapse"&gt;
&lt;tbody&gt;&lt;/tbody&gt;
&lt;/table&gt;
&lt;script&gt;
var dm = ej.DataManager(window.employeeData);
var local = dm.executeLocal(ej.Query().select(["EmployeeID", "LastName", "FirstName", "Country"]).where("EmployeeID","equal","2"));
$("#before").text("before remove:");
var tbody="";
for(var i=0;i&lt;3;i++){ var="" j="dm.dataSource.json[i];" tbody="" +="String.format("&lt;tr&gt;&lt;td&gt;{0}&lt;/td&gt;&lt;td&gt;{1}&lt;/td&gt;&lt;td&gt;{2}&lt;/td&gt;&lt;/tr&gt;"," j.employeeid,="" j.firstname,="" j.lastname,="" j.country);="" $(".table="" tbody").html(tbody);};="" dm.remove("employeeid",local.shift().employeeid);="" $("#after").text("after="" insert:");="" tbody="" ;="" for(var="" i=""&gt;&lt;/3;i++){&gt;&lt;2;i++){ var="" j="dm.dataSource.json[i];" tbody="" +="String.format("&lt;tr&gt;&lt;td&gt;{0}&lt;/td&gt;&lt;td&gt;{1}&lt;/td&gt;&lt;td&gt;{2}&lt;/td&gt;&lt;/tr&gt;"," j.employeeid,="" j.firstname,="" j.lastname,="" j.country);="" $(".table1="" tbody").html(tbody);};="" &lt;/script&gt;=""&gt;&lt;/2;i++){&gt;</code>
</pre>






#### saveChanges<span class="signature">(changes, key, tableName)</span>








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
<td class="name"><code>changes</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
<tr>
<td class="name"><code>key</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
<tr>
<td class="name"><code>tableName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;style&gt;
.table,tr,td{ border:1px solid; padding:3px;}
&lt;/style&gt;
&lt;table class="table" style="border-collapse:collapse"&gt;
&lt;tbody&gt;&lt;/tbody&gt;
&lt;/table&gt;
&lt;script&gt;
var newData = { "added": [{ OrderID: 10248, CustomerID: "VINET", EmployeeID: 25 }], "deleted": {} , "changed":{} };
var data = [{ OrderID: 10249, CustomerID: "AANAR", EmployeeID: 5 },
{ OrderID: 10250, CustomerID: "VINET", EmployeeID: 5 },
{ OrderID: 10251, CustomerID: "SDDER", EmployeeID: 1 }];
var dm = ej.DataManager(griddata).saveChanges(newData);
$(function (){});
&lt;/script&gt;</code>
</pre>






#### update<span class="signature">(keyField, value, tableName)</span>








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
<td class="name"><code>keyField</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
<tr>
<td class="name"><code>tableName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;style&gt;
.table,tr,td{ border:1px solid; padding:3px;}
&lt;/style&gt;
&lt;table class="table" style="border-collapse:collapse"&gt;
&lt;tbody&gt;&lt;/tbody&gt;
&lt;/table&gt;
&lt;script&gt;
var first = [{ OrderID: 10248, CustomerID: "VINET", EmployeeID: 2 },
{ OrderID: 10249, CustomerID: "AANAR", EmployeeID: 9 }];
var updateData = {OrderID: 10249, CustomerID: "Test", EmployeeID: 0 };
ej.DataManager(first).update("OrderID", editedData, first);
$(function (){});
&lt;/script&gt;</code>
</pre>



