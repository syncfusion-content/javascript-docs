---
layout: post
title: concept-and-features-
description: concept and features 
platform: js
control: File Explorer
documentation: ug
---

## Concept and features 

### Toolbar Support

The **FileExplorer** control provides a number of tool items that help manage the remote file system in an effective way. It brings to the Web, popular file management system found in the desktop Windows Explorer.

#### File Management

All the managing tools allow you to manage the file system easily. Using these tools you can add folders, upload files, delete, rename, move, copy, search etc.

##### List of Toolbar Items

* Add & open: Add a new folder, open folder and files.

* Address bar: Used to point the current viewing folder and provide navigation support with options for editing.

* Refreshing: Used to refresh the current viewing folder. 

* Upload: Provides the built-in Upload box control using which you can upload files easily.

* Deletion: You can delete the files and folders from the file system.

* Rename: It is used to rename file and folders easily.

* Download: Provides support for downloading files.

* Search bar: You can search for the files you require, easily with the customizable search option.

##### Backward and Forward

As the name explains, using the Backwardbackward tool you can navigate into the previously selected directories. And using the Forward tool, you can navigate into the forward direction of selected directories.

##### Clipboard action

The most used clipboard actions are cut, copy, and paste. These tools are used to rearrange the files in your file system. You can copy and paste the files or folders from one directory to another directory

* To render **FileExplorer** with the above toolbar options, include the following code in your **HTML** page.



{% highlight html %}

**[HTML]**
<div id="fileExplorer"></div>


{% endhighlight %}



Add the following code in your script section.



{% highlight js %}


**[JavaScript]**

