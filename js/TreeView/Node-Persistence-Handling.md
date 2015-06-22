---
layout: post
title: Node-Persistence-Handling
description: node persistence handling
platform: js
control: TreeView
documentation: ug
---

# Node Persistence Handling

The **TreeView** allows for **Persistence** of its expanded and collapsed state across page view. When you want to maintain the state of the node, like expand or collapse the node, check or uncheck the node, or node display arrangement after a post back, this behavior is achieved by using the **enablePersistence** property.

To enable **Persistence** of a node, you can set the appropriate value for the **enablePersistence** property. To enable this feature, set the **enablePersistence** property as **true**.

The following steps explain how you can enable the **enablePersistence** property for **TreeView**.

In the **HTML** page, add &lt;ul&gt; and &lt;li&gt; elements to configure TreeView.

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


        $("#treeView").ejTreeView({                
            enablePersistence: true
        });


{% endhighlight %}


The output for **TreeView** when **enablePersistence** is set to **True** is as follows.

{% include image.html url="/js/TreeView/Node-Persistence-Handling_images/Node-Persistence-Handling_img1.png" Caption="TreeView with enablePersistence"%}

