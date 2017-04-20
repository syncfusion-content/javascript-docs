---
layout: post
title: getting-started
description: getting started
platform: js
control: Radial Slider
documentation: ug
api: /api/js/ejradialslider
---

# Getting Started

In this section, you can learn how to create a simple **Radial Slider**.      

![](getting-started_images\getting-started_img1.png)

The external script dependencies of the RadialSlider component are,

* [jQuery 1.7.1](http://jquery.com/) and later versions.

And the internal script dependencies of the RadialSlider widget are:

<table>
    <tr>
        <th>File </th>
        <th>Description / Usage </th>
    </tr>
    <tr>
        <td>ej.core.min.js</td>
        <td>Must be referred always before using all the JS controls.</td>
    </tr>
    <tr>
        <td>ej.touch.min.js</td>
        <td>For providing touch support</td>
    </tr>
    <tr>
        <td>ej.radialslider.min.js</td>
        <td>This is main source file specific for rendering RadialSlider</td>
    </tr>
</table>

For getting started you can use the ‘ej.web.all.min.js’ file, which encapsulates all the 'ej' controls and frameworks in one single file.<br/> 

For themes, you can use the ‘ej.web.all.min.css’ CDN link from the snippet given. To add the themes in your application, please refer [this link](https://help.syncfusion.com/js/theming-in-essential-javascript-components#adding-specific-theme-to-your-application).


## Preparing HTML document

Create a new HTML file and add [CDN](https://help.syncfusion.com/js/cdn) links to the [JavaScript](https://help.syncfusion.com/js/dependencies) and [CSS](https://help.syncfusion.com/js/theming-in-essential-javascript-components) dependencies to your project.

{% highlight html %}

    <!DOCTYPE html>

    <html>

    <head>

        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />

        <!-- style sheet for default theme(flat azure) -->

        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css"
              rel="stylesheet" />

        <!--scripts-->

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js"></script>

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>

    </head>

    <body>

        <!--Place element to create RadialSlider-->

        <script>

            // Place your script code here to initialize RadialSlider

        </script>

    </body>

    </html>

{% endhighlight %}

 N>  In production, we highly recommend you to use our [custom script generator](https://help.syncfusion.com/js/include-only-the-needed-widgets#) to create a custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en#text-compression-with-gzip) on your server. 

## Create your first Radial Slider control in JavaScript

Create a **div** element that is a container for **Radial Slider**. You can Refer to the following code example.

        {% highlight html %}
        
                <div id="radialSlider"></div>
                
        {% endhighlight %}

Initialize the "RadialSlider" widgets by adding the script section as below.

    {% highlight js %}
    
            $(function () {
                $("#radialSlider").ejRadialSlider({ innerCircleImageUrl: "../images/radialslider/chevron-right.png" });
            });
            
    {% endhighlight %}


The following screenshot shows the output for the above code example.


![](getting-started_images\getting-started_img2.png)

