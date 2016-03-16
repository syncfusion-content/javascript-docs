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

The FileExplorer can browse and manage files on [http://mvc.syncfusion.com/OdataServices](http://mvc.syncfusion.com/OdataServices#)  servers, which is located in other domains. If a server is located on a different domain, on a different port or using different protocol (HTTP / HTTPS) such requests are considered to be “cross-origin requests”. These type requests are prohibited by IE9 and its earlier browsers.

**Enabling cross-origin request in IE8 and IE9**

By default, Internet Explorer 9 and earlier prohibits cross-origin requests for Internet Zone, also it ignores Access-Control-Allow headers. To enable cross-origin in IE8 and IE9, we have specified two type of options. As per the requirements, you can use any option that is mentioned below.

**Option 1: Enabling cross-origin in IE through browser settings**

To enable cross-origin access using settings of IE browser, go to Tools->Internet Options->Security tab, click on “Custom Level” button. Find the Miscellaneous and select “Enable” option, which is available under “Access data sources across domains” settings.

If your server is located in Intranet Zone, In IE Browser, confirmation dialog will be popped during first cross-domain request as “*This page is accessing information that is not under its control. This poses a security risk. Do you want to continue*?”

To suppress this warning, you need to specify the "*Access data sources across domains*" setting to “allow”.

![](How-To_images/How-To_img1.jpeg)

**Option 2: Using JSONP for cross-origin request**

Using JSONP data type, you can perform cross origin-request. To enable cross-origin request, in your FileExplorer, you have to specify **ajaxDataType** as “**JSONP**”. And we have provided “**doJSONPAction**” method to handle “JSONP” type Ajax request on server side.  Please refer below code snippet to specify **ajaxDataType** as “JSONP”.

    
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
