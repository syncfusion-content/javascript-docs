---
layout: post
title: Data-Binding
description: data binding
platform: js
control: OLAP Client
documentation: ug
---

# Data Binding

**OLAP Client** control enables you to retrieve multidimensional data either from **SSAS** or from any **XMLA** provider and present the **OLAP** information in a meaningful way.

## SSAS

**Bind OLAP Client to the Offline Cube**

The following code example illustrates how to connect to an offline cube.

{% highlight c# %}

**[C#]**
String connectionString = @"DataSource= C:\Users\<UserName>\appdata\local\syncfusion\essentialstudio\x.x.x.x\Common\Data\OfflineCube\Adventure_Works_Ext.cub; Provider = MSOLAP;";
OlapDataManager DataManager = new OlapDataManager(connectionString);


{% endhighlight %}



**Bind OLAP Client to the SQL Server (Local)**

The following code example illustrates how to connect to a local cube in SQL Server.

{% highlight c# %}


**[C#]**
string connectionString = "Data source=localhost; Initial Catalog=Adventure Works DW;";
OlapDataManager DataManager = new OlapDataManager(connectionString);


{% endhighlight %}

## XML/A

**XML for Analysis (XML/A)** is a standard that allows the client applications to transfer multi-dimensional or **OLAP** data sources from an **OLAP** Server which is available online. The back and forth communication is done using the web standards – **HTTP**, **SOAP**, and **XML**. The query language used is **MDX**, which is most widely supported for reporting from multi-dimensional data stores.

**Use Case Scenarios**

**XML/A** provides the most efficient way to access an **OLAP** database over the Internet.

**Connecting to SSAS Server (Online)**

The following code example illustrates how to connect to the **SSAS** server available online.

{% highlight c# %}

**[C#]**
static string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
OlapDataManager DataManager = new OlapDataManager(connectionString);


{% endhighlight %}



**Connect to Mondrian Server**

The following code example illustrates how to connect to the Mondrian Server.

{% include image.html url="/js/OlapClient/Concepts-and-Features/Data-Binding_images/Data-Binding_img1.png" Caption="New Report"%}

**Add Report**

Add a new report along with the existing report collection.

{% include image.html url="/js/OlapClient/Concepts-and-Features/Data-Binding_images/Data-Binding_img2.png" Caption="Add Report"%}

Replace the existing report name with the altered report name.

{% include image.html url="/js/OlapClient/Concepts-and-Features/Data-Binding_images/Data-Binding_img3.png" Caption="Rename Report"%}

**Remove Report**

Removes the current report from the report collection. If only one report is available in the report list, it doesn’t remove it.

{% include image.html url="/js/OlapClient/Concepts-and-Features/Data-Binding_images/Data-Binding_img4.png" Caption="Remove Report"%}

**Save and Load Report**

The **OLAP****Report** collection bound to the **OLAP****Client** component can be passed to a web service, to save the reports in a database. Similarly, the saved **OLAP****Report** collection can be loaded back into the control. Two toolbar items have been added in the control to save and load an **OLAP****Report** collection to the database and to the component respectively.

{% include image.html url="/js/OlapClient/Concepts-and-Features/Data-Binding_images/Data-Binding_img5.png" Caption="Save and Load Icons in Toolbar"%}

On clicking the Save icon, a dialog is displayed to enter the name with which the **OLAP Report** collection is to be saved. On clicking OK, the **OLAP Report** collection associated is passed to the web service and saved in the database connected with the name provided. 

{% include image.html url="/js/OlapClient/Concepts-and-Features/Data-Binding_images/Data-Binding_img6.png" Caption="Save Report"%}

Similarly, on clicking the load icon, a pop-up window is displayed, containing a drop-down with a list of saved **OLAP Reports** in the connected database. On selecting the name containing the **OLAP Report** collection and clicking OK, the selected **OLAP Report** collection is loaded into the control.

{% include image.html url="/js/OlapClient/Concepts-and-Features/Data-Binding_images/Data-Binding_img7.png" Caption="Load Report"%}

