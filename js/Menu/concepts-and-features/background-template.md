---
layout: post
title: background-template
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


**[CSHTML]**

**// Add the following code in your CSHTML page.**

@Html.EJ().Menu("template").Items(items =>

    {

        items.Add().Text("Books").Children(child =>

        {

            child.Add().ContentTemplate(@&lt;div class="temp temp1"&gt;

                <span>BOOKS</span>

                &lt;ul&gt;

                    &lt;li&gt;<a>New Releases</a>&lt;/li&gt;

                    &lt;li&gt;<a>Bestsellers</a>&lt;/li&gt;

                    &lt;li&gt;<a>Upcoming</a>&lt;/li&gt;

                    &lt;li&gt;<a>Box Sets</a>&lt;/li&gt;

                &lt;/ul&gt;

                &lt;ul&gt;

                    &lt;li&gt;<a>HTML Basics</a>&lt;/li&gt;

                    &lt;li&gt;<a>JavaScript</a>&lt;/li&gt;

                    &lt;li&gt;<a>JQuery</a>&lt;/li&gt;

                    &lt;li&gt;<a>PHP Basics</a>&lt;/li&gt;

                &lt;/ul&gt;

            &lt;/div&gt;);

        });

        items.Add().Text("Cameras").Children(child =>

        {

            child.Add().ContentTemplate(@&lt;div class="temp temp2"&gt;

                <span>CAMERAS</span>

                &lt;ul&gt;

                    &lt;li&gt;<a>Point & Shoots</a>&lt;/li&gt;

                    &lt;li&gt;<a>Digital SLR</a>&lt;/li&gt;

                    &lt;li&gt;<a>Camcorders</a>&lt;/li&gt;

                    &lt;li&gt;<a>Bestsellers</a>&lt;/li&gt;

                &lt;/ul&gt;

                &lt;ul&gt;

                    &lt;li&gt;<a>Still Camera</a>&lt;/li&gt;

                    &lt;li&gt;<a>Digital Camera</a>&lt;/li&gt;

                    &lt;li&gt;<a>Video Camera</a>&lt;/li&gt;

                    &lt;li&gt;<a>Virtual Camera</a>&lt;/li&gt;

                &lt;/ul&gt;

            &lt;/div&gt;);

        });

        items.Add().Text("Movies").Children(child =>

        {

            child.Add().ContentTemplate(@&lt;div class="temp temp3"&gt;

                <span>MOVIES</span>

                &lt;ul&gt;

                    &lt;li&gt;<a>Genobili Actions</a>&lt;/li&gt;

                    &lt;li&gt;<a>Jackie Rocks</a>&lt;/li&gt;

                    &lt;li&gt;<a>Men In Blue</a>&lt;/li&gt;

                    &lt;li&gt;<a>Human vs Alien</a>&lt;/li&gt;

                &lt;/ul&gt;

                &lt;ul&gt;

                    &lt;li&gt;<a>Million Dreams</a>&lt;/li&gt;

                    &lt;li&gt;<a>Kung-fu</a>&lt;/li&gt;

                &lt;/ul&gt;

            &lt;/div&gt;);

        });

        items.Add().Text("Musics").Children(child =>

        {

            child.Add().ContentTemplate(@&lt;div class="temp temp4"&gt;

                <span>MUSICS</span>

                &lt;ul&gt;

                    &lt;li&gt;<a>New Releases</a>&lt;/li&gt;

                    &lt;li&gt;<a>Bestsellers</a>&lt;/li&gt;

                    &lt;li&gt;<a>Devotional</a>&lt;/li&gt;

                    &lt;li&gt;<a>Sufi & Ghazal</a>&lt;/li&gt;

                &lt;/ul&gt;

                &lt;ul&gt;

                    &lt;li&gt;<a>Pop songs</a>&lt;/li&gt;

                    &lt;li&gt;<a>Rock Music</a>&lt;/li&gt;

                &lt;/ul&gt;

            &lt;/div&gt;);

        });

        items.Add().Text("Gaming").Children(child =>

        {

            child.Add().ContentTemplate(@&lt;div class="temp temp5"&gt;

                <span>GAMING</span>

                &lt;ul&gt;

                    &lt;li&gt;<a>Upcoming</a>&lt;/li&gt;

                    &lt;li&gt;<a>PC</a>&lt;/li&gt;

                    &lt;li&gt;<a>PS Vista</a>&lt;/li&gt;

                    &lt;li&gt;<a>PS3</a>&lt;/li&gt;

                    &lt;li&gt;<a>XBox</a>&lt;/li&gt;

                    &lt;li&gt;<a>Consoles</a>&lt;/li&gt;

                &lt;/ul&gt;

                &lt;ul&gt;

                    &lt;li&gt;<a>FIFA 2999</a>&lt;/li&gt;

                    &lt;li&gt;<a>NBA Actions</a>&lt;/li&gt;

                    &lt;li&gt;<a>Crick Champions</a>&lt;/li&gt;

                    &lt;li&gt;<a>Carom legend</a>&lt;/li&gt;

                &lt;/ul&gt;

            &lt;/div&gt;);

        });

    })



