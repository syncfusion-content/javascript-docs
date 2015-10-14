---
layout: post
title: Hierarchical-data-with-Editing-cut-copy-paste
description: hierarchical data with editing-cut-copy-paste
platform: js
control: TreeView
documentation: ug
---

# Data with Editing-cut-copy-paste

The **TreeView** control permits you to edit a node and also allows you to cut and paste the node in the **TreeView**. You can edit the tree node name when it is required. This is achieved by using the **allowEditing** property. By setting the property to **“true”**, you can select a node and press F2 or double-click the node to initiate editing.

The following steps explain how to enable the **allowEditing** property for **TreeView**.

In the HTML page, add &lt;ul&gt; and &lt;li&gt; elements to configure TreeView.

{% highlight html %}

    
<ul id="treeView">
   <li class="expanded">
      Favorites
      <ul>
         <li>Desktop</li>
         <li>Downloads</li>
         <li>Recent places</li>
      </ul>
   </li>
   <li class="expanded">
      Libraries
      <ul>
         <li>
            Documents
            <ul>
               <li>My Documents</li>
               <li>Public Documents</li>
            </ul>
         </li>
         <li>
            Pictures
            <ul>
               <li>My Pictures</li>
               <li>Public Pictures</li>
            </ul>
         </li>
         <li>
            Music
            <ul>
               <li>My Music</li>
               <li>Public Music</li>
            </ul>
         </li>
         <li>Subversion</li>
      </ul>
   </li>
   <li>
      Computer
      <ul>
         <li>Folder(C)</li>
         <li>Folder(D)</li>
         <li>Folder(F)</li>
      </ul>
   </li>
</ul>
    
{% endhighlight %}

{% highlight js %}


        // Enable allowEditing for TreeView control as follows.
        $("#treeView").ejTreeView({
            allowEditing: true
        });


{% endhighlight %}


The following screenshot displays the appearance of Editing-cut-paste the node in the TreeView component.

![]("/js/TreeView/Data-with-Editing-cut-copy-paste_images/Data-with-Editing-cut-copy-paste_img1.png")

