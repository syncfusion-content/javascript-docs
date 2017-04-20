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

This feature allows you to upload and remove files **asynchronously**. To achieve this, set the **asyncUpload** property to ‘**true**’. The default value of **asyncUpload** property is ‘**true**’. The data type is **Boolean.**

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

