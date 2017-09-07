---
title: Data binding with Spreadsheet widget for Syncfusion Essential JS
description: How to perform Data Binding and configure its properties like dataSource, query etc.
platform: js
control: Spreadsheet
documentation: ug
api: /api/js/ejspreadsheet
---
# Data Binding

Spreadsheet can be populated with external datasource using [`dataSource`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-datasource "dataSource") property. The [`dataSource`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-datasource "dataSource") property can be assigned either with the instance of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager "ej.DataManager") or JSON data array collection. Spreadsheet supports three different kinds of Data binding.

* Local Data
* Remote Data
* HTML Table Data

## Local Data

To bind local data to the Spreadsheet, you can assign a JSON array to the worksheet [`dataSource`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-datasource "dataSource") property. The following code illustrates how to bind local data to the Spreadsheet,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
    $("#Spreadsheet").ejSpreadsheet({                                
        sheets: [{
            // the datasource "window.filterData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.js'
            dataSource: window.filterData
        }]
    });
});
</script>

{% endhighlight %}

The following output is displayed as a result of the above code snippets.
![](Data-Binding_images/Data-Binding_img1.png)

## Remote Data

To bind remote data to the Spreadsheet, you can assign a service data as an instance of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager "ej.DataManager") to the worksheet [`dataSource`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-datasource "dataSource") property. The following code illustrates how to bind remote data to the Spreadsheet,

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

### Offline Mode

To avoid sending post back request to server on every action, Spreadsheet allows user to create, update and delete data on client side. To enable this, set `offline` property of [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager "ej.DataManager") as `true` to fetch all data from server on initial rendering of Spreadsheet and perform all operation on client side.

The following code illustrates offline data binding for Spreadsheet,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        sheets: [{
            dataSource: ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/",
                offline: true
            }),
            query: ej.Query().select(["OrderID", "CustomerID", "EmployeeID", "ShipName",  "ShipAddress"]),
            primaryKey: "OrderID"
        }],
    });
});
</script>

{% endhighlight %}

The following output is displayed as a result of the above code snippets.
![](Data-Binding_images/Data-Binding_img2.png)

