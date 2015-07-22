---
layout: post
title: Exporting
description: exporting
platform: js
control: Chart
documentation: ug
---

# Exporting

## Image Export

The **EJChart** supports client-side exporting using **canvg** script. **canvg** is a **SVG** parser and renderer. It takes a **URL** to a **SVG** file or the text of an SVG file, parses it to canvas, and renders the canvas image.

{% highlight html %}

<img src="../images/chart/export.png" onclick="onExport()" title="Export Chart" style="float: right" />
<div id="container"></div>
<canvas id="canvas2" style="display: none"></canvas>

{% endhighlight %}

{% highlight js %}    

        $("#chartcontainer").ejChart({   
        });
        function onExport() {
            var canvas = document.getElementById('canvas2');
            svg = $("#container").html();
            canvg(canvas, svg);
            var image = canvas.toDataURL("image/png")
                              .replace("image/png", "image/octet-stream");
            var downloadLink = document.createElement("a");
            downloadLink.href = image;
            downloadLink.download = "Chart.png";
            document.body.appendChild(downloadLink);
            downloadLink.click();
            document.body.removeChild(downloadLink);
            $('#canvas2').hide();
        }         


{% endhighlight %}

## Excel Export

**Exporting** is a server-side operation and JS Chart is a Client-side widget. So it is not feasible to export in pure Javascript platform. For HTTP Content read and write, you need server-side control. You can use **REST** service like **WebApi** to achieve server-side support while exporting in JS Chart. 
Also since JS Chart is a Client-side, it does not have **mapper** property for custom URL mapping. You can achieve this by **export** method, which takes the type of export, URL, multiple export option as argument.

{% highlight html %}

<div style="height:20px;">
  <a id="downloadexcel" style="cursor: pointer; position:absolute;>
  <img src="../images/chart/ExcelExport.png" onclick="downloadExcel()" title="Excel Export"  />
  </a>
</div>

{% endhighlight %}

{% highlight js %}  
      $("#container").ejChart(
             {
             primaryXAxis:
             {
                 title: { text: 'Manager' },
                 majorGridLines: { visible: false }
             }, 
			
             //Initializing Primary Y Axis	
             primaryYAxis:
             {
                 title: { text: 'Sales' },
                 axisLine: { visible: false },
                 range: { min: 0, max: 20000, interval: 2000 }
             },  
			
             //Initializing Series
             series: 
             [
                 {
                     points: [{ x: "John", y: 10000}, { x: "Jake", y: 12000 }, 
                              { x: "Peter", y: 18000 },
                              { x: "James", y: 11000}, { x: "Mary", y: 9700 }],
                     name: 'Person',
                     type: 'column',
                     enableAnimation: true,
                     tooltip:{visible:true}							 
                 }
             ],
 
             title :{text: 'Sales Comparison'},
             size: { height: "600" }, 
         });	
         
        function downloadExcel() {
              var chart = $("#container").ejChart("instance");
              chart.export('Excel', 'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport');
        }
        
        public class JSChartExportController : ApiController
        {
         
        [System.Web.Http.ActionName("ExcelExport")]
        [AcceptVerbs("POST")]
        public void ExcelExport()
        {          
            string chartModel = HttpContext.Current.Request.Params["ChartModel"];  

            ChartProperties chartProperty = ConvertChartObject(chartModel);
            ExcelExport exp = new ExcelExport();          
            exp.Export(chartProperty, null,  "Export.xlsx", ExcelVersion.Excel2010, null, null);
        }

        private ChartProperties ConvertChartObject(string ChartModel)
        {
            JavaScriptSerializer serializer = new JavaScriptSerializer();

            IEnumerable div = (IEnumerable)serializer.Deserialize(ChartModel, typeof(IEnumerable));
            ChartProperties chartProp = new ChartProperties();
            foreach (KeyValuePair<string, object> ds in div)
            {

              var property = chartProp.GetType().GetProperty(ds.Key, BindingFlags.Instance | BindingFlags.Public |  BindingFlags.IgnoreCase);
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

{% include image.html url="/js/Chart/Exporting_images/Exporting_img1.png" %}

### Multiple Export

 Exporting to excel provide supports to export multiple chart on the page. When third argument for **export** method is true, then all the chart in the page get exported to excel. MultipleExportType.AppendToSheet append all the chart in active sheet and MultipleExportType.NewSheet creates a new sheet in excel for exporting each chart.
 
 {% highlight js %}  
    $("#container1").ejChart();
            
    $("#container2").ejChart();
              
         
    function downloadExcel() {
              var chart = $("#container").ejChart("instance");
              chart.export('Excel', 'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport', true);
    }
        
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
                                book = exp.Export((obj as ChartProperties), (IEnumerable)data, "Export1.xlsx", ExcelVersion.Excel2010, true, null, null);
                                initial = false;
                            }                            
                            else
                            {
                                exp.Export((obj as ChartProperties), (IEnumerable)data, "Export.xlsx", ExcelVersion.Excel2010, false, book, MultipleExportType.NewSheet, null, null);
                            }                     
                    }s
                }
            }      
       }

        


{% endhighlight %}

{% include image.html url="/js/Chart/Exporting_images/Exporting_img2.png" %}
 

