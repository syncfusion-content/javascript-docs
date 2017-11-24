---
layout: post
title: Setting-Range
description: setting range
platform: js
control: ProgressBar
documentation: ug
api: /api/js/ejprogressbar
---

# Setting Range

The **range** of the ProgressBar is set by using minimum and maximum values. The Minimum value specifies the value where the ProgressBar shows the process to have started. The Maximum value specifies the value where the process is completed. You can set the range by using the [minValue](https://help.syncfusion.com/api/js/ejprogressbar#members:minvalue) and [maxValue](https://help.syncfusion.com/api/js/ejprogressbar#members:maxvalue) property.

In the **HTML** page, add a **&lt;div&gt;** element to render the ProgressBar widget.

{% highlight html %}


   <div class="control">
        <div id="progressbar"></div>
   </div>

{% endhighlight %}

{% highlight js%}


          // Add Range for the ProgressBar widget as follows.
          $(function () {
                //Declaration.
                $("#progressbar").ejProgressBar({
                    minValue: 40,
                    maxValue: 80,
                    value: 80,
                    height: 20,
                    width: 500
                });
                var progress = $("#progressbar").data("ejProgressBar");
                progress.setModel({ text: progress.getPercentage() + " % Completed" });
           });

{% endhighlight %}

The following screenshot displays the output.

![](/js/ProgressBar/Setting-Range_images/Setting-Range_img1.png) 

