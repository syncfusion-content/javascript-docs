---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: RadialSlider
documentation: ug
---

# Appearance and Styling

## Theme

**RadialSlider** control support rich appearance. This control consist of six flat themes and six gradient themes. To use these twelve themes, refer the themes files in HTML file. 

You need two style sheets to apply styles to **RadialSlider** control; one **ej.widgets.core.min.css** and one **ej.theme.min.css**. If you use **ej.widgets.all.min.css** then you don’t need to use **ej.widgets.core.min.css** and **ej.theme.min.css** because **ej.widgets.all.min.css** is a combination of these two.

The core style sheet applies styles related to positioning and size, but are not related to the color scheme and always require the control to look correct and function properly. The theme styles heet applies theme-specific styles like colors and backgrounds.

The following list is of the twelve themes supported by **RadialSlider**:

* default-theme
* flat-azure-dark
* flat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark
* bootstrap-theme


Add the following code in your **HTML** page.

## Css Class

**RadialSlider** control also allows you to customize its appearance using user-defined CSS and custom skin options such as colors and backgrounds. To apply custom themes you have a property called **cssClass**. **cssClass** property sets the root class for **RadialSlider** theme.

Using this **cssClass** you can override the existing styles under the theme style sheet. The theme style sheet applies theme-specific styles like colors and backgrounds. In the following example, the value of **cssClass** property is set as “**Purple-dark**”. **Purple-dark** is added as root class to **RadialSlider** control at the runtime. From this root class you can customize the **RadialSlider** control theme.

Add the following code in your **HTML** page to render the RadialSlider.

{% highlight html %}
   
    <!DOCTYPE html>
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <title>RadialSlider - cssClass</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
        <link href="http://cdn.syncfusion.com/13.4.0.53/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
        <link href="http://cdn.syncfusion.com/13.4.0.58/js/web/responsive-css/ej.responsive.css" rel="stylesheet"/>
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js" type="text/javascript"> </script>	
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/13.4.0.53/js/web/ej.web.all.min.js" type="text/javascript"></script>    
        <script src="http://cdn.syncfusion.com/13.4.0.53/js/common/ej.widget.angular.min.js" type="text/javascript"></script>
    </head>
    <body>
        <div id="radialSlider">
        </div>
        <script>
            $("#radialSlider").ejRadialSlider({ innerCircleImageUrl:"chevron-right.png",cssClass:"Purple-dark" });
        </script>
    </body>
    </html>


{% endhighlight %}



In the following style sheet the exiting theme style sheet file has been over-ridden using root class “**Purple-dark**”. 

Add the following code in your style section.

{% highlight css %}

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
        
	  .Purple-dark{
		    background-color:pink;
		}

{% endhighlight %}

The following screenshot illustrates the output of the above code.

![](Appearance-and-Styling_images\Appearance-and-Styling_images_img1.png)

