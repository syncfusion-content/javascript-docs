---
layout: post
title: Create or design SSRS RDL, RDLC report | Report Viewer | Syncfusion
description: Create or design SSRS RDL, and RDLC report to render in Syncfusion HTML5 JavaScript Report Viewer.
platform: js
control: Report Viewer
documentation: ug
api: /api/js/ejreportviewer
---

# Create report
This topic describes how to create a RDL and RDLC reports to use in Report Viewer.

## Create RDL report
You can create a RDL reports using any of the following reporting tools,

1.	Syncfusion Web Report Designer.
2.	Microsoft Report Builder.
3.	Visual Studio Report Server project template.

### Syncfusion Web Report Designer
Provides intuitive user interface to create or edit report online. For more details refer to the [Web Report Designer documentation](/js/reportdesigner/overview).

### Microsoft SQL Report Builder
You can create a RDL report using the Microsoft stand-alone Report Builder. For more details refer to the [online documentation](https://docs.microsoft.com/en-us/sql/reporting-services/report-builder/start-report-builder?view=sql-server-2014).

### Visual Studio Report Server template
To create a RDL report in Visual Studio, a Report Server project is required where you can save your report definition (.rdl) file. For more details, refer to the  [Visual Studio documentation](https://docs.microsoft.com/en-us/sql/reporting-services/create-a-basic-table-report-ssrs-tutorial?view=sql-server-2014).

N> If you do not see the Business Intelligence or Report Server Project options, you should update SSDT with the Business Intelligence templates. See [Download SQL Server Data Tools](https://docs.microsoft.com/en-us/sql/ssdt/download-sql-server-data-tools-ssdt?view=sql-server-2017).

## Create RDLC report using business object data source
This section describes step by step procedure to create a RDLC report using Visual Studio Reporting project type.

### Create an application
1.Open Visual Studio 2013, from the File menu, select New Project.
2.Select the Visual C#, Reporting project type from the project type, and then select the Reports Application project type. Set the project's Name to `RDLCReportsApplication` and click OK.
N> If you don't see the Business Intelligence or Report Server Project options, you need to update SSDT with the Business Intelligence templates. See [Download SQL Server Data Tools](https://docs.microsoft.com/en-us/sql/ssdt/previous-releases-of-sql-server-data-tools-ssdt-and-ssdt-bi?view=sql-server-2017#links-to-download-pages).

![Create new reporting application project](images/how-to/create-report/reporting-application.png)

### Create business object class
1.In the Solution Explorer, right-click the project, click Add > Class, and name it as `ProductSales.cs`, and then click Add.
2.Create the properties and method of your choice. You can use the following codes to the newly created class.

{% highlight c# %}
    public class ProductSales
    {
        public string ProdCat { get; set; }

        public string SubCat { get; set; }

        public string OrderYear { get; set; }

        public string OrderQtr { get; set; }

        public double Sales { get; set; }
    }
{% endhighlight %}

3.Clean and build the application.

### Add a RDLC report
1.Right click on the project, click Add -> New Item.
2.Click Reporting project type, select the Report Wizard template then name the report as `SalesReport.rdlc`.
3.Click Add.
![Add a new rdlc using report wizard template](images/how-to/create-report/add-sales-report-rdlc.png)

### Data source and table configuration wizard
1.Choose Object type from the Data Source Configuration Wizard and click Next.
![Select data source type in configuration wizard](images/how-to/create-report/choose-data-source-type.png)

2.Expand the tree view and select `ProductSales` and click Finish.
![Choose data object class in the application namespace](images/how-to/create-report/select-data-objects.png)

3.In the DataSet Properties wizard, specify the dataset name as `SalesData`.
![Set rdlc dataset properties](images/how-to/create-report/rdlc-dataset-properties.png)

4.Drag and drop fields into Values, Row and Column groups, and then click Next.
![Arrange table row, column and value groups](images/how-to/create-report/arrange-table-fields.png)

5.Choose the table layout and click Next.
6.Select table style, and click Finish.
![Choose table toggle, repeat header and total options](images/how-to/create-report/choose-table-layout.png)

7.Once select Finish, the RDLC report is ready and is displayed in the Visual Studio as shown below.
![Visual Studio design output of the sales report](images/how-to/create-report/sales-report-design.png)

To render the RDLC using Report Viewer refer to the section [RDLC Report](/js/reportviewer/rdlc-report).