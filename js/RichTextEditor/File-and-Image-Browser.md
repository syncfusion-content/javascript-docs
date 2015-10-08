---
layout: post
title: File-and-Image-Browser
description: file and image browser
platform: js
control: RichTextEditor
documentation: ug
---

# File and Image Browser

## Image Browser

The **RTE** control normally allows you to insert the images based on the online URL only, optionally specifies the tooltip support. 

![]("/js/RichTextEditor/File-and-Image-Browser_images/File-and-Image-Browser_img1.png") 

But, now a feature is added, in that you can include an image by browsing a list of predefined files and directories. And also supports to showcase the dynamically uploaded images in the directory. 

![]("/js/RichTextEditor/File-and-Image-Browser_images/File-and-Image-Browser_img2.png") 

To retrieve or upload the images in the image browser, it requires a server side implementation.

Add the following code to initialize the **RTE** control in the page.

{% highlight html %}


<div class="rte">
    <textarea id="rteSample"></textarea>
</div>

{% endhighlight %}

{% highlight js %}


    // Render the RTE control in script section.
    var fileService = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";
    $(function() {
       $("#rteSample").ejRTE({
          //to showcase the image browser tool in rte toolbar
          toolsList: ["images"],
          tools: {
             images: ["image"]
          },
          //This api enable the image browser support to the RTE control
          imageBrowser: {
             filePath: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
             ajaxAction: fileService,
             extensionAllow: "*.png, *.gif, *.jpg, *.jpeg, *.docx"
          },
       });
    });

{% endhighlight %}


### filePath

This filePath property is used to define the initial folder to be displayed in the image browser, relative to the root. 

### extensionAllow

This property allows to showcase the specified file types in the image browser. Other types of files are restricted from view.

### ajaxAction

This property specifies the settings for loading and saving data. This property includes the actions such as **Read, CreateFolder, Paste, Delete, Rename, GetDetails, Download** and **Upload**.

The following screenshot displays the output.

![]("/js/RichTextEditor/File-and-Image-Browser_images/File-and-Image-Browser_img3.png") 

## File Browser

The **RTE** control provides the supports file browsing that is same as image browsing, instead of image the selected file path is displayed in the **RTE**.

![]("/js/RichTextEditor/File-and-Image-Browser_images/File-and-Image-Browser_img4.png") 

Add the following code to initialize the **RTE** control in the page.

{% highlight html %}

<div class="rte">
    <textarea id=" rteSample"></textarea>
</div>

{% endhighlight %}

{% highlight js %}

    // Render the RTE control in script section
    var fileService = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";
    $(function() {
       $("#rteSample").ejRTE({
          //to showcase the image browser tool in rte toolbar
          toolsList: ["images"],
          tools: {
             images: ["image"]
          },
          //This api enable the image browser support to the RTE control
          imageBrowser: {
             filePath: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
             ajaxAction: fileService,
             extensionAllow: "*.png, *.gif, *.jpg, *.jpeg, *.docx"
          },
          //This api enable the file browser support to the RTE control
          fileBrowser: {
             filePath: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",
             ajaxAction: fileService,
             extensionAllow: "*.txt, *.doc, *.pdf,*.docx"
          }
       });
    });

{% endhighlight %}


### filePath

This filePath property used to define the initial folder to be displayed in the file browser, relative to the root. 

### extensionAllow

This property allows to showcase the specified file types in the file browser. Other types of files are restricted from view.

### ajaxAction

This property specifies the settings for loading and saving data. This property includes the actions such as **Read, CreateFolder, Paste, Delete, Rename, GetDetails, Download** and **Upload**.

The following screenshot displays the output.

![]("/js/RichTextEditor/File-and-Image-Browser_images/File-and-Image-Browser_img5.png") 

