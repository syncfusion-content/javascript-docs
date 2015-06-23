---
layout: post
title: Separators
description: separators
platform: js
control: Menu
documentation: ug
---

# Separators

Menu can also contain separators that are horizontal bars between menu items. You cannot select a separator. Separators are somewhat similar to [borders](http://docs.oracle.com/javase/tutorial/uiswing/components/border.html), except that they are genuine components and, as such, are drawn inside a control, rather than around the edges of the **Menu** control. **enableSeparator** is the property that is used to display the separators in the **Menu** control. It accepts the Boolean type value. Its default value is true. 

Add the following **&lt;script&gt;** in the above code sample.




The following screenshot displays the output for the above code sample.

{% include image.html url="/js/Menu/Separators_images/Separators_img1.png" %}


Add the following **&lt;script&gt;** in the above code sample to display the **Menu** control without separator by setting **enableSeparator** as **false**.

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


    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            width: 500,
            enableSeparator: true
        });
    });



{% endhighlight %}



The following screenshot displays the output for the above code. 

{% include image.html url="/js/Menu/Separators_images/Separators_img2.png" %}


