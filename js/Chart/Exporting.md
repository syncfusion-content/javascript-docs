---
layout: post
title: Exporting options in Essential JavaScript Chart
description: Learn how to export Chart as excel file or image.
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Exporting Chart

The exporting of the chart is done using the [`exportSettings`](../api/ejchart#members:exportsettings) property. The chart  export can be done in both client-side and in server-side.This can be modified by setting values to the property [`mode`](../api/ejchart#members:exportsettings-mode) in exporting. Default value for mode is client. 

## Client-side Exporting

In client-side rendered chart can be exported as PNG image or as SVG file.The type of export is controlled by using the [`type`](../api/ejchart#members:exportsettings-type)property of the exportSettings.

* Export as PNG - The chart can be exported to image when it is rendered in HTML5 Canvas.To render a chart in canvas, set the [`enableCanvasRendering`](../api/ejchart#members:enablecanvasrendering) option to *true*. To export the chart, you can use the [`export`](../api/ejchart#methods:export) method of the chart. Refer to the online [`KB for exporting`](http://www.syncfusion.com/kb/5045) to know more about chart exporting. 

* Export as SVG - Chart can be exported as SVG if it is rendered as a scalable vector graphics element. By default chart will be rendered as SVG. 

{% highlight html %}
<body>
    <!--Chart download link-->
    <a id="download" style="cursor: pointer; position: absolute;right: 150px;">ExportChart</a>
    <div id="container"></div>
    <script>
        $("#container").ejChart({

            // ...
            //Enable Canvas mode to export chart as image
            enableCanvasRendering: true,

            //Setting up required exporting options
            exportSettings: { type: "png", mode: "client", fileName: "ChartSnapshot" }
        });

        function download() {
            var canvas = $("#container").ejChart("export");
            this.href = canvas;
        }
        if (document.getElementById('download').addEventListener)
            document.getElementById('download').addEventListener('click', download, false);
        else
            document.getElementById('download').attachEvent('onclick', download, false);
    </script>
</body>


{% endhighlight %}

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/chart/exportandprint) here to view the Export chart online demo sample.

## Server-side Exporting

Server-side operation can be done by using the server-side frameworks such as WebApi, WCF service to achieve exporting.

### Server side implementation

* To convert the chart data from client to server-side, refer to the following steps.
* Create an MVC application and add a controller.
* Add Syncfusion.EJ, Syncfusion.EJ.MVC and Syncfusion.EJ.Export as references to the application.
* Parse the data from client in MVC controller and export the chart to client.
* Host the MVC application in your server and get the link for exporting action method. The [`action`](../api/ejchart#members:exportsettings-action) property is used for specifying the hosted link. Example: http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport.
* To pass client data to server-side, you need to call the export method and pass export type (either image or excel) and server-side URL as an argument. The third argument of the export method is a Boolean property that specifies whether only the current chart should be exported or all charts in page should be exported.

{% highlight html %}
<body>
    <!--Export Chart-->
    <a id="download" style="cursor: pointer; position:absolute;">
        <button onclick="download()" value="Export">Export</button>
    </a>
    <div id="container"></div>

    <script>
        //Render Chart
        $("#container").ejChart(
         {
             enableCanvasRendering: true,
             exportSettings: { type: "jpg", action: "http://js.syncfusion.com/ExportingServices/api/JSChartExport/Export" },
         });

        //Export chart to excel
        function download() {
            $("#container").ejChart("export");
        }

    </script>
</body>

{% endhighlight %}

At the server side, chart can be exported as JPG, PNG, SVG, PDF, word document and as excel documents. For this the following code have to place in the controller.

{% highlight csharp %}

public void ExportChart(string Data, string ChartModel)
        {
            // declaration
            ChartProperties obj = ConvertChartObject(ChartModel);
            string type = obj.ExportSettings.Type.ToString().ToLower();
            string fileName = obj.ExportSettings.FileName;
            string orientation = obj.ExportSettings.Orientation.ToString();

            if (type == "svg")      // for svg export
            {
                StringWriter oStringWriter = new StringWriter();
                string data = HttpUtility.HtmlDecode(Data);
                data = HttpUtility.UrlDecode(Data);
                data = System.Uri.UnescapeDataString(Data);
                oStringWriter.WriteLine(System.Uri.UnescapeDataString(Data));
                Response.ContentType = "text/plain";
                Response.AddHeader("Content-Disposition", String.Format("attachment;filename={0}", (obj.ExportSettings.FileName + ".svg")));
                Response.Clear();
                using (StreamWriter writer = new StreamWriter(Response.OutputStream))
                {
                    data = oStringWriter.ToString();
                    writer.Write(oStringWriter.ToString());
                }
                Response.End();
            }

            else if (type == "xlsx")       // to export chart as excel
            {
                List<ExportChartData> chartData = new List<ExportChartData>();
                chartData.Add(new ExportChartData("John", 10));
                chartData.Add(new ExportChartData("Jake", 12));
                chartData.Add(new ExportChartData("Peter", 18));
                chartData.Add(new ExportChartData("James", 11));
                chartData.Add(new ExportChartData("Mary", 9.7));

                ExcelExport exp = new ExcelExport();
                exp.Export(obj, (IEnumerable)chartData, fileName + ".xlsx", ExcelVersion.Excel2010, null, null);
            }

            else
            {
                Data = Data.Remove(0, Data.IndexOf(',') + 1);
                MemoryStream stream = new MemoryStream(Convert.FromBase64String(Data));

                if (type == "docx")        // to export as word document
                {
                    WordDocument document = new WordDocument();
                    IWSection section = document.AddSection();
                    IWParagraph paragraph = section.AddParagraph();
                    if (obj.ExportSettings.Orientation.ToString() == "Landscape")
                        section.PageSetup.Orientation = PageOrientation.Landscape;
                    else
                        section.PageSetup.Orientation = PageOrientation.Portrait;
                    paragraph.AppendPicture(Image.FromStream(stream));
                    document.Save(fileName + ".doc", Syncfusion.DocIO.FormatType.Doc, HttpContext.ApplicationInstance.Response, Syncfusion.DocIO.HttpContentDisposition.Attachment);
                }
                else if (type == "pdf")      // to export as PDF
                {
                    PdfDocument pdfDoc = new PdfDocument();
                    pdfDoc.Pages.Add();
                    if (obj.ExportSettings.Orientation.ToString() == "Landscape")
                        pdfDoc.Pages[0].Section.PageSettings.Orientation = PdfPageOrientation.Landscape;
                    else
                        pdfDoc.Pages[0].Section.PageSettings.Orientation = PdfPageOrientation.Portrait;
                    pdfDoc.Pages[0].Graphics.DrawImage(PdfImage.FromStream(stream), new PointF(10, 30));
                    pdfDoc.Save(obj.ExportSettings.FileName + ".pdf", HttpContext.ApplicationInstance.Response, HttpReadType.Save);
                    pdfDoc.Close();
                }
                else                        // to export as image
                {
                    stream.WriteTo(Response.OutputStream);
                    Response.ContentType = "application/octet-stream";
                    Response.AddHeader("Content-Disposition", String.Format("attachment;filename={0}", fileName + "." + type));
                    Response.Flush();
                    stream.Close();
                    stream.Dispose();
                }
            }
        }
      
        private ChartProperties ConvertChartObject(string ChartModel)
        {
            JavaScriptSerializer serializer = new JavaScriptSerializer();
            IEnumerable div = (IEnumerable)serializer.Deserialize(ChartModel, typeof(IEnumerable));
            ChartProperties chartProp = new ChartProperties();
            foreach (KeyValuePair<string, object> d in div)
            {
                var property = chartProp.GetType().GetProperty(d.Key, BindingFlags.Instance | BindingFlags.Public | BindingFlags.IgnoreCase);
                if (property != null)
                {
                    Type type = property.PropertyType;
                    string serialize = serializer.Serialize(d.Value);
                    object value = serializer.Deserialize(serialize, type);
                   property.SetValue(chartProp, value, null);
                }
            }
            return chartProp;
        }


{% endhighlight %}

### Excel Exporting

Excel exporting is a server-side operation. In addition have to refer Syncfusion.XlsIO assembly to export as excel.

![](/js/Chart/Exporting_images/Exporting_img1.png)

#### Multiple chart excel exporting

EjChart supports exporting more than one charts in a page, with the third argument for the export method.

N> Refer the MultipleExportType.AppendToSheet, MultipleExportType.NewSheet.

{% highlight javascript %}
    //Render Chart1
       $("#container1").ejChart();

       //Render Chart2
        $("#container2").ejChart();

       //Export multiple chart to excel
        function downloadExcel() {
            var chart = $("#container1").ejChart("instance");
            chart.export('Excel',
                      'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport', true);
        }

{% endhighlight %}

Export multiple chart to excel at server-side

{% highlight csharp %}

    public class JSChartExportController : ApiController
        {

            [System.Web.Http.ActionName("ExcelExport")]
            [AcceptVerbs("POST")]
            public void ExcelExport()
            {
                string chartModel = HttpContext.Current.Request.Params["ChartModel"];
                IWorkbook book = null;

                foreach (string chartProperty in ChartModel)
                {
                    if (chartProperty != null)
                    {
                        ExcelExport exp = new ExcelExport();

                        ChartProperties obj = ConvertChartObject(chartProperty);

                        if (initial)
                        {
                            book = exp.Export((obj as ChartProperties), (IEnumerable)data, "Export1.xlsx",
                                                ExcelVersion.Excel2010, true, null, null);
                            initial = false;
                        }
                        else
                        {
                            exp.Export((obj as ChartProperties), (IEnumerable)data, "Export.xlsx",
                           ExcelVersion.Excel2010, false, book, MultipleExportType.NewSheet, null, null);
                        }
                    }
                }
            }
        }

{% endhighlight %}

![](/js/Chart/Exporting_images/Exporting_img2.png)

## Naming the exported file

ejChart provides options to customize the name of the file to be exported. This can be done by setting the name of the file to the property [`fileName`](../api/ejchart#members:exportsettings-filename) in exporting.

## Rotating the chart

We can also rotate the chart and can export it. Possible angles of rotation are 0, 90, -90 and 180 degree. This can be achieved by setting values to the [`angle`](../api/ejchart#members:exportsettings-angle) property in exporting.

{% highlight javascript %}

        //Exporting the chart after rotating
        $("#container").ejChart(
         {
             exportSettings: { angle: 180, action: "http://js.syncfusion.com/ExportingServices/api/JSChartExport/Export" },
         });

{% endhighlight %}

![](/js/Chart/Exporting_images/Exporting_img3.png)

## Setting orientation for the document

This is applicable for PDF, excel and word documents. By setting values to the [`orientation`](../api/ejchart#members:exportsettings-orientation) property in exporting, we can change the orientation of those documents. By default it will export with portrait orientation.

### Multiple Chart Export

Multiple charts can be exported  by setting the [`multipleExport`](../api/ejchart#members:exportsettings-multipleexport) property as true.

{% highlight javascript %}

//Multiple chart export 
        $("#container").ejChart(
         {
                exportSettings: { multipleExport : true }
         });

{% endhighlight %}
