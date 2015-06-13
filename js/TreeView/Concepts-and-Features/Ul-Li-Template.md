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

{% highlight html %}

<ul id="treeView">
    <li class="expanded">
        <a>Favorites</a>
        <ul>
            <li>Desktop<div class="cont-del"></div></li>
            <li>Downloads<div class="cont-del"></div></li>
            <li>Recent places<div class="cont-del"></div></li>
        </ul>
    </li>
    <li class="expanded">
        <a>Libraries</a>
        <ul>
            <li>
                <a>Documents</a>
                <ul>
                    <li>My Documents<div class="cont-del"></div></li>
                    <li>Public Documents<div class="cont-del"></div></li>
                </ul>
            </li>
            <li>
                <a>Pictures</a>
                <ul>
                    <li>My Pictures<div class="cont-del"></div></li>
                    <li>Public Pictures<div class="cont-del"></div></li>
                </ul>
            </li>
            <li>
                <a>Music</a>
                <ul>
                    <li>My Music<div class="cont-del"></div></li>
                    <li>Public Music<div class="cont-del"></div></li>
                </ul>
            </li>
            <li><a>Subversion</a></li>
        </ul>
    </li>
    <li>
        <a>Computer</a>
        <ul>
            <li>Folder(C)<div class="cont-del"></div></li>
            <li>Folder(D)<div class="cont-del"></div></li>
            <li>Folder(F)<div class="cont-del"></div></li>
        </ul>
    </li>
</ul>

{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
    $("#treeView").ejTreeView();
            var treeObj = $("#treeView").data("ejTreeView");
            $("#treeView").find(".cont-del").bind("click", function (e) {
                treeObj.removeNode($(e.target).parents("li").first());
            });
        });
</script>

{% endhighlight %}


2. Adding the style for TreeView control as follows.

{% highlight css %}

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

