---
layout: post
title: Ul-Li-Template
description: ul-li template
platform: js
control: TreeView
documentation: ug
---

# Ul-Li Template

The **TreeView** supports template technology, allowing you to completely customize the element’s appearance and layout. The nodes are provided with rich template support, so that the customizations are done in an easier manner. The look of the **TreeView** default elements are completely modified by creating a specific template, defining how an element is going to be rendered. You can customize the **TreeView** appearance, and give it a new look or style. 

In the following code example, you can delete the child node by clicking the **Delete** icon. This is achieved by the **removeNode** method in **TreeView** and you can change the position of the image where you want to place it.

The following steps explain configuring the template option for **TreeView**.

1. In the HTML page, add &lt;ul&gt; and &lt;li&gt; element to configure TreeView.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;    &lt;li class="expanded"&gt;        <a>Favorites</a>        &lt;ul&gt;            <li>Desktop<div class="cont-del">&lt;/div&gt;&lt;/li&gt;            <li>Downloads<div class="cont-del">&lt;/div&gt;&lt;/li&gt;            <li>Recent places<div class="cont-del">&lt;/div&gt;&lt;/li&gt;        &lt;/ul&gt;    &lt;/li&gt;    &lt;li class="expanded"&gt;        <a>Libraries</a>        &lt;ul&gt;            &lt;li&gt;                <a>Documents</a>                &lt;ul&gt;                    <li>My Documents<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                    <li>Public Documents<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li&gt;                <a>Pictures</a>                &lt;ul&gt;                    <li>My Pictures<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                    <li>Public Pictures<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li&gt;                <a>Music</a>                &lt;ul&gt;                    <li>My Music<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                    <li>Public Music<div class="cont-del">&lt;/div&gt;&lt;/li&gt;                &lt;/ul&gt;            &lt;/li&gt;            &lt;li&gt;<a>Subversion</a>&lt;/li&gt;        &lt;/ul&gt;    &lt;/li&gt;    &lt;li&gt;        <a>Computer</a>        &lt;ul&gt;            <li>Folder(C)&lt;div class="cont-del"&gt;&lt;/div&gt;&lt;/li&gt;            <li>Folder(D)&lt;div class="cont-del"&gt;&lt;/div&gt;&lt;/li&gt;            <li>Folder(F)&lt;div class="cont-del"&gt;&lt;/div&gt;&lt;/li&gt;        &lt;/ul&gt;    &lt;/li&gt;&lt;/ul&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable template for TreeView control in the script as follows.            $("#treeView").ejTreeView();            var treeObj = $("#treeView").data("ejTreeView");            $("#treeView").find(".cont-del").bind("click", function (e) {                treeObj.removeNode($(e.target).parents("li").first());            });        });</td></tr>
</table>


2. Adding the style for TreeView control as follows.

{% highlight css %}

**[CSS]**
<style class="cssStyles">
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

{% include image.html url="/js/TreeView/Concepts-and-Features/Ul-Li-Template_images/Ul-Li-Template_img1.png" Caption="TreeView with template"%}

