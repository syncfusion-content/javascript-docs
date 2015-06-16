---
layout: post
title: RTL-support
description: rtl support
platform: js
control: AutoComplete
documentation: ug
---

# RTL support

This feature allows you to change the alignment of the **AutoComplete** textbox widget from left-to-right to right-to-left (**RTL**). The custom template **AutoComplete** textbox also supports **RTL**. 

## Enabling RTL Support

The following steps explain how you can enable the **right-to-left** property for an **AutoComplete** textbox.

1. In the **HTML** page, add an **&lt;input&gt;** element to configure the **AutoComplete** widget.

{% highlight html %}

         <input type="text" id="autocomplete" />


{% endhighlight %}



2. Enable **RTL** for **AutoComplete** control as follows.****

{% highlight js %}

<script type="text/javascript">
    $('#autocomplete').ejAutocomplete({
                dataSource: countries,
                width: 205,
                popupHeight: "80px",
                enableRTL: true,
                template: '<div class="flag ${sprite}"> </div>' +
                        '<div class="txt"> ${text} </div>'
            });
</script>


{% endhighlight %}



The following image is the output for AutoComplete when **enableRTL** is set to “**True”**.

{% include image.html url="/js/Autocomplete/Concepts-and-Features/RTL-support_images/RTL-support_img1.png" Caption="AutoComplete template with RTL support"%}

