---
layout: post
title: Look-and-Feel
description: look and feel
platform: js
control: Dialog
documentation: ug
---

# Look and Feel

You can customize the appearance of **Dialog** widget using various themes that are available in **Essential JavaScript**. Applying themes customizes the entire control and its appearances. Refer the following link.
[http://help.syncfusion.com/ug/js/Documents/theming.htm](http://help.syncfusion.com/ug/js/Documents/theming.htm)

## CSS Class

The **CSS** properties can be customized by using **css**Class in the **Dialog** control. The following steps explains the implementation of cssClass option in the **Dialog** widget.

1. In the **HTML** page set a **&lt;div&gt;** element with the dialog content for rendering the **Dialog** control. 

{% highlight html %}

**[HTML]**

      <div id="Dialog" title="Syncfusion Dialog">
        The Syncfusion Dialog control is rendered.
    </div>

{% endhighlight %}

{% highlight js %}

**[JavaScript]**

// Set the cssClass property to the Dialog function
    <script type="text/javascript">
        $("#Dialog").ejDialog({
            height: 200,
            width: 300,
            cssClass: "customCss"
        });
    </script>

{% endhighlight %}

2. Customize the **CSS** class by setting **CSS** Properties. 



{% highlight css %}

**[CSS]**

    <style>
        .customCss {            
            border-color: #661e19 !important;
        }

        /*Customize the dialog header*/
        .customCss .e-header {
            background-color: #2c683b;
        }

        /*Customize the dialog content*/
        .customCss .e-dialog, .customCss .e-dialog-scroller {
          color: #b21010;
          background-color: #f6e492;        
         }
    </style>



{% endhighlight %}



3. The output for **Dialog** control after customizing the “**cssClass**” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Look-and-Feel_images/Look-and-Feel_img1.png" Caption="Dialog with cssClass"%}











