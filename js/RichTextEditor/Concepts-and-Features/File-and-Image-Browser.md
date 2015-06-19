---
layout: post
title: File-and-Image-Browser
description: file and image browser
platform: js
control: RichTextEditor
documentation: ug
---

# File and Image Browser

### Image Browser

The **RTE** control normally allows you to insert the images based on the online URL only, optionally specifies the tooltip support. 

{% include image.html url="/js/RichTextEditor/Concepts-and-Features/File-and-Image-Browser_images/File-and-Image-Browser_img1.png" Caption="Figure 14: Default insert image"%}

But, now a feature is added, in that you can include an image by browsing a list of predefined files and directories. And also supports to showcase the dynamically uploaded images in the directory. 

{% include image.html url="/js/RichTextEditor/Concepts-and-Features/File-and-Image-Browser_images/File-and-Image-Browser_img2.png" Caption="Figure 15: Insert image with Image Browser"%}

To retrieve or upload the images in the image browser, it requires a server side implementation.

Add the following code to initialize the **RTE** control in the page.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="rte"&gt;        &lt;textarea id="rteSample"&gt;&lt;/textarea&gt; &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JAVASCRIPT]</b>// Render the RTE control in script section.&lt;script type="text/javascript"&gt;        var fileService = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";        $(function () {            $("#rteSample").ejRTE({                //to showcase the image browser tool in rte toolbar                toolsList: ["images"],                tools: { images: ["image"] },                //This api enable the image browser support to the RTE control                <b>imageBrowser: {</b><b>                    filePath: "http://mvc.syncfusion.com/ODataServices/FileBrowser/", </b><b>                    ajaxAction: fileService,</b><b>                    extensionAllow: "*.png, *.gif, *.jpg, *.jpeg, *.docx"</b><b>                },</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**filePath**

This filePath property is used to define the initial folder to be displayed in the image browser, relative to the root. 

**extensionAllow**

This property allows to showcase the specified file types in the image browser. Other types of files are restricted from view.

**ajaxAction**

This property specifies the settings for loading and saving data. This property includes the actions such as **Read, CreateFolder, Paste, Delete, Rename, GetDetails, Download** and **Upload**.

The following screenshot displays the output.

{% include image.html url="/js/RichTextEditor/Concepts-and-Features/File-and-Image-Browser_images/File-and-Image-Browser_img3.png" Caption="Figure 16: RTE with inserted image"%}

### File Browser

The **RTE** control provides the supports file browsing that is same as image browsing, instead of image the selected file path is displayed in the **RTE**.

{% include image.html url="/js/RichTextEditor/Concepts-and-Features/File-and-Image-Browser_images/File-and-Image-Browser_img4.png" Caption="Figure 17: RTE with File Browser"%}

Add the following code to initialize the **RTE** control in the page.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="rte"&gt;        &lt;textarea id=" rteSample"&gt;&lt;/textarea&gt; &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JAVASCRIPT]</b><b>//</b> Render the RTE control in script section&lt;script type="text/javascript"&gt;        var fileService = "http://mvc.syncfusion.com/OdataServices/fileExplorer/fileoperation/PerformAction";        $(function () {            $("#rteSample").ejRTE({                //to showcase the image browser tool in rte toolbar                toolsList: ["images"],                tools: { images: ["image"] },                //This api enable the image browser support to the RTE control                imageBrowser: {                    filePath: <b>"</b>http://mvc.syncfusion.com/ODataServices/FileBrowser/<b>",</b>                    ajaxAction: fileService,                    extensionAllow: "*.png, *.gif, *.jpg, *.jpeg, *.docx"                },                //This api enable the file browser support to the RTE control                <b>fileBrowser: {</b><b>                    filePath: "http://mvc.syncfusion.com/ODataServices/FileBrowser/",</b><b>                    ajaxAction: fileService,</b><b>                    extensionAllow: "*.txt, *.doc, *.pdf,*.docx"</b><b>                }</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**filePath**

This filePath property used to define the initial folder to be displayed in the file browser, relative to the root. 

**extensionAllow**

This property allows to showcase the specified file types in the file browser. Other types of files are restricted from view.

**ajaxAction**

This property specifies the settings for loading and saving data. This property includes the actions such as **Read, CreateFolder, Paste, Delete, Rename, GetDetails, Download** and **Upload**.

The following screenshot displays the output.

{% include image.html url="/js/RichTextEditor/Concepts-and-Features/File-and-Image-Browser_images/File-and-Image-Browser_img5.png" Caption="Figure 18: RTE with inserted file link"%}

