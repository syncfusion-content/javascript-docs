---
layout: post
title: Enabling-the-ProgressBar
description: enabling the progressbar
platform: js
control: ProgressBar
documentation: ug
api: /api/js/ejprogressbar
---

# Enabling the ProgressBar

The ProgressBar is enabled by using the [enabled](https://help.syncfusion.com/api/js/ejprogressbar#members:enabled) Property. When this property is set to ‘**false**’, it disables the ProgressBar widget. By default, ‘**enabled**’ property is set to ‘**true**’ in the ProgressBar widget.

The following steps explain how to disable the ProgressBar widget when ‘**enabled**’ property is set to ‘**false**’.

In the **HTML** page, add a **&lt;div&gt;** element to render the ProgressBar widget.

{% highlight html %}

<div class="control">
    <div id="progressbar"></div>
</div>

{% endhighlight %}

{% highlight javascript %}


     // Add the ‘enabled’ property as follows.
     $(function () {
         //Declaration.
         $("#progressbar").ejProgressBar({
             enabled: false,
             value: 40,
             width: 500,
             height: 40
         });
         var progress = $("#progressbar").data("ejProgressBar");
         progress.setModel({ text: progress.getValue() + " %" });
     });

{% endhighlight %}

The following screenshot displays the output for the above code.

![](/js/ProgressBar/Enabling-the-ProgressBar_images/Enabling-the-ProgressBar_img1.png) 

