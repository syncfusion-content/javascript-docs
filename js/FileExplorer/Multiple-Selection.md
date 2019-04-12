---
layout: post
title: Multiple Selection | FileExplorer | JavaScript | Syncfusion
description: FileExplorer allows the user to select multiple files
platform: js
control: File Explorer
documentation: ug
api: /api/js/ejfileexplorer
---


# Multiple Selection

The FileExplorer allows the user to select multiple files by enabling the [allowMultiSelection](https://help.syncfusion.com/api/js/ejfileexplorer#members:allowmultiselection) property. The multiple selection can be done by pressing the **Ctrl** key or **Shift** key. You can select all the files in the directory by pressing “**Ctrl + A**”. The multiple selection is useful on copy pasting multiple files, deleting multiple files and downloading multiple files. In another way, multiple files can be selected by mouse down and drag over the desired files. In addition to that, additional files can be selected with the preselected file by holding the ctrl/shift key and drag the mouse over the files. Also, holding the ctrl/shift key and dragging over selected files will unselect the selected files.

The [select](https://help.syncfusion.com/api/js/ejfileexplorer#events:select) event will be triggered when the items of FileExplorer control is selected.
Also [unselect](https://help.syncfusion.com/api/js/ejfileexplorer#events:unselect) event will be triggered when the items of FileExplorer control is unselected.

The [selectedItems](https://help.syncfusion.com/api/js/ejfileexplorer#members:selecteditems) is used to select the specified items (file, folder) of FileExplorer control.

The [selectedFolder](https://help.syncfusion.com/api/js/ejfileexplorer#members:selectedfolder) is used to select the specified folder of FileExplorer control. Also [refresh](https://help.syncfusion.com/api/js/ejfileexplorer#methods:refresh) method is used to refresh the content of the selected folder in FileExplorer control.

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

