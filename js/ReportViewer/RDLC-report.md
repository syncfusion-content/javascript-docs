---
layout: post
title: Render RDLC report | Report Viewer | Syncfusion
description: Render RDLC client report with custom data collection (JSON array, IList, DataSet, and DataTable) using JavaScript Report Viewer.
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# Render RDLC report

Report Viewer has data binding support, which allows you to view RDLC reports that exist on the local file system with JSON array and custom business object data collection. The following steps demonstrates how to render a RDLC report with JSON array and custom business object data collection.

## Bind data source at client side
1.Set the RDLC report path to `reportPath` property.
2.Assign the [`processingMode`](../api/ejreportviewer#members:processingmode) property to `ProcessingMode.Local`.
3.Bind the JSON array collection to [`dataSources`](../api/ejreportviewer#members:datasources) property as shown in below code.

{% highlight javascript %}
<div style="height: 100%; width: 100%;">
        <div style="height: 600px; width: 950px; min-height: 400px;" id="viewer"></div>
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    processingMode: ej.ReportViewer.ProcessingMode.Local,
                    reportPath: 'Product List.rdlc',
                    dataSources: [{
                        value: [
                        {
                            ProductName: "Baked Chicken and Cheese", OrderId: "323B60", Price: 55, Category: "Non-Veg", Ingredients: "Grilled chicken, Corn and Olives.", ProductImage: ""
                        },
                        {
                            ProductName: "Chicken Delite", OrderId: "323B61", Price: 100, Category: "Non-Veg", Ingredients: "Cheese, Chicken chunks, Onions & Pineapple chunks.", ProductImage: ""
                        },
                        {
                            ProductName: "Chicken Tikka", OrderId: "323B62", Price: 64, Category: "Non-Veg", Ingredients: "Onions, Grilled chicken, Chicken salami & Tomatoes.", ProductImage: ""
                        }],
                        name: "list"
                    }]
                });
            });
        </script>
    </div>

{% endhighlight %}

N> The RDLC report used in the above example is taken from the Syncfusion build installed location. You can obtain sample rdlc files from below location. (%userprofile%\AppData\Local\Syncfusion\EssentialStudio\{{ site.releaseversion }}\Common\Data\ejReportTemplate).

4.Build and run the application to view the output result.


## Bind data source in Web API controller
To bind the custom business object data collection in Web API controller.  The following code shows the steps to configure the Web API controller to render RDLC report with business object data collection.

1.Create class and methods that returns business object data collection.

{% highlight c# %}
    public class ProductList
    {
        public string ProductName { get; set; }
        public string OrderId { get; set; }
        public double Price { get; set; }
        public string Category { get; set; }
        public string Ingredients { get; set; }
        public string ProductImage { get; set; }

        public static IList GetData()
        {
            List<ProductList> datas = new List<ProductList>();
            ProductList data = null;
            data = new ProductList()
            {
                ProductName = "Baked Chicken and Cheese",
                OrderId = "323B60",
                Price = 55,
                Category = "Non-Veg",
                Ingredients = "grilled chicken, corn and olives.",
                ProductImage = ""
            };
            datas.Add(data);
            data = new ProductList()
            {
                ProductName = "Chicken Delite",
                OrderId = "323B61",
                Price = 100,
                Category = "Non-Veg",
                Ingredients = "cheese, chicken chunks, onions & pineapple chunks.",
                ProductImage = ""
            };
            datas.Add(data);
            data = new ProductList()
            {
                ProductName = "Chicken Tikka",
                OrderId = "323B62",
                Price = 64,
                Category = "Non-Veg",
                Ingredients = "onions, grilled chicken, chicken salami & tomatoes.",
                ProductImage = ""
            };
            datas.Add(data);

            return datas;
        }
    }
{% endhighlight %}

2.Set the `ProcessingMode` to Local and `ReportPath` to the RDLC report location.
3.Bind the business object data values collection by adding new item to `DataSources` as in the below code snippet.

{% highlight c# %}
public class ReportsApiController : ApiController, IReportController
    {
        ..
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            reportOption.ReportModel.ProcessingMode = ProcessingMode.Local;
            reportOption.ReportModel.ReportPath = System.Web.Hosting.HostingEnvironment.MapPath(@"~/App_Data/Product List.rdlc");
            reportOption.ReportModel.DataSources.Add(new Syncfusion.Reports.EJ.ReportDataSource { Name = "list", Value = ProductList.GetData() });
        }
        ..
    }
{% endhighlight %}

N> Here the `Name` is case sensitive and it should be same as in the data source name in the report definition. The `Value` property accepts IList, DataSet, and DataTable inputs.

4.Build and run the application, the result shown as in below screenshot.

![Product list RDLC report with client side JSON array data binding](images/getting-started/rdlc-local-report.png)

## Load report as stream
To load report as stream, open your report using FileStream and assign the report stream to ReportModel `Stream` property.

{% highlight c# %}
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            string filePath = System.Web.Hosting.HostingEnvironment.MapPath(@"~/App_Data/Product List.rdlc"); ;
            // Here, we have loaded the sample report report from application the folder wwwroot. Sample.rdl should be there in wwwroot application folder.
            FileStream reportStream = new FileStream(filePath, FileMode.Open, FileAccess.Read);
            reportOption.ReportModel.Stream = reportStream;
        }

{% endhighlight %}

N> Here the report Product List.rdlc loaded from App_Data folder location.

## View Report Click
You can get the selected parameter details when user clicks the ViewReport button in Report Viewer. The `viewReportClick` event lets you to handle the ViewReport click at client side as in below code.

{% highlight c# %}
    <script type="text/javascript">
            $(function () {
                $("#container").ejReportViewer({
                    reportServiceUrl: "/api/InternalApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    viewReportClick:"onViewReportClick",
                });
            });

            function onViewReportClick(args) {
                var reportParams = [];
                reportParams.push({ name: 'SalesOrderNumber', labels: ['SO50756'], values: ['SO50756'] });
                args.model.parameters = reportParams;
            }
    </script>

{% endhighlight %}