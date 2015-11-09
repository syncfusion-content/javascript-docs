---
layout: post
title: Customization-layout
description: customization layout 
platform: js
control: File Explorer
documentation: ug
---

# Customization layout 

You can easily customize the layout of the FileExplorer control, enable or disable the sub control parts in File Explorer as per your requirement. For example: disable/ enable toolbar, tree view, grid view, list view, footer part.

To render **FileExplorer** with the above customizing options, include the following code in your **HTML** page.



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
          showToolbar: false,
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

{% endhighlight %}



![](/js/FileExplorer/Customization-layout_images/Customization-layout_img1.png)

To render **FileExplorer** with the above disable tree view and footer options, include the following code in your **HTML** page.



{% highlight html %}

<div id="fileExplorer"></div>

{% endhighlight %}



Add the following code in your script section.



{% highlight js %}

    $(function() {
       var localServ = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";
       $("#fileExplorer").ejFileExplorer({
          fileTypes: "*.png, *.gif, *.jpg, *.jpeg, *.docx",
          layout: "tile",
          path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
          ajaxAction: localServ,
          showToolbar: false,
          showTreeview: false,
          showFooter: false,
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

{% endhighlight %}



![](/js/FileExplorer/Customization-layout_images/Customization-layout_img2.png)

