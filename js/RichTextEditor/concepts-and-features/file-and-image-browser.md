---
layout: post
title: file-and-image-browser
description: file and image browser
platform: js
control: RichTextEditor
documentation: ug
---

# File and Image Browser

### Image Browser

The **RTE** control normally allows you to insert the images based on the online URL only, optionally specifies the tooltip support. 

{% include image.html url="\js\RichTextEditor\concepts-and-features\file-and-image-browser_images\file-and-image-browser_img1.png" Caption="Figure 1426: Default insert image"%}

But, now a feature is added, in that you can include an image by browsing a list of predefined files and directories. And also supports to showcase the dynamically uploaded images in the directory. 

{% include image.html url="\js\RichTextEditor\concepts-and-features\file-and-image-browser_images\file-and-image-browser_img2.png" Caption="Figure 1527: Insert image with Image Browser"%}

To retrieve or upload the images in the image browser, it requires a server side implementation.

Add the following code to initialize the **RTE** control in the page.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="rte"&gt;        &lt;textarea id=" rteSample"&gt;&lt;/textarea&gt; &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JAVASCRIPT]</b>// Render the RTE control in script section.&lt;script type="text/javascript"&gt;        var fileService = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";var fileService = "http://mvc.syncfusion.com/OdataServices/api/fileoperation/";        $(function () {            $("#rteSample").ejRTE({                //to showcase the image browser tool in rte toolbar                toolsList: ["images"],                tools: { images: ["image"] },                //This api enable the image browser support to the RTE control                <b>imageBrowser: {</b><b>                    filePath: "http://mvc.syncfusion.com/ODataServices/FileBrowser/../FileExplorerContent/",   </b>//local path<b>                    ajaxAction: fileService,</b><b>                    extensionAllow: "*.png, *.gif, *.jpg, *.jpeg, *.docx"</b><b>                },</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[MVC]**

**[CSHTML]**



//the FileActionDefault is method to perform the all file related operations. 



@{ List<String> images = new List<string>() { "images" };

  List<String> image = new List<string>() { "image" };}

    @{Html.EJ().RTE("rteSample").Width("850px").ToolsList(images).ShowFooter(true).Tools(tool => tool.Images(image))**.ImageBrowser(img => img.FilePath("~/FileExplorerContent/").ExtensionAllow("*.png,*.gif,*.jpg,*.jpeg").AjaxAction(@Url.Content("FileActionDefault")))**.Render();}



Add the following code example to the corresponding controller page. **FileActionDefault** method is triggered, when the Ajax request is made on the client side. This **FileActionDefault** method finds out the specific operation by using **ActionType** property and calls the **FileExplorerOperations** methods according to that.

**[MVC]**

 **[CS]**

//Add the following method in the controller page 



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

                case "GetImage":

                    return File(FileExplorerOperations.GetImage(args.Path), "*");

                case "Upload":

                    FileExplorerOperations.Upload(args.FileUpload, args.Path);

                    break;

            }

            return Json("");

        }





**filePath**

This filePath property is used to define the initial folder to be displayed in the image browser, relative to the root. 

**extensionAllow**

This property allows to showcase the specified file types in the image browser. Other types of files are restricted from view.

**ajaxAction**

This property specifies the settings for loading and saving data. This property includes the actions such as **Read, CreateFolder, Paste, Delete, Rename, GetDetails, Download** and **Upload**.

The following screenshot displays the output.

{% include image.html url="\js\RichTextEditor\concepts-and-features\file-and-image-browser_images\file-and-image-browser_img3.png" Caption="Figure 1628: RTE with inserted image"%}

### File Browser

The **RTE** control provides the supports file browsing that is same as image browsing, instead of image the selected file path is displayed in the **RTE**.

{% include image.html url="\js\RichTextEditor\concepts-and-features\file-and-image-browser_images\file-and-image-browser_img4.png" Caption="Figure 2917: RTE with File Browser"%}

Add the following code to initialize the **RTE** control in the page.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="rte"&gt;        &lt;textarea id=" rteSample"&gt;&lt;/textarea&gt; &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JAVASCRIPT]</b><b>//</b> Render the RTE control in script section&lt;script type="text/javascript"&gt;        var fileService = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";var fileService = "http://mvc.syncfusion.com/OdataServices/api/fileoperation/";        $(function () {            $("#rteSample").ejRTE({                //to showcase the image browser tool in rte toolbar                toolsList: ["images"],                tools: { images: ["image"] },                //This api enable the image browser support to the RTE control                imageBrowser: {                    filePath: <b>"</b>http://mvc.syncfusion.com/ODataServices/FileBrowser/<b>",</b>"../FileExplorerContent/", //local path                    ajaxAction: fileService,                    extensionAllow: "*.png, *.gif, *.jpg, *.jpeg, *.docx"                },                //This api enable the file browser support to the RTE control                <b>fileBrowser: {</b><b>                    filePath: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",</b>"../FileExplorerContent/", //local path<b>                    ajaxAction: fileService,</b><b>                    extensionAllow: "*.txt, *.doc, *.pdf,*.docx"</b><b>                }</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[MVC]**

**[CSHTML]**



//the FileActionDefault is method to perform the all file related operations. 



@{ List<String> images = new List<string>() { "images" };

   List<String> image = new List<string>() { "image" };}

    @{Html.EJ().RTE("rteSample").Width("850px").ToolsList(images).ShowFooter(true).Tools(tool => tool.Images(image)).ImageBrowser(img => img.FilePath("~/FileExplorerContent/").ExtensionAllow("*.png,*.gif,*.jpg,*.jpeg").AjaxAction(@Url.Content("FileActionDefault"))).**FileBrowser(file => file.FilePath("~/FileExplorerContent/").ExtensionAllow("*.png,*.txt,*.jpg,*.docx").AjaxAction("FileActionDefault"))**.Render();} 



Add the following code example to the corresponding controller page. **FileActionDefault** method is triggered, when ajax request is made on client side. This **FileActionDefault** method finds out the specific operation by using **ActionType** property and calls the **FileExplorerOperations** methods according to that.

**[MVC]**

**[CS]**

//Add the following method in the controller page 



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

                case "GetImage":

                    return File(FileExplorerOperations.GetImage(args.Path), "*");

                case "Upload":

                    FileExplorerOperations.Upload(args.FileUpload, args.Path);

                    break;

            }

            return Json("");

        }





**filePath**

This filePath property used to define the initial folder to be displayed in the file browser, relative to the root. 

**extensionAllow**

This property allows to showcase the specified file types in the file browser. Other types of files are restricted from view.

**ajaxAction**

This property specifies the settings for loading and saving data. This property includes the actions such as **Read, CreateFolder, Paste, Delete, Rename, GetDetails, Download** and **Upload**.

The following screenshot displays the output.

{% include image.html url="\js\RichTextEditor\concepts-and-features\file-and-image-browser_images\file-and-image-browser_img5.png" Caption="Figure 1830: RTE with inserted file link"%}