**[ASPX]**

// Add the code in ASPX page



&lt;ej:Menu ID="template" runat="server"&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="My Computer"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Child1"&gt;

                        &lt;Template&gt;

                            &lt;div class="temp temp1"&gt;

                                <span>Disks</span>

                                &lt;ul&gt;

                                    &lt;li&gt;<a>Local Disk : C</a>&lt;/li&gt;

                                    &lt;li&gt;<a>Local Disk : D</a>&lt;/li&gt;

                                &lt;/ul&gt;

                                &lt;ul&gt;

                                    &lt;li&gt;<a>Local Disk : E</a>&lt;/li&gt;

                                    &lt;li&gt;<a>Local Disk : F</a>&lt;/li&gt;

                                &lt;/ul&gt;

                            &lt;/div&gt;

                        &lt;/Template&gt;

                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

            &lt;ej:MenuItem Text="Libraries"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Child1"&gt;

                        &lt;Template&gt;



                            &lt;div class=" temp temp2"&gt;

                                &lt;div&gt;

                                    <span>Documents</span>

                                    &lt;ul&gt;

                                        &lt;li&gt;<a>Images</a>&lt;/li&gt;

                                        &lt;li&gt;<a>Videos</a>&lt;/li&gt;

                                    &lt;/ul&gt;

                                    &lt;ul&gt;

                                        &lt;li&gt;<a>Documents</a>&lt;/li&gt;

                                        &lt;li&gt;<a>Music</a>&lt;/li&gt;

                                    &lt;/ul&gt;

                                &lt;/div&gt;

                            &lt;/div&gt;



                        &lt;/Template&gt;

                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

            &lt;ej:MenuItem Text="Favourites"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Child1"&gt;

                        &lt;Template&gt;



                            &lt;div class="temp temp3"&gt;

                                &lt;div&gt;

                                    <span>Favourites</span>

                                    &lt;ul&gt;

                                        &lt;li&gt;<a>Download</a>&lt;/li&gt;

                                        &lt;li&gt;<a>Recent Places</a>&lt;/li&gt;

                                    &lt;/ul&gt;

                                    &lt;ul&gt;

                                        &lt;li&gt;<a>Desktop</a>&lt;/li&gt;

                                    &lt;/ul&gt;

                                &lt;/div&gt;

                            &lt;/div&gt;



                        &lt;/Template&gt;

                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

            &lt;ej:MenuItem Text="Gaming"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Child1"&gt;

                        &lt;Template&gt;



                            &lt;div class=" temp temp2"&gt;

                                &lt;div&gt;

                                    <span>GAMING</span>

                                    &lt;ul&gt;

                                        &lt;li&gt;<a>Upcoming</a>&lt;/li&gt;

                                        &lt;li&gt;<a>Consoles</a>&lt;/li&gt;

                                    &lt;/ul&gt;

                                    &lt;ul&gt;

                                        &lt;li&gt;<a>FIFA 2999</a>&lt;/li&gt;

                                        &lt;li&gt;<a>Carom legend</a>&lt;/li&gt;

                                    &lt;/ul&gt;

                                &lt;/div&gt;

                            &lt;/div&gt;



                        &lt;/Template&gt;

                    &lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Menu&gt;



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

![](background-template_images\background-template_img1.png)

_Figure_ _32__18__: Template_