N> For further reference about `offline` property in [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager "ej.DataManager") refer following [`link`](https://help.syncfusion.com/js/datamanager/data-binding#offline-mode "link")

## HTML Table Data

An HTML Table element can also be used as the data source of Spreadsheet. To use HTML Table as data source, the table element should be passed to worksheet [`dataSource`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-datasource "dataSource") property of Spreadsheet as an instance of the [`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager "ej.DataManager"). The following code illustrates how to bind HTML Table data to the Spreadsheet,

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

You can bind data to Spreadsheet in following ways,

* Cell binding
* Range binding
* Sheet binding

### Cell Binding

Spreadsheet can bind data for individual cells in a sheet. The data may contain value, style, format, comment and hyperlink. The individual cell properties are listed below,

<table>
    <tr>
        <th>
            Properties
        </th>
        <th>
            Description
        </th>
    </tr>
    <tr>
        <td>
            index
        </td>
        <td>
            To specify particular cell
        </td>
    </tr>
    <tr>
        <td>
            value
        </td>
        <td>
            To specify value. It may be string, integer, formula etc.
        </td>
    </tr>
    <tr>
        <td>
            style
        </td>
        <td>
            To specify style in the cell
        </td>
    </tr>
    <tr>
        <td>
            format
        </td>
        <td>
            To specify number format in the cell
        </td>
    </tr>
    <tr>
        <td>
            comment
        </td>
        <td>
            To specify comment in the cell
        </td>
    </tr>
    <tr>        
        <td>
            hyperlink
        </td>
        <td>
            To specify hyperlink in the cell
        </td>
    </tr>
</table>

The individual row properties are listed below,

<table>
    <tr>
        <th>
            Properties
        </th>
        <th>
            Description
        </th>
    </tr>
    <tr>
        <td>
            index
        </td>
        <td>
            To specify particular row
        </td>
    </tr>
    <tr>
        <td>
            height
        </td>
        <td>
            To specify height in the row
        </td>
    </tr>
</table>

You can specify particular row with `index` property and its height with `height` property in the rows' property collection. The following code illustrates cell binding in Spreadsheet,

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
                { value: "Casual Shoes", comment: { value: "Casual FootWears with wide variety of colors." } },
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
                { value: "Formal Shoes", comment: { value: "Formal FootWears with wide range of sizes." } },
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

### Range Binding

Spreadsheet can bind data for one or more range in a sheet using [`rangeSettings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-rangesettings "rangeSettings"). The individual range properties are listed below,

<table>
    <tr>
        <th>
            Properties
        </th>
        <th>
            Description
        </th>
    </tr>
    <tr>
        <td>
            {{'[`dataSource`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-rangesettings-datasource "dataSource")'| markdownify }}
        </td>
        <td>
            To specify JSON or {{'[`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager "ej.DataManager")'| markdownify }}
        </td>
    </tr>
    <tr>    
        <td>
            {{'[`query`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-rangesettings-query "query")'| markdownify }}
        </td>
        <td>
            To specify query for {{'[`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager "ej.DataManager")'| markdownify }}
        </td>
    </tr>
    <tr>
        <td>    
            {{'[`startCell`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-rangesettings-startcell "startCell")'| markdownify }}
        </td>
        <td>
            To specify start cell of a range
        </td>
    </tr>
    <tr>
        <td>
            {{'[`primarykey`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-rangesettings-primarykey "primarykey")'| markdownify }}
        </td>
        <td>
            To specify data source primary key
        </td>
    </tr>
    <tr>
        <td>
            {{'[`showHeader`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-rangesettings-showheader "showHeader")'| markdownify }}
        </td>
        <td>
            To show data source header
        </td>
    </tr>
    <tr>
        <td>
            {{'[`headerStyles`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-rangesettings-headerstyles "headerStyles")'| markdownify }}
        </td>
        <td>
            To specify header styles
        </td>
    </tr>
</table>

The following code illustrates range binding in Spreadsheet

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
    $("#Spreadsheet").ejSpreadsheet({               
        sheets: [{
            rangeSettings: [{
                // the datasource "window.markList" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.js'
                dataSource: window.markList,
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

### Sheet Binding

Spreadsheet can bind data for a sheet. The individual sheet properties are listed below,

<table>
    <tr>
        <th>
            Properties
        </th>
        <th>
            Description
        </th>
    </tr>
    <tr>
        <td>
            {{'[`dataSource`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-datasource "dataSource")'| markdownify }}
        </td>
        <td>
            To specify JSON or {{'[`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager "ej.DataManager")'| markdownify }}
        </td>
    </tr>
    <tr>
        <td>
            {{'[`query`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-query "query")'| markdownify }}
        </td>
        <td>
            To specify query for {{'[`ej.DataManager`](https://help.syncfusion.com/api/js/ejdatamanager "ej.DataManager")'| markdownify }}
        </td>
    </tr>
    <tr>
        <td>
            {{'[`startCell`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-startcell "startCell")'| markdownify }}
        </td>
        <td>
            To specify start cell of a range
        </td>
    </tr>
    <tr>
        <td>
            {{'[`primarykey`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-primarykey "primarykey")'| markdownify }}
        </td>
        <td>
            To specify data source primary key
        </td>
    </tr>
    <tr>
        <td>
            {{'[`showHeader`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-showheader "showHeader")'| markdownify }}
        </td>
        <td>
            To show data source header
        </td>
    </tr>
    <tr>
        <td>
            {{'[`headerStyles`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-headerstyles "headerStyles")'| markdownify }}
        </td>
        <td>
            To specify header styles
        </td>
    </tr>
    <tr>
        <td>
            {{'[`fieldAsColumnHeader`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-fieldascolumnheader  "fieldAsColumnHeader")'| markdownify }}
        </td>
        <td>
            To show data source fields in column header
        </td>
    </tr>
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

