---
layout: post
title: Toolbar-Support
description: toolbar support
platform: js
control: File Explorer
documentation: ug
---

# Toolbar Support

The **FileExplorer** control provides a number of tool items that help manage the remote file system in an effective way. It brings to the Web, popular file management system found in the desktop Windows Explorer.

## File Management

All the managing tools allow you to manage the file system easily. Using these tools you can add folders, upload files, delete, rename, move, copy, search etc.

### List of Toolbar Items

* Add & open: Add a new folder, open folder and files.
* Address bar: Used to point the current viewing folder and provide navigation support with options for editing.
* Refreshing: Used to refresh the current viewing folder. 
* Upload: Provides the built-in Upload box control using which you can upload files easily.
* Deletion: You can delete the files and folders from the file system.
* Rename: It is used to rename file and folders easily.
* Download: Provides support for downloading files.
* Search bar: You can search for the files you require, easily with the customizable search option.

### Backward and Forward

As the name explains, using the backward tool you can navigate into the previously selected directories. And using the Forward tool, you can navigate into the forward direction of selected directories.

### Clipboard action

The most used clipboard actions are cut, copy, and paste. These tools are used to rearrange the files in your file system. You can copy and paste the files or folders from one directory to another directory

To render **FileExplorer** with the above toolbar options, include the following code in your **HTML** page.



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
    });

    //here tools API contains following default values, so toolbar render with below tools
    //tools: {
    //    creation: ["NewFolder", "Open"],
    //    navigation: ["Back", "Forward"],
    //    addressBar: ["Addressbar"],
    //    editing: ["Refresh", "Upload", "Delete", "Rename", "Download"],
    //    copyPaste: ["Cut", "Copy", "Paste"],
    //    getProperties: ["Details"],
    //    searchBar: ["Searchbar"]
    //},


{% endhighlight %}





![](/js/FileExplorer/Toolbar-Support_images/Toolbar-Support_img1.png)

