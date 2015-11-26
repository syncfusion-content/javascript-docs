---
layout: post
title: Resizing
description: resize support
platform: js
control: File Explorer
documentation: ug
---

# Resizing 

The FileExplorer has the resize support through the resize handle which appears at right-bottom corner of footer. By clicking the resize handle the user can resize the FileExplorer through the UI. While resizing the dimension of the FileExplorer is automatically adjusted.

The resize behavior can be enabled through the [enableResize](http://help.syncfusion.com/js/api/ejfileexplorer#members:enableresize) property. 

{% highlight js %}

        $(function () {

            var fileSystemPath = "http://mvc.syncfusion.com/ODataServices/FileBrowser/";

            var ajaxActionHandler = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                // it enables the resize functionality

                // and a resize handle added in the Footer element

                enableResize: true

            });

        });

{% endhighlight %}

## Responsiveness

By enabling the [isResponsive](http://help.syncfusion.com/js/api/ejfileexplorer#members:isresponsive) property, you can make the FileExplorer as responsive. While resizing the FileExplorer component, the inner content and toolbar items are automatically adjusted to equalize the size. The toolbar items are displayed within Dropdown on enabling the responsive. Otherwise it floated to the next line to equalize the space. 

{% highlight js %}

        $(function () {

            var fileSystemPath = "http://mvc.syncfusion.com/ODataServices/FileBrowser/";

            var ajaxActionHandler = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                // it enables the resize functionality

                enableResize: true,

                // it enables the control responsiveness

                isResponsive: true

            });

        });


{% endhighlight %}

## Restriction on Resize

You can restrict the dimension of the FileExplorer by setting the [minHeight](http://help.syncfusion.com/js/api/ejfileexplorer#members:minheight), [maxHeight](http://help.syncfusion.com/js/api/ejfileexplorer#members:maxheight) and [minWidth](http://help.syncfusion.com/js/api/ejfileexplorer#members:minwidth),[maxWidth](http://help.syncfusion.com/js/api/ejfileexplorer#members:maxwidth) properties while resizing the FileExplorer. 

{% highlight js %}

        $(function () {

            var fileSystemPath = "http://mvc.syncfusion.com/ODataServices/FileBrowser/";

            var ajaxActionHandler = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                enableResize: true,

                isResponsive: true,

                // restricts the dimensions for height and width

                minHeight: "200px",

                maxHeight: "400px",

                minWidth: "300px",

                maxWidth: "1200px"

            });

        });

{% endhighlight %}

