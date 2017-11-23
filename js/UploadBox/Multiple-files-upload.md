---
layout: post
title: Multiple-files-upload
description: multiple files upload
platform: js
control: Uploadbox
documentation: ug
api: /js/ejuploadbox
---

# Multiple files upload

The **Uploadbox** widget provides support to upload multiple files spontaneously. The [multipleFilesSelection](https://help.syncfusion.com/api/js/ejuploadbox#members:multiplefilesselection) property enables you to select multiple files while browsing.  To achieve this, set the **multipleFilesSelection** property to ‘**true**’. The data type is **Boolean**.

N> The Multiple file selection supports all the latest versions of browser except Internet Explorer 9 and its previous versions.



The following steps explain the configuration of **multipleFilesSelection** property in **Uploadbox**. 

In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.


{% highlight html %}

<div class="control">
    <div id="Uploadbox"></div>
</div>

{% endhighlight %}

{% highlight js %}

    // Initialize the control in JavaScript.
    $(function () {
        //Declaration.
        $("#Uploadbox").ejUploadbox({
            saveUrl: "saveFiles.ashx",
            removeUrl: "removeFiles.ashx",
            multipleFilesSelection: true
        });
    });

{% endhighlight %}

For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

The following screenshot displays the output.



![](/js/UploadBox/Multiple-files-upload_images/Multiple-files-upload_img1.png)



![](/js/UploadBox/Multiple-files-upload_images/Multiple-files-upload_img2.png)

