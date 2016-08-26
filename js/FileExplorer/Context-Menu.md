---
layout: post
title: Context Menu
description: Context Menu support in FileExplorer.
platform: js
control: FileExplorer
documentation: ug
---

# Context Menu

The context-menu has [list of items](#context-menu-items) which helps to perform FileExplorer operations, and it appears based on the target such as file or folder.

## Context menu items

The below table shows the context menu items corresponding to the location where it is opened:

<table>
<tr>
<th>
Context menu location</th><th>
Context menu items</th><th>
Screenshot</th></tr>
<tr>
<td>
While right click on treeview nodes (from navigation pane)<br/><br/></td><td>
* New Folder<br/>* Upload<br/>* Delete<br/>* Rename<br/>* Cut<br/>* Copy<br/>* Paste<br/><br/><br/><br/></td><td>
<br/><br/><br/><br/></td></tr>
<tr>
<td>
While right click on File / Folder<br/><br/></td><td>
* Open<br/>* Download<br/>* Upload<br/>* Delete<br/>* Rename<br/>* Cut<br/>* Copy<br/>* Paste<br/>* Get info<br/><br/><br/><br/></td><td>
<br/><br/><br/><br/></td></tr>
<tr>
<td>
While right click on layout (content pane)<br/><br/></td><td>
* Refresh<br/>* Paste<br/>* Sort by<br/>* New Folder<br/>* Upload <br/>* Get info <br/><br/><br/><br/></td><td>
<br/><br/><br/><br/></td></tr>
</table>
The below table explains the behavior of each context menu item:

<table>
<tr>
<td>
Open<br/><br/></td><td>
It opens the selected folder. When an image file selected it opens the preview of the image. For the remaining files this option becomes disabled.<br/><br/></td></tr>
<tr>
<td>
Download<br/><br/></td><td>
It downloads the selected file. When a file or number of files selected at that time only download option enabled.<br/><br/>If multiple files selected then it downloads all the files in a zip format.<br/><br/></td></tr>
<tr>
<td>
Cut<br/><br/></td><td>
It makes the copy of the selected files or folders into the clipboard. When the user paste the files in any location, the files are removed from the source location.<br/><br/></td></tr>
<tr>
<td>
Copy<br/><br/></td><td>
It makes the copy of the selected files or folders into the clipboard. When the user paste the files, the copy of the files only pasted in the target location.<br/><br/></td></tr>
<tr>
<td>
Paste<br/><br/></td><td>
It paste the files from the clipboard into the current selected folder. Note that when the files are copied into the clipboard at that time only it enabled.<br/><br/></td></tr>
<tr>
<td>
Delete<br/><br/></td><td>
It deletes the current selected file or folder. When you select any file or folder at that time only this option gets enabled.<br/><br/>If multiple files selected then it deletes all the selected items.<br/><br/></td></tr>
<tr>
<td>
Rename<br/><br/></td><td>
This is used to rename the current selected file or folder. When you select any file or folder at that time only this option gets enabled.<br/><br/>Even multiple files selected it renames the single file only.<br/><br/></td></tr>
<tr>
<td>
New Folder<br/><br/></td><td>
It creates a new folder on the current directory.<br/><br/>While click on the NewFolder item a dialog appears to get the folder name. Based on the user input, a new folder create on the current directory.<br/><br/></td></tr>
<tr>
<td>
Upload<br/><br/></td><td>
It uploads a file or list of files into the current directory.<br/><br/></td></tr>
<tr>
<td>
Get info<br/><br/></td><td>
It displays the details of the current selected file or folder.<br/><br/></td></tr>
<tr>
<td>
Sort by<br/><br/></td><td>
It's used to sorting the files and folders from the current directory.The sorting can be done based on the columns availbale from grid,in both ascending and descending order.<br/><br/></td></tr>
</table>
## Context menu Visibility

The presence of the context menu can be controlled by the [showContextMenu](http://help.syncfusion.com/js/api/ejfileexplorer#members:showcontextmenu) property. This was enabled by default, and by disabling this property you can prevent our built-in context menu.

{% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://mvc.syncfusion.com/ODataServices/FileBrowser/";

            var ajaxActionHandler = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                // hides our inbuilt context menu

                showContextMenu: false

            });

        });

{% endhighlight %}

## Enable / Disable the Context menu Item

The context menu items can be enabled or disabled through the client side public methods. It enables or disables the item from all the context menu where it is present. 

For example, if you disable the “Upload” item, it disables in all places wherever it appears such as open the context menu on treeview, open on file/folder, and open on layout.

* [enableMenuItem](http://help.syncfusion.com/js/api/ejfileexplorer#methods:enablemenuitem)
* [disableMenuItem](http://help.syncfusion.com/js/api/ejfileexplorer#methods:disablemenuitem)

These methods only accepts the context menu item name as the parameter. 

{% highlight javascript %}

        $(function () {

            var fileExpObj = $("#fileExplorer").data("ejFileExplorer");

            // this disables the New Folder item

            fileExpObj.disableMenuItem("New Folder");

            // this disables the Download item

            fileExpObj.disableMenuItem("Download");

        });

{% endhighlight %}

