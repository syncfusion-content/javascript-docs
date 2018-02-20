---
layout: post
title: Virtual Scrolling
description: Virtual Scrolling support
platform: js
control: File Explorer
documentation: ug
api: /api/js/ejfileexplorer
---


# Virtual Scrolling

Virtual Scrolling is introduced to provide support for loading files and folders on demand in order to improve performance in FileExplorer when large amount of files are present.

Virtual Scrolling can be enabled by using [virtualItemCount](https://help.syncfusion.com/api/js/ejfileexplorer#members:virtualitemcount) API. It specifies the total files to be loaded initially, and on each scroll the next set of files are loaded. For eg- If [virtualItemCount](https://help.syncfusion.com/api/js/ejfileexplorer#members:virtualitemcount) value is given as ”20”, then 20 items are loaded initially and on each scroll the next/previous 20 items are loaded. If the value of [virtualItemCount](https://help.syncfusion.com/api/js/ejfileexplorer#members:virtualitemcount) is 0, virtual scrolling will be disabled.

N>  Default value of `virtualItemCount` is 0.



{% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                virtualItemCount: 40  //virtualItemCount property is set to 40.

            });

        });

{% endhighlight %}

