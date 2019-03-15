---
title: Getting Started for Syncfusion Essential JavaScript Spreadsheet
description: How to create a Spreadsheet with data source, apply format and export it as excel file.
platform: JS
control: Spreadsheet
documentation: ug
api: /api/js/ejspreadsheet
---
# Getting started

This section explains you the steps required to populate the Spreadsheet with data, format, and export it as excel file. This section covers only the minimal features that you need to know to get started with the Spreadsheet.

## Adding Script Reference

Create an HTML page and add the scripts references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
    <head>
        <!-- Essential Studio for JavaScript  theme reference -->
        <link rel="stylesheet" href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" />
        <!--  jquery script  -->
        <script src="https://code.jquery.com/jquery-1.10.2.min.js"></script>
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
        <script src="http://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js"></script>
        <!--  jsrender script  -->
        <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
        <!-- Essential JS UI widget -->    
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
        <!--Add custom scripts here -->
    </head>
    <body>
    </body>
</html>

{% endhighlight %}

In the above code, `ej.web.all.min.js` script reference has been added for demonstration purpose. It is not recommended to use this for deployment purpose, as its file size is larger since it contains all the widgets. Instead, you can use [`CSG`](http://csg.syncfusion.com "CSG") utility to generate a custom script file with the required widgets for deployment purpose.

N> For details about Spreadsheet internal and external dependencies refer following [`link`](https://help.syncfusion.com/js/spreadsheet/dependencies "link")

## Initialize Spreadsheet

Add a `div` container to render the Spreadsheet.

{% highlight html %}

<!DOCTYPE html>
<html>    
    <body>
        <div id="Spreadsheet"></div>
    </body>
</html>

{% endhighlight %}

Initialize the Spreadsheet by using the ejSpreadsheet method. The Spreadsheet is rendered based on default width and height. You can also customize the Spreadsheet dimension by setting the [`width`](https://help.syncfusion.com/api/js/ejspreadsheet#members:scrollsettings-width "width") and [`height`](https://help.syncfusion.com/api/js/ejspreadsheet#members:scrollsettings-height "height") property in [`scrollSettings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:scrollsettings "scrollSettings").

You can also use [`showRibbon`](https://help.syncfusion.com/api/js/ejspreadsheet#members:showribbon "showRibbon")and [`showPager`](https://help.syncfusion.com/api/js/ejspreadsheet#members:showpager "showPager") property to show/hide ribbon and pager in the spreadsheet.

The method[`showWaitingPopUp`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:showwaitingpopup "showWaitingPopUp") and [`hideWaitingPopUp`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:hidewaitingpopup "hideWaitingPopUp") is used to show/hide the waiting popup in the spreadsheet.

{% highlight html %}

<!DOCTYPE html>
<html>    
    <body>
        <script type="text/javascript">
            $(function () {
                $("#Spreadsheet").ejSpreadsheet();
            });
        </script>
    </body>
</html>

{% endhighlight %}

Now, the Spreadsheet is rendered with default row and column count.

![Getting-Started](Getting-Started_images/Getting-Started_img1.png)

## Populate Spreadsheet with data

Now, this section explains how to populate JSON data to the Spreadsheet. You can set [`dataSource`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets-datasource "dataSource") property in [`sheet`](https://help.syncfusion.com/api/js/ejspreadsheet#members:sheets "sheet") settings to populate JSON data in Spreadsheet.

{% highlight javascript %}

$("#Spreadsheet").ejSpreadsheet({
    // ...
    sheets: [{
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.js'
        dataSource: window.defaultData
    }]
    // ...
});

{% endhighlight %}


![Getting-Started](Getting-Started_images/Getting-Started_img2.png)

N> For more details about `data binding` refer following [`link`](https://help.syncfusion.com/js/spreadsheet/data-binding "link")

## Apply Conditional Formatting

Conditional formatting helps you to apply formats to a cell or range with certain color based on the cells values. You can use [`allowConditionalFormats`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowconditionalformats "allowConditionalFormats") property to enable/disable Conditional formats.

To apply conditional formats for a range use [`setCFRule`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlcformat-setcfrule "setCFRule") method. The following code example illustrates this,

{% highlight javascript %}

$("#Spreadsheet").ejSpreadsheet({
    // ...                                        
    loadComplete: "loadComplete"
    // ...
});

function loadComplete() {                
    this.XLCFormat.setCFRule({ action: "greaterthan", inputs: ["10"], color: "redft", range: "D2:D8" });
}

{% endhighlight %}

![Getting-Started](Getting-Started_images/Getting-Started_img3.png)

N> For more details about `Conditional Formatting` refer following [`link`](https://help.syncfusion.com/js/spreadsheet/data-presentation#conditional-formatting "link")

## Export Spreadsheet as Excel File

The Spreadsheet can save its data, style, format into an excel file. To enable save option in Spreadsheet set [`allowExporting`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings-allowexporting "allowExporting") option in [`exportSettings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings "exportSettings") as `true`. Since Spreadsheet uses server side helper to save documents set [`excelUrl`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings-excelurl "excelUrl") in [`exportSettings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings "exportSettings") option. The following code example illustrates this,

{% highlight javascript %}

$("#Spreadsheet").ejSpreadsheet({
    // ...                    
    exportSettings: {                        
        excelUrl: "http://js.syncfusion.com/demos/ejservices/api/Spreadsheet/ExcelExport"
    }                    
    // ...
});

{% endhighlight %}

Use shortcut [`Ctrl + S`](https://help.syncfusion.com/js/spreadsheet/keyboard-shortcuts "Ctrl + S") to save Spreadsheet as excel file.

N> 1. For more details about `Export` refer following [`link`](https://help.syncfusion.com/js/spreadsheet/open-and-save#save "link")
N> 2. For more details about `Server Configuration` refer following [`link`](https://help.syncfusion.com/js/spreadsheet/open-and-save#server-configuration "link")
N> 3. For more details about `Client dependencies` refer the following [`link`](https://help.syncfusion.com/js/spreadsheet/dependencies "link")
N> 4. For more details about `Server dependencies` refer the following [`link`](https://help.syncfusion.com/js/spreadsheet/open-and-save#server-dependencies "link")


