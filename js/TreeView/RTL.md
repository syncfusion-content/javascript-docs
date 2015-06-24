---
layout: post
title: RTL
description: rtl
platform: js
control: TreeView
documentation: ug
---

# RTL

**TreeView** supports right-to-left layout and the node text is displayed in the **RTL** languages. Arabic and Hebrew are languages written from right to left. When you desire to change the display of **TreeView** as right to left direction, you can do so by using the **enableRTL** property. To enable or disable this option, set the appropriate value for the **enableRTL** property. When **enableRTL** is enabled, the appearance of the **TreeView** is displayed in the right to left direction. You can display the **TreeView** as right to left direction by using this feature.

The following steps explain enabling the **enableRTL** property for **TreeView**.

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
	    enableRTL: true,
	});

{% endhighlight %}


The output for **TreeView** when **enableRTL** is set to “**True**” is as follows.

{% include image.html url="/js/TreeView/RTL_images/RTL_img1.png"%}

