---
layout: post
title: Syncfusion webAPI reference for XlsIO
description: Learn about the Syncfusion Essential Studio XlsIO control's webAPI references to generate Excel document formats like XLS, Excel Template, etc.
documentation: ug
platform: js
keywords: XlsIO, syncfusion, excel webapi
---

# Create Excel document using WebAPI

## CreateDocument

[POST] [/Api/XlsIO/CreateDocument](http://js.syncfusion.com/demos/ejservices/api/XlsIO/CreateDocument)

To generate an Excel document format like XLS, XLSX, CSV, Excel Template, Excel Macro Enabled Template.

### URL parameters

|  Parameter | DataType |  Description | 
|---|---|---|
|SaveType (Mandatory)|string|Represents format of the Excel file. For example: XLS, XLSX, CSV, XLTX, XLTM.|
|ImportType (Optional)|string|Represents import data objects. For example: DataTable, BusinessObjects.|
|MarkerType (Optional)|string|Represents template marker types. For example: ImageOnly, ImageWithSize, ImageWithPosition, ImageWithSizeAndPosition, ImageFitToCell.|

### Response information 

Code: 200

Content-Type: Application/x-msexcel

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejservices/api/XlsIO/CreateDocument

     function formSubmit(){
           var fileVersion = document.querySelector('input[name = "ExcelVersion"]:checked').value;
			var attr = { action:window.baseurl + "api/XlsIO/CreateDocument", method: "post" };
            var form = ej.buildTag("form", "", null, attr);                        
            inputAttr = { name: "SaveType", type: "hidden", value: fileVersion };
            input = ej.buildTag("input", "", null, inputAttr);
            form.append(input);
            $("body").append(form);
            form.submit();
         }

{% endhighlight %}

> Using the above code example we can generate the Excel document with different formats.


## WriteFormula

[POST] [/Api/XlsIO/WriteFormula](http://js.syncfusion.com/demos/ejservices/api/XlsIO/WriteFormula)

Formulas are entries in Excel that have an equation that calculates the value to be displayed. This method will generate an Excel document with different formulae.  

### Response information 

Code: 200

Content-Type: Application/x-msexcel

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejservices/api/XlsIO/WriteFormula

    function Submit1(){
			var attr = { action:window.baseurl + "api/XlsIO/WriteFormula", method: "post" };
            var form = ej.buildTag("form", "", null, attr);                        
            $("body").append(form);
            form.submit();
         }
         }

{% endhighlight %}

> Using the above code example we can generate the Excel document with different formulae.


## ReadFormula

[POST] [/Api/XlsIO/ReadFormula](http://js.syncfusion.com/demos/ejservices/api/XlsIO/ReadFormula)

To read the formula string as well as value from the Excel document.

### Response information 

Code: 200

Content-Type: String 

Response:  Returns the string combination of value and formula with comma.

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejservices/api/XlsIO/ReadFormula

        $.ajax({
                    type: "POST",
                    url: window.baseurl + "api/XlsIO/ReadFormula",
					dataType: "json", //Expected data format from server
                    processdata: true, //True or False
                    success: function (msg) {//On Successfull API call
                        var data=msg.split(",");
						$("#txtFormulaNumber")[0].textContent=data[0];
						$("#txtFormula")[0].textContent=data[1];
                    },
            });     

{% endhighlight %}

> Using the above code we can get the string combination of value and formula with comma.


## CreateChart

[POST] [/Api/XlsIO/CreateChart](http://js.syncfusion.com/demos/ejservices/api/XlsIO/CreateChart)

To generate an embedded chart Excel document with different formats.

### URL parameters

|  Parameter | DataType |  Description | 
|---|---|---|
|SaveType (Mandatory)|string|Represents format of the Excel file. For example: XLS, XLSX.|
|ImportType (Optional)|string|Represents import data objects. For example: DataTable, BusinessObjects.|
|MarkerType (Optional)|string|Represents template marker types. For example: ImageOnly, ImageWithSize, ImageWithPosition, ImageWithSizeAndPosition, ImageFitToCell.|

### Response information 

Code: 200

Content-Type: Application/x-msexcel

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejservices/api/XlsIO/CreateChart

     function formSubmit(){
           var fileVersion = document.querySelector('input[name = "ExcelVersion"]:checked').value;
			var attr = { action:window.baseurl + "api/XlsIO/CreateChart", method: "post" };
            var form = ej.buildTag("form", "", null, attr);                        
            inputAttr = { name: "SaveType", type: "hidden", value: fileVersion };
            input = ej.buildTag("input", "", null, inputAttr);
            form.append(input);
            $("body").append(form);
            form.submit();
         }

{% endhighlight %}

> Using the above code example we can generate an embedded chart Excel document with different formats.


## ImportDataObject

[POST] [/Api/XlsIO/ImportDataObject](http://js.syncfusion.com/demos/ejservices/api/XlsIO/ImportDataObject)

To import data directly from various objects like DataTable, Business Objects, etc to an Excel document.

### URL parameters

|  Parameter | DataType |  Description | 
|---|---|---|
|SaveType (Optional)|string|Represents format of the Excel file. For example: XLS, XLSX.|
|ImportType (Mandatory)|string|Represents import data objects. For example: DataTable, BusinessObjects.|
|MarkerType (Optional)|string|Represents template marker types. For example: ImageOnly, ImageWithSize, ImageWithPosition, ImageWithSizeAndPosition, ImageFitToCell.|

### Response information 

Code: 200

Content-Type: Application/x-msexcel

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejservices/api/XlsIO/ImportDataObject

     function formSubmit1(){
            var option1 = document.querySelector('input[name = "ImportType"]:checked').value;
		    var attr = { action:window.baseurl + "api/XlsIO/ImportDataObject", method: "post" };
            var form = ej.buildTag("form", "", null, attr);                        
            inputAttr = { name: "ImportType", type: "hidden", value: option1 };
            input = ej.buildTag("input", "", null, inputAttr);
			form.append(input);
            $("body").append(form);
            form.submit();
         }

{% endhighlight %}

> Using the above code example we can generate an Excel document with imported data.


## ApplyTemplateMarker

[POST] [/Api/XlsIO/ApplyTemplateMarker](http://js.syncfusion.com/demos/ejservices/api/XlsIO/ApplyTemplateMarker)

Import data to an Excel document using [template marker](https://help.syncfusion.com/file-formats/xlsio/working-with-template-markers).

### URL parameters

|  Parameter | DataType |  Description | 
|---|---|---|
|SaveType (Optional)|string|Represents format of the Excel file. For example: XLS, XLSX.|
|ImportType (Mandatory)|string|Represents import data objects. For example: DataTable, BusinessObjects.|
|MarkerType (Mandatory)|string|Represents template marker types. For example: ImageOnly, ImageWithSize, ImageWithPosition, ImageWithSizeAndPosition, ImageFitToCell.|

### Response information 

Code: 200

Content-Type: Application/x-msexcel

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejservices/api/XlsIO/ApplyTemplateMarker

    function formSubmit1(){
            var option1 = document.querySelector('input[name = "ImportType"]:checked').value;
		    var option2 = document.querySelector('input[name = "MarkerType"]:checked').value;
			var attr = { action:window.baseurl + "api/XlsIO/ApplyTemplateMarker", method: "post" };
            var form = ej.buildTag("form", "", null, attr);                        
            inputAttr = { name: "ImportType", type: "hidden", value: option1 };
            input = ej.buildTag("input", "", null, inputAttr);
			form.append(input);
			inputAttr = { name: "MarkerType", type: "hidden", value: option2 };
            input = ej.buildTag("input", "", null, inputAttr);
            form.append(input);
            $("body").append(form);
            form.submit();
         }

{% endhighlight %}

> Using the above code example we can generate an Excel document with imported data using template marker.


## InputTemplate

[POST] [/Api/XlsIO/InputTemplate](http://js.syncfusion.com/demos/ejservices/api/XlsIO/InputTemplate)

To get an Excel template document used for various template marker types.

### URL parameters

|  Parameter | DataType |  Description | 
|---|---|---|
|SaveType (Optional)|string|Represents format of the Excel file. For example: XLS, XLSX.|
|ImportType (Optional)|string|Represents import data objects. For example: DataTable, BusinessObjects.|
|MarkerType (Mandatory)|string|Represents template marker types. For example: ImageOnly, ImageWithSize, ImageWithPosition, ImageWithSizeAndPosition, ImageFitToCell.|

### Response information 

Code: 200

Content-Type: Application/x-msexcel

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejservices/api/XlsIO/ApplyInputTemplate

    function formSubmit2(){
		    var option2 = document.querySelector('input[name = "MarkerType"]:checked').value;
			var attr = { action:window.baseurl + "api/XlsIO/InputTemplate", method: "post" };
            var form = ej.buildTag("form", "", null, attr);                        
            inputAttr = { name: "MarkerType", type: "hidden", value: option2 };
            input = ej.buildTag("input", "", null, inputAttr);
			form.append(input);
            $("body").append(form);
            form.submit();
         }

{% endhighlight %}

> Using the above code example we can generate an Excel template document for various template marker.