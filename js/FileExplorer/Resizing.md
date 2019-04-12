---
layout: post
title: Resizing | FileExplorer | Syncfusion 
description: resize support
platform: js
control: File Explorer
documentation: ug
api: /api/js/ejfileexplorer
---

# Resizing 

The FileExplorer has the resize support through the resize handle which appears at right-bottom corner of footer. By clicking the resize handle the user can resize the FileExplorer through the UI. While resizing the dimension of the FileExplorer is automatically adjusted.

The resize behavior can be enabled through the [enableResize](https://help.syncfusion.com/api/js/ejfileexplorer#members:enableresize) property. 

{% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                // it enables the resize functionality

                // and a resize handle added in the Footer element

                enableResize: true

            });

        });

{% endhighlight %}

N> When resizing the File explorer control, the [resize](https://help.syncfusion.com/api/js/ejfileexplorer#events:resize) event is triggered. The [resizeStart](https://help.syncfusion.com/api/js/ejfileexplorer#events:resizestart) event is triggered while starting stage of resize and [resizeStop](https://help.syncfusion.com/api/js/ejfileexplorer#events:resizestop) event is triggered in the end of resize.

## Responsiveness

By enabling the [isResponsive](https://help.syncfusion.com/api/js/ejfileexplorer#members:isresponsive) property, you can make the FileExplorer as responsive. While resizing the FileExplorer component, the inner content and toolbar items are automatically adjusted to equalize the size. The toolbar items are displayed within Dropdown on enabling the responsive. Otherwise it floated to the next line to equalize the space.

N> We can use [adjustSize](https://help.syncfusion.com/api/js/ejfileexplorer#methods:adjustsize) method to refresh the size of FileExplorer control.

{% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

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

You can restrict the dimension of the FileExplorer by setting the [minHeight](https://help.syncfusion.com/api/js/ejfileexplorer#members:minheight), [maxHeight](https://help.syncfusion.com/api/js/ejfileexplorer#members:maxheight) and [minWidth](https://help.syncfusion.com/api/js/ejfileexplorer#members:minwidth),[maxWidth](https://help.syncfusion.com/api/js/ejfileexplorer#members:maxwidth) properties while resizing the FileExplorer. 

{% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

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

