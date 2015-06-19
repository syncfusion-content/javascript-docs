---
layout: post
title: Center-Menu
description: center menu
platform: js
control: Menu
documentation: ug
---

# Center Menu

You can align the **Menu** items to center by setting “enableCenterAlign” property as true. “**enableCenterAlign**” property accepts Boolean value. By default, its value is **false**. When set to **true**, then the root menu items is aligned in center.

* Add the following code in your **&lt;script&gt;** section.

<table>
<tr>
<td>
<b>[HTML]    </b>&lt;div&gt;    &lt;ul id="menucontrol"&gt;        &lt;li id="home"&gt;            <a href="#">Home</a>            &lt;ul&gt;                &lt;li&gt;<a>Foundation</a>&lt;/li&gt;                &lt;li&gt;<a>Launch</a>&lt;/li&gt;                &lt;li&gt;                    <a>About</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Company</a>&lt;/li&gt;                        &lt;li&gt;<a>Location</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Services"&gt;            <a>Services</a>            &lt;ul&gt;                &lt;li&gt;<a>Consulting</a>&lt;/li&gt;                &lt;li&gt;<a>Outsourcing</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="About"&gt;<a>About</a>&lt;/li&gt;        &lt;li id="Contact"&gt;            <a>Contact us</a>            &lt;ul&gt;                &lt;li&gt;<a>Contact number</a>&lt;/li&gt;                &lt;li&gt;<a>E-mail</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Careers"&gt;            <a>Careers</a>            &lt;ul&gt;                &lt;li&gt;                    <a>Position</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Developer</a>&lt;/li&gt;                        &lt;li&gt;<a>Manager</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;<a>Apply online</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]   </b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#menucontrol").ejMenu(            {                width:500,                <b>enableCenterAlign: true</b>            });    });&lt;/script&gt;</td></tr>
</table>


The following screenshot displays the output of the above code.

{% include image.html url="/js/Menu/Concepts-and-Features/Center-Menu_images/Center-Menu_img1.png" Caption=""%}

_Figure 20: Center Menu_

