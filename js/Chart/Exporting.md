---
layout: post
title: Exporting
description: exporting
platform: js
control: Chart
documentation: ug
---

# Exporting Chart

## Image Exporting

The chart can be exported to image when it is rendered in canvas. To render a chart in canvas, set the [enableCanvasRendering]{../api/ejchart#members:enablecanvasrendering} option to *true*. To export the chart, you can use the [export]{../api/ejchart#methods:export} method of the chart. Refer to the online [KB for exporting](http://www.syncfusion.com/kb/5045) to know more about chart exporting. 

N> Exporting chart as an image is supported in all major browsers except Internet Explorer due to its restriction towards client side download.

{% highlight html %}

<body>
<!--Chart download link-->
    <a id="download" download="Chart.png" style="cursor: pointer; position: absolute;right: 150px;">ExportChart</a>
   <div id="chartcontainer"></div>
<script>
       
        $("#chartcontainer").ejChart({
   
               // ...
               //Enable Canvas mode to export chart as image
               enableCanvasRendering: true
         });
        function download() {
            var canvas = $("#chartcontainer").ejChart("export");
            var dt = canvas.toDataURL();
            this.href = dt;
        }
        if (document.getElementById('download').addEventListener)
            document.getElementById('download').addEventListener('click', download, false);
        else
            document.getElementById('download').attachEvent('onclick', download, false);
</script>
</body>


{% endhighlight %}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/export) here to view the Export chart online demo sample.


## Excel Exporting

Exporting to excel is a server-side operation, so you can use the server-side frameworks such as **WebApi**, **WCF** service to achieve the excel exporting.

### Server side implementation

To convert the chart data from client to server-side, refer to the following steps.

1. Create an MVC application and add a controller.

2. Add Syncfusion.EJ, Syncfusion.EJ.MVC, Syncfusion.EJ.Export and Syncfusion.XlsIO dll’s as references to the application.

3. Parse the data from client in MVC controller and export the chart to client.  

{% highlight csharp %}

     public class JSChartExportController : ApiController
        {
        [System.Web.Http.ActionName("ExcelExport")]
        [AcceptVerbs("POST")]
        public void ExcelExport()
        {          
            // get Chart data from client side in POST action
            string chartModel = HttpContext.Current.Request.Params["ChartModel"];  

            ChartProperties chartProperty = ConvertChartObject(chartModel);
            ExcelExport exp = new ExcelExport();          
            exp.Export(chartProperty, null,  "Export.xlsx", ExcelVersion.Excel2010, null, null);
        }
        
       // Converting client string data in to server chart object
        private ChartProperties ConvertChartObject(string ChartModel)
        {
            JavaScriptSerializer serializer = new JavaScriptSerializer();

            IEnumerable div = (IEnumerable)serializer.Deserialize(ChartModel, typeof(IEnumerable));
            ChartProperties chartProp = new ChartProperties();
            
            // Mapping each client property to chart object
            foreach (KeyValuePair<string, object> ds in div)
            {

              var property = chartProp.GetType().GetProperty(ds.Key, BindingFlags.Instance | 
                                         BindingFlags.Public |  BindingFlags.IgnoreCase);
                if (property != null)
                {
                    Type type = property.PropertyType;
                    string serialize = serializer.Serialize(ds.Value);
                    object value = serializer.Deserialize(serialize, type);
                    property.SetValue(chartProp, value, null);
                }
            }
            return chartProp;
        } 
    }


{% endhighlight %}

4. Host the MVC application in your server and get the link for exporting action method
Example: http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport

5. To pass client data to server-side, you need to call the [export]{../api/ejchart#methods:export} method and pass export type (either image or excel) and server-side **URL** as an argument. The third argument of the export method is a Boolean property that specifies whether only the current chart should be exported or all charts in page should be exported.


{% highlight html %}

<body>
    <!--Export Char to Excel-->
  <a id="downloadexcel" style="cursor: pointer; position:absolute;">
  <button onclick="downloadExcel()" title="Excel Export" value="Export">Export</button>
      </a>
   <div id="chartcontainer"></div>
   
<script>
       //Render Chart1
        $("#chartcontainer").ejChart();

       //Export chart to excel
        function downloadExcel() {
            var chart = $("#chartcontainer").ejChart("instance");
            var exportChart = chart["export"];
           exportChart.call(chart, 'Excel', 
                                      'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport');
        }

</script>
</body>

{% endhighlight %}

![](/js/Chart/Exporting_images/Exporting_img1.png)

Export chart to excel page
{:.caption}

6.Currently, the chart data can be exported at server-side only through the helper functions in the “.Net”. So to use exporting in your projects, it is required to create a server with any of the following.
 
	i). ASP.Net MVC Controller
    
    ii). ASP.Net Webforms
    
    iii). WebAPI
    
    iv). WCF Service


## Multiple Chart Exporting

EjChart supports exporting more than one charts in a page, with the *third* argument for the [export]{../api/ejchart#methods:export} method.

N> Refer to the MultipleExportType.AppendToSheet, MultipleExportType.NewSheet. 

{% highlight js %}

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

Export multiple chart to excel page
{:.caption}
