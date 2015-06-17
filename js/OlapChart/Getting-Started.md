---
layout: post
title: Getting-Started
description: getting started
platform: js
control: OLAP Chart
documentation: ug
---

## Getting Started

This section explains briefly about how to create an **OLAP Chart** in your application with **JavaScript.**

**Control Structure**

The following screen shot shows the **OLAP Chart** for **JavaScript**.

{% include image.html url="/js/OlapChart/Getting-Started_images/Getting-Started_img1.png" Caption="OLAP Chart"%}

**Syncfusion OLAP Controls – Architecture**

{% include image.html url="/js/OlapChart/Getting-Started_images/Getting-Started_img2.png" Caption="OLAP Controls Architecture"%}

The architecture gives a clear idea about how the control rendering takes place at client-side and all other analytical operations on each action takes place at the server-side.

**Service for OLAP Controls**

The primary reasons for using service in an **OLAP** processing are as follows:

1. **DataSource Connectivity:** You can establish a connection between different cube data sources such as

    * Offline Cube

    * Online Cube (XML/A)

    * Cube within SQL Server (locally or through remote), you can move the connectivity related coding to service-side as it is impossible at the client-side other than **Online Cube** (XML/A) option. Using service, you can connect any cube data source without any limitation.

2. **Cube Schema:** As the connection is moved to service-side, you obviously use **Microsoft ADOMD assembly** to get the entire cube schema. Only with the **cube schema** the following details are achieved for control rendering.

    * Availability of cubes.

    * A complete end-to-end detail such as name, caption, unique name, parent information, child information, its properties etc. about the dimension, hierarchy, level, members are available in cube schema only. 

    * Localized information is also available in cube schema.  

3. **MDX Generator: You can frame the MDX query using an MDX generator in Syncfusion.Olap**.**Base** assembly. To execute the framed **MDX** from the cube data source, you need to send framed MDX via **Microsoft ADOMD assembly**. The executed query is returned in the form of cell set (contain values) that is converted to Pivot Engine and then to JSON data to render any **OLAP** controls.

4. **OLAP Report:** The **OLAP Report** class in the **Syncfusion.Olap.Base** holds the complete information of each axes such as column, row and slicer. Using **OLAP Report** class, you can maintain the dimension element, measure element, hierarchy name, level name as well as the member information that is included and excluded.  

As the **OLAP Control** is the key for each and every operation, initially you need to serialize the **OLAP Report** and send to client-side in a form of string.
When you perform any operation such as drill up/down, filtering, sorting etc., you need to send **OLAP Report** from the client-side to the service in a de-serialized and updated format.
Further operations are carried with updated **OLAP Reports** only and you can send the updated **OLAP Report** back to client-side with **JSON** data in a serialized format again. 
This process has the **OLAP Report** always updated. You cannot operate serialized **OLAP Report** in client-side and hence it is carried to service having its class in **Syncfusion.Olap.Base** assembly to perform the update operation.

**Create an application**

This section encompasses on how to configure an **OLAP Chart** component in an application. You can also learn how to pass the required data to **OLAP Chart** and to customize its various options according to your requirements. 

In the following example, the **OLAP Chart** component displays the customer count over different fiscal years against various geographical locations. This helps you to analyze the summarized data over different fiscal years.

{% include image.html url="/js/OlapChart/Getting-Started_images/Getting-Started_img3.png" Caption="Fiscal year vs Geographical locations"%}

Open Visual Studio and create a new project by clicking **New Project**. Select the **Web** category, select the **ASP.NET Empty Web Application** template, and then click **OK**. The following screen shot displays the Project Creation Wizard:

{% include image.html url="/js/OlapChart/Getting-Started_images/Getting-Started_img4.png" Caption="Project Creation Wizard"%}

**Create HTML Page**

To create a new web form in the application, right-click on the project and select **Add**. The following screen shot shows the Add New Item Wizard.

