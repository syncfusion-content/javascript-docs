---
layout: post
title: Getting Started with Syncfusion Web Report Designer
description: How to start with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Getting Started with JavaScript Application

This section explains briefly about how to create a **ReportDesigner** in your web application with **JavaScript**.

## Project Creation

The following steps displays the Project Creation Wizard in Visual Studio 2013.

Create a new `ASP.NET Empty Web application` project by selecting the **WEB** category from the listed project template in Microsoft Visual Studio IDE.     

![](Images/JS-Sample-Img1.png) 

### Add References

1. In the Solution Explorer, right-click the `References` folder and then click `Add Reference`.

    ![](Images/JS-Sample-Img4.png) 

2. Add the following Syncfusion assemblies to the project that are necessary for using the report designer control and click OK.

   * Syncfusion.Chart.Wpf
   * Syncfusion.Compression.Base
   * Syncfusion.DocIO.Base
   * Syncfusion.EJ.ReportDesigner
   * Syncfusion.EJ.ReportViewer
   * Syncfusion.Gauge.Wpf
   * Syncfusion.Pdf.Base
   * Syncfusion.Presentation.Base
   * Syncfusion.Shared.Wpf
   * Syncfusion.SfMaps.Wpf
   * Syncfusion.XlsIO.Base

    > Refer the above assemblies from the installed location, [Installed Location]:\Program Files (x86)\Syncfusion\Essential Studio\JavaScript\{{ site.releaseversion }}\Assemblies

