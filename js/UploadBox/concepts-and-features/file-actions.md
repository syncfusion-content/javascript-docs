---
layout: post
title: file-actions
description: file actions
platform: js
control: Uploadbox
documentation: ug
---

# File Actions

## Save File Action 

To save the uploaded file in **JS**, create the handler class and trigger the same in **saveUrl** property.  In that handler, save and specify the target location for uploaded files. The data type is **string**.

To save the uploaded file in **MVC**, create an **ActionResult** and trigger the same in **SaveUrl** property.  In **ActionResult**, save and specify the target location as **App_Data** folder for the uploaded files. The data type is **string**.

The following steps explain the configuration of **saveUrl** property in the **UploadBoxUploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                <b>saveUrl</b>: "saveFiles.ashx"            });        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b><b>// In the CSHTML page, add the UploadBox element.</b>@Html.EJ().Uploadbox("uploadbox").<b>SaveUrl</b>("Uploadbox/Save").RemoveUrl("Uploadbox/Remove")</td></tr>
<tr>
<td>
<b>[CS]</b><b>// Configure the ActionResult to save the file in App_Data location. In the following code example,the uploaded files is saved in App_Data folder.</b>public ActionResult Save(IEnumerable<HttpPostedFileBase> uploadbox)        {            foreach (var file in uploadbox)            {                var fileName = Path.GetFileName(file.FileName);                var destinationPath = Path.Combine(Server.MapPath("~/App_Data"), fileName);                file.SaveAs(destinationPath);            }            return Content("");        }</td></tr>
</table>


**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

&lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" &gt;&lt;/ej:UploadBox&gt;



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



* The following screenshot displays the output. 



{% include image.html url="\js\UploadBox\concepts-and-features\file-actions_images\file-actions_img1.png" Caption=" Figure 16: UploadBoxUploadbox with saveUrl property"%}

## Remove File Action 

To **remove** the uploaded file in **JS**, create a handler class and trigger the same in **removeUrl** property.  The uploaded file has to be removed from the handler where the file is saved. This is achieved by clicking **remove** button on **upload** dialog. The data type is **string**.

To remove the uploaded file in **MVC**, create **ActionResult** and trigger the same in **RemoveUrl** property.  This action removes the uploaded file from where it is saved. This is achieved by clicking **remove** button on **upload** dialog. The data type is **string**.

The following steps explain the configuration of **removeUrl** property in **UploadBoxUploadbox**. 

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                <b>removeUrl</b>: "removeFiles.ashx"            });        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b><b>// In the CSHTML page, add the UploadBox element.</b>@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").<b>RemoveUrl</b>("Uploadbox/Remove")</td></tr>
<tr>
<td>
<b>[CS] </b><b>// Configure the action to remove the file in target location. From that location, the file is searched and removed from the App_Data folder.</b> public ActionResult Remove(string[] fileNames)        {            foreach (var fullName in fileNames)            {                var fileName = Path.GetFileName(fullName);                var physicalPath = Path.Combine(Server.MapPath("~/App_Data"), fileName);                if (System.IO.File.Exists(physicalPath))                {                    System.IO.File.Delete(physicalPath);                }            }            return Content("");        }</td></tr>
</table>


**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

&lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" &gt;&lt;/ej:UploadBox&gt;



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

{% include image.html url="\js\UploadBox\concepts-and-features\file-actions_images\file-actions_img2.png" Caption="Figure 17: UploadBoxUploadbox with removeUrl property"%}{% include image.html url="\js\UploadBox\concepts-and-features\file-actions_images\file-actions_img3.png" Caption="Figure 17: UploadBoxUploadbox with removeUrl property"%}

##  Auto Upload

The **UploadBoxUploadbox** widget provides support to upload the file automatically once file is selected by using browse button, that is, without clicking upload button. To achieve this, set the **autoUpload** property to ‘**true**’. The data type is **Boolean**. By default, the value is set to ‘**false**’, so **upload** button is clicked to upload the files. 

The following steps explain the configuration of **autoUpload** property in **UploadBoxUploadbox**

* In the **HTML** page, add the **&lt;div&gt;** element to configure the **UploadBoxUploadbox** element.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="Uploadbox"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// Initialize the control in JavaScript.</b>&lt;script type="text/javascript"&gt;        $(function () {//Declaration.            $("#Uploadbox").ejUploadbox({                saveUrl: "saveFiles.ashx",                removeUrl: "removeFiles.ashx",<b>                autoUpload: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page, add the UploadBox element.**

@Html.EJ().Uploadbox("uploadbox").SaveUrl("Uploadbox/Save").RemoveUrl("Uploadbox/Remove").AutoUpload(true)



**[ASPX]**

**\\ In the ASPX page, add the uploadbox element.**

  &lt;ej:UploadBox ID="Uploadbox" runat="server" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx" AutoUpload="true" &gt;&lt;/ej:UploadBox&gt;  



1. For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 



For **MVC**, configure **Save****ActionResult** and **Remove****ActionResult** files as mentioned in Save file action and Remove file action respectively.

The following screenshot displays the output.



{% include image.html url="\js\UploadBox\concepts-and-features\file-actions_images\file-actions_img4.png" Caption="Figure 18: UploadBoxUploadbox with autoUpload property"%}{% include image.html url="\js\UploadBox\concepts-and-features\file-actions_images\file-actions_img5.png" Caption="Figure 18: UploadBoxUploadbox with autoUpload property"%}

