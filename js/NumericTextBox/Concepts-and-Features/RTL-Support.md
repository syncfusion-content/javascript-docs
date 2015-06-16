---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: NumericTextbox
documentation: ug
---

# RTL Support

The **NumericTextBox** provides **RTL** (**Right-To-Left**) support. The alignment of NumericTextBox can be changed from **Left-To-Right** into **Right-To-Left**.

## Enable RTL

The following steps explain the implementation of **enableRTL** in **NumericTextBox** .

1. In the HTML page set the corresponding &lt;input&gt; elements for rendering NumericTextBox control.

{% highlight html %}

<input id="numeric" type="text" />
	
{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
	        $("#numeric").ejNumericTextbox({
            value: 11,
            enableRTL: true
        });        
</script>

{% endhighlight %}


The output for **NumericTextBox** when **enableRTL** is **“True”** is as follows. 

{% include image.html url="/js/NumericTextBox/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="NumericTextBox with enableRTL"%}