{% include image.html url="/js/OlapChart/Getting-Started_images/Getting-Started_img5.png" Caption="Add New Item Wizard"%}

Click **New Item** and select **HTML Page** from the listed templates. Name the page as **default.html** and click **OK**.

**Add References, Scripts, Styles and Control in HTML page**

**Add References**

In the **Solution Explorer**, right-click the **References** folder, then click **Add Reference**.

{% include image.html url="/js/OlapChart/Getting-Started_images/Getting-Started_img6.png" Caption="Solution Explorer"%}

The following screen shot illustrates how to reference **Syncfusion.Olap.Base.**

{% include image.html url="/js/OlapChart/Getting-Started_images/Getting-Started_img7.png" Caption="Adding reference to Syncfusion.Olap.Base"%}

Select the following assemblies: 

   * Microsoft.AnalysisServices.AdomdClient.dll,  

   * Syncfusion.Core.dll,  Syncfusion.Linq.Base.dll, 

   * Syncfusion.Olap.Base.dll,  

   * Syncfusion.EJ.dll 

   * Syncfusion.EJ.Olap.dll.

Click **OK.**

**Add Scripts and Styles** 

Add the script files and CSS files in the **title** tag of the **default.html** page.

> _**Note: Please follow the following order while adding scripts and styles.**_

{% highlight html %}

<link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"> </script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"> </script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>
<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script>

{% endhighlight %}

**Add Control in HTML page**

Add the following code inside the &lt;body&gt; tag in the **default.html** page.

{% highlight html %}

<div>
     //Creating a div tag which will act as a container for ejOlapChart widget.
    <div id="OlapChart" style="height: 350px; width: 100%; overflow: auto">
    </div>
    <script type="text/javascript">
          //Setting property and initializing ejOlapChart widget.
          $(function () {
                $("#OlapChart").ejOlapChart({
                    url: "../wcf/OlapChartService.svc"

                });
            });
     </script>
</div>

{% endhighlight %}

**Add WCF service for OLAP Chart**

**Create WCF Services**

1. Right-click the project, select **Add > New Folder**.  Name the folder as **WCF.**

2. Now right-click the **WCF** folder created and select **Add > New Item**.  In the **Add New** Item window, select **WCF Service** and name it as **OlapChartService.svc**

3. Click **Add**.

{% include image.html url="/js/OlapChart/Getting-Started_images/Getting-Started_img8.png" Caption="Adding WCF service"%}

**Add service methods inside Interface**

Add the following code sample inside the **IOlapChartService** interface available in the **IOlapChartService.cs** file.

