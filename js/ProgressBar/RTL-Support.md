---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: ProgressBar
documentation: ug
api: /api/js/ejprogressbar
---

# RTL Support

Right-to-left starts from the right of the page and continues to the left. By default, this option is set to ‘**false**’ in the ProgressBar control. The [enableRTL](https://help.syncfusion.com/api/js/ejprogressbar#members:enablertl) option allows the ProgressBar control to display it in the right to left direction.

The following steps explain how to **enable** the **RTL** property of the ProgressBar control.

In the **HTML** page, add a **&lt;div&gt;** element to render the ProgressBar widget.

{% highlight html %}

<div class="control">
   <div id="progressbar"></div>
</div>

{% endhighlight %}

{% highlight javascript %}

        
        // Add the following code example to enable the RTL property of the ProgressBar control.        
        $(function () {
        //Declaration.
        $("#progressbar").ejProgressBar({
            enableRTL: true,
            value: 80,
            text: 80,
            height: 20,
            width: 500
        });
        var progress = $("#progressbar").data("ejProgressbar");
        progress.setModel({ text: progress.getValue() + " % Completed" });
        });

{% endhighlight %}


The following screenshot displays the output.

![](/js/ProgressBar/RTL-Support_images/RTL-Support_img1.png) 























