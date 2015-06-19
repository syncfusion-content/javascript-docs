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

> {% include image.html url="/js/Menu/Concepts-and-Features/Responsive-Layout_images/Responsive-Layout_img1.png" Caption=""%}_**Note: Refer to the ej.responsive.css file after the ej.widgets.all.min.css file**_

Add the above **css** link in the code sample.         

* Add the following code in your **HTML** page.

<table>
<tr>
<td>
<b>[HTML]   </b>&lt;div&gt;    &lt;ul id="menucontrol"&gt;        &lt;li id="home"&gt;            <a href="#">Home</a>            &lt;ul&gt;                &lt;li&gt;<a>Foundation</a>&lt;/li&gt;                &lt;li&gt;<a>Launch</a>&lt;/li&gt;                &lt;li&gt;                    <a>About</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Company</a>&lt;/li&gt;                        &lt;li&gt;<a>Location</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Services"&gt;            <a>Services</a>            &lt;ul&gt;                &lt;li&gt;<a>Consulting</a>&lt;/li&gt;                &lt;li&gt;<a>Outsourcing</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="About"&gt;<a>About</a>&lt;/li&gt;        &lt;li id="Contact"&gt;            <a>Contact us</a>            &lt;ul&gt;                &lt;li&gt;<a>Contact number</a>&lt;/li&gt;                &lt;li&gt;<a>E-mail</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Careers"&gt;            <a>Careers</a>            &lt;ul&gt;                &lt;li&gt;                    <a>Position</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Developer</a>&lt;/li&gt;                        &lt;li&gt;<a>Manager</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;<a>Apply online</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]</b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#menucontrol").ejMenu();    });&lt;/script&gt;</td></tr>
</table>


The following screenshot displays the output for the above code. 

{% include image.html url="/js/Menu/Concepts-and-Features/Responsive-Layout_images/Responsive-Layout_img2.png" Caption=""%}

_Figure 24: Menu with responsive layout_

