---
title: Service reference for ejReportViewer widget
description: Services used in Essential JavaScript ReportViewer.
platform: js
control: ejReportViewer
documentation: api
keywords: ejReportViewer, Services, Essential JS ReportViewer, ReportViewer
api: /api/js/ejreportviewer
---
## ReportViewer services

### RDL Report Services

### URL: http://js.syncfusion.com/demos/ejservices/api/RDLReport/PostReportAction

### Parameter

### ReportLoad

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to load the report
</td>
</tr>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
String
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
reportPath
</td>
<td class="datatype">
String 
</td>
<td class="description">
Report path of the report 
</td>
</tr>
<tr>
<td class="parameter name">
reportServerUrl
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the Report Server url to accessing the report
</td>
</tr>
<tr>
<td class="parameter name">
processingMode
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the processing mode of the report  
</td>
</tr>
</tbody>
</table>

### GetDatasourceCredential

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the Datasource credential
</td>
</tr>
<tr>
<td class="parameter name">
dataSources 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Datasource of the report 
</td>
</tr>
<tr>
<td class="parameter name">
parameters
</td>
<td class="datatype">
String 
</td>
<td class="description">
Specify the parameter collections 
</td>
</tr>
</tbody>
</table>

### ValidateDSCredential

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to validate the datasource credential
</td>
</tr>
<tr>
<td class="parameter name">
dataSources 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Datasource of the report 
</td>
</tr>
</tbody>
</table>

### UpdateDSCredential

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to update the datasource credential
</td>
</tr>
<tr>
<td class="parameter name">
dataSources 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Datasource of the report 
</td>
</tr>
</tbody>
</table>

### GetParameters

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the parameters
</td>
</tr>
</tbody>
</table>

### SetParameters

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to set the parameters
</td>
</tr>
<tr>
<td class="parameter name">
parameters 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Specify the parameters details to set the parameters
</td>
</tr>
</tbody>
</table>

### UpdateParameters

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to update the parameters
</td>
</tr>
<tr>
<td class="parameter name">
update param 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Specify the parameters details to update the parameters
</td>
</tr>
</tbody>
</table>

### UpdateDataSource

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to update the datasource
</td>
</tr>
</tbody>
</table>

### GetPageModel

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the page model
</td>
</tr>
<tr>
<td class="parameter name">
refresh
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
Specify whether the report refresh or not 
</td>
</tr>
<tr>
<td class="parameter name">
dataRefresh 
</td>
<td class="datatype">
Boolean 
</td>
<td class="description">
Specify whether the data refresh or not
</td>
</tr>
<tr>
<td class="parameter name">
pageIndex 
</td>
<td class="datatype">
Int
</td>
<td class="description">
Specify the page index of the report
</td>
</tr>
<tr>
<td class="parameter name">
pageInit 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
Specify whether the page initialized or not  
</td>
</tr>
<tr>
<td class="parameter name">
isPrint 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
Specify whether the page layout is print or not
</td>
</tr>
</tbody>
</table>

### GetPrintModel

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the print model
</td>
</tr>
</tbody>
</table>

### DrillDown

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to process drill down
</td>
</tr>
<tr>
<td class="parameter name">
pageIndex 
</td>
<td class="datatype">
Int
</td>
<td class="description">
specify the page index of the report
</td>
</tr>
<tr>
<td class="parameter name">
toggleInfo 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
specify the toggle information to process toggle
</td>
</tr>
<tr>
<td class="parameter name">
refresh
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
specify whether the report refresh or not 
</td>
</tr>
<tr>
<td class="parameter name">
dataRefresh 
</td>
<td class="datatype">
Boolean 
</td>
<td class="description">
specify whether the data refresh or not
</td>
</tr>
<tr>
<td class="parameter name">
pageInit 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
specify whether the page initialized or not  
</td>
</tr>
<tr>
<td class="parameter name">
isPrint 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
specify whether the page layout is print or not  
</td>
</tr>
</tbody>
</table>

### ClearCache

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to clear the cache
</td>
</tr>
</tbody>
</table>

