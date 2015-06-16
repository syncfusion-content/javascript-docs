---
layout: post
title: Getting-Started
description: getting started
platform: js
control: File Explorer
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **FileExplorer** in your application with **JavaScript.**

## Create your first FileExplorer in JavaScript

**Essential JavaScript FileExplorer** widget provides support to access the online file system and manage the files in an efficient way. From the following guidelines, you can learn how to access online file system and managing the files using FileExplorer control.

The following screenshot demonstrates the functionality of **FileExplorer** with details view and thumbnail view.

{% include image.html url="/js/FileExplorer/Getting-Started_images/Getting-Started_img1.png" Caption="Figure 1: FileExplorer Control with Grid view"%}



{% include image.html url="/js/FileExplorer/Getting-Started_images/Getting-Started_img2.png" Caption="Figure 2: FileExplorer Control with Thumbnail view"%}

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
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />      
    <script src=" http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js "></script>
    <script src=" http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js "></script>
    <script src=" http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js "></script>
    <script src=" http://cdn.syncfusion.com/js/assets/external/jsrender.min.js "></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script>    
</head>
<body>
    <!--add your FileExplorer elements here-->
    <!--add your Script section at here-->
    <!--add your CSS section at here-->    
</body>
</html>

{% endhighlight %}



Add div element to render a **FileExplorer.**



{% highlight html %}

<div id="fileExplorer"></div>


{% endhighlight %}



Initialize the script for **FileExplorer.**

> {% include image.html url="/js/FileExplorer/Getting-Started_images/Getting-Started_img3.png" Caption=""%}

_**Note: ajaxAction API used to perform ajax operation like read, delete creating folder etc, using ajaxAction property, mention the server class url. This server class that is provided handles ajax action, that is triggered client-side, same as uploading file and downloading file, customizable ajaxSettings are used. The upload property is used to call server action method, that uploads files to the server and downloads the property used to call server action to download files, that are located in the given path.  Here the path property is an important one, as you can mention the root path of file system using the path.**_



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



{% endhighlight %}



The following screenshot displays a **FileExplorer** control.



{% include image.html url="/js/FileExplorer/Getting-Started_images/Getting-Started_img4.png" Caption="Figure 3: FileExplorer Control with grid view"%}

