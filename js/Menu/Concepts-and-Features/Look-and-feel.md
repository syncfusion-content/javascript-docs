---
layout: post
title: Look-and-feel
description: look and feel
platform: js
control: Menu
documentation: ug
---

# Look and feel

**Essential JavaScript** controls feature 12 built-in themes, six flat and gradient effects, and also supports custom skin options for user-defined themes.

12 themes support available for **Menu** control namely,

default-theme

flat-azure-dark

flat-lime

flat-lime-dark

flat-saffron

flat-saffron-dark

gradient-azure

gradient-azure-dark

gradient-lime

gradient-lime-dark

gradient-saffron

gradient-saffron-dark

**Cssclass**

**Menu** control also customizes its appearance using user-defined **CSS** and custom skin options (colors and backgrounds). To apply custom themes you can use the “cssClass” property. “cssClass” property sets the root class for **Menu** control theme.

Using this **cssClass** you can override the existing styles under the theme style sheet. The theme stylesheet applies theme-specific styles like colors and backgrounds. In the following sample the value of “cssClass” property is set as “Purple-dark”. Purple-dark is added as root class to **Menu** control at the runtime. From this root class you can customize the **Menu** control theme.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div&gt;    &lt;div&gt;        &lt;ul id="menucontrol"&gt;            &lt;li id="home"&gt;                <a href="#">Home</a>                &lt;ul&gt;                    &lt;li&gt;<a>Foundation</a>&lt;/li&gt;                    &lt;li&gt;<a>Launch</a>&lt;/li&gt;                    &lt;li&gt;                        <a>About</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Location</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Services"&gt;                <a>Services</a>                &lt;ul&gt;                    &lt;li&gt;<a>Outsourcing</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="About"&gt;<a>About</a>&lt;/li&gt;            &lt;li id="Contact"&gt;                <a>Contact us</a>                &lt;ul&gt;                    &lt;li&gt;<a>E-mail</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Careers"&gt;                <a>Careers</a>                &lt;ul&gt;                    &lt;li&gt;                        <a>Position</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Developer</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>Apply online</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;        &lt;/ul&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#menucontrol").ejMenu({            width: 500,            cssClass: "Purple-dark"        });    });&lt;/script&gt;</td></tr>
</table>


* Add the following code in your style section.

{% highlight css %}

**[CSS]**

<style type="text/css" class="cssStyles">
    .Purple-dark {
        background: pink;
    }

    .Purple-dark.e-horizontal .e-list > a {
            color: #4800ff;
     }
</style>


{% endhighlight %}



Following screenshot displays the output of the above code.

{% include image.html url="/js/Menu/Concepts-and-Features/Look-and-feel_images/Look-and-feel_img1.png" Caption=""%}

_Figure 17: Look and feel of a Menu_

