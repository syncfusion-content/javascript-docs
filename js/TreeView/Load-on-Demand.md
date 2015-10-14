---
layout: post
title: Load-on-Demand
description: load on demand
platform: js
control: TreeView
documentation: ug
---

# Load on Demand

**Load on Demand** option is useful when the full content of the **TreeView** is too large to be loaded completely, up front. The mechanism lets the nodes load their child nodes as you expand the parent by clicking the **expand icon**. While clicking on the parent node it first loads their particular child nodes and then loads the first level of nodes.

This feature is used reduce the loading time of the large number nodes in **TreeView**. For example, when you are using the **TreeView** with 10,000 nodes or greater, it takes a long time to load their child nodes. In this case, **Load on Demand** is used to load the particular part of child nodes when you click their parent node. Hence it reduces the loading time of **TreeView.**

To enable **load on demand**, set the appropriate value for the **loadOnDemand** property.

The following steps explain how to enable the **loadOnDemand** property for **TreeView**.

In the **HTML** page, add a &lt;div&gt; element to configure TreeView.

{% highlight html %}

<div id="treeView"></div>

{% endhighlight %}

{% highlight js %}

    var localData = [
                   { id: 1, name: "Favorites", hasChild: true },
                   { id: 2, pid: 1, name: "Desktop" },
                   { id: 3, pid: 1, name: "Downloads" },
                   { id: 4, pid: 1, name: "Recent places" },
                   { id: 5, name: "libraries", hasChild: true },
                   { id: 6, pid: 5, name: "Documents", hasChild: true },
                   { id: 7, pid: 6, name: "My Documents" },
                   { id: 8, pid: 6, name: "Public Documents" },
                   { id: 9, pid: 5, name: "Pictures", hasChild: true },
                   { id: 10, pid: 9, name: "My Pictures" },
                   { id: 11, pid: 9, name: "Public Pictures" },
                   { id: 12, pid: 5, name: "Music", hasChild: true },
                   { id: 13, pid: 9, name: "My Music" },
                   { id: 14, pid: 9, name: "Public Music" },
                   { id: 15, pid: 5, name: "Subversion" },
                   { id: 16, name: "Computer", hasChild: true },
                   { id: 17, pid: 16, name: "Folder(C)" },
                   { id: 18, pid: 16, name: "Folder(D)" },
                   { id: 19, pid: 16, name: "Folder(F)" },
        ];
        $("#treeView").ejTreeView({
            loadOnDemand: true,
            fields: { dataSource: localData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" }
        });

{% endhighlight %}

The output for TreeView when loadOnDemand is set to “True” is as follows.

![]("/js/TreeView/Load-on-Demand_images/Load-on-Demand_img1.png")

