---
layout: post
title: Background-Template
description: background template
platform: js
control: Menu
documentation: ug
---

# Background Template

**Menu** control also provides support for template support. Normally **Menu** control can be created by using **UL** and **L** tags in the preferred way. But in template supporting, you can customize the appearance of sub menu items rendering. 

Initialize the Template **Menu** as illustrated in the following code example. 

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="content-container-fluid"&gt;    &lt;div class="row"&gt;        &lt;div class="cols-sample-area"&gt;            &lt;ul id="template"&gt;                &lt;li&gt;                    <a>My Computer</a>                    &lt;ul&gt;                        &lt;li&gt;                            &lt;div class="temp temp1"&gt;                                <span>Disks</span>                                &lt;ul&gt;                                    &lt;li&gt;<a>Local Disk : C</a>&lt;/li&gt;                                    &lt;li&gt;<a>Local Disk : D</a>&lt;/li&gt;                                &lt;/ul&gt;                                &lt;ul&gt;                                    &lt;li&gt;<a>Local Disk : E</a>&lt;/li&gt;                                    &lt;li&gt;<a>Local Disk : F</a>&lt;/li&gt;                                &lt;/ul&gt;                            &lt;/div&gt;                        &lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    <a>Libraries</a>                    &lt;ul&gt;                        &lt;li&gt;                            &lt;div class=" temp temp2"&gt;                                &lt;div&gt;                                    <span>Documents</span>                                    &lt;ul&gt;                                        &lt;li&gt;<a>Images</a>&lt;/li&gt;                                        &lt;li&gt;<a>Videos</a>&lt;/li&gt;                                    &lt;/ul&gt;                                    &lt;ul&gt;                                        &lt;li&gt;<a>Documents</a>&lt;/li&gt;                                        &lt;li&gt;<a>Music</a>&lt;/li&gt;                                    &lt;/ul&gt;                                &lt;/div&gt;                            &lt;/div&gt;                        &lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    <a>Favourites &lt;/a&gt;                    &lt;ul&gt;                        &lt;li&gt;                            &lt;div class="temp temp3"&gt;                                &lt;div&gt;                                    <span>Favourites</span>                                    &lt;ul&gt;                                        &lt;li&gt;<a>Downloads</a>&lt;/li&gt;                                        &lt;li&gt;<a>Recent Places</a>&lt;/li&gt;                                    &lt;/ul&gt;                                    &lt;ul&gt;                                        &lt;li&gt;<a>Desktop</a>&lt;/li&gt;                                    &lt;/ul&gt;                                &lt;/div&gt;                            &lt;/div&gt;                        &lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    <a>Gaming</a>                    &lt;ul&gt;                        &lt;li&gt;                            &lt;div class="temp temp4"&gt;                                &lt;div&gt;                                    <span>GAMING</span>                                    &lt;ul&gt;                                        &lt;li&gt;<a>Upcoming</a>&lt;/li&gt;                                        &lt;li&gt;<a>Consoles</a>&lt;/li&gt;                                    &lt;/ul&gt;                                    &lt;ul&gt;                                        &lt;li&gt;<a>FIFA 2999</a>&lt;/li&gt;                                        &lt;li&gt;<a>Carom legend</a>&lt;/li&gt;                                    &lt;/ul&gt;                                &lt;/div&gt;                            &lt;/div&gt;                        &lt;/li&gt;                    &lt;/ul&gt;                &lt;/li&gt;            &lt;/ul&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#template").ejMenu();    });&lt;/script&gt;</td></tr>
</table>


* Add the following code in your style section.

{% highlight css %}

**[CSS]**

<style type="text/css">
    .temp {
        height: 237px;
        width: 375px;
        font-family: segoe UI;
        cursor: default;
        background-size: 100% 100%;
    }

        .temp span {
            color: red;
            float: left;
            font-size: 20px;
            left: 20px;
            position: relative;
            top: 25px;
            width: 100px;
        }

        .temp ul {
            float: left;
            font-size: 14px;
            left: -79px;
            list-style-type: none;
            margin: 0;
            padding: 0;
            position: relative;
            top: 50px;
            width: 128px;
        }

            .temp ul li {
                font-size: 13px;
            }

                .temp ul li a {
                    text-decoration: underline;
                    cursor: pointer;
                    color: #000;
                }

    .temp1 {
        background-image: url("1.jpg");
    }

    .temp2 {
        background-image: url("2.jpg");
    }

    .temp3 {
        background-image: url("3.jpg");
    }

    .temp4 {
        background-image: url("4.jpg");
    }

    .e-menu.e-horizontal li > ul, .e-menu.e-horizontal li > ul > li:hover {
        background-color: #fff;
    }

    .e-menu.e-horizontal > li > ul:after {
        border-color: transparent transparent #fff;
    }
</style>


{% endhighlight %}



Execute the above code to render the following output.                       

{% include image.html url="/js/Menu/Concepts-and-Features/Background-Template_images/Background-Template_img1.png" Caption=""%}

_Figure 18: Template_

