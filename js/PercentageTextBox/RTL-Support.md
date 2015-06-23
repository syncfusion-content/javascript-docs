---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: PercentageTextBox 
documentation: ug
---

# RTL Support

The **PercentageTextBox** provides **RTL** (**Right-To-Left**) support. The alignment of **PercentageTextBox** can be changed from **Left-To-Right** into **Right-To-Left**.

## Enable RTL

The following steps explain the implementation of **enableRTL** in **PercentageTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.



{% highlight html %}

<table cellpadding="10">
    <tbody>
        <tr>
            <td>
                <label for="percent">Percent</label>
            </td>
            <td>
                <input id="percent" type="text" />
            </td>
        </tr>
    </tbody>
</table>

{% endhighlight %}

{% highlight js %}


	    $("#percent").ejPercentageTextbox({
            value: 22,
            enableRTL: true
        });


{% endhighlight %}


The output for **PercentageTextBox** when **enableRTL** is **“true”** is as follows. 

{% include image.html url="/js/PercentageTextBox/RTL-Support_images/RTL-Support_img1.png" %}

