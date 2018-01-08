---
layout: post
title: Digital-Elements
description: digital elements
platform: js
control: Digital Gauge
documentation: ug
api : /api/js/ejdigitalgauge
---

# Digital Elements

**Text Customization**

* The attribute [`value`](../api/ejdigitalgauge#members:items-value) refers the text displayed in the **Digital Gauge**. This text is applicable only for that item instead of all items. Text color is changed by using the property [`textColor`](../api/ejdigitalgauge#members:items-textcolor)

* It is possible to align the text inside the **Digital Gauge** control by using the property [`textAlign`](../api/ejdigitalgauge#members:items-textalign). Two possible values for text align are as follows

  * left

  * right


{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

  $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            items: [{
                // For setting alignment
                textAlign: "right",
                // For setting text
                value: "STOP",
            }]
        })
    });


{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.

![](/js/DigitalGauge/Digital-Elements_images/Digital-Elements_img1.png)

The [`custom font`](../api/ejdigitalgauge#members:items-enablecustomfont) is to be applied to the text by setting the value as true to the gauge.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

  $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            items: [{
                // For setting alignment
                textAlign: "right",
                // For setting text
                value: "STOP",
                enableCustomFont: true
            }]
        })
    });


{% endhighlight %}