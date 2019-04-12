---
title: How To| FileExplorer | Syncfusion
description: How to do - section for FileExplorer
platform: JS
control: FileExplorer
documentation: UG
keywords: FileExplorer,  Syncfusion, FileExplorer UG Doc, How To
api: /api/js/ejfileexplorer
---

# How To

## Cross-origin resource sharing support for FileExplorer

**Cross-origin request**

The FileExplorer can browse and manage files on remote servers, which is located in other domains. If a server is located on a different domain, on a different port or using different protocol (HTTP / HTTPS) such requests are considered to be “**cross-origin requests**”. These type of requests are prohibited by IE9 and its earlier browsers.

**Enabling cross-origin request in IE8 and IE9**

By default, Internet Explorer 9 and earlier prohibits cross-origin requests for Internet Zone, also it ignores Access-Control-Allow headers. To enable cross-origin in IE8 and IE9, we have specified two type of options. As per the requirements, you can use any option that is mentioned below.

**Option 1: Enabling cross-origin in IE through browser settings**

To enable cross-origin access using settings of IE browser, go to **Tools->Internet Options->Security** tab, click on “**Custom Level**” button. Find the Miscellaneous and select “**Enable**” option, which is available under “**Access data sources across domains**” settings.

If your server is located in Intranet Zone, In IE Browser, confirmation dialog will be popped during first cross-domain request as “**This page is accessing information that is not under its control. This poses a security risk. Do you want to continue?**”

To suppress this warning, you need to specify the "**Access data sources across domains**" setting to “**allow**”.

![Enabling cross-origin](How-To_images/How-To_img1.jpeg)

**Option 2: Using JSONP for cross-origin request**

Using JSONP data type, you can perform cross origin-request. To enable cross-origin request, in your FileExplorer, you have to specify **ajaxDataType** as “**JSONP**”. And we have provided “**doJSONPAction**” method to handle “**JSONP**” type AJAX request on server side.  Please refer below code snippet to specify **ajaxDataType** as “**JSONP**”.

    
    {% highlight javascript %}
    
        $("#fileExplorer").ejFileExplorer({
            path: "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/",
            ajaxAction:  "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations",
            ajaxDataType: "jsonp"
        });
        
    {% endhighlight %}
    
