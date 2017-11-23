---
layout: post
title: RTL-Support
description: rtl support 
platform: js
control: Uploadbox
documentation: ug
api: /js/ejuploadbox
---

# RTL Support 

This feature supports the change of left-to-right alignment of the **Uploadbox** widget to right-to-left (**RTL**). That is, it sets the **Uploadbox** to right-to-left actions.

The following steps explain the configuration of [enableRTL](https://help.syncfusion.com/api/js/ejuploadbox#members:enablertl) property in **Uploadbox**. 

In the **HTML** page, add the **&lt;div&gt;** element to configure the **Uploadbox** element.

{% highlight html %}

<div class="control">
    <div id="Uploadbox"></div>
</div>

{% endhighlight %}

{% highlight js %}

    $(function () {
        //Declaration.
        $("#uploadbox").ejUploadbox({
            saveUrl: "saveFiles.ashx",
            removeUrl: "removeFiles.ashx",
            enableRTL: true
        });
    });

{% endhighlight %}

For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively.

The following screenshot displays the output.



![](/js/UploadBox/RTL-Support_images/RTL-Support_img1.png) 



