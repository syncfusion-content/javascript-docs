---
layout: post
title: webAPI reference for DocIO
description: webAPI reference for DocIO
documentation: API
platform: js-webapi
keywords: DocIO, syncfusion,DocIO webapi
---

## ConvertToPDF

[POST&nbsp;&nbsp;/Api/DocIO/ConvertToPDF](http://js.syncfusion.com/demos/ejservices/api/DocIO/ConvertToPDF)

It is used to generate the PDF document.

### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Type: application/pdf

### Code example

```html

URL: http://js.syncfusion.com/demos/ejServices/api/DocIO/ConvertToPDF
<form name="form1" method="post" action="http://js.syncfusion.com/demos/ejservices/api/DocIO/ConvertToPDF" enctype="multipart/form-data">
	<div class="Common">
		<div class="tablediv">
			<div class="rowdiv">
				<label>
					This sample illustrates how to convert a Word document to PDF in ASP.NET Core application using Web API.
				</label>
				<label>
					Click the button to view the resultant PDF document being converted from Word document using Essential DocIO and Essential PDF.
					Please note that you need to have a PDF viewer installed in order to view the generated PDF file.
				</label>
			</div>
			<br />
			<div class="rowdiv">
				<div class="celldiv">
					<input name="file" type="file" value="Choose Word document" />
				</div>
				<br />
				<div class="celldiv">
					<input class="buttonStyle" type="submit" value="Convert to PDF" style="width: 200px;" />
				</div>
			</div>
			<br />
		</div>
	</div>
</form>

```

>Using the above code example we can convert the Word to PDF Document.