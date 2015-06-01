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

* Add the following **&lt;script&gt;** in the above code sample.

<table>
<tr>
<td>
<b>[HTML]    </b>&lt;div&gt;    &lt;ul id="menucontrol"&gt;        &lt;li id="home"&gt;            <a href="#">Home</a>            &lt;ul&gt;                &lt;li&gt;<a>Foundation</a>&lt;/li&gt;                &lt;li&gt;<a>Launch</a>&lt;/li&gt;                &lt;li&gt;                    <a>About</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Company</a>&lt;/li&gt;                        &lt;li&gt;<a>Location</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Services"&gt;            <a>Services</a>            &lt;ul&gt;                &lt;li&gt;<a>Consulting</a>&lt;/li&gt;                &lt;li&gt;<a>Outsourcing</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="About"&gt;<a>About</a>&lt;/li&gt;        &lt;li id="Contact"&gt;            <a>Contact us</a>            &lt;ul&gt;                &lt;li&gt;<a>Contact number</a>&lt;/li&gt;                &lt;li&gt;<a>E-mail</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li id="Careers"&gt;            <a>Careers</a>            &lt;ul&gt;                &lt;li&gt;                    <a>Position</a>                    &lt;ul&gt;                        &lt;li&gt;<a>Developer</a>&lt;/li&gt;                        &lt;li&gt;<a>Manager</a>&lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;<a>Apply online</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#menucontrol").ejMenu({            <b>enableSeparator: true</b>        });    });&lt;/script&gt;</td></tr>
</table>


The following screenshot displays the output for the above code sample.

{% include image.html url="/js/Menu/Concepts-and-Features/Separators_images/Separators_img1.png" Caption=""%}

_Figure 22: Menu with Separators_

* Add the following **&lt;script&gt;** in the above code sample to display the **Menu** control without separator by setting **enableSeparator** as **false**.



{% highlight js %}

**[Javascript]**
<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            width: 500,
**enableSeparator: false**
        });
    });
</script> 


{% endhighlight %}



The following screenshot displays the output for the above code. 

{% include image.html url="/js/Menu/Concepts-and-Features/Separators_images/Separators_img2.png" Caption=""%}

_Figure 23: Menu without Separators_