### DrillThrough

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to process the drill through
</td>
</tr>
<tr>
<td class="parameter name">
reportName  
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the child report name to drill through navigation
</td>
</tr>
<tr>
<td class="parameter name">
parameters  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Specify the parameters details to process drill through
</td>
</tr>
<tr>
<td class="parameter name">
authentication Key  
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the authentication key to process drill through
</td>
</tr>
</tbody>
</table>

### Request

~~~html
        <div id="container" style="position: absolute; height: 100%; width: 100%;"></div>
        <script type="text/javascript">
            $(function () {
                $("#container").ejReportViewer(
                {
                    reportServiceUrl: '/api/ReportApi',
                    processingMode: ej.ReportViewer.ProcessingMode.Remote,
                    reportPath: '~/App_Data/Sales Dashboard.rdl'
                });
            });       
        </script>
~~~

### Response

#### Code:  200

#### Content-Type:”application/json:charset=utf-8”;

#### Response Text:

Browser will render the reportviewer control with specified RDL report.

### URL: http://js.syncfusion.com/demos/ejservices/api/RDLReport/OnInitReportOptions

### Parameter

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
string
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
reportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Report model items.
</td>
</tr>
<tr>
<td class="parameter name">
SubReportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Sub Report model items.
</td>
</tr>
</tbody>
</table>

### Request

~~~csharp
    reportOption.ReportModel.ReportingServer = new ReportingServerExt();
    reportOption.ReportModel.ReportServerCredential = new System.Net.NetworkCredential("guest", "demo");   
~~~

### Response

#### Code:  200

#### Content-Type:”application/json:charset=utf-8”;

#### Response Text:
ReportOptions will be Initialized for RDL report

### URL: http://js.syncfusion.com/demos/ejservices/api/RDLReport/OnReportLoaded

### Parameter

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
string
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
reportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Report model items.
</td>
</tr>
<tr>
<td class="parameter name">
SubReportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Sub Report model items.
</td>
</tr>
</tbody>
</table>

### Request

~~~csharp
        reportOptions.ReportModel.DataSources.Clear();
        var DataSources = reportOptions.ReportModel.DataSources;   
        List<ReportParameter> parameters = new List<ReportParameter>();
        parameters.Add(new ReportParameter() { Name = "InvoiceID", Labels = new List<string>() { "InvoiceID" }, Values = new List<string>() { "10250" } });
        reportOptions.ReportModel.Parameters = parameters;      
~~~

### Response

#### Code:  200

#### Content-Type:”application/json:charset=utf-8”;

#### Response Text:
ReportOptions will be updated when loading the RDL report.

### RDLC Report Services

### URL: http://js.syncfusion.com/demos/ejservices/api/RDLCReport/PostReportAction

### Parameter

### ReportLoad

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to load the report
</td>
</tr>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
String
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
reportPath
</td>
<td class="datatype">
String 
</td>
<td class="description">
Report path of the report 
</td>
</tr>
<tr>
<td class="parameter name">
reportServerUrl
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the Report Server url to accessing the report
</td>
</tr>
<tr>
<td class="parameter name">
processingMode
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the processing mode of the report  
</td>
</tr>
</tbody>
</table>

### GetDatasourceCredential

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the Datasource credential
</td>
</tr>
<tr>
<td class="parameter name">
dataSources 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Datasource of the report 
</td>
</tr>
<tr>
<td class="parameter name">
parameters
</td>
<td class="datatype">
String 
</td>
<td class="description">
Specify the parameter collections 
</td>
</tr>
</tbody>
</table>

### ValidateDSCredential

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to validate the datasource credential
</td>
</tr>
<tr>
<td class="parameter name">
dataSources 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Datasource of the report 
</td>
</tr>
</tbody>
</table>

### UpdateDSCredential

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to update the datasource credential
</td>
</tr>
<tr>
<td class="parameter name">
dataSources 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Datasource of the report 
</td>
</tr>
</tbody>
</table>

### GetParameters

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the parameters
</td>
</tr>
</tbody>
</table>

### SetParameters

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to set the parameters
</td>
</tr>
<tr>
<td class="parameter name">
parameters 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Specify the parameters details to set the parameters
</td>
</tr>
</tbody>
</table>

### UpdateParameters

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to update the parameters
</td>
</tr>
<tr>
<td class="parameter name">
update param 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Specify the parameters details to update the parameters
</td>
</tr>
</tbody>
</table>

