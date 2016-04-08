---
layout: post
title: getting-started
description: getting started
platform: js
control: Radial Slider
documentation: ug
---

# Getting Started

## Create your first Radial Slider control in JavaScript

In this section, you can learn how to create a simple **Radial Slider**.      

![](getting-started_images\getting-started_img1.png)

**Create a simple Radial Slider**

The following steps guide you to add a **Radial Slider** control.

1. Create an **HTML** file and paste the following template for web layout.

        {% highlight html %}

            <html>
            <head>
            <title>Radial Slider</title>
            <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css"rel="stylesheet"/>
            <script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>
            <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
            </head>
            <body>
                    <!-- Adds Radial Slider control Here -->
            </body>
            </html>

        {% endhighlight %}

2. Create a **div** element that is a container for **Radial Slider**. You can Refer to the following code example.

        {% highlight html %}
        
            <!DOCTYPE html>
            <html xmlns="http://www.w3.org/1999/xhtml">
            <head>
                <title>RadialSlider - GettingStarted</title>
                <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
                <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
                <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css" rel="stylesheet"/>
                <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js" type="text/javascript"> </script>	
                <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
                <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js" type="text/javascript"></script>
                <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>    
                <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.angular.min.js" type="text/javascript"></script>

            </head>
            <body>
                <div id="radialSlider">
                </div>
                <script>
                //Add the below script elements here.
                </script>
            </body>
            </html>

        {% endhighlight %}

3. Add the following styles in your code.
    
    {% highlight css %}

        <style type="text/css" class="cssStyles">
        
            .content {
                padding: 0 25px;
            }

            p {
                text-indent: 1em;
                text-align: justify;
            }

            #radialSlider.e-radialslider {
                margin: 0 auto;
            }
    
        </style>
       
       {% endhighlight %}

4. Initialize the "RadialSlider" widgets by adding the script section as below.

    {% highlight js %}
    
            $(function () {
                $("#radialSlider").ejRadialSlider({ innerCircleImageUrl: "../images/radialslider/chevron-right.png" });
            });
            
    {% endhighlight %}


The following screenshot shows the output for the above code example.


![](getting-started_images\getting-started_img2.png)

