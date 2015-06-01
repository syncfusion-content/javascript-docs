---
layout: post
title: File-Actions
description: file actions
platform: js
control: Uploadbox
documentation: ug
---

# File Actions

## Save File Action 

To save the uploaded file in **JS**, create the handler class and trigger the same in **saveUrl** property.  In that handler, save and specify the target location for uploaded files. The data type is **string**.

The following steps explain the configuration of **saveUrl** property in the **Uploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                <b>saveUrl</b>: "saveFiles.ashx"            });        });    &lt;/script&gt;</td></tr>
</table>


* Configure the handler to save the file. Create a folder (for example, uploadfiles) and save the uploaded files into this folder.  

{% highlight c# %}

#saveFiles.ashx
**[ashx]**  

public class saveFiles : IHttpHandler {

    public void ProcessRequest(HttpContext context)
    {
        string targetFolder = HttpContext.Current.Server.MapPath("uploadfiles");
        if (!Directory.Exists(targetFolder))
        {
            Directory.CreateDirectory(targetFolder);
        }
        HttpRequest request = context.Request;
            HttpFileCollection uploadedFiles = context.Request.Files;
            if (uploadedFiles != null && uploadedFiles.Count > 0)
            {
                for (int i = 0; i < uploadedFiles.Count; i++)
                {
                    string fileName = uploadedFiles[i].FileName;
                    int indx = fileName.LastIndexOf("\\");
                    if (indx > -1)
                    {
                        fileName = fileName.Substring(indx + 1);
                    }
                    uploadedFiles[i].SaveAs(targetFolder + "\\" + fileName);
                }
            }
    }
    public bool IsReusable
    {
        get
        {
            return false;
        }
    }


{% endhighlight %}



The following screenshot displays the output. 

{% include image.html url="/js/UploadBox/Concepts-and-features/File-Actions_images/File-Actions_img1.png" Caption="Uploadbox with saveUrl property"%}

## Remove File Action 

To **remove** the uploaded file in **JS**, create a handler class and trigger the same in **removeUrl** property.  The uploaded file has to be removed from the handler where the file is saved. This is achieved by clicking **remove** button on **upload** dialog. The data type is **string**.

The following steps explain the configuration of **removeUrl** property in **Uploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                <b>removeUrl</b>: "removeFiles.ashx"            });        });    &lt;/script&gt;</td></tr>
</table>


* Configure the handlers to remove the file from the target location. From that location, the file is searched and removed from the ‘**uploadfiles’** folder.

{% highlight c# %}

#removeFiles.ashx
**[ashx]**  
public class removeFiles : IHttpHandler
{

    public void ProcessRequest(HttpContext context)
    {
        System.Collections.Specialized.NameValueCollection s = context.Request.Params;
        string fileName = s["fileNames"];
        string targetFolder = HttpContext.Current.Server.MapPath("uploadfiles");
        if (!Directory.Exists(targetFolder))
        {
            Directory.CreateDirectory(targetFolder);
        }

        string physicalPath = targetFolder + "\\" + fileName;
        if (System.IO.File.Exists(physicalPath))
        {
            System.IO.File.Delete(physicalPath);
        }

    }
    public bool IsReusable
    {
        get
        {
            return false;
        }
    }
}


{% endhighlight %}



The following screenshot displays the output. 

{% include image.html url="/js/UploadBox/Concepts-and-features/File-Actions_images/File-Actions_img2.png" Caption="Uploadbox with removeUrl property"%}

##  Auto Upload

The **Uploadbox** widget provides support to upload the file automatically once file is selected by using browse button, that is, without clicking upload button. To achieve this, set the **autoUpload** property to ‘**true**’. The data type is **Boolean**. By default, the value is set to ‘**false**’, so **upload** button is clicked to upload the files. 

The following steps explain the configuration of **autoUpload** property in **Uploadbox**

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                autoUpload: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

The following screenshot displays the output.



{% include image.html url="/js/UploadBox/Concepts-and-features/File-Actions_images/File-Actions_img3.png" Caption="Uploadbox with autoUpload property"%}

