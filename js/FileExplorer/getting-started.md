---
layout: post
title: getting-started
description: getting started
platform: js
control: File Explorer
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **FileExplorer** in your application with **JavaScript****JavaScript**and **ASP.NET MVC.**

## Create your first File ExplorerFileExplorer in JavaScript

**Essential Java Script File ExplorerFileExplorer** widget provides support to access the online file system and manage the files in an efficient way. From the following guidelines, you can learn how to access online file system and managing the files using File Explorer control.

The following screenshot demonstrates the functionality of **File Explorer** with details view and thumbnail view.

{% include image.html url="\js\FileExplorer\getting-started_images\getting-started_img1.png" Caption="Figure 1: File Explorer Control with Grid view"%}{% include image.html url="\js\FileExplorer\getting-started_images\getting-started_img2.png" Caption="Figure 1: File Explorer Control with Grid view"%}



{% include image.html url="\js\FileExplorer\getting-started_images\getting-started_img3.png" Caption="Figure 2: File Explorer Control with Thumbnail view"%}{% include image.html url="\js\FileExplorer\getting-started_images\getting-started_img4.png" Caption="Figure 2: File Explorer Control with Thumbnail view"%}

In the above screenshot, you can access and manage the remote file system. While performing the operation on files like delete, rename etc, this is handled using Web API service.

### Create FileExplorer widgets



**Essential JavaScript FileExplorer** widget basically renders built-in features like accessing online file system through web and manage files like creating a folder, upload files, delete, rename, move or copy and searching files.  You can easily create the FileExplorer widget by using the following steps.

* Create an **HTML** file and add the following template to the **HTML** file.



{% highlight html %}

<!doctype html>
    <html>
    <head>
        <title>Essential Studio for JavaScript :FileExplorer</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
        <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /><link href=" http://cdn.syncfusion.com/12.1/js/web/flat-azure/ej.web.all.min.css " rel="stylesheet" />

  <script src=" http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js "></script>
        <script src=" http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js "></script>
        <script src=" http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js "></script>
        <script src=" http://cdn.syncfusion.com/js/assets/external/jsrender.min.js "></script>
        <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script><script src="http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js"></script>
    </head>
    <body>
        <!--add your FileExplorer elements here-->
    <!--add your Script section at here-->
    <!--add your CSS section at here--><!—add your File explorer elements here at here-->
        <!—add your Script section at here-->
        <!—add your CSS section at here-->

   </body>
   </html>


{% endhighlight %}



Add div element to render a **File Explorer.**



{% highlight html %}

<div id="fileExplorer"></div>


{% endhighlight %}



Initialize the script for **File ExplorerFileExplorer.**

> ![](getting-started_images\getting-started_img5.png)_**Note: ajaxAction API used to perform ajax operation like read, delete creating folder etc, using ajaxAction property, mention the server class url. This server class that is provided handles ajax action, that is triggered client-side, same as uploading file and downloading file, customizable ajaxSettings are used. The upload property is used to call server action method, that uploads files to the server and downloads the property used to call server action to download files, that are located in the given path.  Here the path property is an import**__**ant one, as you can mention the root path of file system using the path.**_



{% highlight js %}


<script type="text/javascript">
        $(function () {
            var localServ = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";
            $("#fileExplorer").ejFileExplorer({
                fileTypes: "*.png, *.gif, *.jpg, *.jpeg, *.docx",
                layout: "list",
                path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
                ajaxAction: localServ,
                ajaxSettings: {
                    upload: {
                        url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Upload{0}"
                    },
                    download: {
                        url: "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/Download{0}"
                    }
                }
            });
        });
    </script>
