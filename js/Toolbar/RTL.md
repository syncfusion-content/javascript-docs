---
layout: post
title: RTL
description: rtl
platform: js
control: Toolbar
documentation: ug
---

# RTL

This feature allows you to change the left-to-right alignment of the **Toolbar** to right-to-left (**RTL**) that sets the **Toolbar** to do its actions from right to left. The **enableRTL** property sets the **Toolbar** from right to left. Set the value to this property as **Boolean** type.

{% highlight js %}

    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ width: "290px", enableRTL: true });
    });

{% endhighlight %}

![]("/js/Toolbar/RTL_images/RTL_img1.png")
