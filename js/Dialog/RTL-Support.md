---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: Dialog
documentation: ug
---

# RTL Support

The **Dialog** supports Right-To-Left feature. The alignment of **Dialog** content can be changed from Left-To-Right into Right-To-Left.

## Enable RTL Support

The following steps explain enabling the right-to-left property for **Dialog** control.

In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 

{% highlight html %}

      <div id="rtlDialog" title="WinRT">
        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications <span>including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more.</span>
        It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
      </div>

{% endhighlight %}

{% highlight js %}


    // Enable RTL to the Dialog control by setting enableRTL property as true
    $("#rtlDialog").ejDialog({
        enableRTL: true,
        width: 550            
    });


{% endhighlight %}

The output for **Dialog** when **enabelRTL** is “**True**” is as follows.

{% include image.html url="/js/Dialog/RTL-Support_images/RTL-Support_img1.png" Caption="Dialog with enableRTL"%}

