---
layout: post
title: ServerConfiguration 
description: serverconfiguration
platform: JS
control: Spreadsheet
documentation: ug
api: /api/js/ejspreadsheet
---

# Server Configuration

In Spreadsheet control, the import and export to and from excel is processed in server-side only, through Syncfusion.EJ.Export helper functions provided for .NET Framework. So, to use importing and exporting in your projects, it is required to create a server with any of the following web services. 

* WebAPI 
* WCF Service
* ASP.NET MVC Controller Action 
* ASP.NET WebForm's WebMethod 

Following code snippet demonstrate importing and exporting with WebAPI controller.

{% highlight c# %}
public class JSXLExportController: ApiController

{

	// GET API /

	[System.Web.Http.ActionName("ExportToExcel")]

	[AcceptVerbs("POST")]

	public void ExportToExcel()

	{

		string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"];

		SpreadSheet exp = new SpreadSheet();

		exp.Save(sheetModel, sheetData, "sample", ExportFormat.XLSX, ExcelVersion.Excel2013);

	}

	[System.Web.Http.ActionName("ExportToCsv")]

	[AcceptVerbs("Post")]

	public void ExportToCsv()

	{

		string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"];

		SpreadSheet exp = new SpreadSheet();

		exp.Save(sheetModel, sheetData, "sample", ExportFormat.CSV);

	}

	[OperationContract]

	[WebGet(BodyStyle = WebMessageBodyStyle.Bare)]

	[System.Web.Http.ActionName("Import")]

	[AcceptVerbs("Post")]

	public HttpResponseMessage Import()

	{

		var files = HttpContext.Current.Request.Files;

		if (files.Count > 0 && files[0].ContentType.IndexOf("image") > -1)

		return Img(files[0]);

		ImportRequest importRequest = new ImportRequest();

		if (files.Count == 0)

		importRequest.Url = HttpContext.Current.Request.Form["url"];

		else

		{

			var obj = files[0];

			importRequest.FileStream = obj.InputStream;

			importRequest.FileType = obj.FileName.Split('.')[obj.FileName.Split('.').Length - 1];

			importRequest.File = null;

		}

		SpreadSheet imp = new SpreadSheet();

		string str = imp.Open(importRequest);

		return new HttpResponseMessage() {
			Content = new StringContent(str, Encoding.UTF8, "text/plain")
		};

	}

	private HttpResponseMessage Img(HttpPostedFile importRequest)

	{

		string base64 = "";

		var file = importRequest;

		byte[] binaryData;

		binaryData = new Byte[file.InputStream.Length];

		file.InputStream.Read(binaryData, 0, (int) file.InputStream.Length);

		file.InputStream.Close();

		if (file.ContentType.StartsWith("image"))

		base64 = "data:" + file.ContentType + ";base64," + System.Convert.ToBase64String(binaryData, 0, binaryData.Length);

		else base64 = "Invalid file type";

		return new HttpResponseMessage() {
			Content = new StringContent(base64, Encoding.UTF8, "text/plain")
		};

	}

}
{% endhighlight %}

## Server dependencies

Import and Export Helper functions are available in the Assembly `Syncfusion.EJ.Export`, which is available in Essential Studio and Essential JavaScript builds. The full list of assemblies needed for Spreadsheet import and export is follows.

1. Syncfusion.EJ
2. Syncfusion.EJ.Export
3. Syncfusion.Linq.Base
4. Syncfusion.Compression.Base
5. Syncfusion.DocIO.Base
6. Syncfusion.XlsIO.Base
7. Syncfusion.PDF.Base

N> 1. The above mentioned assemblies will be available in below location after Essential Studio build installation.
N> 2. C:\Program Files (x86)\Syncfusion\Essential Studio\x.x.x.x\precompiledassemblies\x.x.x.x\y.y.
N> 3. x.x.x.x defines build version of Essential Studio and y.y defines .NET Framework version.