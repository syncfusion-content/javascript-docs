---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: Menu
documentation: ug
---

# Responsive Layout

Responsive Layout is aimed at crafting sites to provide an optimal viewing experience—easy reading and navigation with a minimum of resizing, panning, and scrolling—across a wide range of devices (from mobile phones to desktop computer monitors). In order to get responsive layout, you can add **ej.responsive.css** file in this sample. **CDN** link for the responsive css file is as follows.

[http://cdn.syncfusion.com/13.1.0.21/js/web/responsive-css/ej.responsive.css](http://cdn.syncfusion.com/13.1.0.21/js/web/responsive-css/ej.responsive.css)

> {% include image.html url="/js/Menu/Responsive-Layout_images/Responsive-Layout_img1.png" Caption=""%}**Note**: Refer to the ej.responsive.css file after the ej.widgets.all.min.css file

Add the above **css** link in the code sample.         

Add the following code in your **HTML** page.

{% highlight html %}


<div>
    <ul id="menucontrol">
        <li id="home">
            <a href="#">Home</a>
            <ul>
                <li><a>Foundation</a></li>
                <li><a>Launch</a></li>
                <li>
                    <a>About</a>
                    <ul>
                        <li><a>Company</a></li>
                        <li><a>Location</a></li>
                    </ul>
                </li>
            </ul>
        </li>
        <li id="Services">
            <a>Services</a>
            <ul>
                <li><a>Consulting</a></li>
                <li><a>Outsourcing</a></li>
            </ul>
        </li>
        <li id="About"><a>About</a></li>
        <li id="Contact">
            <a>Contact us</a>
            <ul>
                <li><a>Contact number</a></li>
                <li><a>E-mail</a></li>
            </ul>
        </li>
        <li id="Careers">
            <a>Careers</a>
            <ul>
                <li>
                    <a>Position</a>
                    <ul>
                        <li><a>Developer</a></li>
                        <li><a>Manager</a></li>
                    </ul>
                </li>
                <li><a>Apply online</a></li>
            </ul>
        </li>
    </ul>
</div>

{% endhighlight %}

{% highlight js %}


    // Add the following code in your script section.
    jQuery(function ($) {
        $("#menucontrol").ejMenu();
    });


{% endhighlight %}

The following screenshot displays the output for the above code. 

{% include image.html url="/js/Menu/Responsive-Layout_images/Responsive-Layout_img2.png" Caption="Menu with responsive layout"%}

