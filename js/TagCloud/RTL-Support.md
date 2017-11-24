---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: TagCloud
documentation: ug
api: /api/js/ejtagcloud
---

# RTL Support

This feature supports you to change the left-to-right alignment of the **TagCloud** widget to right-to-left (RTL). This displays the content from right-to-left in the widget. You can achieve this using [enableRTL](https://help.syncfusion.com/api/js/ejtagcloud#members:enablertl) property that is set false by default.

## Enabling RTL Support

The following steps explains you the enabling of right-to-left property in **TagCloud**.

 In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.

{% highlight html %}

 <div id="website"></div>

{% endhighlight %}

{% highlight javascript %}


    // Enable RTL property for TagCloud.  
    $("#website").ejTagCloud({
       enableRTL:true,
        titleText: "Tech Sites",
        dataSource: websiteCollection
    });


{% endhighlight %}

The following screenshot illustrates the **TagCloud** control with RTL support.



![](/js/TagCloud/RTL-Support_images/RTL-Support_img1.png) 



