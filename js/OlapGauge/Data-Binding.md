---
layout: post
title: Data-Binding
description: data binding
platform: js
control: OlapGauge
documentation: ug
---

# Data Binding

**OlapGauge** control enables you to retrieve multidimensional data either from cube directly or through any **XML/A** provider and present the OLAP information in a meaningful way.

## SSAS

###Binding OlapGauge to the Offline Cube

The following code illustrates how to connect to an offline cube:

{% highlight c# %}

string connectionString = @"DataSource= system drive:\OfflineCube\Adventure_Works_Ext.cub; Provider = MSOLAP;";
OlapDataManager DataManager = new OlapDataManager(connectionString);


{% endhighlight %}

###Binding OlapGauge to the SQL Server (Local)

The following code illustrates how to connect to a Cube available in local SQL Server:

{% highlight c# %}

string connectionString = @"DataSource= system drive:\OfflineCube\Adventure_Works_Ext.cub; Provider = MSOLAP;";
OlapDataManager DataManager = new OlapDataManager(connectionString);


{% endhighlight %}

## XML/A

###Use Case Scenarios

**XML for Analysis** (XML/A) provides the most efficient way to access an OLAP database over the Internet.

###Connecting to SSAS Server (Online)

The following code illustrates how to connect to the **SSAS** server available online:

{% highlight c# %}

static string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
OlapDataManager DataManager = new OlapDataManager(connectionString);


{% endhighlight %}

###Connecting to Mondrian Server

The following code illustrates how to connect to the **Mondrian Server**:

{% highlight c# %}

// Connecting to Mondrian Server
string connectionString = @"Data Source = http://localhost:8080/mondrian/xmla; Initial Catalog =FoodMart;";
OlapDataManager DataManager = new OlapDataManager(connectionString);
DataManager.DataProvider.ProviderName = Syncfusion.Olap.DataProvider.Providers.Mondrian;


{% endhighlight %}

###Connecting to ActivePivot Server

The following code illustrates how to connect to **ActivePivot Server**:

{% highlight c# %}

// Connecting to ActivePivot Server
string connectionString= @"Data Source=http://localhost:8081/var_s/xmla; Initial Catalog=VaRCubes; User ID=; Password=; Transport Compression=None;";
OlapDataManager DataManager = new OlapDataManager(connectionString);
DataManager.DataProvider.ProviderName = Syncfusion.Olap.DataProvider.Providers.ActivePivot;


{% endhighlight %}



