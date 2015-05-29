---
layout: post
title: ul-li-template
description: ul-li template
platform: js
control: TreeView
documentation: ug
---

# Ul-Li Template

The **TreeView** supports template technology, allowing you to completely customize the element’s appearance and layout. The nodes are provided with rich template support, so that the customizations are done in an easier manner. The look of the **TreeView** default elements are completely modified by creating a specific template, defining how an element is going to be rendered. You can customize the **TreeView** appearance, and give it a new look or style. 

In the following code example, you can delete the child node by clicking the **Delete** icon. This is achieved by the **removeNode** method in **TreeView** and you can change the position of the image where you want to place it.

The following steps explain configuring the template option for **TreeView**.

1. In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** element to configure **TreeView.**



<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;    &lt;li class="expanded"&gt;        <a>Favorites</a>        &lt;ul&gt;            <li>Desktop<div class="cont-del">&lt;/div&gt;&lt;/li&gt;            <li>Downloads<div class="cont-del">&lt;/div&gt;&lt;/li&gt;            <li>Recent places<div class="cont-del">&lt;/div&gt;&lt;/li&gt;        &lt;/ul&gt;    &lt;/li&gt;    &lt;li class="expanded"&gt;        <a>Libraries</a>        &lt;ul&gt;            &lt;li&gt;                <a>Documents</a>                &lt;ul&gt;                    <li>My Documents<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                    <li>Public Documents<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li&gt;                <a>Pictures</a>                &lt;ul&gt;                    <li>My Pictures<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                    <li>Public Pictures<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li&gt;                <a>Music</a>                &lt;ul&gt;                    <li>My Music<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                    <li>Public Music<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li&gt;<a>Subversion</a>&lt;/li&gt;        &lt;/ul&gt;    &lt;/li&gt;    &lt;li&gt;        <a>Computer</a>        &lt;ul&gt;            <li>Folder(C)&lt;div class="cont-del"&gt;&lt;/div&gt;&lt;/li&gt;            <li>Folder(D)&lt;div class="cont-del"&gt;&lt;/div&gt;&lt;/li&gt;            <li>Folder(F)&lt;div class="cont-del"&gt;&lt;/div&gt;&lt;/li&gt;        &lt;/ul&gt;    &lt;/li&gt;&lt;/ul&gt;&lt;ul id="treeView"&gt;        &lt;ul&gt;            &lt;li&gt;            &lt;li class="expanded"&gt;                <a>Favorites</a>                &lt;ul&gt;                    &lt;div class="cont-details"&gt;                        <li>Desktop<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                        <li>Downloads<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                        <li>Recent places<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                    &lt;/div&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li class="expanded"&gt;                <a>Libraries</a>                &lt;ul&gt;                    &lt;li&gt;                        <a>Documents</a>                        &lt;ul&gt;                            &lt;div class="cont-details"&gt;                                <li>My Documents<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                                <li>Public Documents<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                            &lt;/div&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;                        <a>Pictures</a>                        &lt;ul&gt;                            &lt;div class="cont-details"&gt;                                <li>My Pictures<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                                <li>Public Pictures<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                            &lt;/div&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;                        <a>Music</a>                        &lt;ul&gt;                            &lt;div class="cont-details"&gt;                                <li>My Music<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                                <li>Public Music<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                            &lt;/div&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;<a>Subversion</a>&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li&gt;                <a>Computer</a>                &lt;ul&gt;                    &lt;div class="cont-details"&gt;                        <li>Folder(C)&lt;div class="cont-del"&gt;&lt;/div&gt;&lt;/li&gt;                        <li>Folder(D)&lt;div class="cont-del"&gt;&lt;/div&gt;&lt;/li&gt;                        <li>Folder(F)&lt;div class="cont-del"&gt;&lt;/div&gt;&lt;/li&gt;                    &lt;/div&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;/li&gt;        &lt;/ul&gt;    &lt;/ul&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Enable template for TreeView control in the script as follows.</b>            $("#treeView").ejTreeView();            var treeObj = $("#treeView").data("ejTreeView");            $("#treeView").find(".cont-del").bind("click", function (e) {                treeObj.removeNode($(e.target).parents("li").first());            });        });</td></tr>
<tr>
<td>
            <b>[JavaScript]</b><b>// Enable template for TreeView control in the script as follows.</b>            $("#treeView").ejTreeView();            var treeObj = $("#treeView").data("ejTreeView");            $("#treeView").find(".cont-del").bind("click", function (e) {                treeObj.removeNode($(e.target).parents("li").first());            });        });</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]</b><b>\\ To configure TreeView in the CSHTML page</b> @Html.EJ().TreeView("treeview").Items(items =>                {                    items.Add().Text("Favorites").Expanded(true).Children(child =>                    {                        child.Add().Text("Desktop").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                        child.Add().Text("Downloads").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                        child.Add().Text("Recent places").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                    });                    items.Add().Text("Libraries").Expanded(true).Children(child =>                   {                      child.Add().Text("Documents").Children(child1 =>                           {                                child1.Add().Text("My Documents").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                                child1.Add().Text("Public Documents").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                            });                       child.Add().Text("Pictures").Children(child1 =>                        {                            child1.Add().Text("My Pictures").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                            child1.Add().Text("Public Pictures").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                        });                        child.Add().Text("Music").Children(child1 =>                        {                            child1.Add().Text("My Music").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                            child1.Add().Text("Public Music").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                        });                        child.Add().Text("Subversion");                    });                    items.Add().Text("Computer").Children(child =>                    {                        child.Add().Text("Folder(C)").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                        child.Add().Text("Folder(D)").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                        child.Add().Text("Folder(E)").ContentTemplate(@&lt;div class="cont-del"&gt;&lt;/div&gt;);                    });                })</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script&gt;    $(function () {       $("#treeview").ejTreeView();       var treeObj = $("#treeview").data("ejTreeView");       $("#treeview").find(".cont-del").bind("click", function (e) {                treeObj.removeNode($(e.target).parents("li").first());       });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b><b>\\Configure TreeView in the aspx page.</b>&lt;ej:TreeView ID="treeview" runat="server"&gt;        &lt;Nodes&gt;            &lt;ej:TreeViewNode Expanded="True" Text="Favorites"&gt;                &lt;Nodes&gt;                    &lt;ej:TreeViewNode Text="Desktop"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Downloads"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Recent places"&gt;&lt;/ej:TreeViewNode&gt;                &lt;/Nodes&gt;            &lt;/ej:TreeViewNode&gt;            &lt;ej:TreeViewNode Expanded="True" Text="Libraries"&gt;                &lt;Nodes&gt;                    &lt;ej:TreeViewNode Text="Documents"&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="My Documents"&gt;&lt;/ej:TreeViewNode&gt;                            &lt;ej:TreeViewNode Text="Public Documents"&gt;&lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                    &lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Pictures"&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="My Pictures"&gt;&lt;/ej:TreeViewNode&gt;                            &lt;ej:TreeViewNode Text="Public Pictures"&gt;&lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                    &lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Music"&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="My Music"&gt;&lt;/ej:TreeViewNode&gt;                            &lt;ej:TreeViewNode Text="Public Music"&gt;&lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                    &lt;/ej:TreeViewNode&gt;                &lt;/Nodes&gt;            &lt;/ej:TreeViewNode&gt;            &lt;ej:TreeViewNode Text="Computer"&gt;                &lt;Nodes&gt;                    &lt;ej:TreeViewNode Text="Folder(C)"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Folder(D)"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Folder(E)"&gt;&lt;/ej:TreeViewNode&gt;                &lt;/Nodes&gt;            &lt;/ej:TreeViewNode&gt;        &lt;/Nodes&gt;<b>    &lt;/ej:TreeView&gt;</b></td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>\\</b> Enable Template for TreeView control in script.&lt;script&gt;    $(function () {       $("#treeview").ejTreeView();       var treeObj = $("#treeview").data("ejTreeView");       $("#treeview").find(".cont-del").bind("click", function (e) {                treeObj.removeNode($(e.target).parents("li").first());       });    });<b>&lt;/script&gt;</b></td></tr>
</table>


2. Adding the style for **TreeView** control as follows.

****

{% highlight css %}

**[CSS]**
<style class="cssStyles">
        .cont-details {
            margin-top: 10px;
            margin-left: 10px;
            font-size: 13px;
            font-family: Georgia;
            color: black;
            width: 100px;
            text-align: left;
        }

        .cont-del {
            background: url("../images/treeview/remove-icon.png") no-repeat 50% 50%;
            width: 12px;
            height: 12px;
            display: inline-block;
            cursor: pointer;
        }
    </style>



{% endhighlight %}



The **TreeView** control template displays the following output.



{% include image.html url="\js\TreeView\concepts-and-features\ul-li-template_images\ul-li-template_img1.png" Caption="Figure 520: TreeView with template"%}{% include image.html url="\js\TreeView\concepts-and-features\ul-li-template_images\ul-li-template_img2.png" Caption="Figure 520: TreeView with template"%}

