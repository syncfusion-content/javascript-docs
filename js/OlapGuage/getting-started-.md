---
layout: post
title: getting-started-
description: getting started 
platform: js
control: OLAP Gauge
documentation: ug
---

# Getting Started 

This section explains briefly about how to create an **OLAP Gauge** in your application with **JavaScript.**

**Control structure**

The following screen shot shows the structure of an **OLAP Gauge** control.

{% include image.html url="\js\OlapGuage\getting-started-_images\getting-started-_img1.png" Caption="Figure: OLAP Gauge Control for JavaScript"%}

**Syncfusion OLAP Controls – Architecture**

{% include image.html url="\js\OlapGuage\getting-started-_images\getting-started-_img2.png" Caption="Figure: Architecture of OLAP controls"%}

As shown in an above architecture, control rendering takes place at client-side and all other analytical operations on each action takes place at server-side.

**Service for OLAP Controls**

The primary reasons for using service in an **OLAP** processing are as follows:

1. **DataSource Connectivity:** You can establish a connection between different cube data sources such as

1. Offline Cube

2. Online Cube (XML/A)

3. Cube within SQL Server (locally or through remote), you can move the connectivity related coding to service-side as it is impossible at the client-side other than **Online Cube** (XML/A) option. Using service, you can connect any cube data source without any limitation.

2. **Cube Schema:** As the connection is moved to service-side, you obviously use **Microsoft**_****_**ADOMD**_****_**assembly** to get the entire cube schema. Only with the **cube schema** the following details are achieved for control rendering.

1. Availability of cubes.

2. A complete end-to-end detail such as name, caption, unique name, parent information, child information, its properties etc. about the dimension, hierarchy, level, members are available in cube schema only.

3. Localized information is also available in cube schema.

3. **MDX Generator:** You can frame the MDX query using an MDX generator in **Syncfusion.Olap**.**Base** assembly. To execute the framed **MDX** from the cube data source, you need to send framed MDX via **Microsoft****ADOMD****assembly**. The executed query is returned in the form of cell set (contain values) that is converted to Pivot Engine and then to JSON data to render any **OLAP** controls.

4. **OLAP Report:** The **OlapReport** class in the **Syncfusion.Olap.Base** holds the complete information of each axes such as column, row and slicer. Using **OlapReport** class, you can maintain the dimension element, measure element, hierarchy name, level name as well as the member information that is included and excluded.

As the **OlapControl** is the key for each and every operation, initially you need to serialize the **OlapReport** and send to client-side in a form of string.

When you perform any operation such as drill up/down, filtering, sorting etc., you need to send **OlapReport** from the client-side to the service in a de-serialized and updated format.

Further operations are carried with updated **OlapReports** only and you can send the updated **OlapReport** back to client-side with **JSON** data in a serialized format again. 

This process has the **OlapReport** always updated. You cannot operate serialized **OlapReport** in client-side and hence it is carried to service having its class in **Syncfusion.Olap.Base** assembly to perform the update operation_**.**_

**Create an application**

This section encompasses on how to configure the **OLAP Gauge** control in applications. You can also learn how to pass the required data to **OLAP Gauge** and to customize its various options according to your requirements.

In the following example, **OLAP gauge** is used to visualize the Revenue for Reseller over a Fiscal Year 2004 on the product category - Accessories.



{% include image.html url="\js\OlapGuage\getting-started-_images\getting-started-_img3.png" Caption="Figure: Revenue for Reseller – FY 2004 – Accessories"%}

Open Visual Studio and create a new project by clicking **New Project**. Select the **Web** category, select the **ASP.NET Empty Web Application** template, and then click **OK**.

The following screen shot displays the Project Creation Wizard:



{% include image.html url="\js\OlapGuage\getting-started-_images\getting-started-_img4.png" Caption="Figure: New Project Wizard"%}

**Create HTML page**

To create a new web form in the application

1. Right-click on the project and select Add.

{% include image.html url="\js\OlapGuage\getting-started-_images\getting-started-_img5.png" Caption="Figure: Add New Item Wizard"%}

2. Click on New Item and select HTML Page from the listed templates.

3. Name the page as default.html and click OK.

**Add References, Scripts, Styles and Control in HTML page**

**Add References**

1. In the Solution Explorer, right-click the References folder, and then click Add Reference.

![](getting-started-_images\getting-started-_img6.png)

Figure: Adding Reference

{% include image.html url="\js\OlapGuage\getting-started-_images\getting-started-_img7.png" Caption="Figure: Referencing Syncfusion.Olap.Base"%}

