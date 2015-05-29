---
layout: post
title: context-menu
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
<b>[HTML]</b>    &lt;div&gt;        &lt;div id="target" class="textarea"&gt;            HTML is written in the form of HTML elements consisting of tags enclosed in angle            brackets (like            &lt;html&gt;            ),within the web page content. HTML tags most commonly come in pairs like and ,although            some tags, known as empty elements, are unpaired, for example            &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into            visible or audible web pages. The browser does not display the HTML tags, but uses            the tags to interpret the content of the page.        &lt;/div&gt;        &lt;ul id="contextMenu"&gt;            &lt;li&gt;<a>Open</a>&lt;/li&gt;            &lt;li&gt;<a>Edit</a>&lt;/li&gt;            &lt;li&gt;<a>Save</a>&lt;/li&gt;            &lt;li class="separator"&gt;&lt;/li&gt;            &lt;li&gt;<a>Save as</a>&lt;/li&gt;            &lt;li&gt;<a>Print</a>&lt;/li&gt;            &lt;li&gt;<a>Properties</a>&lt;/li&gt;        &lt;/ul&gt;    &lt;/div&gt;&lt;div&gt;    &lt;div id="menucontrol" class="textarea"&gt;        HTML is written in the form of HTML elements consisting of tags enclosed in angle        brackets (like        &lt;html&gt;        ),within the web page content. HTML tags most commonly come in pairs like and ,although        some tags, known as empty elements, are unpaired, for example        &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into        visible or audible web pages. The browser does not display the HTML tags, but uses        the tags to interpret the content of the page.    &lt;/div&gt;    &lt;ul id="contextMenu"&gt;        &lt;li&gt;<a>Open</a>&lt;/li&gt;        &lt;li&gt;<a>Edit</a>&lt;/li&gt;        &lt;li&gt;<a>Save</a>&lt;/li&gt;        &lt;li class="separator"&gt;&lt;/li&gt;        &lt;li&gt;<a>Save as</a>&lt;/li&gt;        &lt;li&gt;<a>Print</a>&lt;/li&gt;        &lt;li&gt;<a>Properties</a>&lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]   </b><b>// Add the following code in your &lt;script&gt; section.</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#contextMenu").ejMenu(            {                menuType: ej.MenuType.ContextMenu,                openOnClick: false,                contextMenuTarget: "#target"            });    });    &lt;/script&gt;&lt;script type="text/javascript"&gt;    jQuery(function ($) {        $("#menucontrol").ejMenu(            {                menuType: ej.MenuType.ContextMenu,                openOnClick: false,                <b>contextMenuTargetID: "target"</b>            });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code in your CSHTML page.**

&lt;div id="target" class="textarea"&gt;

    HTML is written in the form of HTML elements consisting of tags enclosed in angle

    brackets (like &lt;html&gt; ),within the web page content. HTML tags most commonly

    come in pairs like and ,although some tags, known as empty elements, are unpaired,

    for example &lt;img&gt;. The purpose of a web browser is to read HTML documents

    and compose them into visible or audible web pages. The browser does not display

    the HTML tags, but uses the tags to interpret the content of the page.

&lt;/div&gt;

@Html.EJ().Menu("docfile").Items(items =>

                   {

                       items.Add().Url("").Text("Open").Children(child =>

                       {

                           child.Add().Url("").Text("Open with notepad");

                           child.Add().Url("").Text("Open with notepad++");

                       });

                       items.Add().Url("").Text("Edit");

                       items.Add().Url("").Text("Save");

                       items.Add().Url("").Text("Save as");

                       items.Add().Url("").Text("Print");

                       items.Add().Url("").Text("Properties");

                   }).MenuType(MenuType.ContextMenu).OpenOnClick(true).**ContextMenuTarget("#target")**



[ASPX]

// Add the code in ASPX page

&lt;div id="target" class="textarea"&gt;

        HTML is written in the form of HTML elements consisting of tags enclosed in angle

        brackets (like

        &lt;html&gt;

        ),within the web page content. HTML tags most commonly come in pairs like and ,although

        some tags, known as empty elements, are unpaired, for example

        &lt;img&gt;. The purpose of a web browser is to read HTML documents and compose them into

        visible or audible web pages. The browser does not display the HTML tags, but uses

        the tags to interpret the content of the page.

    &lt;/div&gt;

    &lt;ej:Menu ID="Menu1" MenuType="ContextMenu" OpenOnClick="false" runat="server" ContextMenuTarget="#target"&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Open"&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Open with notepad"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

                &lt;Items&gt;

                    &lt;ej:MenuItem Text="Open with notepad++"&gt;&lt;/ej:MenuItem&gt;

                &lt;/Items&gt;

            &lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Edit"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Save"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Save as"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Print"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

        &lt;Items&gt;

            &lt;ej:MenuItem Text="Properties"&gt;&lt;/ej:MenuItem&gt;

        &lt;/Items&gt;

    &lt;/ej:Menu&gt;



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

![](context-menu_images\context-menu_img1.png)![](context-menu_images\context-menu_img2.png)

_Figure_ _33__19__: Context Menu_



You can hide and show the context menu using the following methods.

**HideContextMenu**

Hides the context mMenu control. Add the following script code in the sample in order to hide the context menu.


**[Javascript]**

&lt;script type="text/javascript"&gt;

    jQuery(function ($) {

        $("#contextMenu").ejMenu(

            {

                menuType: ej.MenuType.ContextMenu,

                openOnClick: false,

                contextMenuTarget: "#target"

            });

        $("#menucontrol").ejMenu({

            width: 500,



        });

        //initialize the menu object

        var menuObj = $("#contextMenu menucontrol").data("ejMenu");



        //To hide the context menu enable Menu item using item id

        menuObj.**hide ContextMenu**();

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

&lt;/script&gt;&lt;script type="text/javascript"&gt;

    jQuery(function ($) {

        $("#menucontrol").ejMenu({

            width: 500,



        });

        //initialize the menu object

        var menuObj = $("#menucontrol").data("ejMenu");



        //To enable Menu item using item id

        menuObj.**showContextMenu**();



    });

&lt;/script&gt;