{% highlight c# %}

    [ServiceContract]

    public interface IOlapChartService

    {

        [OperationContract]

        Dictionary<string, object> InitializeChart(string action, string customObject);        
        
        [OperationContract]

        Dictionary<string, object> **DrillChart**(string action, string drilledSeries, string olapReport, string customObject);

    }
{% endhighlight %}

**Add Namespaces**

Add the following namespaces to implement the service methods.

{% highlight c# %}


using System;

using System.Collections.Generic;

using System.Linq;

using System.Runtime.Serialization;

using System.ServiceModel;

using System.Text;

using System.ServiceModel.Activation;

using Syncfusion.Olap.Manager;

using Syncfusion.Olap.Reports;

using Syncfusion.JavaScript.Olap;

using System.Web.Script.Serialization;

{% endhighlight %}

**Create Class in Service file**

Create the **OlapChartService** class to implement the service methods. Inherit the class from **IOlapChartService** interface, which is created automatically when any new service is added.

{% highlight c# %}

namespace **WebApplication2**

{

    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]

    public class OlapChartService : IOlapChartService

    {

    }

}

{% endhighlight %}

**Implement Service Methods**

Add the following methods to the service, which is invoked during any server-side operations performed in **OLAP Chart**.

* Initialize the **OLAP Charts** helper class and **OLAP DataManager** with appropriate connection string. 

{% highlight c# %}

JavaScriptSerializer serializer = new JavaScriptSerializer();

OlapChart htmlHelper = new OlapChart();        

static string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";   

OlapDataManager DataManager = new OlapDataManager(connectionString);

{% endhighlight %}

* Initialize the following service methods.

{% highlight c# %}

//This method provides the required information from the server side to initialize the OlapChart.

         public Dictionary<string, object> InitializeChart(string action, string customObject)

        {

            OlapDataManager DataManager = null;

            dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());

            DataManager = new OlapDataManager(connectionString); 

            DataManager.SetCurrentReport(CreateOlapReport());

            return htmlHelper.GetJsonData(action, DataManager);

        }

//This method provides the required information from the server side while drill up/down operation is performed in OlapChart.

        public Dictionary<string, object> **DrillChart**(string action, string drilledSeries, string olapReport, string customObject)

        {

            DataManager.SetCurrentReport(Utils.DeserializeOlapReport(olapReport)); 

            dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());            

            return htmlHelper.GetJsonData(action, DataManager, drilledSeries);

        }

//This method carries information about the default report rendered within OlapChart initially. 

        private OlapReport CreateOlapReport()

        {

            OlapReport olapReport = new OlapReport();

            olapReport.Name = "Default Report";

            olapReport.CurrentCubeName = "Adventure Works";


            DimensionElement dimensionElementColumn = new DimensionElement();

            dimensionElementColumn.Name = "Customer";

            dimensionElementColumn.AddLevel("Customer Geography", "Country");


            MeasureElements measureElementColumn = new MeasureElements();

            measureElementColumn.Elements.Add(new MeasureElement { Name = "Customer Count" });



            DimensionElement dimensionElementRow = new DimensionElement();

            dimensionElementRow.Name = "Date";

            dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");



            olapReport.SeriesElements.Add(dimensionElementRow);

            olapReport.CategoricalElements.Add(dimensionElementColumn);

            olapReport.CategoricalElements.Add(measureElementColumn);

            return olapReport;

        }

{% endhighlight %}

**Configuring Web.Config**

* You can expose services through the properties such as binding, contract and address etc. using an **endpoint**. In your application the service name is "**WebApplication2.OlapChartService**" where "**OlapChartService**" is the service class name and “**WebApplication2**" is the namespace name where service class appears. The following are the properties that meet the appropriate endpoint.  

   1. **Contract:** This property indicates the contract of the endpoint is exposing. Here you are referring **IOlapChartService** contract and hence it is "**WebApplication2.IOlapChartService**".

   2. **Binding:** In your application, you use **webHttpBinding** to post and receive the requests and responses between the client-end and the service.

   3. **behaviorConfiguration:** This property contains the name of the behavior to be used in the endpoint. **endpointBehaviors** are illustrated as follows

{% highlight xml %}

<services>
      <service name="**WebApplication2.OlapChartService**">
        <endpoint address="" behaviorConfiguration="**WebApplication2.OlapChartServiceAspNetAjaxBehavior**"
          binding="webHttpBinding" contract="**WebApplication2.IOlapChartService**" />
      </service>
</services>

{% endhighlight %}

* The **endpointBehaviors** contain all the behaviors for an endpoint. You can link each endpoint to the respective behavior only using this **name** property. In the following code sample, "**WebApplication2.OlapChartServiceAspNetAjaxBehavior**" refers to the **OlapChartService** class under
the namespace **WebApplication2** in **OlapChartService.svc.cs** file that is the appropriate behavior for the endpoint. 

{% highlight xml %}

<endpointBehaviors>
        <behavior name="**WebApplication2.OlapChartServiceAspNetAjaxBehavior**">
          <enableWebScript />
        </behavior>
</endpointBehaviors>


{% endhighlight %}

> _**Note: In this example, “WebApplication2” indicates the name of the project and “OlapChartService” indicates the name of the WCF service created.**_



