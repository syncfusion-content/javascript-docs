---
layout: post
title: Filtering
description: filtering
platform: js
control: DataManager
documentation: ug
keywords: filter Operators, lessThan, lessThanOrEqual, less, contains
---

# Filtering

Filtering is a basic technique in **DataManager** query. The “where” query is used to filter some particular or related records from the data source to review details of records. 

## Filter Operators

Filter operators are generally used to specify the filter type. The various filter operators corresponding to the type of the column is listed in the following table.

<table>
<tr>
<th>
Column type</th><th>
Filter operators</th></tr>
<tr>
<td>
Number</td><td>
ej.FilterOperators.greaterThan<br/>ej.FilterOperators.greaterThanOrEqual<br/>ej.FilterOperators.lessThan<br/>ej.FilterOperators.lessThanOrEqual<br/>ej.FilterOperators.equal</td></tr>
<tr>
<td>
String</td><td>
ej.FilterOperators.startsWith<br/>ej.FilterOperators.endsWith<br/>ej.FilterOperators.contains<br/>ej.FilterOperators.equal<br/>ej.FilterOperators.notEqual</td></tr>
<tr>
<td>
Boolean</td><td>
ej.FilterOperators.equal<br/>ej.FilterOperators.notEqual</td></tr>
<tr>
<td>
Date</td><td>
ej.FilterOperators.greaterThan<br/>ej.FilterOperators.greaterThanOrEqual<br/>ej.FilterOperators.lessThan<br/>ej.FilterOperators.lessThanOrEqual<br/>ej.FilterOperators.equal</td></tr>
</table>


## lessThan

This operator is used to get the records with values less than that of the filter value.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders").select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,10).where("OrderID", "lessThan", 10252, false);
        
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>          
        </tr>
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img1.png) 

## greaterThan

This operator is used to get the records with values greater than that of the filter value.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
            var query = ej.Query()            
                .from("Orders").select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,5)
                .where("OrderID", "greaterThan", 10263, false);
        
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });  
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>       
        </tr>  
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img2.png) 

## lessThanOrEqual

This operator is used to get the records with values less than or equal to the filter value.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders")
                .select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,10)
                .where("OrderID", "lessThanOrEqual", 10251, false);
        
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>    
        </tr>
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img3.png) 

## greaterThanOrEqual

This operator is used to get the records with values greater than or equal to the filter value.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders").select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,5)
                .where("OrderID", "greaterThanOrEqual", 10256, false);
        
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>         
        </tr>
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img4.png) 

## equal

This operator is used to get the records with values equal to that of the filter value.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders").select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,5).where("EmployeeID", "equal", 6, false);
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>      
        </tr>
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img5.png) 

## notEqual

This operator is used to get the records with values not equal to that of the filter value specified.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
                    var dataManager = ej.DataManager({//oData Adaptor with DataManager
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders")
                .select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,5)
                .where("ShipCountry", "notEqual", "Rio de Janeiro", false);
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">        
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>    
        </tr>                 
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img6.png) 

## contains

This operator is used to get the records that contains the filter value.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders")
                .select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,5)
                .where("CustomerID", "contains", "A", false);
        
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>        
        </tr>
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img7.png) 

## startswith

This operator is used to get the records that starts with the filter value specified.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders").select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,5).where("CustomerID", "startswith", "V", false);
        
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>      
        </tr>
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img8.png) 

## endswith

This operator is used to get the records that ends with the filter value specified.


{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders").select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,5).where("CustomerID", "endswith", "E", false);
        
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
        <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>    
        </tr>
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img9.png) 

## and predicate

The `and` predicate is used to add n-number of predicates with “and” condition and filter the data.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders")
                .select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,5)
                .where(ej.Predicate("OrderID", ej.FilterOperators.greaterThan, 10399, true).and("CustomerID", ej.FilterOperators.startsWith, "V", true));
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>      
        </tr>
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img10.png) 

## or predicate

Using this method you can add n-number of predicates with `or` condition and filter the data.

{% highlight html %}

    <div class="datatable">
        <table id="table1" class=" table table-striped table-bordered" style="width:700px">
            <thead>
                <tr>
                    <th>Order ID</th>
                    <th>Customer ID</th>
                    <th>Employee ID</th>
                    <th>Freight</th>
                    <th>Ship Country</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
    </div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            //oData Adaptor with DataManager
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
        
            var query = ej.Query()            
                .from("Orders")
                .select("OrderID", "CustomerID", " EmployeeID", "Freight", "ShipCountry")
                .page(1,5)
                .where(ej.Predicate("EmployeeID", ej.FilterOperators.greaterThan, 6, true)**.or**("CustomerID", ej.FilterOperators.startsWith, "S", true));
        
            var execute = dataManager.executeQuery(query) // executing query
                    .done(function (e) {
                        $("#table1 tbody").html($("#tableTemplate").render(e.result));
                    });
        });
    </script>
    <script id="tableTemplate" type="text/x-jsrender">
        <tr>
            <td>{{"{{"}}>OrderID{{}}}}</td>
            <td>{{"{{"}}>CustomerID{{}}}}</td>
            <td>{{"{{"}}>EmployeeID{{}}}}</td>
            <td>{{"{{"}}>Freight{{}}}}</td>
            <td>{{"{{"}}>ShipCountry{{}}}}</td>       
        </tr>
    </script>

{% endhighlight %}

Result of the above code example is illustrated as follows.

![](Filtering_images/Filtering_img11.png) 

