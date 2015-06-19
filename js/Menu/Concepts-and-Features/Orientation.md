---
layout: post
title: Orientation
description: orientation
platform: js
control: Menu
documentation: ug
---

# Orientation

It gets or sets the direction in which the **Menu** control renders and specifies the orientation of the normal menu.  According to the orientation property the **Menu** control renders in horizontal or vertical.

**Horizontal Menu**

Horizontal orientation displays the menu items horizontally and it is the default orientation behavior of **Menu** control. 

The following steps explains you the details on rendering the **Menu** control. 

* In an **HTML** page, add the **&lt;ul&gt;** and **&lt;li&gt;** to configure **Menu** control.



<table>
<tr>
<td>
<b>[HTML]    </b>&lt;div&gt;    &lt;ul id="menucontrol"&gt;        &lt;li id="home"&gt;            <a href="#">Home</a>            &lt;ul&gt;                &lt;li&gt;<a>Foundation</a>&lt;/li&gt;                &lt;li&gt;<a>Launch</a>&lt;/li&gt;                &lt;li&gt;                    <a>About</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Company</a>&lt;/li&gt;                        &lt;li&gt;<a>Location</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Services"&gt;            <a>Services</a>            &lt;ul&gt;                &lt;li&gt;<a>Consulting</a>&lt;/li&gt;                &lt;li&gt;<a>Outsourcing</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="About"&gt;<a>About</a>&lt;/li&gt;        &lt;li id="Contact"&gt;            <a>Contact us</a>            &lt;ul&gt;                &lt;li&gt;<a>Contact number</a>&lt;/li&gt;                &lt;li&gt;<a>E-mail</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Careers"&gt;            <a>Careers</a>            &lt;ul&gt;                &lt;li&gt;                    <a>Position</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Developer</a>&lt;/li&gt;                        &lt;li&gt;<a>Manager</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;<a>Apply online</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b> [Javascript]     </b><b>// Initialize the control in JavaScript.</b><br>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#menucontrol").ejMenu({ width: 500 });    });&lt;/script&gt;</td></tr>
</table>


The following screenshot displays the output of the above code.        

{% include image.html url="/js/Menu/Concepts-and-Features/Orientation_images/Orientation_img1.png" Caption=""%}

_Figure 6: Horizontal Menu_

**Vertical Menu**

You can also render **Menu** control in vertical direction using orientation.****To set the vertical orientation of **Menu** control, replace the following script in the above sample code example.

* Add the following code in your **&lt;script&gt;** section.



{% highlight js %}

**[JavaScript]**
<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            orientation: ej.Orientation.Vertical
        });
    });
</script>


{% endhighlight %}



The following screen shot displays the output of the above code.                       

{% include image.html url="/js/Menu/Concepts-and-Features/Orientation_images/Orientation_img2.png" Caption=""%}

_Figure 7: Vertical Menu_

