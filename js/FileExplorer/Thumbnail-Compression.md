---
title: Thumbnail Compression | FileExplorer | JavaScript | Syncfusion
description: Thumbnail image size reduction option in FileExplorer
platform: js
control: FileExplorer
documentation: UG
keywords: Thumbnail compression, image compression, reduce image size
api: /api/js/ejfileexplorer
---

# Thumbnail Compression

The “FileExplorer” allows thumbnail images to be compressed on the server side and loaded into the “FileExplorer” layout to improve performance when working with large size images.

You can enable this option using “**enableThumbnailCompress**” API of FileExplorer. For enabling this API, [showThumbnail](https://help.syncfusion.com/api/js/ejfileexplorer#members:showthumbnail) must be set to true in order to render thumbnail preview of images in Tile and LargeIcons layout.

The [beforeGetImage](https://help.syncfusion.com/api/js/ejfileexplorer#events:beforegetimage) event is triggered before loading a requested image from the server and [getImage](https://help.syncfusion.com/api/js/ejfileexplorer#events:getimage) event is triggered after the requested image is loaded.

Refer following code block that will be helpful to you.



    {% highlight javascript %}

    $(function () {
        var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/webapi/FileExplorer/FileBrowser/";
        var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/fileoperation/doJSONAction";
        $("#fileExplorer").ejFileExplorer({
            path: fileSystemPath,
            ajaxAction: ajaxActionHandler,
            width: "100%",
            layout: "tile",
            enableThumbnailCompress: true
        });
    });

    {% endhighlight %}



N> In server side, don’t forget to add “[GetImage](https://help.syncfusion.com/cr/aspnetmvc/Syncfusion.JavaScript.FileExplorerOperations.html#Syncfusion_JavaScript_FileExplorerOperations_GetImage )” handling operation that helps to reduce the image size before loading.
