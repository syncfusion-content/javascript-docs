---
title: How To| FileExplorer | Syncfusion
description: How to do - section for FileExplorer
platform: JS
control: FileExplorer
documentation: UG
keywords: FileExplorer,  Syncfusion, FileExplorer UG Doc, How To
---

# How To

## Cross-origin resource sharing support for FileExplorer

**Cross-origin request**

The FileExplorer can browse and manage files on remote servers, which is located in other domains. If a server is located on a different domain, on a different port or using different protocol (HTTP / HTTPS) such requests are considered to be “**cross-origin requests**”. These type of requests are prohibited by IE9 and its earlier browsers.

**Enabling cross-origin request in IE8 and IE9**

By default, Internet Explorer 9 and earlier prohibits cross-origin requests for Internet Zone, also it ignores Access-Control-Allow headers. To enable cross-origin in IE8 and IE9, we have specified two type of options. As per the requirements, you can use any option that is mentioned below.

**Option 1: Enabling cross-origin in IE through browser settings**

To enable cross-origin access using settings of IE browser, go to Tools->Internet Options->Security tab, click on “Custom Level” button. Find the Miscellaneous and select “Enable” option, which is available under “Access data sources across domains” settings.

If your server is located in Intranet Zone, In IE Browser, confirmation dialog will be popped during first cross-domain request as “*This page is accessing information that is not under its control. This poses a security risk. Do you want to continue*?”

To suppress this warning, you need to specify the "*Access data sources across domains*" setting to “allow”.

![](How-To_images/How-To_img1.jpeg)

**Option 2: Using JSONP for cross-origin request**

Using JSONP data type, you can perform cross origin-request. To enable cross-origin request, in your FileExplorer, you have to specify **ajaxDataType** as “**JSONP**”. And we have provided “**doJSONPAction**” method to handle “JSONP” type AJAX request on server side.  Please refer below code snippet to specify **ajaxDataType** as “JSONP”.

    
    {% highlight javascript %}
    
        $("#fileExplorer").ejFileExplorer({
            path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
            ajaxAction: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/doJSONPAction",
            ajaxDataType: "jsonp"
        });
        
    {% endhighlight %}
    
If we specify “ajaxDataType” as “JSONP”, data will be received in string format while calling “doJSONPAction” method of Web API Controller, here you need to deserialize the received “json” data into FileExplorerParams object. After performing corresponding operations, you have to specify the response data in serialized format with wrapped callback function. Please refer below code snippet to handle “JSONP” operations on server.

    
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


## Local service for FileExplorer

You can implement the file handling operations in your server as per your requirement. By default, we have provided built-in “FileExplorerOperations.cs” class for handling the file operation of “FileExplorer” in server side and you can find the file at following Web API service project. Please refer following Web API service, this may be helpful to you.