2. Select the following assemblies: 

Microsoft.AnalysisServices.AdomdClient.dll

Syncfusion.Core.dll, 

Syncfusion.Linq.Base.dll 

Syncfusion.Olap.Base.dll, 

Syncfusion.EJ.dll  

Syncfusion.EJ.Olap.dll.

3. Click **OK**

**Add Scripts and Styles**

Add the script files and CSS files in the title tag of the default.html page.

> ![](getting-started-_images\getting-started-_img8.jpeg)_**Note: Please follow the given order while adding scripts and styles.**_

{% highlight html %}

**[HTML]**
<link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"> </script>
<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script>



{% endhighlight %}



**Add Control in HTML page**

Add the following code inside the **&lt;Body&gt;** tag in the **default.html** page.

{% highlight html %}

**[HTML]**

//Creating a div tag, which will act as a container for ejOlapGauge widget.


<div id="OlapGauge" style="height: 350px; width: 100%; position:relative">
    </div>

//Setting properties and initializing ejOlapGauge widget.

    <script type="text/javascript">
        $(function () {
            $("#OlapGauge").ejOlapGauge({
                url: "../wcf/OlapGaugeService.svc", enableTooltip: true,
                load: "loadGaugeTheme", backgroundColor: "transparent",
                scales: [{
                    showRanges: true,
                    radius: 150, showScaleBar: true, size: 1,
                    border: {
                        width: 0.5
                    },
                    showIndicators: true, showLabels: true,
                    pointers: [{
                        showBackNeedle: true,
                        backNeedleLength: 20,
                        length: 120,
                        width: 7
                    },
            {
                type: "marker",
                markerType: "diamond",
                distanceFromScale: 5,
                placement: "center",
                backgroundColor: "#29A4D9",
                length: 25,
                width: 15
            }],
                    ticks: [{
                        type: "major",
                        distanceFromScale: 2,
                        height: 16,
                        width: 1, color: "#8c8c8c"
                    },
                    {
                        type: "minor",
                        height: 6,
                        width: 1,
                        distanceFromScale: 2,
                        color: "#8c8c8c"
                    }],
                    labels: [{
                        color: "#8c8c8c"
                    }],
                    ranges: [{
                        distanceFromScale: -5,
                        backgroundColor: "#fc0606",
                        border: { color: "#fc0606" }
                    }, {
                        distanceFromScale: -5
                    }],
                    customLabels: [{
                        position: { x: 180, y: 290 },
                        font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                    }, {
                        position: { x: 180, y: 320 },
                        font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                    }, {
                        position: { x: 180, y: 150 },
                        font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                    }]
                }]
            });
        });
    </script>



{% endhighlight %}

**Add WCF Service for OLAP Gauge**

**Create WCF Services**

1. Right-click the project and select Add > New Folder.  Name the folder as WCF.

4. Right-click the WCF folder created and select Add > New Item.  In the Add New Item window, select WCF Service and name it OlapGaugeService.svc

5. Click Add.

{% include image.html url="\js\OlapGuage\getting-started-_images\getting-started-_img9.png" Caption="Figure: Creating WCF Service"%}

**Add service methods inside Interface**

Add the following code inside the **IOlapGaugeService** interface available in the **IOlapGaugeService.cs** file.

