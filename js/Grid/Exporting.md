---
layout: post
title: Export with Grid widget for Syncfusion Essential JS
description: How to export the Grid to Microsoft Word,Microsoft Excel and PDF file format
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# Export

To export the grid, `export` method should  be called with export mapper as parameter. To make it work from the grid toolbar, `ExcelExport`, `WordExport` and `PdfExport` toolbar items needs to be added in [`toolbarSettings.toolbarItems`](https://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-toolbaritems) property and equivalent server action mapper should be defined in `exportToExcelAction`, `exportToWordAction`, and `exportToPdfAction` properties. The code snippet for this is

{% highlight html %}
<div id="Grid"></div>

<script type="text/javascript">

$(function () {

	$("#Grid").ejGrid({
		dataSource: ej.DataManager({ url: "http://js.syncfusion.com/ExportingServices/Northwnd.svc/Orders/" }),
		allowPaging: true,
		allowSorting: true,
		exportToExcelAction: 'http://js.syncfusion.com/ExportingServices/api/JSGridExport/ExcelExport',
		exportToWordAction: 'http://js.syncfusion.com/ExportingServices/api/JSGridExport/WordExport',
		exportToPdfAction: 'http://js.syncfusion.com/ExportingServices/api/JSGridExport/PdfExport',
		toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.ExcelExport, ej.Grid.ToolBarItems.WordExport, ej.Grid.ToolBarItems.PdfExport] },
		columns: [
					{ field: "OrderID", headerText: "Order ID", width: 75, textAlign: ej.TextAlign.Right },
					{ field: "CustomerID", headerText: "Customer ID", width: 80 },
					{ field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
					{ field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign: ej.TextAlign.Right },
					{ field: "ShipCity", headerText: "Ship City", width: 110 }
				]

		});

	});

</script>





{% endhighlight %}

![](Exporting_images/Exporting_img1.png)


## Server configuration

Currently grid data can be converted to different file formats in server-side only, through **EJ's** helper functions in .NET. So, to use exporting in your projects, it is required to create a server with any of the following web services. 

* Web API 
* WCF Service
* ASP.NET MVC Controller Action 
* ASP.NET WebMethod 

Following code snippet demonstrate exporting with WebAPI controller.