<script type="text/javascript">
        $(function () {
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
    </script>
$(function () {
               var localServ = "http://mvc.syncfusion.com/OdataServices/api/fileoperation/PerformAction";
            $("#fileExplorer").ejFileExplorer({
                 path: "http://mvc.syncfusion.com/ODataServices/api/FileExplorer/FileExplorerContent/",
                ajaxAction: localServ,
                ajaxSettings: {
                    upload: {
                        url: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Upload{0}"
                    },
                    download: {
                        url: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Download{0}"
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



To render **FileExplorer** in MVC with the above toolbar options, include the following code in your **View** page.



[_cshtml]

@Html.EJ().FileExplorer("fileExplorer").Path("~/FileExplorerContent/").AjaxAction(@Url.Content("FileActionDefault"))



Add the following code block to the corresponding controller page, the **FileActionDefault** method is triggered, when you have made ajax request on client-side. This **FileActionDefault** method finds out the specific operation using the **ActionType** property and then call **FileExplorerOperations** methods according to that.



[cs]

using System;

using System.Collections.Generic;

using System.Linq;

using System.Web;

using System.Web.Mvc;

using Syncfusion.JavaScript;

using MVCSampleBrowser.Models;



namespace MVCSampleBrowser.Controllers

{

    public partial class FileExplorerController : Controller

    {                

        public ActionResult Default()

        {

            return View();

        }



        public ActionResult FileActionDefault(FileExplorerParams args)

        {

            switch (args.ActionType)

            {

                case "Read":

                    return Json(FileExplorerOperations.Read(args.Path,                        args.ExtensionsAllow));

                case "CreateFolder":

                    return Json(FileExplorerOperations.CreateFolder(args.Path, args.Name));

                case "Paste":

                    FileExplorerOperations.Paste(args.LocationFrom, args.LocationTo, args.Name, args.Type, args.Action);

                    break;

                case "Delete":

                    FileExplorerOperations.Delete(args.Name.Split(','), args.Path);

                    break;

                case "Rename":

                    FileExplorerOperations.Rename(args.Path, args.PreviousName, args.NewName, args.Type);

                    break;

                case "GetDetails":

                    return Json(FileExplorerOperations.GetDetails(args.Path, args.Name, args.Type));

                case "Download":

                    FileExplorerOperations.Download(args.Path);

                    break;                

                case "Upload":

                    FileExplorerOperations.Upload(args.FileUpload, args.Path);

                    break;

            }

            return Json("");

        }

    }

}





**FileExplorerOperations** is a predefined Class, that is used to perform File Explorer-based operations like read, createFolder, download, upload, rename, paste and getImage. It minimizes the work load on server-side.



{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img1.png" Caption="Figure 74: File Explorer with a list of toolbar items"%}{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img2.png" Caption="Figure 74: File Explorer with a list of toolbar items"%}

### Customization layout 

You can easily customize the layout of the File Explorer control, enable or disable the sub control parts in File Explorer as per your requirement. For example: disable/ enable toolbar, tree view, grid view, list view, footer part.

* To render **FileExplorer** with the above customizing options, include the following code in your **HTML** page.



{% highlight html %}

**[HTML]**
<div id="fileExplorer"></div>


{% endhighlight %}



Add the following code in your script section.



{% highlight js %}


**[JavaScript]**

    <script type="text/javascript">
        $(function () {
            var localServ = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";
            $("#fileExplorer").ejFileExplorer({
                fileTypes: "*.png, *.gif, *.jpg, *.jpeg, *.docx",
                layout: "list",
                path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
                ajaxAction: localServ,
                showToolbar: false,
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
    </script>$(function () {
            var localServ = "http://mvc.syncfusion.com/OdataServices/api/fileoperation/PerformAction";

            $("#fileExplorer").ejFileExplorer({
                 path: "http://mvc.syncfusion.com/ODataServices/api/FileExplorer/FileExplorerContent/",
                ajaxAction: localServ,
                showToolbar: false,
                ajaxSettings: {
                    upload: {
                        url: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Upload{0}"
                    },
                    download: {
                        url: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Download{0}"
                    }
                }              
                });
        });


{% endhighlight %}



In MVC,

**[_cshtml]**

@Html.EJ().FileExplorer("fileExplorer").Path("~/FileExplorerContent/").AjaxAction(@Url.Content("FileActionDefault")).ShowToolbar(false)



There is no change in the controller part, the same controller part is used as mentioned above.



{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img3.png" Caption="Figure 85: File Explorer with toolbar disabled"%}{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img4.png" Caption="Figure 85: File Explorer with toolbar disabled"%}

To render **FileExplorer** with the above disable tree view and footer options, include the following code in your **HTML** page.



{% highlight html %}

**[HTML]**
<div id="fileExplorer"></div>


{% endhighlight %}



Add the following code in your script section.



{% highlight js %}


**[JavaScript]**

<script type="text/javascript">
        $(function () {
            var localServ = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";
            $("#fileExplorer").ejFileExplorer({
                fileTypes: "*.png, *.gif, *.jpg, *.jpeg, *.docx",
                layout: "tile",
                path: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
                ajaxAction: localServ,
                showToolbar: false,
                showTreeview: false,
                showFooter: false,
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
    </script>$(function () {
            var localServ = "http://mvc.syncfusion.com/OdataServices/api/fileoperation/PerformAction";
            $("#fileExplorer").ejFileExplorer({
                 path: "http://mvc.syncfusion.com/ODataServices/api/FileExplorer/FileExplorerContent/",
                layout:"tile",
                ajaxAction: localServ,
                showTreeview: false,
                showFooter:false,
                ajaxSettings: {
                    upload: {
                        url: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Upload{0}"
                    },
                    download: {
                        url: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Download{0}"
                    }
                }
                });
        });


{% endhighlight %}



In MVC,

**[_cshtml]**

@Html.EJ().FileExplorer("fileExplorer").Path("~/FileExplorerContent/").AjaxAction(@Url.Content("FileActionDefault")).ShowTreeview(false).ShowFooter(false).Layout(LayoutType.Tile)



There is no change in the controller part, the same controller part is used as mentioned above.

{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img5.png" Caption="Figure 96: File Explorer with tree view and footer disabled"%}{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img6.png" Caption="Figure 96: File Explorer with tree view and footer disabled"%}

### File management options

#### Creating New Folder

By clicking the New Folder Icon, the highlighted model dialog opens as shown in the following screenshot using which you can add a new folder in the file system with the required name.



{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img7.png" Caption="Figure 107: File Explorer with adding folder model dialog"%}{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img8.png" Caption="Figure 107: File Explorer with adding folder model dialog"%}

#### Download option

The Download option is used to download the required files from the online file system. After selecting the download option, the following model dialog opens with the downloadable option.



{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img9.png" Caption="Figure 118: File Explorer with download file option"%}{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img10.png" Caption="Figure 118: File Explorer with download file option"%}

#### Upload option

You can upload files to the required place using the built-in Upload box control.



{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img11.png" Caption="Figure 129: File Explorer with upload option"%}{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img12.png" Caption="Figure 129: File Explorer with upload option"%}

#### Search support

To easily search the files in file system, you are provided with the Search bar option.



{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img13.png" Caption="Figure 1310: File Explorer with search option"%}{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img14.png" Caption="Figure 1310: File Explorer with search option"%}

#### Sorting support

In the Details view, you can sort the files using required fields. For example, in the following screenshot the Details view files are sorted in ascending order with respect to the modified date of files and folders.



{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img15.png" Caption="Figure 1411: File Explorer in details view with sorting support"%}{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img16.png" Caption="Figure 1411: File Explorer in details view with sorting support"%}

### Disable or Enabling toolbar tool

In Toolbar, you can disable or enable the tools as per your requirement. For example when you want to disable the Add a new folder tool, you can achieve it using the following code.

* To render **FileExplorer** with the Toolbar Tool Disabled option, include the following code in your **HTML** page.



{% highlight html %}

**[HTML]**
<div id="fileExplorer"></div>


{% endhighlight %}



Add the following code in your script section.



{% highlight js %}


**[JavaScript]**

    <script type="text/javascript">
        $(function () {
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

            // create the object for the file explorer.
            obj = $("#fileExplorer").data("ejFileExplorer");
            // Disable the toolbar items.
            obj.disableToolbarItem("fileExplorerNewFolder");

        });
    </script>$(function () {
            var localServ = "http://mvc.syncfusion.com/OdataServices/api/fileoperation/PerformAction";
            $("#fileExplorer").ejFileExplorer({
                 path: "http://mvc.syncfusion.com/ODataServices/api/FileExplorer/FileExplorerContent/",
                ajaxAction: localServ,
                 ajaxSettings: {
                    upload: {
                        url: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Upload{0}"
                    },
                    download: {
                        url: "http://mvc.syncfusion.com/OdataServices/api/fileoperation/Download{0}"
                    }
                }
                });
obj = $("#fileExplorer").data("ejFileExplorer");
obj.disableToolbarItem("fileExplorerNewFolder");
        });


{% endhighlight %}



In MVC,

**[_cshtml]**

@Html.EJ().FileExplorer("fileExplorer").Path("~/FileExplorerContent/").AjaxAction(@Url.Content("FileActionDefault"))



In your script section please add following code to diable toolbar tool.



**[JavaScript]**

&lt;script&gt;

        $(function () {          

            obj = $("#fileExplorer").data("ejFileExplorer");

            obj.disableToolbarItem("fileExplorerNewFolder");

        });



&lt;/script&gt;



There is no change in the controller part, it is the same controller part used as mentioned above.



{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img17.png" Caption="Figure 1512: In File Eexplorer, adding new folder icon is in disabled state"%}{% include image.html url="\js\FileExplorer\concept-and-features-_images\concept-and-features-_img18.png" Caption="Figure 1512: In File Eexplorer, adding new folder icon is in disabled state"%}



