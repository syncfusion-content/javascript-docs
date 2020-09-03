---
layout: post
title: Exporting
description: exporting
platform: js
control: Gantt
documentation: ug
---
# Export

Gantt provides support to export the contents in PDF and excel. To export the contents, the `ExcelExport` and `PdfExport` toolbar items must be included in the [`toolbarSettings.toolbarItems`](https://help.syncfusion.com/api/js/ejgantt#members:toolbarsettings-toolbaritems) property. And you need to call the [`export`](/api/js/ejgantt#methods:export "export(action, [serverEvent], [multipleExport])") method with the export mapper as parameter in the toolbar button click action. We can export multiple Gantt control in same file by using multiple exporting support, this can be enabled by setting [`allowMultipleExporting`](/api/js/ejgantt#members:allowmultipleexporting) property as `true`.

The below code snippet explains the above behavior.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
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

The below screen shot shows Gantt with excel and PDF exporting enabled.
![](/js/Gantt/Export_images/Export_img1.png)

## Server Configuration
Gantt data can be converted to PDF and excel file formats in server-side only, through EJ’s helper functions in .NET. 
To use Gantt PDF export in projects, it is required to create a server with any of the following web services. 

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
Export Helper functions are available in the Assembly Syncfusion.EJ.Export, which is available in the Essential Studio & Essential JavaScript builds. The list of assemblies needed for Gantt Export as follows.

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

The desired theme should be passed as a parameter to the Export method and the code snippet for this as follows.

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

## Customization

In Gantt, we can customize Grid cells, taskbars in Excel and PDF files by using exporting events. While exporting the Gantt as Excel or PDF files, events are triggered to customize the Grid cells and taskbars.

### Customize Excel cell

Excel cells can be customized by using `ServerExcelQueryCellInfo` event, in this event we can get the details about current record, Excel cell and current column information. Using this information we can customize the background color, font color and value of Excel cell, please find the event argument details below.

<table>
<tr>
<th>Name</th><th>Description</th><th>Type</th>
</tr>
<tr>
<td>Data</td><td>Returns the current row details </td><td>GanttRecordDetails</td>
</tr>
<td>Cell</td><td>Returns current Excel cell information</td><td>IRange</td>
</tr>
<tr>
<td>Column</td><td>Returns current column information</td><td>GanttColumn</td>
</tr>
</table>

The following code snippets shows how to bind `ServerExcelQueryCellInfo` event in Web API controller and how to customize Excel cell using this event.

{% highlight c# %}

    public class GanttController : ApiController
    {
        GanttProperties.GanttEJExportEventHandler queryExcelCellDelegate = new GanttProperties.GanttEJExportEventHandler(GanttExcelQueryCell);

        [System.Web.Http.ActionName("ExcelCustomExport")]
        [AcceptVerbs("POST")]
        public void ExcelCustomExport()
        {
            string gridModel = HttpContext.Current.Request.Params["GanttModel"];
            GanttProperties controlProperty = ConvertGridObject(gridModel);
            `controlProperty.ServerExcelQueryCellInfo = queryExcelCellDelegate;`
            ExcelExport exportObject = new ExcelExport();
            TaskDetailsCollection taskDetails = new TaskDetailsCollection();
            IEnumerable<TaskDetails> result = taskDetails.GetExportDataSource();
            exportObject.Export(controlProperty, result, "ExcelExport.xlsx", ExcelVersion.Excel2010, new GanttExportSettings() { Theme = ExportTheme.FlatAzure });
        }
        
        public static void GanttExcelQueryCell(object model, object arguments)
        {
            var record = (GanttRecordDetails)((Dictionary<string, object>)arguments)["Data"];
            var cell = (IRange)((Dictionary<string, object>)arguments)["Cell"];
            var column = (GanttColumn)((Dictionary<string, object>)arguments)["Column"];
            var ganttModel = (GanttProperties)model;

            if (column.MappingName == ganttModel.ProgressMapping && !record.IsParentRow)
            {
                if (float.Parse(cell.Value) > 80)
                    cell.CellStyle.Color = ColorConversion.GetColor(new PdfColor(165, 105, 189));
                else if (float.Parse(cell.Value) < 20)
                    cell.CellStyle.Color = ColorConversion.GetColor(new PdfColor(240, 128, 128));
            } 
        }

        private GanttProperties ConvertGridObject(string controlProperty)
        {
            JavaScriptSerializer serializer = new JavaScriptSerializer();
            IEnumerable outputObject = (IEnumerable)serializer.Deserialize(controlProperty, typeof(IEnumerable));
            GanttProperties gridProp = new GanttProperties();
            foreach (KeyValuePair<string, object> currentProperty in outputObject)
            {
                var property = gridProp.GetType().GetProperty(currentProperty.Key, BindingFlags.Instance | BindingFlags.Public | BindingFlags.IgnoreCase);
                if (property != null)
                {
                    Type type = property.PropertyType;
                    string serialize = serializer.Serialize(currentProperty.Value);
                    object value = serializer.Deserialize(serialize, type);
                    property.SetValue(gridProp, value, null);
                }
            }
            return gridProp;
        }
    }
      
{% endhighlight %}

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/export/conditionalformatting) here to view the online demo sample with above code example.

N> Refer this [link](https://help.syncfusion.com/cr/aspnetmvc/Syncfusion.XlsIO.IExtendedFormat.html) to know more about what are the properties are available in Excel cell and it's type values.

### Customize PDF cell

PDF cells in Gantt can be customized by using `ServerPdfQueryCellInfo` event, in this event we can get the details about current record, PDF cell and current column information. Using this information we can customize the background color and font color of PDF cells, please find the event argument details below.

<table>
<tr>
<th>Name</th><th>Description</th><th>Type</th>
</tr>
<tr>
<td>Data</td><td>Returns the current row details </td><td>GanttRecord</td>
</tr>
<td>Cell</td><td>Returns current Excel cell information</td><td>PdfTreeGridCell</td>
</tr>
<tr>
<td>Column</td><td>Returns current column information</td><td>GanttColumn</td>
</tr>
</table>

The following code snippets shows how to bind `ServerPdfQueryCellInfo` event in Web API controller and how to customize PDF cell using this event.


{% highlight c# %}

    public class GanttController : ApiController
    {
        GanttProperties.GanttEJExportEventHandler queryCellDelegate = new GanttProperties.GanttEJExportEventHandler(GanttPdfQueryCell);

        [System.Web.Http.ActionName("PdfCustomExport")]
        [AcceptVerbs("POST")]
        public void PdfCustomExport()
        {
            string gridModel = HttpContext.Current.Request.Params["GanttModel"];
            string locale = HttpContext.Current.Request.Params["locale"];
            GanttProperties gridProperty = ConvertGridObject(gridModel);
            `gridProperty.ServerPdfQueryCellInfo = queryCellDelegate;`
            PdfExport export = new PdfExport();
            TaskDetailsCollection taskCollection = new TaskDetailsCollection();
            IEnumerable<TaskDetails> result = taskCollection.GetExportDataSource();
            GanttPdfExportSettings settings = new GanttPdfExportSettings();
            settings.EnableFooter = true;
            settings.IsFitToWidth = true;
            settings.ProjectName = "Project Tracker";
            settings.Locale = locale;
            export.Export(gridProperty, result, settings, "Gantt");
        }

        public static void GanttPdfQueryCell(object model, object arguments)
        {
            var record = (GanttRecord)((Dictionary<string, object>)arguments)["Data"];
            var cell = (PdfTreeGridCell)((Dictionary<string, object>)arguments)["Cell"];
            var column = (GanttColumn)((Dictionary<string, object>)arguments)["Column"];
            var ganttModel = (GanttProperties)model;

            if (column.MappingName == ganttModel.ProgressMapping && !record.IsParentRow)
            {
                if (record.Progress > 80)
                {
                    PdfBrush color = new PdfSolidBrush(new PdfColor(165, 105, 189));
                    cell.Style.BackgroundBrush = color;
                }
                else if (record.Progress < 20)
                {
                    PdfBrush color = new PdfSolidBrush(new PdfColor(240, 128, 128));
                    cell.Style.BackgroundBrush = color;
                }
            }       
        }

        private GanttProperties ConvertGridObject(string controlProperty)
        {
            JavaScriptSerializer serializer = new JavaScriptSerializer();
            IEnumerable outputObject = (IEnumerable)serializer.Deserialize(controlProperty, typeof(IEnumerable));
            GanttProperties gridProperty = new GanttProperties();
            foreach (KeyValuePair<string, object> currentProperty in outputObject)
            {
                var property = gridProperty.GetType().GetProperty(currentProperty.Key, BindingFlags.Instance | BindingFlags.Public | BindingFlags.IgnoreCase);
                if (property != null)
                {
                    Type type = property.PropertyType;
                    string serialize = serializer.Serialize(currentProperty.Value);
                    object value = serializer.Deserialize(serialize, type);
                    property.SetValue(gridProperty, value, null);
                }
            }
            return gridProperty;
        }
    }

{% endhighlight %}

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/export/conditionalformatting) here to view the online demo sample with above code example.

N> Refer this [link](http://help.syncfusion.com/cr/cref_files/aspnetmvc/Syncfusion.EJ.Export~Syncfusion.EJ.Export.PdfTreeGridCellStyle_members.html) to know more about what are the properties are available in PDF cell and it's type values.

### Customize PDF taskbar

PDF taskbars in Gantt can be customized by using `ServerPdfQueryTaskbarInfo` event, in this event we can get the details about current record and taskbar information. Using this information we can customize the background color of taskbar and progress bar, please find the event argument details below.

<table>
<tr>
<th>Name</th><th>Description</th><th>Type</th>
</tr>
<tr>
<td>Data</td><td>Returns the current row details </td><td>GanttRecord</td>
</tr>   
<td>Taskbar</td><td>Returns current Excel cell information</td><td>PdfGanttTaskbar</td>
</tr>
</table>

The following code snippets shows how to bind `ServerPdfQueryTaskbarInfo` event in Web API controller and how to customize PDF taskbar using this event.


{% highlight c# %}

    public class GanttController : ApiController
    {
        GanttProperties.GanttEJExportEventHandler queryTaskbarDelegate = new GanttProperties.GanttEJExportEventHandler(GanttQueryTaskbar);

        [System.Web.Http.ActionName("PdfCustomExport")]
        [AcceptVerbs("POST")]
        public void PdfCustomExport()
        {
            string gridModel = HttpContext.Current.Request.Params["GanttModel"];
            string locale = HttpContext.Current.Request.Params["locale"];
            GanttProperties gridProperty = ConvertGridObject(gridModel);
            `gridProperty.ServerPdfQueryTaskbarInfo = queryTaskbarDelegate;`
            PdfExport export = new PdfExport();
            TaskDetailsCollection taskCollection = new TaskDetailsCollection();
            IEnumerable<TaskDetails> result = taskCollection.GetExportDataSource();
            GanttPdfExportSettings settings = new GanttPdfExportSettings();
            settings.EnableFooter = true;
            settings.IsFitToWidth = true;
            settings.ProjectName = "Project Tracker";
            settings.Locale = locale;
            export.Export(gridProperty, result, settings, "Gantt");
        }

        public static void GanttQueryTaskbar(object model, object arguments)
        {
            var record = (GanttRecord)((Dictionary<string, object>)arguments)["Data"];
            var taskbar = (PdfGanttTaskbar)((Dictionary<string, object>)arguments)["Taskbar"];
            if (!record.IsParentRow)
            {
                if (record.Progress > 80)
                {
                    taskbar.ProgressColor = new PdfColor(108, 52, 131);
                    taskbar.TaskBorderColor = taskbar.TaskColor = new PdfColor(165, 105, 189);
                }
                else if (record.Progress < 20)
                {
                    taskbar.ProgressColor = new PdfColor(205, 92, 92);
                    taskbar.TaskBorderColor = taskbar.TaskColor = new PdfColor(240, 128, 128);
                }
            }
        }

        private GanttProperties ConvertGridObject(string controlProperty)
        {
            JavaScriptSerializer serializer = new JavaScriptSerializer();
            IEnumerable outputObject = (IEnumerable)serializer.Deserialize(controlProperty, typeof(IEnumerable));
            GanttProperties gridProperty = new GanttProperties();
            foreach (KeyValuePair<string, object> currentProperty in outputObject)
            {
                var property = gridProperty.GetType().GetProperty(currentProperty.Key, BindingFlags.Instance | BindingFlags.Public | BindingFlags.IgnoreCase);
                if (property != null)
                {
                    Type type = property.PropertyType;
                    string serialize = serializer.Serialize(currentProperty.Value);
                    object value = serializer.Deserialize(serialize, type);
                    property.SetValue(gridProperty, value, null);
                }
            }
            return gridProperty;
        }
    }

{% endhighlight %}

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/export/conditionalformatting) here to view the online demo sample with above code example.