### UpdateDataSource

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to update the datasource
</td>
</tr>
</tbody>
</table>

### GetPageModel

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the page model
</td>
</tr>
<tr>
<td class="parameter name">
refresh
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
Specify whether the report refresh or not 
</td>
</tr>
<tr>
<td class="parameter name">
dataRefresh 
</td>
<td class="datatype">
Boolean 
</td>
<td class="description">
Specify whether the data refresh or not
</td>
</tr>
<tr>
<td class="parameter name">
pageIndex 
</td>
<td class="datatype">
Int
</td>
<td class="description">
Specify the page index of the report
</td>
</tr>
<tr>
<td class="parameter name">
pageInit 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
Specify whether the page initialized or not  
</td>
</tr>
<tr>
<td class="parameter name">
isPrint 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
Specify whether the page layout is print or not
</td>
</tr>
</tbody>
</table>

### GetPrintModel

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the print model
</td>
</tr>
</tbody>
</table>

### DrillDown

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to process drill down
</td>
</tr>
<tr>
<td class="parameter name">
pageIndex 
</td>
<td class="datatype">
Int
</td>
<td class="description">
specify the page index of the report
</td>
</tr>
<tr>
<td class="parameter name">
toggleInfo 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
specify the toggle information to process toggle
</td>
</tr>
<tr>
<td class="parameter name">
refresh
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
specify whether the report refresh or not 
</td>
</tr>
<tr>
<td class="parameter name">
dataRefresh 
</td>
<td class="datatype">
Boolean 
</td>
<td class="description">
specify whether the data refresh or not
</td>
</tr>
<tr>
<td class="parameter name">
pageInit 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
specify whether the page initialized or not  
</td>
</tr>
<tr>
<td class="parameter name">
isPrint 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
specify whether the page layout is print or not  
</td>
</tr>
</tbody>
</table>

### ClearCache

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to clear the cache
</td>
</tr>
</tbody>
</table>

### DrillThrough

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to process the drill through
</td>
</tr>
<tr>
<td class="parameter name">
reportName  
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the child report name to drill through navigation
</td>
</tr>
<tr>
<td class="parameter name">
parameters  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Specify the parameters details to process drill through
</td>
</tr>
<tr>
<td class="parameter name">
authentication Key  
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the authentication key to process drill through
</td>
</tr>
</tbody>
</table>

### Request

~~~html
<div>
        <!-- Creating a div tag which will act as a container for ejReportViewer widget.-->
        <div  style="height: 650px;width: 950px;min-height:404px;" id="viewer"></div>
        <!-- Setting property and initializing ejReportViewer widget.-->
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportApi",
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
~~~

### Response

#### Code:  200

#### Content-Type:”application/json:charset=utf-8”;

#### Response Text:

Browser will render the reportviewer control with specified RDLC report.

### URL: http://js.syncfusion.com/demos/ejservices/api/RDLCReport/OnInitReportOptions

### Parameter

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
string
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
reportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Report model items.
</td>
</tr>
<tr>
<td class="parameter name">
SubReportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Sub Report model items.
</td>
</tr>
</tbody>
</table>

### Request

~~~csharp
            if (reportOption.ReportModel.IsDrillthroughReport)            
                return;
            var reportName = reportOption.ReportModel.ReportPath;
            reportOption.ReportModel.ReportPath = ReportViewerHelper.GetReportPath(reportOption.ReportModel.ReportPath);
            if (reportName.Contains("Product Catalog.rdlc"))
            {
                reportOption.ReportModel.DataSources.Clear();
                reportOption.ReportModel.DataSources.Add(new ReportDataSource { Name = "ProductCatalog", Value = ProductCatalog.GetData() });
            }  
~~~

### Response

#### Code:  200

#### Content-Type:”application/json:charset=utf-8”;

#### Response Text:
ReportOptions will be Initialized for RDLC Report

### URL: http://js.syncfusion.com/demos/ejservices/api/RDLCReport/OnReportLoaded

### Parameter

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
string
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
reportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Report model items.
</td>
</tr>
<tr>
<td class="parameter name">
SubReportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Sub Report model items.
</td>
</tr>
</tbody>
</table>

### Request

