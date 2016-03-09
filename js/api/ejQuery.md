---
layout: post
title: ej.Query
documentation: API
platform: js
metaname: 
metacontent: 
---

Communicates with data source and returns the desired result based on the Query provided.


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
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().take(5));
var tbody = ""; 
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td><td>{3}</td></tr>"," dm[i].orderid,="" dm[i].customerid,="" dm[i].shipcity,="" dm[i].freight);="" $(".table="" tbody").html(tbody);};=""></3;i++){>{% endhighlight %}







## Methods








### addParams<span class="signature">(key, value)</span>
{:#methods:addparams}








Passes custom parameters to our API URL.

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
<td class="name">{% highlight html %}
key{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last"></td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<script>
var dm = ej.DataManager({url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/"}).executeQuery(new ej.Query().addParams("test","value"));
</script>{% endhighlight %}







### clone<span class="signature">()</span>
{:#methods:clone}








clone is used to duplicate the data.





#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().where("OrderID","equal","10250").clone());
var tbody="";
tbody += String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>", dm[0].OrderID, dm[0].CustomerID, dm[0].ShipCity);
$(".table tbody").html(tbody);
</script>{% endhighlight %}







### execute<span class="signature">(dataManager)</span>
{:#methods:execute}

It is used to execute the query on URL Binding

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
<td class="name">{% highlight html %}
dataManager{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">json data or OData</td>
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
var dataManager = ej.DataManager({url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/"});
var promise =  ej.Query().select(["OrderID", "CustomerID", "ShipName", "ShipCity", "Freight"]).execute(dataManager,done).take(3);
promise.done(function(e){}) 
</script>{% endhighlight %}







### executeLocal<span class="signature">(dataManager)</span>
{:#methods:executelocal}








It is used to execute the query on Local Binding

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
<td class="name">{% highlight html %}
dataManager{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">json data</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<script>
var dm = ej.DataManager(window.gridData);
var promise =  ej.Query().select(["OrderID", "CustomerID", "ShipName", "ShipCity", "Freight"]).executeLocal(dm).take(3);
</script>{% endhighlight %}







### expand<span class="signature">(tables)</span>
{:#methods:expand}








expand is used to performs complex binding.

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
<td class="name">{% highlight html %}
tables{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the tables</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<script>
var dm = ej.DataManager({url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"})
.executeQuery(ej.Query().from("Orders").select("OrderID", "CustomerID", "ShipCity", "Employee.FirstName").expand("Employee"));
</script>{% endhighlight %}







### foreignKey<span class="signature">(key)</span>
{:#methods:foreignkey}








Relates two tables. A foreign key is a column or combination of columns which is used to establish and enforce a link between two tables.

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
<td class="name">{% highlight html %}
key{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">primary key field name</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<script>
var dm = ej.DataManager({url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"})
.executeQuery(ej.Query().from("Orders")
.hierarchy(ej.Query().from("Order_Details").foreignKey("OrderID").sortBy("Quantity"),function () {
 return [10250, 10251, 10252, 10253] }));
</script>{% endhighlight %}







### from<span class="signature">(tableName)</span>
{:#methods:from}








Specifies the name of table(s) to retrieve data.

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
<td class="name">{% highlight html %}
tableName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the table</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().from("Orders"));
var tbody="";
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].orderid,="" dm[i].customerid,="" dm[i].shipcity);="" $(".table="" tbody").html(tbody);}=""></3;i++){>{% endhighlight %}







### group<span class="signature">(fieldName)</span>
{:#methods:group}








Groups records based on the given field name.

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
<td class="name">{% highlight html %}
fieldName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the column</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().group("CustomerID"));
var tbody="";
for(var i=0;i<3;i++){ row="dm[0].items[i];" tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," row.orderid,="" row.customerid,="" row.shipcity);="" $(".table="" tbody").html(tbody);}=""></3;i++){>{% endhighlight %}







### hierarchy<span class="signature">(query)</span>
{:#methods:hierarchy}








Displays the records in hierarchical relationships. The foreign key is used to relate two tables.

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
<td class="name">{% highlight html %}
query{% endhighlight %}</td>
<td class="type"><span class="param-type">ej.Query</span></td>
<td class="description last">query the json data</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<script>
var dm = ej.DataManager({url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"})
.executeQuery(ej.Query().from("Orders")
.hierarchy(ej.Query().foreignKey("OrderID").from("Order_Details"),function () {
 return [10248] }));
</script>{% endhighlight %}







### page<span class="signature">(pageIndex, pageSize)</span>
{:#methods:page}








Retrieves records based on the given page index and size.

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
<td class="name">{% highlight html %}
pageIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">page number</td>
</tr>
<tr>
<td class="name">{% highlight html %}
pageSize{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Number of rows in the page</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
//page(pageIndex,pageSize)
var dm = ej.DataManager(window.employeeData).executeLocal(ej.Query().page(2,3));
var tbody="";
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].employeeid,="" dm[i].lastname,="" dm[i].firstname);="" $(".table="" tbody").html(tbody);}=""></3;i++){>{% endhighlight %}







### range<span class="signature">(start, end)</span>
{:#methods:range}








The range property is used to retrieve the records based on the given start and end index.

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
<td class="name">{% highlight html %}
start{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">start index of json data</td>
</tr>
<tr>
<td class="name">{% highlight html %}
end{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">end index of json data</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
//range(startIndex,endIndex)
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().take(20).range(2,5));
var tbody="";
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].orderid,="" dm[i].customerid,="" dm[i].shipcity);="" $(".table="" tbody").html(tbody);}=""></3;i++){>{% endhighlight %}







#Requires
{:.require}Count<span class="signature">()</span>








It is used to count records.





#### Example
{:.example}


{% highlight html %}
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().Requires
{:.require}Count()));
</script>{% endhighlight %}







### search<span class="signature">(fieldName, operator, value, ignoreCase)</span>
{:#methods:search}








It is used to search the given search key value in JSON data

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
<td class="name">{% highlight html %}
fieldName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the column</td>
</tr>
<tr>
<td class="name">{% highlight html %}
operator{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">conditional Operators</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">value to filter the field name</td>
</tr>
<tr>
<td class="name">{% highlight html %}
ignoreCase{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">on/off case sensitive.</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().select(["OrderID","ShipCity","CustomerID"]).search("10251","OrderID","equal"));
var tbody="";
tbody += String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>", dm[0].OrderID, dm[0].CustomerID, dm[0].ShipCity);
$(".table tbody").html(tbody);
</script>{% endhighlight %}







### select<span class="signature">(fieldName)</span>
{:#methods:select}








Selects specified columns from the data source.

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
<td class="name">{% highlight html %}
fieldName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the columns</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().select(["OrderID","CustomerID","ShipCity"]));
var tbody="";
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].orderid,="" dm[i].customerid,="" dm[i].shipcity);="" $(".table="" tbody").html(tbody);}=""></3;i++){>{% endhighlight %}







### skip<span class="signature">(nos)</span>
{:#methods:skip}








Skips the given count of records from the data source.

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
<td class="name">{% highlight html %}
nos{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">number of records</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.employeeData).executeLocal(ej.Query().skip(5));
var tbody="";
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].employeeid,="" dm[i].lastname,="" dm[i].firstname);="" $(".table="" tbody").html(tbody);}=""></3;i++){>{% endhighlight %}







### sortBy<span class="signature">(fieldName)</span>
{:#methods:sortby}








Sort items or records in an ordered sequence.

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
<td class="name">{% highlight html %}
fieldName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the column</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().sortBy("CustomerID desc"));
var tbody="";
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].orderid,="" dm[i].customerid,="" dm[i].shipcity);="" $(".table="" tbody").html(tbody);}=""></3;i++){>{% endhighlight %}







### sortByDesc<span class="signature">(fieldName)</span>
{:#methods:sortbydesc}








Sort items or records in descending order.

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
<td class="name">{% highlight html %}
fieldName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the column</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().sortByDesc("CustomerID"));
var tbody="";
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].orderid,="" dm[i].customerid,="" dm[i].shipcity);="" $(".table="" tbody").html(tbody);}=""></3;i++){>{% endhighlight %}







### take<span class="signature">(nos)</span>
{:#methods:take}








Picks the given count of records from the top of the datasource.

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
<td class="name">{% highlight html %}
nos{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">number of records</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().take(5));
var tbody="";
for(var i=0;i<5;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].orderid,="" dm[i].customerid,="" dm[i].shipcity);="" $(".table="" tbody").html(tbody);}=""></5;i++){>{% endhighlight %}







### using<span class="signature">(dataManager)</span>
{:#methods:using}








using is a method used to query the data manager.

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
<td class="name">{% highlight html %}
dataManager{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Pass new data source</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData);
var local = dm.executeLocal(ej.Query().using(dm).take(1));
var tbody = ""; 
 tbody += String.format("<tr><td>{0}</td><td>{1}</td></tr>", local[0].OrderID, local[0].CustomerID);
 $(".table tbody").html(tbody); 
</script>{% endhighlight %}







### where<span class="signature">(fieldName, operator, value, ignoreCase)</span>
{:#methods:where}








It is used to filter records based on the filter condition.

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
<td class="name">{% highlight html %}
fieldName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the column</td>
</tr>
<tr>
<td class="name">{% highlight html %}
operator{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">conditional Operators</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">value to filter the field name</td>
</tr>
<tr>
<td class="name">{% highlight html %}
ignoreCase{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">on/off case sensitive.</td>
</tr>
</tbody>
</table>




#### Example
{:.example}


{% highlight html %}
<style>
.table,tr,td{ border:1px solid;padding:3px;}
</style>
<table class="table" style="border-collapse:collapse">
<tbody></tbody>
</table>
<script>
var dm = ej.DataManager(window.gridData).executeLocal(ej.Query().where("OrderID","lessthan","10253"));
var tbody="";
for(var i=0;i<3;i++){ tbody="" +="String.format("<tr><td>{0}</td><td>{1}</td><td>{2}</td></tr>"," dm[i].orderid,="" dm[i].customerid,="" dm[i].shipcity);="" $(".table="" tbody").html(tbody);}=""></3;i++){>{% endhighlight %}




