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

* In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**

****

<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;        &lt;li class="expanded"&gt;            Favorites            &lt;ul&gt;                <li>Desktop</li>                <li>Downloads</li>                <li>Recent places</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li class="expanded"&gt;            Libraries            &lt;ul&gt;                &lt;li&gt;                    Documents                    &lt;ul&gt;                        <li>My Documents</li>                        <li>Public Documents</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Pictures                    &lt;ul&gt;                        <li>My Pictures</li>                        <li>Public Pictures</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Music                    &lt;ul&gt;                        <li>My Music</li>                        <li>Public Music</li>                    &lt;/ul&gt;                &lt;/li&gt;                <li>Subversion</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;            Computer            &lt;ul&gt;                <li>Folder(C)&lt;/li&gt;                <li>Folder(D)&lt;/li&gt;                <li>Folder(F)&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Set enablePersistence to “True” for TreeView control.</b>            $("#treeView").ejTreeView(                {                    <b>enablePersistence</b>: true                });</td></tr>
</table>


The output for **TreeView** when **enablePersistence** is set to **True** is as follows.

















{% include image.html url="/js/TreeView/Concepts-and-Features/Node-Persistence-Handling_images/Node-Persistence-Handling_img1.png" Caption="Figure 22: TreeView with enablePersistence"%}

