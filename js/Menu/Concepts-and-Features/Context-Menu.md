---
layout: post
title: Context-Menu
description: context menu
platform: js
control: Menu
documentation: ug
---

# Context Menu

A context menu is a type of menu in a graphical user interface (GUI) that appears when you perform right click operation. In this **Menu** control you can use a context menu by specifying the type of menu as **ContextMenu**. A context also provides support for nested level of menu items.

Before you use the context menu, provide the target area for it. 

In the following example, a context menu for the division containing text is created. In this, when you perform right click operation, the following menu appears with open, edit, etc.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div&gt;        &lt;div id="target" class="textarea"&gt;            HTML is written in the form of HTML elements consisting of tags enclosed in angle            brackets (like            &lt;html&gt;            ),within the web page content. HTML tags most commonly come in pairs like and ,although            some tags, known as empty elements, are unpaired, for example            &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into            visible or audible web pages. The browser does not display the HTML tags, but uses            the tags to interpret the content of the page.        &lt;/div&gt;        &lt;ul id="contextMenu"&gt;            &lt;li&gt;<a>Open</a>&lt;/li&gt;            &lt;li&gt;<a>Edit</a>&lt;/li&gt;            &lt;li&gt;<a>Save</a>&lt;/li&gt;            &lt;li class="separator"&gt;&lt;/li&gt;            &lt;li&gt;<a>Save as</a>&lt;/li&gt;            &lt;li&gt;<a>Print</a>&lt;/li&gt;            &lt;li&gt;<a>Properties</a>&lt;/li&gt;        &lt;/ul&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]   </b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#contextMenu").ejMenu(            {                menuType: ej.MenuType.ContextMenu,                openOnClick: false,                contextMenuTarget: "#target"            });    });    &lt;/script&gt;</td></tr>
</table>


Add the following code in your style section.

**[CSS]**

&lt;style type="text/css"&gt;

    .textarea {

        border: 1px solid;

        padding: 10px;

        position: relative;

        text-align: justify;

        width: 463px;

        color: gray;

        margin: 0 auto;

    }

&lt;/style&gt;



The following screen shot displays the output of the above code.

{% include image.html url="/js/Menu/Concepts-and-Features/Context-Menu_images/Context-Menu_img1.png" Caption=""%}

_Figure 19: Context Menu_



You can hide and show the context menu using the following methods.

**HideContextMenu**

Hides the context menu control. Add the following script code in the sample in order to hide the context menu.


**[Javascript]**

&lt;script type="text/javascript"&gt;

    jQuery(function ($) {

        $("#contextMenu").ejMenu(

            {

                menuType: ej.MenuType.ContextMenu,

                openOnClick: false,

                contextMenuTarget: "#target"

            });

        //initialize the menu object

        var menuObj = $("#contextMenu ").data("ejMenu");



        //To hide the context menu

        menuObj.**hide** ();

    });

&lt;/script&gt;

**ShowContextMenu**

Shows the context menu control. Add the following script code in the sample in order to show the context menu.


**[Javascript]**

&lt;script type="text/javascript"&gt;

    jQuery(function ($) {

        $("#contextMenu").ejMenu(

            {

                menuType: ej.MenuType.ContextMenu,

                openOnClick: false,

                contextMenuTarget: "#target"

            });

        //initialize the menu object

        var menuObj = $("#contextMenu ").data("ejMenu");



        //To show the context menu

        menuObj.**show**();

    });

&lt;/script&gt;



