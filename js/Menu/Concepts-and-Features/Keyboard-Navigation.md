---
layout: post
title: Keyboard-Navigation
description: keyboard navigation
platform: js
control: Menu
documentation: ug
---

# Keyboard Navigation

The **Menu** control also provides support for keyboard navigation. In the **Menu** control, it is possible to control the entire menu control items by using the provided shortcut keys. 

The various keyboard shortcuts available within the **Menu** control are discussed in the following table, 

_Table_ _2__: List of keyboard shortcut keys_

<table>
<tr>
<td>
<b>Keys</b></td><td>
<b>Usage</b></td></tr>
<tr>
<td>
Esc</td><td>
Closes the opened Menu control.</td></tr>
<tr>
<td>
Enter</td><td>
Selects the focused item.</td></tr>
<tr>
<td>
Up/left/down/right arrow keys</td><td>
Navigates up or previous item.</td></tr>
<tr>
<td>
Down</td><td>
Navigates down or next item.</td></tr>
<tr>
<td>
Left</td><td>
Navigates to previous group.</td></tr>
<tr>
<td>
Right</td><td>
Navigates to next group.</td></tr>
</table>


* Add the following code for Keyboard navigation in your **Menu** control.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div&gt;    &lt;div&gt;        &lt;ul id="menucontrol"&gt;            &lt;li id="home"&gt;                <a href="#">Home</a>                &lt;ul&gt;                    &lt;li&gt;<a>Foundation</a>&lt;/li&gt;                    &lt;li&gt;<a>Launch</a>&lt;/li&gt;                    &lt;li&gt;                        <a>About</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Company</a>&lt;/li&gt;                            &lt;li&gt;<a>Location</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Services"&gt;                <a>Services</a>                &lt;ul&gt;                    &lt;li&gt;<a>Consulting</a>&lt;/li&gt;                    &lt;li&gt;<a>Outsourcing</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="About"&gt;<a>About</a>&lt;/li&gt;            &lt;li id="Contact"&gt;                <a>Contact us</a>                &lt;ul&gt;                    &lt;li&gt;<a>Contact number</a>&lt;/li&gt;                    &lt;li&gt;<a>E-mail</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Careers"&gt;                <a>Careers</a>                &lt;ul&gt;                    &lt;li&gt;                        <a>Position</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Developer</a>&lt;/li&gt;                            &lt;li&gt;<a>Manager</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>Apply online</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;        &lt;/ul&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;        jQuery(function ($) {            $("#menucontrol").ejMenu();            //Control focus key            $(document).on("keydown", function (e) {                if (e.altKey && e.keyCode === 74) { // j- key code.                    $("#menucontrol").focus();                }            });        });&lt;/script&gt;</td></tr>
</table>


* Add the following code in your style section.

{% highlight css %}

**[CSS]**
<style type="text/css">
    #keyboard {
        margin-left: 50px;
    }
</style>


{% endhighlight %}

Following screenshot displays the output of the above code. 

{% include image.html url="/js/Menu/Concepts-and-Features/Keyboard-Navigation_images/Keyboard-Navigation_img1.png" Caption=""%}

_Figure 25: Accessibility_

When you press **alt+j,** the first item of the **Menu** control only gets focused as displayed in the following screenshot.

{% include image.html url="/js/Menu/Concepts-and-Features/Keyboard-Navigation_images/Keyboard-Navigation_img2.png" Caption=""%}

_Figure 26: Keyboard Navigation_

Similarly you can access the **Menu** control using keyboard itself.