<script type="text/javascript">
        $(function () {
    var localServ = "http://mvc.syncfusion.com/OdataServices/api/fileoperation/PerformAction";	         	 
    $("#fileExplorer").ejFileExplorer({
           path: "http://mvc.syncfusion.com/ODataServices/api/FileExplorer/FileExplorerContent/",
           ajaxAction: localServ,
ajaxSettings: {
                    upload: {
                        url: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Upload{0}"
                    },
                    download: {
                        url:       "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Download{0}"
                    }
                } 
    });
  </script>


{% endhighlight %}



The following screenshot displays a **FileExplorer** control.



{% include image.html url="\js\FileExplorer\getting-started_images\getting-started_img6.png" Caption="Figure 3: File Explorer Control with grid view"%}{% include image.html url="\js\FileExplorer\getting-started_images\getting-started_img7.png" Caption="Figure 3: File Explorer Control with grid view"%}

## Create your first FileExplorer in MVC

**ASP.NET MVC File Explorer** widget provides support to access the online file system and managing the files in an efficient way. From the following guidelines, you can learn how to access online file system and managing the files using File Explorer control.

The following screenshot demonstrates the functionality of **File Explorer** with Details view and Thumbnail view.

{% include image.html url="\js\FileExplorer\getting-started_images\getting-started_img8.png" Caption="Figure 4: File Explorer Control with Grid view"%}



{% include image.html url="\js\FileExplorer\getting-started_images\getting-started_img9.png" Caption="Figure 5: File Explorer Control with Thumbnail view"%}

In the above screenshot, you can access and manage the remote file system. While you perform the operation on files like delete or rename , this is handled in the controller part.

**Create FileExplorer**

**ASP.NET MVC FileExplorer** widget renders built-in features like accessing online file system through web and managing files like creating a folder, upload files, delete, rename, move or copy and search files.  You can easily create the FileExplorer widget by using the following steps.

* You can create an **MVC** project and add necessary assemblies, styles, and scripts with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

* Add the following code example to the corresponding View page to render the **File Explorer.**



@Html.EJ().FileExplorer("fileExplorer").Path("~/FileExplorerContent/").AjaxAction(@Url.Content("FileActionDefault"))



Add the following code example to the corresponding controller page, **FileActionDefault** method is triggered, when you have made ajax request on client-side. This **FileActionDefault** method finds out the specific operations using the **ActionType** property and calls the **FileExplorerOperations** methods according to that.



using System;

using System.Collections.Generic;

using System.Linq;

using System.Web;

using System.Web.Mvc;

using Syncfusion.JavaScript;

using MVCSampleBrowser.Models;



namespace MVCSampleBrowser.Controllers

{

    public partial class FileExplorerController : Controller

    {                

        public ActionResult Default()

        {

            return View();

        }



        public ActionResult FileActionDefault(FileExplorerParams args)

        {

            switch (args.ActionType)

            {

                case "Read":

                    return Json(FileExplorerOperations.Read(args.Path,                        args.ExtensionsAllow));

                case "CreateFolder":

                    return Json(FileExplorerOperations.CreateFolder(args.Path, args.Name));

                case "Paste":

                    FileExplorerOperations.Paste(args.LocationFrom, args.LocationTo, args.Name, args.Type, args.Action);

                    break;

                case "Delete":

                    FileExplorerOperations.Delete(args.Name.Split(','), args.Path);

                    break;

                case "Rename":

                    FileExplorerOperations.Rename(args.Path, args.PreviousName, args.NewName, args.Type);

                    break;

                case "GetDetails":

                    return Json(FileExplorerOperations.GetDetails(args.Path, args.Name, args.Type));

                case "Download":

                    FileExplorerOperations.Download(args.Path);

                    break;

                case "Upload":

                    FileExplorerOperations.Upload(args.FileUpload, args.Path);

                    break;

            }

            return Json("");

        }

    }

}





**FileExplorerOperations** is a predefined Class, that is used to perform File Explorer-based operations like read, createFolder, download, upload, rename, paste, getImage. It minimizes the work load on server-side.

The following screenshot displays a **FileExplorer** control.



{% include image.html url="\js\FileExplorer\getting-started_images\getting-started_img10.png" Caption="Figure 6: File Explorer Control with Grid view"%}