If we specify “**ajaxDataType**” as “**JSONP**”, data will be received in string format while calling “**doJSONPAction**” method of Web API Controller, here you need to deserialize the received “**json**” data into FileExplorerParams object. After performing corresponding operations, you have to specify the response data in serialized format with wrapped callback function. Please refer below code snippet to handle “**JSONP**” operations on server.

    
    {% highlight c# %}
    
            [HttpGet]
            [ActionName("doJSONPAction")]
            public object doJSONPAction(string callback, string json)
            {	
                object Data = null;
                var serializer = new JavaScriptSerializer();
                FileExplorerParams args = (FileExplorerParams)serializer.Deserialize(json, typeof(FileExplorerParams));
                try
                {            
                    switch (args.ActionType)
                    {
                        case "Read":
                            Data = FileExplorerOperations.ReadData(args.Path, args.ExtensionsAllow);
                            break;
                        case "Search":
                            Data = FileExplorerOperations.Search(args.Path, args.ExtensionsAllow, args.SearchString, args.CaseSensitive);
                            break;
                        case "CreateFolder":
                            Data = FileExplorerOperations.NewFolder(args.Path, args.Name);
                            break;
                        case "Paste":
                            Data = FileExplorerOperations.Paste(args.LocationFrom, args.LocationTo, args.Names, args.Action, args.CommonFiles);
                            break;
                        case "Remove":
                            Data = FileExplorerOperations.Remove(args.Names, args.Path);
                            break;
                        case "Rename":
                            Data = FileExplorerOperations.Rename(args.Path, args.Name, args.NewName, args.CommonFiles);
                            break;
                        case "GetDetails":
                            Data = FileExplorerOperations.GetDetails(args.Path, args.Names);
                            break;
                    }
                    HttpContext.Current.Response.Write(string.Format("{0}({1});", callback, serializer.Serialize(Data)));
                    return "";
                }
                catch (Exception e)
                {
                    FileExplorerResponse Response = new FileExplorerResponse();
                    Response.error = e.GetType().FullName + ", " + e.Message;
                    HttpContext.Current.Response.Write(string.Format("{0}({1});", callback, serializer.Serialize(Response)));
                    return "";
                }
            }
            [HttpPost]
            [ActionName("doJSONPAction")]
            public void doJSONPAction()
            {
                if (HttpContext.Current.Request.Files.Count > 0)
                    FileExplorerOperations.Upload(HttpContext.Current.Request.Files, HttpContext.Current.Request.QueryString.GetValues("Path")[0]);
            }
            [HttpGet]
            [ActionName("doJSONPAction")]
            public void doJSONPAction(string ActionType, string Path, string SelectedItems)
            {
                if (ActionType == "Download")
                FileExplorerOperations.Download(Path, HttpContext.Current.Request.QueryString.GetValues("Names"));
            else if (ActionType == "GetImage")
                FileExplorerOperations.GetImage(Path);
            }
            
    {% endhighlight %}
    
In IE8 and IE9 Browser, These options helps to render our FileExplorer control with cross-origin resource support.


## Service for FileExplorer

Generally web based file explorer needs a service for handling the file related operations in server end.  In same way, our “**FileExplorer**” control uses server side functionalities for handling the file operations in flexible way, that means you can implement this server side functions in any languages (like C#, VB, Java, PHP, etc.) and can customize it as per your requirement. 

By default, we have provided these server side AJAX handling functionalities in “**C#**” for managing physical filesystem and you can check it with “**FileExplorerOperations**” file, which is available at following Web API service application.

**Web API service**: [http://www.syncfusion.com/downloads/support/directtrac/general/ze/FileExplorer_WebAPI1406113770.zip](http://www.syncfusion.com/downloads/support/directtrac/general/ze/FileExplorer_WebAPI1406113770.zip#) 

**Note**: In this Web API application, we have provided “**FileOperationController**” file, which contains “**doJSONAction**” action method. When you make AJAX request, “**doJSONAction**” method will be called with AJAX request parameters then it calls the corresponding built-in file handling methods (Read, Search, Download, Upload, Remove, Rename etc.) that are available in our “**FileExplorerOperations**” class based on the “**ActionType**” parameter value.

For your convenience, we have prepared a sample based on this and you can find it under following location.

Sample: [http://jsplayground.syncfusion.com/gysvwdcp](http://jsplayground.syncfusion.com/gysvwdcp#) 

**Note**: First run the provided Web API service, then you will get an URL like ”[http://localhost:51460/](http://localhost:51460/#)“ (Here port number may change). As per port number, replace the specified URL in “**path**” and “**ajaxAction**” of “**FileExplorer**” sample.

Here we have created the file handling service using Web API application (.NET). If you want to use any other languages or platform for implementing this file handling service, you can achieve this. Please refer following table, this may be helpful to you to create your own service for FileExplorer.

### Create a Web API service for FileExplorer using “Syncfusion.EJ” assembly 

Please refer following steps to create a Web API service for FileExplorer using “**Syncfusion.EJ**” assembly. 

**Step 1**: Create a new ASP.NET Web API project using Visual Studio. 

Reference [link](https://docs.microsoft.com/en-us/aspnet/web-api/overview/getting-started-with-aspnet-web-api/tutorial-your-first-web-api#)  

**Step 2**: Add "**Syncfusion.EJ**" assembly reference, which is available at following location of your system. 

(Installed location)\Syncfusion\Essential Studio\\{15.1.0.33}\Assemblies

For example, If you have installed the Essential Studio package within C:\Program Files(x86), then navigate to the below location,

C:\Program Files (x86)\Syncfusion\Essential Studio\\{15.1.0.33}\Assemblies\4.5

This assembly contain built-in file handling methods such as (Read, Search, Download, Upload, Remove, Rename etc.) and it will be available in "**FileExplorerOperations**" class.

**Step 3**: Add “[FileExplorerController.cs](http://www.syncfusion.com/downloads/support/directtrac/general/ze/FileExplorerController-2059296017#)” file in the controller part of Web API project.
This file, contains action handler methods. Based on the request parameters, it helps to call the built-in file handling methods of **Syncfusion.EJ** assembly.

**Step 4**: Add following content in the “**WebApiApplication**” class of “**Global.asax.cs**” file.



  {% highlight c# %}

    protected void Application_Start()
    {
        RouteTable.Routes.MapHttpRoute(
        name: "Action",
        routeTemplate: "api/{controller}/{action}/{id}",
        defaults: new { id = System.Web.Http.RouteParameter.Optional }
        );
    }
    protected void Application_BeginRequest(object sender, EventArgs e)
    {
        if (Request.Headers.AllKeys.Contains("Origin") && Request.HttpMethod == "OPTIONS")
        {
            Response.StatusCode = 200;
            Response.End();
        }
    }

  {% endhighlight %}



**Step 5**: In “**Web.config**” add following code under **&lt;system.webServer&gt;** tag


{% highlight c# %}

    <httpProtocol>
      <customHeaders>
        <add name="Access-Control-Allow-Headers" value="accept, maxdataserviceversion, origin, x-requested-with, dataserviceversion,content-type" />
        <add name="Access-Control-Allow-Origin" value="*" />
        <add name="Access-Control-Max-Age" value="1728000" />
      </customHeaders>
    </httpProtocol>

{% endhighlight %}


**Step 6**: Add “**FileBrowser**” directory and it contains a files that is viewed by FileExplorer.

Now the Web API service for FileExplorer component is created. After running that service, you will get a base URL like "http://localhost:64218/". (Port number may vary)

After that, you can use this service for your FileExplorer component as shown in below code block.


  {% highlight javascript %}

    $("#fileExplorer").ejFileExplorer({
      //Path of the folder that you want to view in FileExplorer.
      path: "http://localhost:64218/FileBrowser/",	
      //Path of file handling operation method					
      ajaxAction: "http://localhost:64218/api/FileExplorer/FileOperations"
    });
  
  {% endhighlight %}

### Parameter list for AJAX request and response of FileExplorer

By default, we send following parameters in AJAX request. Using this details, you can perform the file handling operations of FileExplorer. After performing the file operations, you have to return the response data in proper format. This response data and request parameters are explained in following table. By referring to below table, you can create your custom functions to perform server side operations of “**FileExplorer**”. 

<table>
<tr>
<td>
Operation
<br/>
<br/>
</td>
<td>
Default Request Parameter<br/>
<br/>
</td>
<td>
Response data
<br/>
<br/>
</td>
<td>
Action Performed/ Details
<br/>
<br/>
</td>
</tr>
<tr>
<td>
Read<br/>
<br/>
</td>
<td>
String ActionType,
<br/>
<br/>
String Path,
<br/>
<br/>
String ExtensionsAllow,
<br/>
<br/>IEnumerable&lt;object&gt; SelectedItems<br/>
<br/>
</td>
<td>
Response data should be in JSON format with key name as ‘files’ and JSON fields should be with following field names.<br/><br/>If needed, customer can also add additional data along with the JSON result.<br/><br/>{files:[{name: "7.png", type: "File", size: 11439, dateModified: "3/31/2015 3:16:38 PM", hasChild: false},{name: "human.png", type: "File", size: 11059, dateModified: "3/31/2015 3:16:35 PM", hasChild: false}]}<br/>
<br/>
</td>
<td>
Read the file and folder details from the given path and return details in specified JSON format.<br/>
<br/>
</td>
</tr>
<tr>
<td>
CreateFolder<br/>
<br/>
</td>
<td>
String ActionType,<br/>
<br/>
String Path,
<br/>
<br/>
String Name,
<br/>
<br/>
IEnumerable&lt;object&gt; SelectedItems
<br/>
<br/>
</td>
<td>
Response data should be in JSON format with key name as ‘files’. In that returning JSON, "name” field is necessary.<br/><br/>{"files":[{"name":"New folder","type":"Directory","size":0,"dateModified":"2/25/2016 7:31:02 AM","hasChild":true,"isFile":false,"filterPath":null}],"details":null,"error":null}<br/><br/>
</td>
<td>
Create the new folder in given path<br/><br/>
</td>
</tr>
<tr>
<td>
Paste<br/><br/>
</td>
<td>
String ActionType,<br/>
<br/>String LocationFrom,
 <br/><br/>
String LocationTo,
<br/><br/>
String[] Names,
<br/><br/>
String Action,
<br/><br/>IEnumerable&lt;CommonFileDetails&gt; CommonFiles
<br/><br/>IEnumerable&lt;object&gt; SelectedItems
<br/><br/>IEnumerable&lt;object&gt; TargetFolder
<br/><br/></td><td>
Here you may return the pasted file details or empty.
<br/><br/><br/><br/></td><td>
Paste the content from source to target place.<br/><br/>Here Action specifies the operation type “move” or “copy”<br/><br/></td></tr>
<tr>
<td>
Remove<br/><br/></td><td>
String ActionType,
 <br/><br/>String[] Names,
<br/><br/>String Path
<br/><br/>IEnumerable&lt;object&gt; SelectedItems
<br/><br/>
</td><td>
Here you may return the removed file details or empty.
<br/><br/>
<br/><br/>
</td><td>
Delete the file/ folder from given path<br/><br/></td></tr>
<tr>
<td>
Rename<br/><br/>
</td><td>
String ActionType, 
<br/><br/>
String Path,
<br/><br/>
String Name,
<br/><br/>
String NewName,
<br/><br/>
IEnumerable&lt;CommonFileDetails&gt;&lt;CommonFileDetails&gt; CommonFiles<br/><br/>IEnumerable&lt;object&gt; SelectedItems<br/><br/>
</td><td>
Here you may return the renamed file details or empty.<br/><br/><br/><br/>
</td><td>
Rename the file or folder from the given path<br/><br/></td></tr>
<tr>
<td>
GetDetails<br/><br/>
</td><td>
String ActionType, <br/><br/>String Path,<br/><br/>String[] Names,<br/><br/>IEnumerable&lt;object&gt; SelectedItems<br/><br/>
</td><td>
Response data should be in JSON format like below<br/><br/>{details:[{CreationTime:"4/28/2015 9:44:32 AM", Extension:".png", Format:"Archive", FullName:"F:\All samples\FileExplorer_Custom\FileExplorerContent\human.png", LastAccessTime:"4/28/2015 9:44:32 AM", LastWriteTime:"3/31/2015 3:16:35 PM", Length:11059, Name:"human.png"}]}<br/><br/>
</td><td>
get the details of the file/folder from the given path and return data in JSON format<br/><br/>
</td></tr>
<tr>
<td>
Download<br/><br/>
</td><td>
String ActionType,<br/><br/>String Path,<br/><br/>String[] Names,<br/><br/>IEnumerable&lt;object&gt; SelectedItems<br/><br/>
</td><td>
Void<br/><br/>
</td><td>
download the file from the given path<br/><br/>
</td></tr>
<tr>
<td>
Upload<br/><br/>
</td><td>
String ActionType, <br/><br/>IEnumerable&lt;HttpPostedFileBase&gt; FileUpload,<br/><br/>String Path<br/><br/>IEnumerable&lt;object&gt; SelectedItems <br/><br/>
</td><td>
Void<br/><br/>
</td><td>
upload the file to the given path<br/><br/>
<br/><br/>
</td></tr>
<tr>
<td>
GetImage<br/><br/>
</td><td>
String Path,<br/><br/>IEnumerable&lt;object&gt; SelectedItems<br/><br/>
</td><td>
Should return image in HttpResponseMessage.<br/><br/>
</td><td>
Used to get image form the given physical path.<br/><br/>
</td></tr>
<tr>
<td>
Search<br/><br/></td><td>
String ActionType,<br/><br/>String Path,<br/><br/>String SearchString,<br/><br/>Bool CaseSensitive<br/><br/>String ExtensionsAllow<br/><br/>IEnumerable&lt;object&gt; SelectedItems<br/><br/>
</td><td>
It should return data in JSON format with key name as ‘files’ and JSON fields need to be with following field names.<br/><br/>{"files":[{"name":"bird.jpg","type":"File","size":102182,"dateModified":"1/9/2016 6:48:42 AM","hasChild":false,"isFile":true,"filterPath":null},<br/><br/>{"name":"sea.jpg","type":"File","size":97145,"dateModified":"1/9/2016 6:48:42 AM","hasChild":false,"isFile":true,"filterPath":null }],"details":null,"error":null}<br/><br/></td><td>
It used to search all the matched files and sub-folders in the given folder path also it filters the specified files using it types.<br/><br/><br/><br/>
</td></tr>
</table>

## Customize the Root Folder name in FileExplorer

You can set the alias name to the root folder of FileExplorer by using [`rootFolderName`](https://help.syncfusion.com/api/js/ejfileexplorer#members:rootfoldername) API. It is used to replace the actual root folder name in the FileExplorer UI. Refer to the below sample to set the alias name for the root folder of FileExplorer.

Sample Link: [link](http://jsplayground.syncfusion.com/psx0vwle)


## Use the FTP connection using FileExplorer

You can access your FTP service using our FileExplorer component and can manage your files easily.

### FTP Login

First you will need the FTP account login information. You can connect with the primary username and password or an FTP account. The FTP server is open to the public, using anonymous access. But most of the FTP servers are password protected. 
Username: username or user@example.com
Password: The password that was created for the user you are using.

### FTP with FileExplorer server

In this FTP Web API application, we have provided “FTPFileOperationController” file, which contains “doJSONAction” action method. When you make AJAX request to this controller part, “doJSONAction” method will be called after based on ActionType” parameter value, then it calls the corresponding built-in FTP file handling methods such as ‘Read’, ‘Search’, ‘Download’, ‘Upload’, ‘Remove’, ‘Rename’ which are available in our “FTPFileExplorerOperations” class.

### Steps to create FileExplorer application to access FTP server

**Step 1:** Create a new ASP.NET MVC project using Visual Studio.

**Step 2:** Include **“FTPFileExplorerOperations”** file in that application. This file contains built-in file handling methods which helps to connect our FileExplorer with FTP service.

[http://www.syncfusion.com/downloads/support/directtrac/general/ze/FTPFileExplorerOperations901960089.zip](http://www.syncfusion.com/downloads/support/directtrac/general/ze/FTPFileExplorerOperations901960089.zip#)

**Step 3:** Add **“FileExplorerController.cs”** file in the controller part of FTP project.

This file, contains action handler methods. Based on the request parameters, it helps to call the built-in file handling methods of **FTPFileExplorerOperations** and perform corresponding actions.

{% highlight c# %}

        FTPFileExplorerOperations operation = new FTPFileExplorerOperations();
        
        [HttpPost]
        [ActionName("doJSONAction")]
        public object doJSONAction()
        {
            FileExplorerParams args = GetAjaxData(Request);

            if (args.ActionType == "Upload")
            {
                operation.Upload(args.Files, args.Path);
            }

            try
            {
                switch (args.ActionType)
                {
                    case "Read":
                        return operation.Read(args.Path, args.ExtensionsAllow);
                    case "Search":
                        return operation.Search(args.Path, args.ExtensionsAllow, args.SearchString, args.CaseSensitive);
                    case "CreateFolder":
                        return operation.CreateFolder(args.Path, args.Name);
                    case "Paste":
                        return operation.Paste(args.LocationFrom, args.LocationTo, args.Names, args.Action, null);
                    case "Remove":
                        return operation.Remove(args.Names, args.Path);
                    case "Rename":
                        return operation.Rename(args.Path, args.Name, args.NewName, null);
                    case "GetDetails":
                        return operation.GetDetails(args.Path, args.Names);
                }
                return "";

            }
            catch (Exception e)
            {
                FileExplorerResponse Response = new FileExplorerResponse();
                Response.error = e.GetType().FullName + ", " + e.Message;
                return Response;
            }
        }

        [HttpGet]
        [ActionName("PerformAction")]
        public void PerformAction(string ActionType, string Path)
        {

            if (ActionType == "Download")
                operation.Download(Path, HttpContext.Current.Request.QueryString.GetValues("Names"));
            else if (ActionType == "GetImage")
                operation.GetImage(Path, null);


        }

        [HttpGet]
        [ActionName("doJSONAction")]
        public void doJSONAction(string ActionType, string Path)
        {
            PerformAction(ActionType, Path);
        }

        public FileExplorerParams GetAjaxData(HttpRequestMessage request)
        {
            FileExplorerParams args = new FileExplorerParams();
            if (HttpContext.Current.Request.Files.Count > 0)
            {
                args.Path = HttpContext.Current.Request.QueryString.GetValues("Path")[0];
                args.ActionType = "Upload";
            }
            else
            {
                var serializer = new JavaScriptSerializer();
                args = (FileExplorerParams)serializer.Deserialize(request.Content.ReadAsStringAsync().Result, typeof(FileExplorerParams));
            }
            return args;
        }


{% endhighlight %}

**Step 4:** Add FTP Storage path that is viewed by FileExplorer.
You will create FTP URL like “ftp://localhost/FileBrowser/” (Port number may vary).
After that, you need to specify the FTP folder path and AJAX action handler name as shown in below code block.

{% highlight javascript %}

$("#fileExplorer").ejFileExplorer({ 
//Path of the folder that you want to view in FileExplorer. 
path: "ftp://localHost/FileBrowser/", 
//Path of file handling operation method 
ajaxAction: "http://localhost/FileExplorer/FileOperation/doJSONAction" });

{% endhighlight %}

We have prepared a demo based on above steps, please refer this.

[http://www.syncfusion.com/downloads/support/directtrac/general/ze/FTPWebAPI1239740174.zip](http://www.syncfusion.com/downloads/support/directtrac/general/ze/FTPWebAPI1239740174.zip#)