---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: NumericTextbox
documentation: ug
api: /api/js/
---

# RTL Support

The **NumericTextBox** provides **RTL** (**Right-To-Left**) support. The alignment of NumericTextBox can be changed from **Left-To-Right** into **Right-To-Left**.

## Enable RTL

The following steps explain the implementation of **enableRTL** in **NumericTextBox** .

In the HTML page set the corresponding &lt;input&gt; elements for rendering NumericTextBox control.

{% highlight html %}

<input id="numeric" type="text" />
	
{% endhighlight %}

{% highlight javascript %}


	    $("#numeric").ejNumericTextbox({
            value: 11,
            enableRTL: true
        });        


{% endhighlight %}


The output for **NumericTextBox** when **enableRTL** is **“true”** is as follows. 

![](/js/NumericTextBox/RTL-Support_images/RTL-Support_img1.png) 