~~~csharp
            var reportName = reportOption.ReportModel.ReportPath;
            if (reportName.Contains("Region.rdlc"))
            {
                reportOption.ReportModel.DataSources.Clear();
                reportOption.ReportModel.DataSources.Add(new ReportDataSource { Name = "StoreSales", Value = StoreSales.GetData() });
            }        
~~~

### Response

#### Code:  200

#### Content-Type:”application/json:charset=utf-8”;

#### Response Text:
ReportOptions will be updated when loading the RDLC report.

### SSRS Report Services

### URL: http://js.syncfusion.com/demos/ejservices/api/SSRSReport/PostReportAction

### Parameter

### ReportLoad

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to load the report
</td>
</tr>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
String
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
reportPath
</td>
<td class="datatype">
String 
</td>
<td class="description">
Report path of the report 
</td>
</tr>
<tr>
<td class="parameter name">
reportServerUrl
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the Report Server url to accessing the report
</td>
</tr>
<tr>
<td class="parameter name">
processingMode
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the processing mode of the report  
</td>
</tr>
</tbody>
</table>

### GetDatasourceCredential

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the Datasource credential
</td>
</tr>
<tr>
<td class="parameter name">
dataSources 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Datasource of the report 
</td>
</tr>
<tr>
<td class="parameter name">
parameters
</td>
<td class="datatype">
String 
</td>
<td class="description">
Specify the parameter collections 
</td>
</tr>
</tbody>
</table>

### ValidateDSCredential

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to validate the datasource credential
</td>
</tr>
<tr>
<td class="parameter name">
dataSources 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Datasource of the report 
</td>
</tr>
</tbody>
</table>

### UpdateDSCredential

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to update the datasource credential
</td>
</tr>
<tr>
<td class="parameter name">
dataSources 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Datasource of the report 
</td>
</tr>
</tbody>
</table>

### GetParameters

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the parameters
</td>
</tr>
</tbody>
</table>

### SetParameters

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to set the parameters
</td>
</tr>
<tr>
<td class="parameter name">
parameters 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Specify the parameters details to set the parameters
</td>
</tr>
</tbody>
</table>

### UpdateParameters

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to update the parameters
</td>
</tr>
<tr>
<td class="parameter name">
update param 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Specify the parameters details to update the parameters
</td>
</tr>
</tbody>
</table>

### UpdateDataSource

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to update the datasource
</td>
</tr>
</tbody>
</table>

### GetPageModel

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the page model
</td>
</tr>
<tr>
<td class="parameter name">
refresh
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
Specify whether the report refresh or not 
</td>
</tr>
<tr>
<td class="parameter name">
dataRefresh 
</td>
<td class="datatype">
Boolean 
</td>
<td class="description">
Specify whether the data refresh or not
</td>
</tr>
<tr>
<td class="parameter name">
pageIndex 
</td>
<td class="datatype">
Int
</td>
<td class="description">
Specify the page index of the report
</td>
</tr>
<tr>
<td class="parameter name">
pageInit 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
Specify whether the page initialized or not  
</td>
</tr>
<tr>
<td class="parameter name">
isPrint 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
Specify whether the page layout is print or not
</td>
</tr>
</tbody>
</table>

### GetPrintModel

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to get the print model
</td>
</tr>
</tbody>
</table>

### DrillDown

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to process drill down
</td>
</tr>
<tr>
<td class="parameter name">
pageIndex 
</td>
<td class="datatype">
Int
</td>
<td class="description">
specify the page index of the report
</td>
</tr>
<tr>
<td class="parameter name">
toggleInfo 
</td>
<td class="datatype">
JSON
</td>
<td class="description">
specify the toggle information to process toggle
</td>
</tr>
<tr>
<td class="parameter name">
refresh
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
specify whether the report refresh or not 
</td>
</tr>
<tr>
<td class="parameter name">
dataRefresh 
</td>
<td class="datatype">
Boolean 
</td>
<td class="description">
specify whether the data refresh or not
</td>
</tr>
<tr>
<td class="parameter name">
pageInit 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
specify whether the page initialized or not  
</td>
</tr>
<tr>
<td class="parameter name">
isPrint 
</td>
<td class="datatype">
Boolean
</td>
<td class="description">
specify whether the page layout is print or not  
</td>
</tr>
</tbody>
</table>

