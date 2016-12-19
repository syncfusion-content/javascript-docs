---
layout: post
title: WCF reference for Northwind services
description: WCF reference for Northwind services
documentation: ug
platform: js
keywords: Northwind, syncfusion, Northwind wcf
---

## NorthwindDataService

 [GET] [/WCF/Northwind.svc](http://js.syncfusion.com/demos/ejservices/Wcf/Northwind.svc)

This is an [OData](http://www.odata.org/) endpoint for Microsoft Northwind sample database with limited data tables like `Orders` and `Customers`.

## Grid

 [GET] [/WCF/Northwind.svc/Orders](http://js.syncfusion.com/demos/ejServices/wcf/NorthWind.svc/Orders)<br>
 [GET] [/WCF/Northwind.svc/Customers](http://js.syncfusion.com/demos/ejServices/wcf/NorthWind.svc/Customers)

We have used Northwind services for Grid control where it has the data tables like "Orders" and "Customers".

### URL parameters

|  Parameter |  Description | 
|---|---|
|$top|Returns only the first n results.| 
|$skip|Used to skip the first n results.| 

> We can use other query options in order to perform the filtering in Northwind database. For demo purpose we have used [Northwind database](http://services.odata.org/V3/Northwind/Northwind.svc/$metadata). To know more about the query option click [here](https://msdn.microsoft.com/en-us/library/dd728283(v=vs.110).aspx)

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

## Kanban

 [GET] [/WCF/Northwind.svc/Tasks](http://js.syncfusion.com/demos/ejServices/wcf/NorthWind.svc/Tasks)

For Kanban control we have added the custom table along with the Northwind service.

### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

Response (JSON):   

{% highlight js %}

{

"__metadata":{"id":"http://js.syncfusion.com/demos/ejservices/Wcf/Northwind.svc/Tasks(1)",
"uri":"http://js.syncfusion.com/demos/ejservices/Wcf/Northwind.svc/Tasks(1)","type":"EJServices.Models.Task"},
"Id":1,
"Status":"Open",
"Summary":"Analyze new requirements gathered from customer",
"Type":"UG","Priority":"Low",
"Tags":"Analyze,Requirements",
"Estimate":3.5,
"Assignee":"Nancy Davloio",
"ImgUrl":"content/images/kanban/1.png",
"RankId":1

}, 	 //... 9 more records

{% endhighlight %} 

> We can see that the first ten results from the `Tasks` table of Northwind database in the above JSON reponse where it uses `$top` query option.   