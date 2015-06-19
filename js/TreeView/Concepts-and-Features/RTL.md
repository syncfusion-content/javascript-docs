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

* In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**

****

<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;        &lt;li class="expanded"&gt;            Favorites            &lt;ul&gt;                <li>Desktop</li>                <li>Downloads</li>                <li>Recent places</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li class="expanded"&gt;            Libraries            &lt;ul&gt;                &lt;li&gt;                    Documents                    &lt;ul&gt;                        <li>My Documents</li>                        <li>Public Documents</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Pictures                    &lt;ul&gt;                        <li>My Pictures</li>                        <li>Public Pictures</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Music                    &lt;ul&gt;                        <li>My Music</li>                        <li>Public Music</li>                    &lt;/ul&gt;                &lt;/li&gt;                <li>Subversion</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;            Computer            &lt;ul&gt;                <li>Folder(C)&lt;/li&gt;                <li>Folder(D)&lt;/li&gt;                <li>Folder(F)&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;</td></tr>
<tr>
<td>
            <b>[JavaScript]</b><b>// Enable the property enableRTL for TreeView control as follows.</b>           $("#treeView").ejTreeView(			{			    <b>enableRTL</b>: true,			});</td></tr>
</table>


The output for **TreeView** when **enableRTL** is set to “**True**” is as follows.

{% include image.html url="/js/TreeView/Concepts-and-Features/RTL_images/RTL_img1.png" Caption="Figure 21: TreeView with enableRTL"%}