{% highlight c# %}

public class OrdersController: ApiController

{
	private NORTHWNDEntities db = new NORTHWNDEntities();
	public IEnumerable < Order > Get()
	{
		return db.Orders.ToList();
	}
	
	[System.Web.Http.ActionName("ExcelExport")]
	[AcceptVerbs("POST")]
	public void ExcelExport()
	{
		string gridModel = HttpContext.Current.Request.Params["GridModel"];
		GridProperties gridProperty = ConvertGridObject(gridModel);
		ExcelExport exp = new ExcelExport();
		IEnumerable < Order > result = db.Orders.ToList();
		exp.Export(gridProperty, result, "Export.xlsx", ExcelVersion.Excel2010, false, false, "flat-saffron");
	}
	
	[System.Web.Http.ActionName("PdfExport")]
	[AcceptVerbs("POST")]
	public void PdfExport()
	{
		string gridModel = HttpContext.Current.Request.Params["GridModel"];
		GridProperties gridProperty = ConvertGridObject(gridModel);
		PdfExport exp = new PdfExport();
		IEnumerable < Order > result = db.Orders.ToList();
		exp.Export(gridProperty, result, "Export.pdf");
	}
	
	[System.Web.Http.ActionName("WordExport")]
	[AcceptVerbs("POST")]
	public void WordExport()
	{
		string gridModel = HttpContext.Current.Request.Params["GridModel"];
		GridProperties gridProperties = ConvertGridObject(gridModel);
		WordExport exp = new WordExport();
		IEnumerable < Order > data = db.Orders.ToList();
		exp.Export(gridProperties, (IEnumerable) data, "Export.docx");
	}
	
	private GridProperties ConvertGridObject(string gridProperty)
	{
		JavaScriptSerializer serializer = new JavaScriptSerializer();
		IEnumerable div = (IEnumerable) serializer.Deserialize(gridProperty, typeof(IEnumerable));
		GridProperties gridProp = new GridProperties();
		foreach(KeyValuePair < string, object > datasource in div)
		{
			var property = gridProp.GetType()
				.GetProperty(datasource.Key, BindingFlags.Instance ' BindingFlags.Public ' BindingFlags.IgnoreCase);
			if (property != null)
			{
				Type type = property.PropertyType;
				string serialize = serializer.Serialize(datasource.Value);
				object value = serializer.Deserialize(serialize, type);
				property.SetValue(gridProp, value, null);
			}
		}
		return gridProp;
	}
}



{% endhighlight %}

### Server dependencies

Export Helper functions are available in the Assembly `Syncfusion.EJ.Export`, which is available in the Essential Studio & Essential JavaScript builds. Full list of assemblies needed for grid Export as follows

1. Syncfusion.EJ
2. Syncfusion.EJ.Export
3. Syncfusion.Linq.Base
4. Syncfusion.Compression.Base
5. Syncfusion.DocIO.Base
6. Syncfusion.XlsIO.Base
7. Syncfusion.PDF.Base

### Supported Export types


Currently server helper functions allows following three types of exporting 

* Word
* Excel
* PDF


## Multiple Grid export to single file


To export multiple grids in current page, the method `ej.Grid.exportAll` can be used with 'jquery selector' as the parameter.

The JavaScript code snippet for it is 

{% highlight javascript %}
	$('#exportAll').click(function(){
			ej.Grid.exportAll('MultipleExportToExcel',['#Grid1', '#Grid2']);
		});



{% endhighlight %}


The Server side C# snippet is

{% highlight c# %}

// Excel export

public void MultipleExportToExcel(string[] GridModel)

{
	ExcelExport exp = new ExcelExport();
	var EmployeeData = new NorthwindDataContext().EmployeeViews.Take(5).ToList();
	var OrderData = new NorthwindDataContext().OrdersViews.Take(5).ToList();
	bool initial = true;
	IWorkbook book = null;
	foreach(string gridProperty in GridModel)
	{
		GridProperties gridProp = ConvertObject(gridProperty);
		if (initial)
		{
			book = exp.Export(gridProp, EmployeeData, "Export.xlsx", ExcelVersion.Excel2010, true, true, "flat-saffron", true);
			initial = false;
		} 
		else
		{
			exp.Export(gridProp, OrderData, "Export.xlsx", ExcelVersion.Excel2010, true, true, "flat-saffron", false, book, MultipleExportType.AppendToSheet, "Second Grid");
		}

	}

}

// Word export

public void MultipleExportToWord(string[] GridModel)

{
	WordExport exp = new WordExport();
	var EmployeeData = new NorthwindDataContext().EmployeeViews.Take(5).ToList();
	var OrderData = new NorthwindDataContext().OrdersViews.Take(5).ToList();
	IWordDocument document = null;
	bool initial = true;;
	foreach(string gridProperty in GridModel)
	{
		GridProperties gridProp = ConvertObject(gridProperty);
		if (initial)
		{
			document = exp.Export(gridProp, EmployeeData, "Export.docx", true, true, "flat-saffron", true);
			initial = false;
		} else
		{
			exp.Export(gridProp, OrderData, "Export.docx", true, true, "flat-saffron", false, document, "Second Grid");
		}

	}

}

// PDF export

public void MultipleExportToPdf(string[] GridModel)

{
	PdfExport exp = new PdfExport();
	var EmployeeData = new NorthwindDataContext().EmployeeViews.Take(5).ToList();
	var OrderData = new NorthwindDataContext().OrdersViews.Take(5).ToList();
	PdfDocument document = null;
	bool initial = true;
	foreach(string gridProperty in GridModel)
	{
		GridProperties gridProp = ConvertObject(gridProperty);
		if (initial)
		{
			document = exp.Export(gridProp, EmployeeData, "Export.pdf", true, true, "flat-saffron", true);
			initial = false;
		} else

		{
			exp.Export(gridProp, OrderData, "Export.pdf", true, true, "flat-saffron", false, document, "Second Grid");
		}
	}
}


{% endhighlight %}

## List of properties ignored on export

Following are the list of properties that are exclude during grid export, to reduce the unwanted data transfer to server.  

* dataSource
* query
* rowTemplate
* detailsTemplate
* pageSettings
* enableRTL
* cssClass


##Export only visible records


By default `pageSettings` is ignored in export to facilitate all pages export. To achieve current visible page record export, `pageSettings` should be removed from ignore list using following code.

The snippet for this is.

{% highlight javascript %}

	var grid = $('#Grid').ejGrid('instance');
	grid.ignoreOnExport.splice(grid.ignoreOnExport.indexOf('pageSettings'), 1);

{% endhighlight %}

On server before calling the `Export` function, the data source should be processed using DataOperations's Execute function. 

{% highlight c# %}

public void ExportToExcel(string GridModel)
{
	ExcelExport exp = new ExcelExport();
	var DataSource = new NorthwindDataContext().OrdersViews.ToList();
	GridProperties properties = ConvertGridObject(GridModel);
	var dataSource = new DataOperations().Execute(GridModel, DataSource);
	exp.Export(properties, dataSource, "Export.xlsx", ExcelVersion.Excel2010, false, false, "flat-saffron");

}

public void ExportToWord(string GridModel)
{
	WordExport exp = new WordExport();
	var DataSource = new NorthwindDataContext().OrdersViews.ToList();
	GridProperties properties = ConvertGridObject(GridModel);
	var dataSource = new DataOperations().Execute(GridModel, DataSource);
	exp.Export(properties, dataSource, "Export.docx", false, false, "flat-saffron");
}
public void ExportToPdf(string GridModel)
{
	PdfExport exp = new PdfExport();
	var DataSource = new NorthwindDataContext().OrdersViews.ToList();
	GridProperties properties = ConvertGridProperties(GridModel);
	var dataSource = new DataOperations().Execute(GridModel, DataSource);
	exp.Export(properties, dataSource, "Export.pdf", false, false, "flat-saffron");
}

private GridProperties ConvertGridProperties(string gridProperty)
{
	JavaScriptSerializer serializer = new JavaScriptSerializer();
	IEnumerable div = (IEnumerable) serializer.Deserialize(gridProperty, typeof(IEnumerable));
	GridProperties gridProp = new GridProperties();
	foreach(KeyValuePair < string, propertiesSection > datasource in div)
	{
		var property = gridProp.GetType().GetProperty(datasource.Key, BindingFlags.Instance ' BindingFlags.Public ' BindingFlags.IgnoreCase);
		if (property != null)
		{
			Type type = property.PropertyType;
			string serialize = serializer.Serialize(datasource.Value);
			propertiesSection value = serializer.Deserialize(serialize, type);
			property.SetValue(gridProp, value, null);
		}
	}

	return gridProp;
}


{% endhighlight %}

## Local data 

By default, client data source is not sent to server to prevent unwanted data transfer since all data origin is server. In case, if you don't want to query the data source again for exporting in server, the grid's client [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource) can be sent to server on export postback by removing the [`dataSource`](https://help.syncfusion.com/api/js/ejgrid#members:datasource) property in grid's ignore list. The code snippet for this as follows

{% highlight javascript %}

var grid = $('#GridId').ejGrid('instance');
grid.ignoreOnExport.splice(grid.ignoreOnExport.indexOf('dataSource'), 1);

{% endhighlight %}


##Theme

The grid export have 13 theme option to match with our [built-in control themes](https://help.syncfusion.com/js/theming-in-essential-javascript-components#). They are

* default-theme
* flat-azure-dark
* flat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark
* bootstrap-theme

Also, it has `none` option which will export the grid without any theme.  The desired theme name can be passed as a parameter to `Export` method and the code snippet for this as follows

{% highlight c# %}

[System.Web.Http.ActionName("ExcelExport")]

[AcceptVerbs("POST")]

public void ExcelExport()

{
	string gridModel = HttpContext.Current.Request.Params["GridModel"];
	GridProperties gridProperty = ConvertGridObject(gridModel);
	ExcelExport exp = new ExcelExport();
	IEnumerable < Order > result = db.Orders.ToList();
	exp.Export(gridProperty, result, "Export.xlsx", ExcelVersion.Excel2010, false, false, " gradient-azure");
}

{% endhighlight %}

