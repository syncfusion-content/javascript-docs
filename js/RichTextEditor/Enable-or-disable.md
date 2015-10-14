---
layout: post
title: Enable-or-disable
description: enable or disable
platform: js
control: RichTextEditor
documentation: ug
---

# Enable or Disable

You can enable or disable the tool items that are available in the **RTE** toolbar. Intermittently, some tool item actions are not allowed in the editing area. To avoid errors in such situations, you can disable the unnecessary tool items. Later, you can enable the disabled tool items, and when you don't use images in your blog, you can disable the image tool item by using the “**disableToolbarItem**” method. The following example illustrates how to disable the “**image**” tool.

Add the following code example in your **HTML** page.

{% highlight html %}

<div class="rte">
    <textarea id="disable_tool"></textarea>
</div>

{% endhighlight %}

{% highlight js %}

    //Add the following code in your script section to render RTE
    var rteobj;
    $(function () {
        $("#disable_tool").ejRTE();
        rteobj = $("#disable_tool").data("ejRTE");
        rteobj.disableToolbarItem("image");
    });


{% endhighlight %}


![](Enable-or-disable_images/Enable-or-disable_img1.png)


