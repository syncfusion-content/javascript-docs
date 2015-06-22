---
layout: post
title: Drag-and-Drop
description: drag and drop
platform: js
control: TreeView
documentation: ug
---

# Drag and Drop

You can **Drag and Drop** the nodes within the **TreeView** control or drag a particular node from one tree to another tree.

To enable or disable this option, set the appropriate value for the **allowDragAndDrop** property. When **allowDragAndDrop** is enabled, the nodes of a **TreeView** are dragged and dropped between all levels. 

The following steps explain enabling the **allowDragAndDrop** property for **TreeView**.

In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**

{% highlight html %}


    <ul id="treeView">
        <li class="expanded">Favorites
                <ul>

                    <li>Desktop</li>
                    <li>Downloads</li>
                    <li>Recent places</li>
                </ul>
        </li>
        <li class="expanded">Libraries
                <ul>
                    <li>Documents
                        <ul>
                            <li>My Documents</li>
                            <li>Public Documents</li>
                        </ul>
                    </li>
                    <li>Pictures
                        <ul>
                            <li>My Pictures</li>
                            <li>Public Pictures</li>
                        </ul>
                    </li>
                    <li>Music
                        <ul>
                            <li>My Music</li>
                            <li>Public Music</li>
                        </ul>
                    </li>
                    <li>Subversion</li>
                </ul>
        </li>
        <li>Computer
                <ul>
                    <li>Folder(C)</li>
                    <li>Folder(D)</li>
                    <li>Folder(F)</li>
                </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight js %}


        // Enable allowDragAndDrop for TreeView control as follows.

        $("#treeView").ejTreeView({              
              allowDragAndDrop: true,              
        });


{% endhighlight %}

The output for **TreeView** when **allowDragAndDrop** is set to **True**.

{% include image.html url="/js/TreeView/Concepts-and-Features/Drag-and-Drop_images/Drag-and-Drop_img1.png" Caption="Drag And Drop TreeView"%}

## Allow Drop Child

You can allow the child level of specified node to be dropped in **TreeView** by using the **allowDropChild** property, and it is specified in the script as follows.

{% highlight js %}

    $("#treeView").ejTreeView({ allowDropChild: true });


{% endhighlight %}

### Allow Drop Sibling

You can drag the root node and drop it into the same level of node that is a sibling node in **TreeView** by using the property **allowDropSibling**. You can specify the property **allowDropSibling** in **TreeView** control as follows.

{% highlight js %}

    $("#treeView").ejTreeView({ allowDropSibling: true });


{% endhighlight %}



