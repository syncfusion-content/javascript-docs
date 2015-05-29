---
layout: post
title: file-size-
description: file size 
platform: js
control: Uploadbox
documentation: ug
---

# File Size 

## Maximum File Size for UploadBoxUploadbox

In the **UploadBoxUploadbox** control, you can browse files with the size going up to gigabytes. You can restrict the files from being browsed using the **fileSize** property. When you do not use this property, it takes a default size, 31457280B, that is, 31MB.When this size exceeds, you cannot browse the file. 

* Add the following code example to the corresponding **HTML** page to render the **UploadBoxUploadbox** control with the customized file size.



{% highlight html %}

**[HTML]**
<div class="control">
     <div id="Uploadbox"></div>
</div>


{% endhighlight %}



* Initialize the **UploadBoxUploadbox** using the following code example.



{% highlight js %}

**[JavaScript]**
<script type="text/javascript">
        $("#UploadDefault").ejUploadbox({
            saveUrl: "save.ashx",
            removeUrl: "removeFiles.ashx",
            error: "fileuploaderror",
            **fileSize:1048576** //bytes
        });
        function fileuploaderror(e, ui) {
            alert(e.error);
        }
</script>


{% endhighlight %}



**EJMVC:**



**[CSHTML]**

&lt;div class="control"&gt;                 @Html.EJ().Uploadbox("UploadBox").SaveUrl("Uploadbox/Save").RemoveUrl("UploadBox/Remove").**FileSize(1048576)**

&lt;/div&gt;



**[Javascript]**

&lt;script type="text/javascript"&gt;

           function fileuploaderror(e, ui) {

            alert(e.error);

        }

&lt;/script&gt;



**EJWEB:**



**[ASPX]**

&lt;div class="control"&gt;

       &lt;ej:UploadBox ID="Uploadbox" runat="server" FileSize="1048576" SaveUrl="saveFiles.ashx" RemoveUrl="removeFiles.ashx"&gt;&lt;/ej:UploadBox&gt;

     &lt;/div&gt;



**[Javascript]**

&lt;script type="text/javascript"&gt;

           function fileuploaderror(e, ui) {

            alert(e.error);

        }

&lt;/script&gt;







To know about file action, we need to refer link:

[http://help.syncfusion.com/ug/js/default.htm#!documents/fileactions.htm](http://help.syncfusion.com/ug/js/default.htm)

The following screenshot displays **UploadBoxUploadbox** control with customized file size.

When you want to browse the file within the fileSize, you can browse and upload the files.



{% include image.html url="\js\UploadBox\concepts-and-features\file-size-_images\file-size-_img1.png" Caption="Figure 19: Maximum upload size within the fileSize property"%}

When you try to browse the file with exceeded fileSize, we cannot browse and upload the files.





{% include image.html url="\js\UploadBox\concepts-and-features\file-size-_images\file-size-_img2.png" Caption="Figure 120: Maximum Upload Size with exceeded fileSize property"%}

## Maximum File Upload Size in IIS

By default, the IIS web server allows for limited file size to be uploaded to the web server. By default, **Machine.config** is configured to accept HTTP Requests up to 4096 KB, that is, 4 MB. 

### How to upload files up to 28.6 MB?

In order to allow larger file size uploads, such as above 4MB, you can override it by modifying the “maxRequestLenth” attribute in the web application’s configuration file **web.config**. The property **maxRequestLength** indicates the maximum file upload size of 28.6MB, supported by ASP.NET. You cannot upload the files when the **fileSize** property is below the **maxRequestLength** value.



_Table_ _1__:_ _Property_

<table>
<tr>
<td>
Use-Case Description</td><td>
Type</td><td>
Maximum request size</td><td>
Details</td></tr>
<tr>
<td>
<a href=https://msdn.microsoft.com/en-us/library/system.web.configuration.httpruntimesection.maxrequestlength.aspx>maxRequestLength</a></td><td>
Property</td><td>
28.6 MB</td><td>
Maximum request sizesupported by ASP.NET.</td></tr>
</table>


*  Add the following code to your **web.config** file.



{% highlight c# %}

**[web.config]**
<configuration>
    <system.web>
        <httpruntime maxRequestLength="102400" /> //kilobytes
    </system.web>
</configuration>


{% endhighlight %}



> ![](file-size-_images\file-size-_img3.png)_**Note:  maxRequestLength is measured in kilobytes.**_

{% include image.html url="\js\UploadBox\concepts-and-features\file-size-_images\file-size-_img4.png" Caption="Figure 121: Maximum file upload using maxRequestLength		"%}

### How to upload the files above 28.6 MB?

The **maxRequestLength** property can be increased by modifying the “maxAllowedContentLength” attribute in the web application's configuration file **web.config**. The default maximum length of the content in a request supported by IIS is around 28.6 MB or 30000000bytes.



_Table_ _2__:_ _Property_

<table>
<tr>
<td>
Use-Case Description</td><td>
Type</td><td>
Default value</td><td>
Details</td></tr>
<tr>
<td>
<a href=https://msdn.microsoft.com/en-us/library/ms689462(v=vs.90).aspx>maxAllowedContentLength</a></td><td>
Property</td><td>
28.6 MB</td><td>
maxAllowedContentLength specifies the maximum length of content in a request supported by IIS.</td></tr>
</table>


* You can add the following code to your **web.config** file in order to set that value to 100 MB.



{% highlight c# %}

**[web.config]**
<system.webServer>
    <security>
        <requestFiltering>
            <requestLimits maxAllowedContentLength="104857600" /> //bytes
        </requestFiltering>
    </security>
</system.webServer>


{% endhighlight %}



> ![](file-size-_images\file-size-_img5.png)_**Note: maxAllowedContentLength is measured in bytes.**_

> _****_

{% include image.html url="\js\UploadBox\concepts-and-features\file-size-_images\file-size-_img6.png" Caption="Figure 122: Maximum file upload using maxAllowedContentLength"%}

__

> ![](file-size-_images\file-size-_img7.png)_**Note :**_                         

> * _**When you configure both maxAllowedContentLength, maxRequestLength attributes, then maxAllowedContentLength is considered for execution.**_

> * _**When the upload file’s size exceeds maxAllowedContentLength, you get a 404.13 error page.**_

> * _**When the upload file’s size exceeds maxRequestLength value, you get an exception “System.Web.HttpException: Maximum request length exceeded”.**_

> * _**The ASP.NET method of maxRequestLength is greater than or equal to the IIS method of limiting the request length (maxAllowedContentLength).**_

{% include image.html url="\js\UploadBox\concepts-and-features\file-size-_images\file-size-_img8.png" Caption="Figure 123: Maximum filesize for UploadBoxUploadbox with multiple file upload"%}

