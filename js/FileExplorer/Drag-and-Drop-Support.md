---
title: Drag and Drop Support | FileExplorer | JavaScript | Syncfusion
description: Drag and Drop option in FileExplorer
platform: js
control: FileExplorer
documentation: UG
keywords: Drag and drop option
---

# Drag and Drop Support

The FileExplorer allows files to be moved from one folder to another by using drag and drop. It also supports uploading a file by dragging it from Windows Explorer to a folder in the FileExplorer control.

You can enable or disable this support by using “**allowDragAndDrop**” API of FileExplorer.


    {% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://mvc.syncfusion.com/ODataServices/FileBrowser/";

            var ajaxActionHandler = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                allowDragAndDrop: false

            });

        });

    {% endhighlight %}

