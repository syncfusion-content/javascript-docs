---
layout: post
title: Multiple Selection
description: FileExplorer allows the user to select multiple files
platform: js
control: File Explorer
documentation: ug
---


# Multiple Selection

The FileExplorer allows the user to select multiple files by enabling the [allowMultiSelection](http://help.syncfusion.com/api/js/ejfileexplorer#members:allowmultiselection) property. The multiple selection can be done by pressing the **Ctrl** key or **Shift** key. You can select all the files in the directory by pressing “**Ctrl + A**”. The multiple selection is useful on copy pasting multiple files, deleting multiple files and downloading multiple files.

{% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://mvc.syncfusion.com/ODataServices/FileBrowser/";

            var ajaxActionHandler = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                allowMultiSelection: false

            });

        });

{% endhighlight %}

