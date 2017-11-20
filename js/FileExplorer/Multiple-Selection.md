---
layout: post
title: Multiple Selection
description: FileExplorer allows the user to select multiple files
platform: js
control: File Explorer
documentation: ug
api: /api/js/ejfileexplorer
---


# Multiple Selection

The FileExplorer allows the user to select multiple files by enabling the [allowMultiSelection](https://help.syncfusion.com/api/js/ejfileexplorer#members:allowmultiselection) property. The multiple selection can be done by pressing the **Ctrl** key or **Shift** key. You can select all the files in the directory by pressing “**Ctrl + A**”. The multiple selection is useful on copy pasting multiple files, deleting multiple files and downloading multiple files. In another way, multiple files can be selected by mouse down and drag over the desired files. In addition to that, additional files can be selected with the preselected file by holding the ctrl/shift key and drag the mouse over the files. Also, holding the ctrl/shift key and dragging over selected files will unselect the selected files.

N>  For selecting files by mouse down and drag set `allowMultiSelection` property as true.



{% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                allowMultiSelection: true  //allowMultiSelection property is true by default

            });

        });

{% endhighlight %}

