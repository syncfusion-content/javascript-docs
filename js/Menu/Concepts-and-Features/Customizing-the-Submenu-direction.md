---
layout: post
title: Customizing-the-Submenu-direction
description: customizing the submenu direction
platform: js
control: Menu
documentation: ug
---

# Customizing the Submenu direction

You can customize the direction to open the sub menu items using **subMenuDirection** property. **subMenuDirection** accepts the type as string or enum and value as “Left” and “Right”. 

In the following example, the Sub menus opens in the Left side of the menu.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]    </b>&lt;div class="content-container-fluid"&gt;    &lt;div class="row"&gt;        &lt;div class="cols-sample-area"&gt;            &lt;ul id="coProducts"&gt;                &lt;li id="Products"&gt;                    <a href="#">Products</a>                    &lt;ul&gt;                        &lt;li&gt;<a>ASP.NET</a>&lt;/li&gt;                        &lt;li&gt;<a>ASP.NET MVC</a>&lt;/li&gt;                        &lt;ul&gt;                            &lt;li&gt;<a>WinRT (XMAL)&lt;/a&gt;&lt;/li&gt;                            &lt;li&gt;<a>Silverlight</a>&lt;/li&gt;                        &lt;/ul&gt;                &lt;/li&gt;            &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Support"&gt;                <a>Support</a>                &lt;ul&gt;                    &lt;li&gt;<a>Direct-Trac Support</a>&lt;/li&gt;                    &lt;li&gt;                        <a>Services</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Consulting</a>&lt;/li&gt;                            &lt;li&gt;<a>Training</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Purchase"&gt;<a>Purchase</a>&lt;/li&gt;            &lt;li id="Downloads"&gt;                <a>Downloads</a>                &lt;ul&gt;                    &lt;li&gt;<a>Evaluation</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Resources"&gt;                <a>Resources</a>                &lt;ul&gt;                    &lt;li&gt;                        <a>Technology Resource Portal &lt;/a&gt;                        &lt;ul&gt;                            &lt;li&gt;<a>White Papers</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>FAQ</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li id="Company"&gt;                <a>Company</a>                &lt;ul&gt;                    &lt;li&gt;                        <a>About Us</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Media Kit</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>Company Blog</a>&lt;/li&gt;                    &lt;li&gt;<a>Technical Blog</a>&lt;/li&gt;                    &lt;li&gt;<a>Newsletter</a>&lt;/li&gt;                    &lt;li&gt;                        <a>Partners</a>                        &lt;ul&gt;                            &lt;li&gt;<a>Technology Partners</a>&lt;/li&gt;                            &lt;li&gt;<a>Training Partners</a>&lt;/li&gt;                            &lt;li&gt;<a>Consulting Partners</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;                        <a>Locations</a>                        &lt;ul&gt;                            &lt;li&gt;<a>RDU</a>&lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>Contact Us</a>&lt;/li&gt;                    &lt;li&gt;<a>Careers</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;/ul&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#coProducts").ejMenu(        {            subMenuDirection: "left"        });    });&lt;/script&gt;</td></tr>
</table>


The output for the above code example is as follows.          

{% include image.html url="/js/Menu/Concepts-and-Features/Customizing-the-Submenu-direction_images/Customizing-the-Submenu-direction_img1.png" Caption=""%}

_Figure 15: Customizing Submenu Direction_

You can even achieve auto positioning for Context Menu. Use the following code sample for context menu in order to open the submenu items of context menu in left side.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]     </b> &lt;div&gt;    &lt;div id="target" class="textarea"&gt;        HTML is written in the form of HTML elements consisting of tags enclosed in angle        brackets (like        &lt;html&gt;        ),within the web page content. HTML tags most commonly come in pairs like and ,although        some tags, known as empty elements, are unpaired, for example        &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into        visible or audible web pages. The browser does not display the HTML tags, but uses        the tags to interpret the content of the page.    &lt;/div&gt;    &lt;ul id="contextMenu"&gt;        &lt;li&gt;            <a>Cut</a>            &lt;ul&gt;                &lt;li&gt;                    <a>Cut Particular</a>                &lt;/li&gt;                &lt;li&gt;<a>Cut Fully</a>&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;<a>Copy</a>&lt;/li&gt;        &lt;li&gt;<a>Paste</a>&lt;/li&gt;        &lt;li class="separator"&gt;&lt;/li&gt;        &lt;li&gt;<a>Comments</a>&lt;/li&gt;        &lt;li&gt;<a>Links</a>&lt;/li&gt;        &lt;li&gt;<a>Clear Formatting</a>&lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#contextMenu").ejMenu(             {                 menuType: ej.MenuType.ContextMenu,                 openOnClick: false,                 contextMenuTarget: "#target",                 <b>subMenuDirection: ej.Direction.Left</b>             });    });&lt;/script&gt;</td></tr>
</table>


* Add the following code in your style section.

{% highlight css %}

**[CSS]**

<style type="text/css">
    .textarea {
        border: 1px solid;
        padding: 10px;
        position: relative;
        text-align: justify;
        width: 463px;
        color: gray;
        margin: 0 auto;
    }
</style>


{% endhighlight %}


The output for the above code example is as follows.

{% include image.html url="/js/Menu/Concepts-and-Features/Customizing-the-Submenu-direction_images/Customizing-the-Submenu-direction_img2.png" Caption=""%}

_Figure 16: Customizing Submenu direction in Context Menu_