{% highlight c# %}

**[C#]**
    [ServiceContract]
    public interface IOlapGaugeService
    {
       [OperationContract]
        Dictionary<string, object> InitializeGauge(string action,string customObject);                }


{% endhighlight %}

**Add Namespaces**

Add necessary namespaces required to implement the service methods.

{% highlight c# %}

**[C#]**
using System;
using System.Collections.Generic;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.Text;
using System.ServiceModel.Activation;
using Syncfusion.JavaScript.Olap;
using System.Web.Script.Serialization;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;


{% endhighlight %}

**Create Class in Service file**

Create the **OlapGaugeService** class to implement the service methods. Inherit the class from the **IOlapGaugeService** interface created automatically when any new service is added.

{% highlight c# %}

**[C#]**
namespace WebApplication2
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OlapGaugeService : IOlapGaugeService
    {
    }
}


{% endhighlight %}

**Implement Service Methods**

Add the following methods to the service invoked for any server-side operations performed in **OlapGauge**.

1. Initialize the OlapGauges helper class.

{% highlight c# %}

**[C#]**
        OlapGauge htmlHelper = new OlapGauge();       
        static string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();




{% endhighlight %}



2. Initialize the following relevant service methods to be added.

{% highlight c# %}

**[C#]**

         //This method provides the required information from the server side for initializing the OlapGauge.
          public Dictionary<string, object> InitializeGauge(string action,string customObject)
        {
            OlapDataManager DataManager = null;
            dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());

                DataManager = new OlapDataManager(connectionString);                         
            DataManager.SetCurrentReport(CreateOlapReport());
            return htmlHelper.GetJsonData(action, DataManager);
        }        
        //This method carries the information about the default report which would be rendered within OlapGauge initially. 
        private OlapReport CreateOlapReport()
        {
            OlapReport report = new OlapReport();
            report.CurrentCubeName = "Adventure Works";

            KpiElements kpiElement = new KpiElements();
            kpiElement.Elements.Add(new KpiElement { Name = "Revenue", ShowKPIGoal = true, ShowKPIStatus = true, ShowKPIValue = true, ShowKPITrend = true });

            DimensionElement dimensionElement1 = new DimensionElement();
            DimensionElement dimensionElement2 = new DimensionElement();
            DimensionElement dimensionElement3 = new DimensionElement();

            MeasureElements measureElement = new MeasureElements();
            measureElement.Elements.Add(new MeasureElement { UniqueName = "[Measures].[Customer Count]" });

            dimensionElement1.Name = "Date";
            dimensionElement1.AddLevel("Fiscal Year", "Fiscal Year");
            dimensionElement1.Hierarchy.LevelElements["Fiscal Year"].Add("FY 2004");
            dimensionElement1.Hierarchy.LevelElements["Fiscal Year"].IncludeAvailableMembers = true;

            dimensionElement2.Name = "Sales Channel";
            dimensionElement2.AddLevel("Sales Channel", "Sales Channel");
            dimensionElement2.Hierarchy.LevelElements["Sales Channel"].Add("Reseller");
            dimensionElement2.Hierarchy.LevelElements["Sales Channel"].IncludeAvailableMembers = true;

            dimensionElement3.Name = "Product";
            dimensionElement3.AddLevel("Product Model Lines", "Product Line");

            report.CategoricalElements.Add(new Item { ElementValue = dimensionElement2 });
            report.CategoricalElements.Add(new Item { ElementValue = dimensionElement1 });
            report.CategoricalElements.Add(new Item { ElementValue = kpiElement });
            report.SeriesElements.Add(new Item { ElementValue = dimensionElement3 });
            return report;
        }



{% endhighlight %}

**Configure Web.Config** 

1. You can expose services through the properties such as binding, contract and address etc. using an **endpoint**. In your application the service name is "**WebApplication2.OlapGuageService**" where "**OlapGuageService**" is the service class name and “**WebApplication2**" is the namespace name where service class appears.The following are the properties that meet the appropriate endpoint.

**Contract:** This property indicates the contract of the endpoint is exposing. Here you are referring **IOlapGaugeService** contract and hence it is "**WebApplication2.IOlapGaugeService**".

**Binding:** In your application, you can use **webHttpBinding** to post and receive the requests and responses between client-end and service-end.

**BehaviorConfiguration:** This property contains the name of the behavior used in the endpoint. **endpointBehaviors** are illustrated as follows**.**





{% highlight xml %}

**[Web.Config]**

 <services>
      <service name="**WebApplication2.OlapGaugeService**">
        <endpoint address="" behaviorConfiguration="**WebApplication2.OlapGaugeServiceAspNetAjaxBehavior**"
          binding="webHttpBinding" contract="**WebApplication2.IOlapGaugeService**" />
      </service>
    </services>


{% endhighlight %}



2. The **endpointBehaviors** contain all the behaviors for an endpoint. You can link each endpoint to the respective behavior only by using the **name** property. In the following code sample, "**WebApplication2.OlapGaugeServiceAspNetAjaxBehavior**" refers to the **OlapGaugeService** class under the namespace **WebApplication2** in **OlapGaugeService.svc.cs** file that is the appropriate behavior for the endpoint.

{% highlight xml %}

**[Web.Config]**

   <endpointBehaviors>
        <behavior name="**WebApplication2.OlapGaugeServiceAspNetAjaxBehavior**">
          <enableWebScript />
        </behavior>
    </endpointBehaviors>


{% endhighlight %}

> ![](getting-started-_images\getting-started-_img10.jpeg)_**Note: In this example, “WebApplication2” indicates the name of the project and “OlapGaugeService” indicates the name of the WCF service created.**_

