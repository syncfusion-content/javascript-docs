---
layout: post
title: Asynchronous-Upload
description: asynchronous upload
platform: js
control: Uploadbox
documentation: ug
api: /js/ejuploadbox
---

# Asynchronous Upload

This feature allows you to upload and remove files **asynchronously**.When multiple files are chosen in Asynchronous upload,files will be uploaded one by one to the server.User interaction with the page will not be interrupted at the time of upload.User can also remove the file even after uploading.This is the best way of file upload when compared to synchronous so by default UploadBox works with asynchronous upload option only. To achieve this, set the **asyncUpload** property to ‘**true**’. The default value of [asyncUpload](https://help.syncfusion.com/api/js/ejuploadbox#members:asyncupload) property is ‘**true**’. The data type is **Boolean.**

The following steps guide you in uploading the file **asynchronously**.

In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.

{% highlight html %}

<div id="Uploadbox"></div>

{% endhighlight %}

{% highlight js %}

    // Initialize the control in JavaScript.
    $(function () {
        //Declaration.
        $("#Uploadbox").ejUploadbox({
            saveUrl: "saveFiles.ashx",
            removeUrl: "removeFiles.ashx",
            asyncUpload: true
        });
    });

{% endhighlight %}

For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

