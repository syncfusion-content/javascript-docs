---
layout: post
title: Multiple-Selection
description: multiple selection
platform: js
control: TreeView
documentation: ug
api: /api/js/ejtreeview
---


# Multiple Selection

TreeView supports to select the multiple nodes by specifying [allowMultiSelection](https://help.syncfusion.com/api/js/ejtreeview#members:allowmultiselection) as true. It allows you to select more than one nodes in TreeView.

{% highlight html %}

	<!--create the TreeView wrapper-->
	
	<div id="treeMultiSelect"></div>

{% endhighlight %}

{% highlight js %}

	var localData = [

		{ id: 1, text: "Item 1" },
	
		{ id: 2, text: "Item 2" },
	
		{ id: 3, text: "Item 3" },
	
		{ id: 4, text: "Item 4" },
	
		{ id: 5, parent: 1, text: "Item 1.1" },
	
		{ id: 6, parent: 1, text: "Item 1.2" },
	
		{ id: 7, parent: 1, text: "Item 1.3" },
	
		{ id: 8, parent: 3, text: "Item 3.1" },
	
		{ id: 9, parent: 3, text: "Item 3.2" },
	
		{ id: 10, parent: 5, text: "Item 1.1.1" }
	
	];
	
	$(function () {
	
		// initialize and bind the TreeView with local data
	
		$("#treeMultiSelect").ejTreeView({
	
			allowMultiSelection: true, //enable multiple selection in TreeView
	
			fields: { dataSource: localData, id: "id", parentId: "parent", text: "text" }
	
		});
	
	});

	
{% endhighlight %}

For more details about multiple selection in TreeView, refer the sample [here](http://jsplayground.syncfusion.com/Sync_wuoxgu3q).

## Select Nodes

To select more than one nodes of TreeView, you can use [selectedNodes](https://help.syncfusion.com/api/js/ejtreeview#members:selectednodes) property. It will select the TreeView nodes from the given indexes.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeMultiSelect"></div>

{% endhighlight %}

{% highlight js %}

	var localData = [

		{ id: 1, text: "Item 1" },
	
		{ id: 2, text: "Item 2" },
	
		{ id: 3, text: "Item 3" },
	
		{ id: 4, text: "Item 4" },
	
		{ id: 5, parent: 1, text: "Item 1.1" },
	
		{ id: 6, parent: 1, text: "Item 1.2" },
	
		{ id: 7, parent: 1, text: "Item 1.3" },
	
		{ id: 8, parent: 3, text: "Item 3.1" },
	
		{ id: 9, parent: 3, text: "Item 3.2" },
	
		{ id: 10, parent: 5, text: "Item 1.1.1" }
	
	];
	
	$(function () {
	
		// initialize and bind the TreeView with local data
	
		$("#treeMultiSelect").ejTreeView({
	
			allowMultiSelection: true, //enable multiple selection in TreeView
	
			fields: { dataSource: localData, id: "id", parentId: "parent", text: "text" }
	
		});
		
		// create instance for TreeView
		var treeObj = $("#treeMultiSelect").data("ejTreeView");
	
		treeObj.option("selectedNodes", [0, 5, 6]); //select the TreeView nodes from the given indexes
	
	});
	
{% endhighlight %}

## Get Selected Nodes

To get the selected Nodes of TreeView, you can use [getSelectedNodes](https://help.syncfusion.com/api/js/ejtreeview#methods:getselectednodes) method. It returns the collections of TreeView selected nodes.
You can use [getSelectedNodesIndex](https://help.syncfusion.com/api/js/ejtreeview#methods:getselectednodesindex) method to get the index positions of currently selected nodes.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeMultiSelect"></div>

{% endhighlight %}

{% highlight js %}

	var localData = [

		{ id: 1, text: "Item 1" },
	
		{ id: 2, text: "Item 2" },
	
		{ id: 3, text: "Item 3" },
	
		{ id: 4, text: "Item 4" },
	
		{ id: 5, parent: 1, text: "Item 1.1" },
	
		{ id: 6, parent: 1, text: "Item 1.2" },
	
		{ id: 7, parent: 1, text: "Item 1.3" },
	
		{ id: 8, parent: 3, text: "Item 3.1" },
	
		{ id: 9, parent: 3, text: "Item 3.2" },
	
		{ id: 10, parent: 5, text: "Item 1.1.1" }
	
	];
	
	$(function () {
	
		// initialize and bind the TreeView with local data
	
		$("#treeMultiSelect").ejTreeView({
	
			allowMultiSelection: true, //enable multiple selection in TreeView
	
			fields: { dataSource: localData, id: "id", parentId: "parent", text: "text" }
	
		});
		
		// create instance for TreeView
		var treeObj = $("#treeMultiSelect").data("ejTreeView");
	
		treeObj.getSelectedNodes(); //returns the collections of TreeView selected nodes
	
	});
	
{% endhighlight %}