3.  Add the following WebAPI assemblies from [NuGet package](https://www.nuget.org/packages/Microsoft.AspNet.WebApi/ "Web NuGet Package Details").

    * System.Web.Http
    * System. Web.Http.WebHost
    * System.Net.Http.WebRequest
    * System.Net.Http.Formatting

    > The System.Web.Routing and System.Net.Http assemblies are also required, which are referred by default when creating the project.

### Create HTML Page

1. Right-Click on the project and select `Add` then click `New Item`. 

    ![](Images/JS-Sample-Img2.png)

2. Select `HTML Page` from the listed templates and name the page as **Default.html**.

    ![](Images/JS-Sample-Img3.png) 

3. Click Add.

    ![](Images/JS-Sample-Img7.png)

### Add Scripts and Styles

For complete dependencies list of report designer control [Click here](/js/ReportDesigner/Dependencies).

Add the script files and theme files in the &lt;head&gt; tag of the Default.html page.

#### Themes

{% highlight html %}

<link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.reportdesigner.min.css" rel="stylesheet" />

{% endhighlight %} 

#### Scripts

##### External dependencies

{% highlight html %}

<script src="http://code.jquery.com/jquery-1.10.2.min.js" type="text/javascript"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jsrender/0.9.90/jsrender.min.js" type="text/javascript"></script>

{% endhighlight %} 

##### Internal dependencies

Refer the below scripts to render report designer control.

{% highlight html %}

<script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
<script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.reportdesigner.min.js" type="text/javascript"></script>
 
{% endhighlight %} 

###### Code Mirror

To edit the SQL queries with syntax highlighter need to refer the below code mirror scripts and themes.

{% highlight html %}

<link href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.37.0/codemirror.min.css" rel="stylesheet" />
<link href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.37.0/addon/hint/show-hint.min.css" rel="stylesheet" />

<script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.37.0/codemirror.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.37.0/addon/hint/show-hint.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.37.0/addon/hint/sql-hint.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.37.0/mode/sql/sql.min.js" type="text/javascript"></script>

{% endhighlight %} 

Use the above code example while adding scripts and styles.

> [Click here](https://help.syncfusion.com/js/installation-and-deployment# "Installation and deployment") to know more about script and style sheets installed in local machine.

### Control Initialization

Initialize Report Designer by using the following code example in the &lt;body&gt; tag of the **Default.html** page.

{% highlight html %}

<div id="container" style="position: absolute; height: 100%; width: 100%;"></div>
<script type="text/javascript">
    $(function() {
        $("#container").ejReportDesigner({
            serviceUrl: '../../api/ReportDesigner'
        });
    });
</script>

{% endhighlight %}

### Add WebAPI controller for Report Designer
 
The JavaScript Report Designer uses WebApi services to process the report file and get the request from control.

**Add Controller**

1. Right-Click on the project and select `Add` then click `New Item`. 

    ![](Images/JS-Sample-Img2.png)

2. Select `Web API Controller Class` from the listed templates and name the controller as **ReportDesignerController.cs**. 

    ![](Images/JS-Sample-Img5.png)

3. Click Add.

    ![](Images/JS-Sample-Img8.png)

#### Inherit IReportDesignerController
 
The ApiController should inherit the `IReportDesignerController` and to process the report file. The interface `IReportDesignerController` contains the required actions and helper methods declaration to process the report. The `ReportDesignerHelper` and `ReportHelper` class contains helper methods that helps to process Post/Get request from control and return the response to control.

Please add the following code example in `ReportDesignerController.cs`.

{% highlight c# %}

using System;
using System.Collections.Generic;
using System.Linq;
using System.Net;
using System.Net.Http;
using System.Web.Http;
using System.IO;
using System.Web;
using Syncfusion.EJ.ReportViewer;
using Syncfusion.Reports.EJ;
using Syncfusion.EJ.ReportDesigner;

namespace ReportDesignerSample
{
    public class ReportDesignerController : ApiController, Syncfusion.EJ.ReportDesigner.IReportDesignerController
    {
        public string GetFilePath(string fileName)
        {
            string targetFolder = HttpContext.Current.Server.MapPath("~/");
            targetFolder += "Cache";

            if (!Directory.Exists(targetFolder))
            {
                Directory.CreateDirectory(targetFolder);
            }

            if (!Directory.Exists(targetFolder + "\\" + ReportDesignerHelper.EJReportDesignerToken))
            {
                Directory.CreateDirectory(targetFolder + "\\" + ReportDesignerHelper.EJReportDesignerToken);
            }

            var folderPath = HttpContext.Current.Server.MapPath("~/") + "Cache\\" + ReportDesignerHelper.EJReportDesignerToken + "\\";
            return folderPath + fileName;
        }

        public object GetImage(string key, string image)
        {
            return ReportDesignerHelper.GetImage(key, image, this);
        }

        public object PostDesignerAction(Dictionary<string, object> jsonResult)
        {
            return ReportDesignerHelper.ProcessDesigner(jsonResult, this, null);
        }

        public bool UploadFile(System.Web.HttpPostedFile httpPostedFile)
        {
            string targetFolder = HttpContext.Current.Server.MapPath("~/");
            string fileName = !string.IsNullOrEmpty(ReportDesignerHelper.SaveFileName) ? ReportDesignerHelper.SaveFileName : Path.GetFileName(httpPostedFile.FileName);
            targetFolder += "Cache";

            if (!Directory.Exists(targetFolder))
            {
                Directory.CreateDirectory(targetFolder);
            }

            if (!Directory.Exists(targetFolder + "\\" + ReportDesignerHelper.EJReportDesignerToken))
            {
                Directory.CreateDirectory(targetFolder + "\\" + ReportDesignerHelper.EJReportDesignerToken);
            }

            httpPostedFile.SaveAs(targetFolder + "\\" + ReportDesignerHelper.EJReportDesignerToken + "\\" + fileName);
            return true;
        }

        public void UploadReportAction()
        {
            ReportDesignerHelper.ProcessDesigner(null, this, HttpContext.Current.Request.Files[0]);
        }

        public object GetResource(string key, string resourcetype, bool isPrint)
        {
            return ReportHelper.GetResource(key, resourcetype, isPrint);
        }

        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            //You can update report options here
        }

        public void OnReportLoaded(ReportViewerOptions reportOption)
        {
            //You can update report options here
        }

        public object PostReportAction(Dictionary<string, object> jsonResult)
        {
            return ReportHelper.ProcessReport(jsonResult, this as IReportController);
        }

        public FileModel GetFile(string filename, bool isOverride)
        {
            throw new NotImplementedException();
        }

        public List<FileModel> GetFiles(FileType fileType)
        {
            throw new NotImplementedException();
        }
    }
}

{% endhighlight %}

### WebAPI Routing

If `Global Application Class` file already exists in your application skip the below **Add Global Application Class** section.

#### Add Global Application Class

1. Right-Click on the project and select `Add` then click `New Item`. 

    ![](Images/JS-Sample-Img2.png) 

2. Select `Global Application Class` from the listed templates and name it as `Global.asax`.

    ![](images/JS-Sample-img6.png)

3. Click Add.

    ![](Images/JS-Sample-Img9.png)
 
#### Route WebAPI

Modify the WebAPI routing in Application_Start event of `Global.asax` file as follows.

{% highlight c# %}

using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.Security;
using System.Web.SessionState;
using System.Web.Http;

namespace ReportDesignerSample
{
    public class Global : System.Web.HttpApplication
    {
        protected void Application_Start(object sender, EventArgs e)
        {
            System.Web.Http.GlobalConfiguration.Configuration.Routes.MapHttpRoute(
            name: "DefaultApi",
            routeTemplate: "api/{controller}/{action}/{id}",
            defaults: new { id = RouteParameter.Optional });
            AppDomain.CurrentDomain.SetData("SQLServerCompactEditionUnderWebHosting", true);
        }
    }
}

{% endhighlight %}

On running the application, Report Designer will be rendered like below.

   ![](Images/Getting-Started-img7.png)

## Integrate the component with Report Server

Report Designer can be integrated with the Report Server by using below code snippet. After integrating you can open, browse and edit the reports in the Report Server using Report designer.

Set the Report Server `serviceUrl` and `serviceAuthorizationToken` in the ReportDesigner properties.

{% highlight html %}

<div id="container" style="position: absolute; height: 100%; width: 100%;"></div>
<script type="text/javascript">
   $(function () {
            var dataValue = "";
            var apiRequest = new Object();
            apiRequest.password = "demo";
            apiRequest.userid = "guest";
            $.ajax({
                type: "POST",
                url: "http://reportserver.syncfusion.com/api/get-user-key",
                data: apiRequest,
                success: function (data) {
                    dataValue = data.Token;
                    var token = JSON.parse(dataValue);
                    $("#container").ejReportDesigner(
                    {
                       serviceUrl: 'http://reportserver.syncfusion.com/ReportService/api/Designer',
                       serviceAuthorizationToken: token['token_type'] + ' ' + token['access_token']
                    });
                }
            });
   });
</script>

{% endhighlight %} 
