---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: Menu
documentation: ug
---

# RTL Support

The **enableRTL** option allows the **Menu** control to display it in the right to left direction. By default, this option is set to “false” in the **Menu** control.

* The following code depicts you on how to enable the **rtl** property of the **Menu** control.

<table>
<tr>
<td>
<b>[HTML]    </b>&lt;div&gt;    &lt;ul id="menucontrol"&gt;        &lt;li id="home"&gt;            <a href="#">Home</a>            &lt;ul&gt;                &lt;li&gt;<a>Foundation</a>&lt;/li&gt;                &lt;li&gt;<a>Launch</a>&lt;/li&gt;                &lt;li&gt;                    <a>About</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Company</a>&lt;/li&gt;                        &lt;li&gt;<a>Location</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Services"&gt;            <a>Services</a>            &lt;ul&gt;                &lt;li&gt;<a>Consulting</a>&lt;/li&gt;                &lt;li&gt;<a>Outsourcing</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="About"&gt;<a>About</a>&lt;/li&gt;        &lt;li id="Contact"&gt;            <a>Contact us</a>            &lt;ul&gt;                &lt;li&gt;<a>Contact number</a>&lt;/li&gt;                &lt;li&gt;<a>E-mail</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Careers"&gt;            <a>Careers</a>            &lt;ul&gt;                &lt;li&gt;                    <a>Position</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Developer</a>&lt;/li&gt;                        &lt;li&gt;<a>Manager</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;<a>Apply online</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#menucontrol").ejMenu({ <b>enableRTL: true</b> });    });&lt;/script&gt;</td></tr>
</table>


Following screenshot displays the output for the above code.

{% include image.html url="/js/Menu/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption=""%}

_Figure 21: RTL Support_

