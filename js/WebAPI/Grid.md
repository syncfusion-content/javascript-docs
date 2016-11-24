---
layout: post
title: webAPI reference for ejGrid
description: webAPI reference for ejGrid
documentation: API
platform: js-webapi
keywords: grid, ejGrid, syncfusion, grid webapi
---

## NorthwindDataService

[GET&nbsp;&nbsp;/wcf/northwind.svc](http://js.syncfusion.com/demos/ejservices/Wcf/Northwind.svc)

It is used to retrieve the records from the tables like `Orders` and `Customers` in `Northwind data service`.

### URL parameters

|  Parameter |  Description | 
|---|---|
|  $top | Returns only the first n results| 
|  $skip | Used to skip the first n results| 
|  $filter	| Filters the results based on a Boolean condition|

> We can use other query options in order to perform the filtering in Northwind database. For demo purpose we have used <a href="http://services.odata.org/V3/Northwind/Northwind.svc/$metadata">Northwind database</a>. To know more about the query option click <a href="https://msdn.microsoft.com/en-us/library/dd728283(v=vs.110).aspx">here</a>

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

Response (JSON):   

```javascript

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

```
> We can see that the first ten results from the `Orders` table of Northwind database in the above JSON reponse where it uses `$top` query option.   
        
## ExcelExport

[POST&nbsp;&nbsp;/Api/Grid/ExcelExport](http://js.syncfusion.com/demos/ejservices/api/Grid/ExcelExport)

It is used to export the Grid data in Excel.

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

Essential Grid Excel-Exporting in javascript

```javascript

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
    
```

Essential Grid Excel-Exporting in C# 

```csharp

        public void ExportToExcel(string GridModel)
        {
            ExcelExport exp = new ExcelExport();
            var DataSource = new NorthwindDataContext().OrdersViews.Take(100).ToList();
            GridProperties obj = ConvertGridObject(GridModel);
            exp.Export(obj, DataSource, "Export.xlsx", ExcelVersion.Excel2010, false, false, "flat-saffron");
        }    
        
```
>The above example shows that the Grid data has been exported in Excel file.
        
## PdfExport

[POST&nbsp;&nbsp;/Api/Grid/PdfExport](http://js.syncfusion.com/demos/ejservices/api/Grid/PdfExport)

It is used to export the Grid data in PDF.

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

Essential Grid PDF-Exporting in javascript

```javascript
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
```

Essential Grid PDF-Exporting in C# 

```csharp

public void ExportToPdf(string GridModel)
        {
            PdfExport exp = new PdfExport();
            var DataSource = new NorthwindDataContext().OrdersViews.Take(100).ToList();
            GridProperties obj = ConvertGridObject(GridModel);
            exp.Export(obj, DataSource, "Export.pdf", false, false, "flat-saffron");
        }
```
>The above example shows that the Grid data has been exported in PDF file.

        
## WordExport

[POST&nbsp;&nbsp;/Api/Grid/WordExport](http://js.syncfusion.com/demos/ejservices/api/Grid/WordExport)

It is used to export the Grid data in Word.

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example

Essential Grid Word-Exporting in javascript

```javascript

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
        })
 ```
        
Essential Grid Word-Exporting in C# 

  ```csharp
  
  public void ExportToWord(string GridModel)
        {
            WordExport exp = new WordExport();
            var DataSource = new NorthwindDataContext().OrdersViews.Take(100).ToList();
            GridProperties obj = ConvertGridObject(GridModel);
            exp.Export(obj, DataSource, "Export.docx", false, false, "flat-saffron");
        }
  ```      

>The above example shows that the Grid data has been exported in Word file.

## Get

[GET&nbsp;&nbsp;Api/Grid/Get](http://js.syncfusion.com/demos/ejservices/api/Grid/Get)

It is used to get the dataSource from Northwind dataSource.

### URL parameters

|  Parameter |  Description | 
|---|---|
|  $top | Returns only the first n results| 
|  $skip | Used to skip the first n results| 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

Response (JSON):   

```javascript
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

```

### Code example 


```javascript

```

> We can see that the first ten results from the `Orders` table of Northwind database in the above JSON reponse where it uses `$top` query option.   


## Post

[POST&nbsp;&nbsp;/Api/Grid/Post](http://js.syncfusion.com/demos/ejservices/api/Grid/Post)

It is used to add the data to the grid column. 

### URL parameters

|  Parameter |  Description | 
|---|---|
|   | | 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

### Code example 


```javascript

```

## Put

[POST&nbsp;&nbsp;/Api/Grid/Put](http://js.syncfusion.com/demos/ejservices/api/Grid/Put)

It is used to update the Grid data. 

|  Parameter |  Description | 
|---|---|
|   | | 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

### Code example 


```javascript

```

## Delete

[POST&nbsp;&nbsp;/Api/Grid/Delete](http://js.syncfusion.com/demos/ejservices/api/Grid/Delete)

It is used to delete the data which is present in Grid column. 

|  Parameter |  Description | 
|---|---|
|   | | 

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

### Code example 


```javascript

```


