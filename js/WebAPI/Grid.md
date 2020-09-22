---
layout: post
title: Syncfusion webAPI reference for ejGrid
description: Learn about the webAPI references available for the Syncfusion Essential Studio ejGrid control to export Grid data in Excel.
documentation: ug
platform: js
keywords: grid, ejGrid, syncfusion, grid webapi
---
       
# Grid ExcelExport using WebAPI

## ExcelExport

 [POST] [/Api/Grid/ExcelExport](http://js.syncfusion.com/demos/ejservices/api/Grid/ExcelExport)

It is used to export the Grid data in Excel.

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

Essential Grid Excel-Exporting in JavaScript

{% highlight js %}

$(function () {
    $("#Grid").ejGrid({
    dataSource: window.gridData,
    allowPaging: true,
    toolbarSettings: {
    showToolbar: true,
    toolbarItems: [ej.Grid.ToolBarItems.ExcelExport]
    },
    toolbarClick: function (e) {
    this.exportGrid = this["export"];
    if (e.itemName == "Excel Export") {              
    this.exportGrid('http://js.syncfusion.com/demos/ejservices/api/Grid/ExcelExport')
    e.cancel = true;
    }
    },
    })
})

{% endhighlight %}

Essential Grid Excel-Exporting in C# 

{% highlight c# %}

public void ExportToExcel(string GridModel)
{
    ExcelExport exp = new ExcelExport();
    var DataSource = new NorthwindDataContext().OrdersViews.Take(100).ToList();
    GridProperties obj = ConvertGridObject(GridModel);
    exp.Export(obj, DataSource, "Export.xlsx", ExcelVersion.Excel2010, false, false, "flat-saffron");
}    

{% endhighlight %}
> The above example shows that the Grid data has been exported in Excel file.
        
## PdfExport

 [POST] [/Api/Grid/PdfExport](http://js.syncfusion.com/demos/ejservices/api/Grid/PdfExport)

It is used to export the Grid data in PDF.

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

Essential Grid PDF-Exporting in JavaScript

{% highlight js %}

$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging: true,
        toolbarSettings: {
            showToolbar: true,
            toolbarItems: [ej.Grid.ToolBarItems.PdfExport]
        },
        toolbarClick: function (e) {
            this.exportGrid = this["export"];
            if (e.itemName == "PDF Export") {
                this.exportGrid('http://js.syncfusion.com/demos/ejservices/api/Grid/PdfExport')
                e.cancel = true;
            }
        },
    })

})

{% endhighlight %}

Essential Grid PDF-Exporting in C# 

{% highlight c# %}

public void ExportToPdf(string GridModel)
{
    PdfExport exp = new PdfExport();
    var DataSource = new NorthwindDataContext().OrdersViews.Take(100).ToList();
    GridProperties obj = ConvertGridObject(GridModel);
    exp.Export(obj, DataSource, "Export.pdf", false, false, "flat-saffron");
}

{% endhighlight %}
> The above example shows that the Grid data has been exported in PDF file.

        
## WordExport

 [POST] [/Api/Grid/WordExport](http://js.syncfusion.com/demos/ejservices/api/Grid/WordExport)

It is used to export the Grid data in Word.

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example

Essential Grid Word-Exporting in JavaScript

{% highlight js %}

$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging: true,
        toolbarSettings: {
            showToolbar: true,
            toolbarItems: [ej.Grid.ToolBarItems.WordExport, ]
        },
        toolbarClick: function (e) {
            this.exportGrid = this["export"];
            if (e.itemName == "Word Export") {
                this.exportGrid('http://js.syncfusion.com/demos/ejservices/api/Grid/WordExport')
                e.cancel = true;
            }
        },
    })
});

{% endhighlight %}

Essential Grid Word-Exporting in C#

{% highlight c# %}
  
public void ExportToWord(string GridModel)
{
    WordExport exp = new WordExport();
    var DataSource = new NorthwindDataContext().OrdersViews.Take(100).ToList();
    GridProperties obj = ConvertGridObject(GridModel);
    exp.Export(obj, DataSource, "Export.docx", false, false, "flat-saffron");
}

 {% endhighlight %}

> The above example shows that the Grid data has been exported in Word file.


## Get

 [GET] [/Api/Grid/Get](http://js.syncfusion.com/demos/ejservices/api/Grid/Get)

It is used to get the dataSource from Northwind dataSource.

### URL parameters

|  Parameter |  Description | 
|---|---|
|$top|Returns only the first n results| 
|$skip|Used to skip the first n results| 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

Response (JSON):   

{% highlight js %}
{
"__metadata":

{"id":"http://js.syncfusion.com/demos/ejservices/Wcf/Northwind.svc/Orders(10248)",
"uri":"http://js.syncfusion.com/demos/ejservices/Wcf/Northwind.svc/Orders(10248)",
"type":"EJServices.Models.Order"},

"Customer":
{"__deferred":{"uri":"http://js.syncfusion.com/demos/ejservices/Wcf/Northwind.svc/Orders(10248)/Customer"}},

"OrderID":10248,
"CustomerID":"VINET",
"EmployeeID":5,
"OrderDate":"\/Date(836438400000)\/",
"RequiredDate":"\/Date(838857600000)\/",
"ShippedDate":"\/Date(837475200000)\/",
"ShipVia":3,
"Freight":"32.3800",
"ShipName":"Vins et alcools Chevalier",
"ShipAddress":"59 rue de l'Abbaye",
"ShipCity":"Reims",
"ShipRegion":null,
"ShipPostalCode":"51100",
"ShipCountry":"France"
}, 	 //... 9 more records

{% endhighlight %}

> We can see that the first ten results from the `Orders` table of Northwind database in the above JSON reponse where it uses `$top` query option.   


## Post

 [POST] [/Api/Grid/Post](http://js.syncfusion.com/demos/ejservices/api/Grid/Post)

It is used to add the data to the grid column. 

### URL parameters

|  Parameter |  Description | 
|---|---|
|   | | 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

### Code example 


{% highlight js %}

{% endhighlight %}

## Put

 [PUT] [/Api/Grid/Put](http://js.syncfusion.com/demos/ejservices/api/Grid/Put)

It is used to update the Grid data. 

|  Parameter |  Description | 
|---|---|
|   | | 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

### Code example 


{% highlight js %}

{% endhighlight %}

## Delete

 [DELETE] [/Api/Grid/Delete](http://js.syncfusion.com/demos/ejservices/api/Grid/Delete)

It is used to delete the data which is present in Grid column. 

|  Parameter |  Description | 
|---|---|
|   | | 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

### Code example 


{% highlight js %}

{% endhighlight %}


