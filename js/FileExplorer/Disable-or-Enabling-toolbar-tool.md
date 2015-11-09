---
layout: post
title: Disable-or-Enabling-toolbar-tool
description: disable or enabling toolbar tool
platform: js
control: File Explorer
documentation: ug
---

# Disable or Enabling toolbar tool

In Toolbar, you can disable or enable the tools as per your requirement. For example when you want to disable the Add a new folder tool, you can achieve it using the following code.

To render **FileExplorer** with the Toolbar Tool Disabled option, include the following code in your **HTML** page.



{% highlight html %}

<div id="fileExplorer"></div>

{% endhighlight %}



Add the following code in your script section.



{% highlight js %}

    $(function() {
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
       // create the object for the file explorer.
       obj = $("#fileExplorer").data("ejFileExplorer");
       // Disable the toolbar items.
       obj.disableToolbarItem("fileExplorerNewFolder");
    });

{% endhighlight %}





![](/js/FileExplorer/Disable-or-Enabling-toolbar-tool_images/Disable-or-Enabling-toolbar-tool_img1.png)



