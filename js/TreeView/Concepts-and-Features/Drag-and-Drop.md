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

1. In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**

****

<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;        &lt;li class="expanded"&gt;            Favorites            &lt;ul&gt;                <li>Desktop</li>                <li>Downloads</li>                <li>Recent places</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li class="expanded"&gt;            Libraries            &lt;ul&gt;                &lt;li&gt;                    Documents                    &lt;ul&gt;                        <li>My Documents</li>                        <li>Public Documents</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Pictures                    &lt;ul&gt;                        <li>My Pictures</li>                        <li>Public Pictures</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Music                    &lt;ul&gt;                        <li>My Music</li>                        <li>Public Music</li>                    &lt;/ul&gt;                &lt;/li&gt;                <li>Subversion</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;            Computer            &lt;ul&gt;                <li>Folder(C)&lt;/li&gt;                <li>Folder(D)&lt;/li&gt;                <li>Folder(F)&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;</td></tr>
<tr>
<td>
          <b>[JavaScript]</b><b>// Enable allowDragAndDrop for TreeView control as follows.</b>            $("#treeView").ejTreeView(              {              <b>allowDragAndDrop</b>: true,               });</td></tr>
</table>


The output for **TreeView** when **allowDragAndDrop** is set to **True**.



























{% include image.html url="/js/TreeView/Concepts-and-Features/Drag-and-Drop_images/Drag-and-Drop_img1.png" Caption="Figure 15: Drag And Drop TreeView"%}

## Allow Drop Child

You can allow the child level of specified node to be dropped in **TreeView** by using the **allowDropChild** property, and it is specified in the script as follows.



{% highlight js %}

**[JavaScript]**
    $("#treeView").ejTreeView({ **allowDropChild**: true });



{% endhighlight %}

### Allow Drop Sibling

You can drag the root node and drop it into the same level of node that is a sibling node in **TreeView** by using the property **allowDropSibling**. You can specify the property **allowDropSibling** in **TreeView** control as follows.



{% highlight js %}

**[JavaScript]**
    $("#treeView").ejTreeView({ **allowDropSibling**: true });



{% endhighlight %}