Web API service: [http://www.syncfusion.com/downloads/support/directtrac/general/ze/FileExplorer_WebAPI1406113770.zip](http://www.syncfusion.com/downloads/support/directtrac/general/ze/FileExplorer_WebAPI1406113770.zip#) 

N> Based on the “ActionType” parameter value that is available in the “doJSONPAction” action method of “FileOperationController” class, you can call the corresponding built-in file handling methods (Read, Search, Download, Upload, Remove, Rename etc...) that are available in our “FileExplorerOperations” class.

For your convenience, we have prepared a sample and service based on this and you can find it under following location.

Sample: [http://jsplayground.syncfusion.com/rm4zm5yw](http://jsplayground.syncfusion.com/rm4zm5yw#) 

N> First run the provided Web API service, then you will get an URL like [http://localhost:51460/](http://localhost:51460/#) (Here port number may change). As per port number, use the specified URL in “path” and “ajaxAction” of “FileExplorer” sample.

### Parameter list for AJAX request and response of FileExplorer

By default, we send following parameters in data field of the corresponding AJAX request. This helps to handle the server side operation. Some Server side action methods only will return the response data. This response data and request parameters are explained in following table. By referring to below table, you can create custom functions to perform server side operations of “FileExplorer”. 

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
<br/>IEnumerable<object> SelectedItems<br/>
<br/>
</td>
<td>
Response data should be in JSON format with key name as ‘files’ and JSON fields should be with following field names {{'__“__'| markdownify }}{{'__name__'| markdownify }}{{'__,__  '| markdownify }}{{'__isFile__'| markdownify }}{{'__,__ '| markdownify }}{{'__hasChild__'| markdownify }}{{'__”.__'| markdownify }}<br/><br/>If needed, customer can also add additional data along with the JSON result.<br/><br/>{{'__For__ '| markdownify }}{{'__example__'| markdownify }}{{'__:__'| markdownify }}<br/><br/>{files:[{name: "7.png", type: "File", size: 11439, dateModified: "3/31/2015 3:16:38 PM", hasChild: false},{name: "human.png", type: "File", size: 11059, dateModified: "3/31/2015 3:16:35 PM", hasChild: false}]}<br/>
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
IEnumerable<object> SelectedItems
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
<br/><br/>IEnumerable<CommonFileDetails> CommonFiles
<br/><br/>IEnumerable<object> SelectedItems
<br/><br/>IEnumerable<object> TargetFolder
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
<br/><br/>IEnumerable<object> SelectedItems
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
IEnumerable<CommonFileDetails> CommonFiles<br/><br/>IEnumerable<object> SelectedItems<br/><br/>
</td><td>
Here you may return the renamed file details or empty.<br/><br/><br/><br/>
</td><td>
Rename the file or folder from the given path<br/><br/></td></tr>
<tr>
<td>
GetDetails<br/><br/>
</td><td>
String ActionType, <br/><br/>String Path,<br/><br/>String[] Names,<br/><br/>IEnumerable<object> SelectedItems<br/><br/>
</td><td>
Response data should be in JSON format like below<br/><br/>{details:[{CreationTime:"4/28/2015 9:44:32 AM", Extension:".png", Format:"Archive", FullName:"F:\All samples\FileExplorer_Custom\FileExplorerContent\human.png", LastAccessTime:"4/28/2015 9:44:32 AM", LastWriteTime:"3/31/2015 3:16:35 PM", Length:11059, Name:"human.png"}]}<br/><br/>
</td><td>
get the details of the file/folder from the given path and return data in JSON format<br/><br/>
</td></tr>
<tr>
<td>
Download<br/><br/>
</td><td>
String ActionType,<br/><br/>String Path,<br/><br/>String[] Names,<br/><br/>IEnumerable<object> SelectedItems<br/><br/>
</td><td>
Void<br/><br/>
</td><td>
download the file from the given path<br/><br/>
</td></tr>
<tr>
<td>
Upload<br/><br/>
</td><td>
String ActionType, <br/><br/>IEnumerable<HttpPostedFileBase> FileUpload,<br/><br/>String Path<br/><br/>IEnumerable<object> SelectedItems <br/><br/>
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
String Path,<br/><br/>IEnumerable<object> SelectedItems<br/><br/>
</td><td>
Should return image in HttpResponseMessage.<br/><br/>
</td><td>
Used to get image form the given physical path.<br/><br/>
</td></tr>
<tr>
<td>
Search<br/><br/></td><td>
String ActionType,<br/><br/>String Path,<br/><br/>String SearchString,<br/><br/>Bool CaseSensitive<br/><br/>String ExtensionsAllow<br/><br/>IEnumerable<object> SelectedItems<br/><br/>
</td><td>
It should return data in JSON format with key name as ‘files’ and JSON fields need to be with following field names {{'__“__'| markdownify }}{{'__name__'| markdownify }}{{'__,__  '| markdownify }}{{'__isFile__'| markdownify }}{{'__,__ '| markdownify }}{{'__hasChild__'| markdownify }}{{'__”.__'| markdownify }}{{'____'| markdownify }}<br/><br/>{<br/><br/>"files":[{"name":"bird.jpg","type":"File","size":102182,"dateModified":"1/9/2016 6:48:42 AM","hasChild":false,"isFile":true,"filterPath":null},<br/><br/>{"name":"sea.jpg","type":"File","size":97145,"dateModified":"1/9/2016 6:48:42 AM","hasChild":false,"isFile":true,"filterPath":null }],<br/><br/>"details":null,<br/><br/>"error":null<br/><br/>}<br/><br/></td><td>
It used to search all the matched files and sub-folders in the given folder path also it filters the specified files using it types.<br/><br/><br/><br/>
</td></tr>
</table>
