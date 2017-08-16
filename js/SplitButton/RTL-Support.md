---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: Split Button
documentation: ug
api: /api/js/ejsplitbutton
---

# RTL Support

In some cases it is necessary to use right to left alignment. **RTL** support is provided by using **enableRTL** property. In **RTL** mode when there is more than one content (image/text, image/image) in **Split Button**, then the content is aligned in right to left format. For example, when text is in left and image is in right position, after applying right to left alignment these position are interchanged.

The following steps explains you the details about rendering the button with Right to left alignment support

In the **HTML** page, add the following button elements to configure **Split Button** widget.

{% highlight html %}

<div class="spltspan">
    <button id="splitButton_rtl">login</button>
    <ul id="Ul11">
        <li><span>User</span></li>
        <li><span>Guest</span></li>
        <li><span>Admin</span></li>
    </ul>
</div>

{% endhighlight %}


{% highlight javascript %}

    // Initialize the control in JavaScript
     
    $(function () {
        $("#splitButton_rtl").ejSplitButton({
            //used to enable or disable RTL support for split button
            enableRTL: true,
            size: "large",
            contentType: "textandimage",
            showRoundedCorner: true,
            targetID: "Ul11",
            prefixIcon: "e-icon e-login"
        });
    });
    

{% endhighlight %}


Configure the styles 

{% highlight css %}

<style>
    .spltspan {
        margin-left: 120px;
    }
</style>


{% endhighlight %}



Execute the above code to render the following output.

![](/js/SplitButton/RTL-Support_images/RTL-Support_img1.png) 

