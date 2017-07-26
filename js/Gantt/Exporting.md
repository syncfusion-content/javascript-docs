---
layout: post
title: Exporting
description: exporting
platform: js
control: Gantt
documentation: ug
---
# Export

Gantt provides support to export the contents in PDF and excel. To export the contents, the `ExcelExport` and `PdfExport` toolbar items must be included in the [toolbarSettings.toolbarItems](https://help.syncfusion.com/api/js/ejgantt#members:toolbarsettings-toolbaritems) property. And you need to call the `export` method with the export mapper as parameter in the toolbar button click action. 

The below code snippet explains the above behavior,

{% highlight javascript %}

$("#Gantt").ejGantt({
    //...
    toolbarSettings: {
        showToolbar: true,
        toolbarItems: [
            ej.Gantt.ToolbarItems.ExcelExport,
            ej.Gantt.ToolbarItems.PdfExport
        ]
    },

    toolbarClick: toolbarClick
    //...
});

function toolbarClick(args) {
    var id = $(args.currentTarget).attr("id");
    this.exportGantt = this["export"];

    if (id == "GanttContainer_pdfExport") {
        this. exportGantt("http://js.syncfusion.com/demos/ejServices/api/Gantt/PdfExport", "", false);
            args.cancel = true;
        }

        if (id == "GanttContainer_excelExport") {
            this. exportGantt("http://js.syncfusion.com/demos/ejServices/api/Gantt/ExcelExport", "", false);
                args.cancel = true;
        }
}

{% endhighlight %}

The PDF and Excel exporting services for Gantt are explained in detail [here](https://help.syncfusion.com/js/gantt/services-reference).

The below screen shot shows Gantt with excel and Pdf exporting enabled.
![](/js/Gantt/Export_images/Export_img1.png)

## Server Configuration
Gantt data can be converted to PDF and excel file formats in server side only, through EJ’s helper functions in .NET. 
To use Gantt pdf export in projects, it is required to create a server with any of the following web services. 

* Web API
* WCF Service
* ASP.NET MVC Controller Action
* ASP.NET WebMethod

Following code snippet demonstrate exporting with Web API controller.

{% highlight c# %}

public class GanttController : ApiController
{       
        [System.Web.Http.ActionName("ExcelExport")]
        [AcceptVerbs("POST")]
        public void ExcelExport()
        {
            string ganttModel = HttpContext.Current.Request.Params["GanttModel"];
            GanttProperties ganttProperty = ConvertGanttObject(ganttModel);
            ExcelExport exp = new ExcelExport();
            TaskDetailsCollection task = new TaskDetailsCollection();
            IEnumerable<TaskDetails> data = task.GetDataSource();
            exp.Export(ganttProperty, data, "ExcelExport.xlsx", ExcelVersion.Excel2010, new GanttExportSettings() { Theme = ExportTheme.FlatAzure });
        }
       
        [System.Web.Http.ActionName("PdfExport")]
        [AcceptVerbs("POST")]
        public void GanttPdfExport()
        {
            string ganttModel = HttpContext.Current.Request.Params["GanttModel"];
            string locale = HttpContext.Current.Request.Params["locale"];
            GanttProperties ganttProperty = ConvertGanttObject(ganttModel);
            PdfExport exp = new PdfExport();
            TaskDetailsCollection task = new TaskDetailsCollection();
            IEnumerable<TaskDetails> data = task.GetDataSource();
            GanttPdfExportSettings settings = new GanttPdfExportSettings();
            settings.EnableFooter = true;
            settings.IsFitToWidth = isFitToWidth;
            settings.ProjectName = "Project Tracker";
            settings.Locale = locale;
            exp.Export(ganttProperty, data, settings, "Gantt");
        }

        private GanttProperties ConvertGanttObject(string ganttProperty)
        {
            JavaScriptSerializer serializer = new JavaScriptSerializer();
            IEnumerable div = (IEnumerable)serializer.Deserialize(ganttProperty, typeof(IEnumerable));
            GanttProperties ganttProp = new GanttProperties();
            foreach (KeyValuePair<string, object> dataSource in div)
            {
                var property = ganttProp.GetType().GetProperty(dataSource.Key, BindingFlags.Instance | BindingFlags.Public | BindingFlags.IgnoreCase);
                if (property != null)
                {
                    Type type = property.PropertyType;
                    string serialize = serializer.Serialize(dataSource.Value);
                    object value = serializer.Deserialize(serialize, type);
                    property.SetValue(ganttProp, value, null);
                }
            }
            return ganttProp;
        }
 }

{% endhighlight %}


## Server dependencies
Export Helper functions are available in the Assembly Syncfusion.EJ.Export, which is available in the Essential Studio & Essential JavaScript builds. The list of assemblies needed for Gantt Export as follows

* Syncfusion.EJ
* Syncfusion.EJ.Export
* Syncfusion.Linq.Base
* Syncfusion.Compression.Base
* Syncfusion.XlsIO.Base
* Syncfusion.PDF.Base

## Export Theme
The Gantt export supports the below themes, 

* flat-azure
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

The desired theme should be passed as a parameter to the Export method and the code snippet for this as follows

{% highlight c# %}

[System.Web.Http.ActionName("ExcelExport")]
[AcceptVerbs("POST")]
public void ExcelExport()
{
   string ganttModel = HttpContext.Current.Request.Params["GanttModel"];
   GanttProperties ganttProperty = ConvertGridObject(ganttModel);
   ExcelExport exp = new ExcelExport();
   TaskDetailsCollection task = new TaskDetailsCollection();
   IEnumerable<TaskDetails> data = task.GetDataSource();
   exp.Export(ganttProperty, data, "ExcelExport.xlsx", ExcelVersion.Excel2010, new GanttExportSettings() { Theme = ExportTheme.FlatAzure });
}

{% endhighlight %}