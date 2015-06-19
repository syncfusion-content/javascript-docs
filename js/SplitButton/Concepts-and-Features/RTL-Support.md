---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: Split Button
documentation: ug
---

# RTL Support

In some cases it is necessary to use right to left alignment. **RTL** support is provided by using **enableRTL** property. In **RTL** mode when there is more than one content (image/text, image/image) in **Split Button**, then the content is aligned in right to left format. For example, when text is in left and image is in right position, after applying right to left alignment these position are interchanged.

The following steps explains you the details about rendering the button with Right to left alignment support

* In the **HTML** page, add the following button elements to configure **Split Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="spltspan"&gt;        <button id="spltbutton_rtl">login</button>        &lt;ul id="Ul11"&gt;            &lt;li&gt;<span>User</span>&lt;/li&gt;            &lt;li&gt;<span>Guest</span>&lt;/li&gt;            &lt;li&gt;<span>Admin</span>&lt;/li&gt;        &lt;/ul&gt; &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>     &lt;script type="text/javascript"&gt;            $(function () {                $("#spltbutton_rtl").ejSplitButton({                    //used to enable or disable RTL support for split button<b>                    enableRTL: true,</b>                    size: "small",                    contentType: "textandimage",                    showRoundedCorner: true,                    targetID: "Ul11",                    prefixIcon: "e-uiLight e-login"                });            });    &lt;/script&gt;</td></tr>
</table>


Configure the styles 



{% highlight css %}

[CSS]
   <style>
        .spltspan {
            margin-left: 120px;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 10: Split button in RTL alignment"%}

