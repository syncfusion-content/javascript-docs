---
layout: post
title: Enabling-the-ProgressBar
description: enabling the progressbar
platform: js
control: ProgressBar
documentation: ug
---

# Enabling the ProgressBar

The **ProgressBar** is enabled by using the ‘**enabled**’ Property. When this property is set to ‘**false**’, it disables the **ProgressBar** widget. By default, ‘**enabled**’ property is set to ‘**true**’ in the **ProgressBar** widget.

The following steps explain how to disable the **ProgressBar** widget when ‘**enabled**’ property is set to ‘**false**’.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.

{% highlight html %}

**[HTML]**
            <div class="control">
            <div id="progressbar"></div>
            </div>

{% endhighlight %}

{% highlight js %}

**[JavaScript]**

// Add the ‘enabled’ property as follows.
<script type="text/javascript">
    $(function () {
//Declaration.
        $("#Progrssbar").ejProgressBar({
            enabled: false,
            value: 40,
            width: 500,
            height: 40
        });
        var progress = $("#progressbar").data("ejProgressBar");
        progress.setModel({ text: progress.getValue() + " %" });

    });

</script>

{% endhighlight %}

* The following screenshot displays the output for the above code.

{% include image.html url="/js/ProgressBar/Concepts-and-features/Enabling-the-ProgressBar_images/Enabling-the-ProgressBar_img1.png" Caption="Figure 12: Disabled ProgressBar"%}

