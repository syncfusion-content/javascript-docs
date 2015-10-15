---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: OlapGauge
documentation: ug
---

#Getting Started 

This section briefly explains how you can create an **OlapGauge** in your application with **Essential JavaScript.**

##Syncfusion OLAP Controls – Architecture

![]("/js/OlapGauge/Getting-Started_images/Getting-Started_img2.png") 

As shown in the above architecture, control rendering takes place client-side and all other analytical operations on each action takes place server-side.

##Service for OLAP Controls

The primary reasons for using service in an **OLAP** processing are as follows:

1.**DataSource Connectivity:** You can establish a connection between different cube data sources such as

   * Offline Cube
   * Online Cube (XML/A)
   * Cube within SQL Server, locally or through remote, you can move the connectivity related coding to service-side as it is impossible at the client-side other than <b>Online Cube</b> (XML/A) option. Using service, you can connect any cube data source without any limitation.
    
2.**Cube Schema:** As the connection is moved to service-side, you obviously use **Microsoft ADOMD assembly** to get the entire cube schema. Only with the **cube schema** the following details are achieved for control rendering.

   * Availability of cubes.
   * A complete end-to-end detail such as name, caption, unique name, parent information, child information, its properties, etc., about the dimension, hierarchy, level, members are available in cube schema only. 
   * Localized information is also available in cube schema.

3.**MDX Generator:** You can frame the MDX query using an MDX generator in **Syncfusion.Olap.Base** assembly. To execute the framed **MDX** from the cube data source, you need to send framed MDX via **Microsoft ADOMD assembly**. The executed query is returned in the form of cell set (contain values) that is converted to Pivot Engine and then to JSON data to render any **OLAP** controls.

4.**OLAP Report:** The OlapReport holds the complete information of each axis such as column, row and slicer. Using OlapReport, you can maintain the dimension element, measure element, hierarchy name, level name as well as the member information that
is included and excluded.

As the **OlapControl** is the key for each and every operation, initially you need to serialize the OLAP Reports and send to client-side in a form of string. When you perform any operation such as drill up or down, filtering, sorting etc., you can send OLAP Reports from the client-side to the service in a de-serialized and updated format. Further operations are carried with updated OLAP Reports only and you can send the updated OLAP Reports back to client-side with **JSON** data in a serialized format again. This process has the OLAP Reports always updated. You cannot operate serialized OlapReport in client-side and hence it is carried to service for performing the update operation.

##Create an application

This section explains how you can configure the **OlapGauge** control in applications. You can also learn how to pass the required data to **OlapGauge** and to customize its various options according to your requirements.

In the following example, **OlapGauge** is used to visualize the Revenue for Reseller over a Fiscal Year 2004 on the product category - Accessories.

![]("/js/OlapGauge/Getting-Started_images/Getting-Started_img3.png") 

Open Visual Studio and create a new project by clicking **New Project**. Select the **Web** category, select the **ASP.NET Empty Web Application** template, and then click **OK**. The following screenshot displays the Project Creation Wizard:

![]("/js/OlapGauge/Getting-Started_images/Getting-Started_img4.png") 

##Create HTML page

To create a new web form in the application, right-click on the project and select Add. The following screenshot displays the Add New Item Wizard.

![]("/js/OlapGauge/Getting-Started_images/Getting-Started_img5.png") 

Click on New Item and select HTML Page from the listed templates. Name the page as default.html and click OK.

##Add References, Scripts, Styles and Control in HTML page

###Add References

* In the Solution Explorer, right-click the References folder, and then click Add Reference.
![]("/js/OlapGauge/Getting-Started_images/Getting-Started_img6.png") 
![]("/js/OlapGauge/Getting-Started_images/Getting-Started_img7.png") 
* Select the following assemblies: 

   1. Microsoft.AnalysisServices.AdomdClient.dll
   2. Syncfusion.Linq.Base.dll 
   3. Syncfusion.Olap.Base.dll, 
   4. Syncfusion.EJ.dll  
   5. Syncfusion.EJ.Olap.dll.
* Click OK

###Add Scripts and Styles

Add the script files and CSS files in the **&lt;head&gt;** tag of the **default.html** page.

N>  You can follow the order given here while adding scripts and styles.

{% highlight html %}

<link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js">
</script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript">
</script>
<script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js">
</script>

{% endhighlight %}

###Add Control in HTML page

Add the following code inside the **&lt;body&gt;** tag in the **default.html** page.

{% highlight html %}

<!--Creating a div tag, that acts as a container for ejOlapGauge widget.-->
<div id = "OlapGauge" style = "height: 350px; width: 100%; position:relative">
</div>

