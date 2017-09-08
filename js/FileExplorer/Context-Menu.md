---
layout: post
title: Context Menu
description: Context Menu support in FileExplorer.
platform: js
control: FileExplorer
documentation: ug
api: /api/js/ejfileexplorer
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
* New folder<br/>* Upload<br/>* Delete<br/>* Rename<br/>* Cut<br/>* Copy<br/>* Paste<br/><br/><br/><br/></td><td>
<br/><br/><br/><br/></td></tr>
<tr>
<td>
While right click on File / Folder<br/><br/></td><td>
* Open<br/>* Download<br/>* Upload<br/>* Delete<br/>* Rename<br/>* Cut<br/>* Copy<br/>* Paste<br/>* Get info<br/><br/><br/><br/></td><td>
<br/><br/><br/><br/></td></tr>
<tr>
<td>
While right click on layout (content pane)<br/><br/></td><td>
* Refresh<br/>* Paste<br/>* Sort By<br/>* New folder<br/>* Upload <br/>* Get info <br/><br/><br/><br/></td><td>
<br/><br/><br/><br/></td></tr>
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
New folder<br/><br/></td><td>
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
<td>Sort By<br/><br/></td>
<td>
It's used to sorting the files and folders from the current directory.The sorting can be done based on the columns available from grid,in both ascending and descending order.<br/><br/>
</td></tr>
</table>

## Context menu Visibility

The presence of the context menu can be controlled by the [showContextMenu](https://help.syncfusion.com/api/js/ejfileexplorer#members:showcontextmenu) property. This was enabled by default, and by disabling this property you can prevent our built-in context menu.

{% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler,

                // hides our built-in context menu

                showContextMenu: false

            });

        });

{% endhighlight %}

## Enable / Disable the Context menu Item

The context menu items can be enabled or disabled through the client side public methods. It enables or disables the item from all the context menu where it is present. 

For example, if you disable the “Upload” item, it disables in all places wherever it appears such as open the context menu on treeview, open on file/folder, and open on layout.

* [enableMenuItem](https://help.syncfusion.com/api/js/ejfileexplorer#methods:enablemenuitem)
* [disableMenuItem](https://help.syncfusion.com/api/js/ejfileexplorer#methods:disablemenuitem)

These methods only accepts the context menu item name as the parameter. 

{% highlight javascript %}

        $(function () {

            var fileExpObj = $("#fileExplorer").data("ejFileExplorer");

            // this disables the New Folder item

            fileExpObj.disableMenuItem("New folder");

            // this disables the Download item

            fileExpObj.disableMenuItem("Download");

        });

{% endhighlight %}

## Context Menu Customization

You can customize the ContextMenu of FileExplorer control by using [contextMenuSettings](https://help.syncfusion.com/api/js/ejfileexplorer#members:contextmenusettings) property. 

You can add your own context menu items and its action along with default context menu items of FileExplorer control. You can also remove the default context menu items in FileExplorer control. 

To add/remove/re-arrange context menu items, you need to use [contextMenuSettings.items](https://help.syncfusion.com/api/js/ejfileexplorer#members:contextmenusettings-items) property and to bind required actions for newly added menu items and add sub menu items, use [contextMenuSettings.customMenuFields](https://help.syncfusion.com/api/js/ejfileexplorer#members:contextmenusettings-custommenufields) property. 

{% highlight html %}

<!--create the FileExplorer wrapper-->
	
<div id="fileExplorer"></div>

{% endhighlight %}

{% highlight js %}

$(function () {
    $("#fileExplorer").ejFileExplorer({
        isResponsive: true,
        width: "100%",
        minWidth: "150px",
        contextMenuSettings: {
            //define the ContextMenu items
            items: {
                // removed the "NewFolder" item from NavigationPane ContextMenu
                navbar: ["Upload", "|", "Delete", "Rename", "|", "Cut", "Copy", "Paste", "|", "Getinfo"],
                // added the custom ContextMenu item (View) to Current working directory ContextMenu
                cwd: ["Refresh", "Paste", "|", "SortBy", "View", "|", "NewFolder", "Upload", "|", "Getinfo"],
                // removed "Upload" item from Selected files/ folder's ContextMenu
                files: ["Open", "Download", "|", "Delete", "Rename", "|", "Cut", "Copy", "Paste", "|",
                    "OpenFolderLocation", "Getinfo"]
            },
            //added the custom ContextMenu item's (View) functionality
            customMenuFields: [
            {
                id: "View",
                text: "View by",
                spriteCssClass: "custom-grid",
                //added sub menu items
                child: [
                {
                    id: "tile",
                    text: "Tile view",
                    //specify the action for this menu item
                    action: "onLayout"
                },
                {
                    id: "grid",
                    text: "Grid view",
                    //specify the action for this menu item
                    action: "onLayout"
                },
                {
                    id: "largeIcons",
                    text: "Large icons view",
                    //specify the action for this menu item
                    action: "onLayout"
                }, ]
            }, ]
        },
        path: "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/",
        ajaxAction: "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations",
        layoutChange: "onLayoutChange",
        menuOpen: "onMenuOpen"
    });
});
function onLayout(args) {
    //perform actions while click custom menu items
    var explorerObj = $('#fileExplorer').data("ejFileExplorer");
    explorerObj && explorerObj.option("layout", args.ID);
}
function onMenuOpen(args) {
    //customize the custom menu items
    if (args.contextMenu == "cwd") {
        $(".fe-context-menu").find(".e-fe-activeicon").removeClass("e-fe-activeicon");
        $(".fe-context-menu").find("." + this.model.layout).addClass("e-fe-activeicon");
    }
}
function onLayoutChange(args) {
    $(".fe-context-menu .View").removeClass("custom-grid custom-tile custom-largeicons");
    $(".fe-context-menu .View").addClass("custom-" + this.model.layout);
}

{% endhighlight %}

Icons of context menu items can be customized by overriding the default context menu item style. The following code example illustrates how to customize the icon of context menu items.

{% highlight css %}

<style>
    .fe-context-menu .custom-grid:before {
        content: "\e7b9";
    }

    .fe-context-menu .custom-largeicons:before {
        content: "\e7bb";
    }

    .fe-context-menu .custom-tile:before {
        content: "\e7be";
    }
</style>

{% endhighlight %}

The following screenshot displays the customization of context menu in FileExplorer control.

![](Context-Menu_images/Context-Menu_img1.png)

For more details about context menu customization, refer the sample [here](http://jsplayground.syncfusion.com/Sync_nz201mh4).

## Context Menu Events

You would be notified with events when you try to open the context menu items (**menuBeforeOpen**), after context menu items is opened (**menuOpen**) and when you click the menu items (**menuClick**). The following code example illustrates how to define those events.

{% highlight js %}

$("#fileExplorer").ejFileExplorer({
    menuBeforeOpen: function (args) {
        //you add/remove the context menu items in run time
        //do your custom action here.
        args.dataSource.pop();
    },
    menuOpen: function (args) {
        //you can also identify which context menu is opened by 
        if (args.contextMenu == "cwd") {
            //do your custom action here.
        }
    },
    menuClick: function (args) {
        switch (args.text) {
            case "largeicons":
                //do your custom action here.
                break;
        }
    }
});

{% endhighlight %}