### ClearCache

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to clear the cache
</td>
</tr>
</tbody>
</table>

### DrillThrough

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
reportAction  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format to process the drill through
</td>
</tr>
<tr>
<td class="parameter name">
reportName  
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the child report name to drill through navigation
</td>
</tr>
<tr>
<td class="parameter name">
parameters  
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Specify the parameters details to process drill through
</td>
</tr>
<tr>
<td class="parameter name">
authentication Key  
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the authentication key to process drill through
</td>
</tr>
</tbody>
</table>

### Request

~~~html
<div id="container" style="position: absolute; height: 100%; width: 100%;"></div>
<script type="text/javascript">
    $(function () {
        $("#container").ejReportViewer(
           {
                reportServiceUrl: "/api/SSRSReport",
                processingMode: ej.ReportViewer.ProcessingMode.Remote,
                reportPath: "/SSRSSamples2/Territory Sales new",
                reportServerUrl: "http://mvc.syncfusion.com/reportserver"
           });
    });       
</script>
~~~

### Response

#### Code:  200

#### Content-Type:”application/json:charset=utf-8”;

#### Response Text:

Browser will render the reportviewer control with specified SSRS report.

### URL: http://js.syncfusion.com/demos/ejservices/api/SSRSReport/OnInitReportOptions

### Parameter

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
string
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
reportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Report model items.
</td>
</tr>
<tr>
<td class="parameter name">
SubReportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Sub Report model items.
</td>
</tr>
</tbody>
</table>

### Request

~~~csharp
                string reportserverUrl = WebConfigurationManager.AppSettings["ReportServerUrl"];
                reportOption.ReportModel.ReportServerUrl = reportserverUrl;           
                reportOption.ReportModel.ReportServerCredential = new System.Net.NetworkCredential("ssrs", "RDLReport1");
                reportOption.ReportModel.DataSourceCredentials.Add(new DataSourceCredentials("NorthWindIO", "ssrs1", "RDLReport1"));  
~~~

### Response

#### Code:  200

#### Content-Type:”application/json:charset=utf-8”;

#### Response Text:
ReportOptions will be Initialized for SSRS report

### URL: http://js.syncfusion.com/demos/ejservices/api/SSRSReport/OnReportLoaded

### Parameter

<table>
<thead>
<tr>
<th>
Parameter name
</th>
<th>
Data type
</th>
<th>
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
string
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
reportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Report model items.
</td>
</tr>
<tr>
<td class="parameter name">
SubReportModel
</td>
<td class="datatype">
property
</td>
<td class="description">
Contains the collections of Sub Report model items.
</td>
</tr>
</tbody>
</table>

### Request

~~~csharp
        reportOptions.ReportModel.DataSources.Clear();
        var DataSources = reportOptions.ReportModel.DataSources;  
        List<ReportParameter> parameters = new List<ReportParameter>();
        parameters.Add(new ReportParameter() { Name = "InvoiceID", Labels = new List<string>() { "InvoiceID" }, Values = new List<string>() { "10250" } });
        reportOptions.ReportModel.Parameters = parameters;      
~~~

### Response

#### Code:  200

#### Content-Type:”application/json:charset=utf-8”;

#### Response Text:
ReportOptions will be updated when loading the SSRS report.

## ReportViewerHelper

ReportViewerHelper class used to process the ReportViewer control in server side.

### Methods:

### ProcessReport(Dictionary<string, object> jsonResult, IReportController reportController)

Process the Report in Reportviewer Control  with specified report details

Code snippet:

return.ProcessReport(jsonResult, this);

### GetReport(string key, string type)

Getting the Report to be processed in Reportviewer Control

Code snippet:

return.GetReport(string key, string type);

### GetResource(string key, string resourceType, bool isPrint)

Getting the Resource from Reportviewer Control and It will process the report Exporting.

Code snippet:

return.GetResource(string key, string resourceType, bool isPrint);

### GetParameters()

Getting the Report Parameters of the Reportviewer Control

Code snippet:

return.GetParameters();

### GetDataSources()

Getting the Report DataSource of the Reportviewer Control

Code snippet:

return.GetDataSources();

### GetDataSetNames()

Getting the Report Dataset of the Reportviewer Control

Code snippet:

return.GetDataSetNames();