//Setting properties and initializing ejOlapGauge widget.
<script type = "text/javascript">
    $(function() {
        $("#OlapGauge").ejOlapGauge({
            url: "../wcf/OlapGaugeService.svc",
            enableTooltip: true,
            load: "loadGaugeTheme",
            backgroundColor: "transparent",
            scales: [{
                showRanges: true,
                radius: 150,
                showScaleBar: true,
                size: 1,
                border: {
                    width: 0.5
                },
                showIndicators: true,
                showLabels: true,
                pointers: [{
                    showBackNeedle: true,
                    backNeedleLength: 20,
                    length: 120,
                    width: 7
                }, {
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
                    width: 1,
                    color: "#8c8c8c"
                }, {
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
                    border: {
                        color: "#fc0606"
                    }
                }, {
                    distanceFromScale: -5
                }],
                customLabels: [{
                    position: {
                        x: 180,
                        y: 290
                    },
                    font: {
                        size: "10px",
                        fontFamily: "Segoe UI",
                        fontStyle: "Normal"
                    },
                    color: "#666666"
                }, {
                    position: {
                        x: 180,
                        y: 320
                    },
                    font: {
                        size: "10px",
                        fontFamily: "Segoe UI",
                        fontStyle: "Normal"
                    },
                    color: "#666666"
                }, {
                    position: {
                        x: 180,
                        y: 150
                    },
                    font: {
                        size: "12px",
                        fontFamily: "Segoe UI",
                        fontStyle: "Normal"
                    },
                    color: "#666666"
                }]
            }]
        });
    }); 
</script>
    
{% endhighlight %}

##Add WCF Service for OlapGauge

###Create WCF Service

Right-click the project and select Add > New Folder.  Name the folder as wcf. Let the folder name "wcf" be in lower case. Right-click the wcf folder created and select Add > New Item.  In the Add New Item window, select WCF Service and name it OlapGaugeService.svc. And then Click Add.
![]("/js/OlapGauge/Getting-Started_images/Getting-Started_img8.png") 

###Add service methods inside Interface

Add the following code example inside the `IOlapGaugeService` interface available in the IOlapGaugeService.cs file.

{% highlight c# %}

[ServiceContract]
public interface IOlapGaugeService
{
   [OperationContract]
   Dictionary<string, object> InitializeGauge(string action,string customObject);                
}

{% endhighlight %}

###Add Namespaces

Add necessary namespaces required to implement the service methods.

{% highlight c# %}

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

###Create Class in Service file

Create the `OlapGaugeService` class to implement the service methods. Inherit the class from the `IOlapGaugeService` interface created automatically when any new service is added.

{% highlight c# %}

namespace WebApplication2.wcf
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OlapGaugeService : IOlapGaugeService
    {
    }
}


{% endhighlight %}

###Implement Service Methods

Add the following methods to the service invoked for any server-side operations performed in **OlapGauge**.

Initialize the OlapGauge helper class.

{% highlight c# %}

OlapGauge htmlHelper = new OlapGauge();       
static string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
JavaScriptSerializer serializer = new JavaScriptSerializer();

{% endhighlight %}

Initialize the following relevant **service** methods to be added.

{% highlight c# %}

//This method provides the required information from server-side for initializing the OlapGauge.
public Dictionary<string, object> InitializeGauge(string action,string customObject)
{
   OlapDataManager DataManager = null;
   dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
   DataManager = new OlapDataManager(connectionString);                         
   DataManager.SetCurrentReport(CreateOlapReport());
   return htmlHelper.GetJsonData(action, DataManager);
}  
      
//This method carries the information about the default report that is rendered within OlapGauge initially. 
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

###Configure Web.Config 

* You can expose services through the properties such as binding, contract and address etc., using an endpoint. In your application the service name is `WebApplication2.wcf.OlapGaugeService` where **"OlapGaugeService"** is the service class name and **“WebApplication2.wcf"** is the namespace name where service class appears. The following are the properties that meet the appropriate endpoint.

   1. **Contract:** This property indicates the contract of the endpoint that is exposed. Here you are referring to the **IOlapGaugeService** contract and hence it is `WebApplication2.wcf.IOlapGaugeService`.
   2. **Binding:** In your application, you can use `webHttpBinding` to post and receive the requests and responses between client-end and service-end.
   3. **BehaviorConfiguration:** This property contains the name of the behavior used in the endpoint. **endpointBehaviors** are illustrated as follows**.**

{% highlight xml %}

 <services>
      <service name="WebApplication2.wcf.OlapGaugeService">
        <endpoint address="" behaviorConfiguration="WebApplication2.wcf.OlapGaugeServiceAspNetAjaxBehavior"
          binding="webHttpBinding" contract="WebApplication2.wcf.IOlapGaugeService" />
      </service>
    </services>

{% endhighlight %}

* The `endpointBehaviors` contains all the behaviors for an endpoint. You can link each endpoint to the respective behavior only by using the name property. In the following code example, `WebApplication2.wcf.OlapGaugeServiceAspNetAjaxBehavior` refers to the OlapGaugeService class under the namespace **WebApplication2.wcf** in **OlapGaugeService.svc.cs** file which is the appropriate behavior for the endpoint.

{% highlight xml %}

   <endpointBehaviors>
        <behavior name="WebApplication2.wcf.OlapGaugeServiceAspNetAjaxBehavior">
          <enableWebScript />
        </behavior>
    </endpointBehaviors>


{% endhighlight %} 

N>  In this example, “WebApplication2.wcf” indicates the namespace in the WCF Service and “OlapGaugeService” indicates the class name in the WCF Service.



