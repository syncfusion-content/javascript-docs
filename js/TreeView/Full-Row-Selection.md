---
layout: post
title: Full-Row-Selection
description: full row selection
platform: js
control: TreeView
documentation: ug
api: /api/js/ejtreeview
---


# Full Row Selection

The TreeView control provides the option to highlight a full row of tree view nodes. When [fullRowSelect](https://help.syncfusion.com/api/js/ejtreeview#members:fullrowselect) is **true**, a selection highlights the entire width of the tree view, display instead of the width of just the tree node text. It makes selection easier.

{% highlight html %}

<!--create the TreeView wrapper-->
	
<div id="fullRowTree"></div>

{% endhighlight %}

{% highlight js %}

var localData = [
    { id: 1, name: "Discover Music", hasChild: true, expanded: true },
    { id: 2, pid: 1, name: "Hot Singles", selected: true },
    { id: 3, pid: 1, name: "Rising Artists" },
    { id: 4, pid: 1, name: "Live Music" },
    { id: 6, pid: 1, name: "Best of 2013 So Far" },
    { id: 7, name: "Sales and Events", hasChild: true, expanded: true },
    { id: 8, pid: 7, name: "100 Albums - $5 Each" },
    { id: 9, pid: 7, name: "Hip-Hop and R&B Sale" },
    { id: 10, pid: 7, name: "CD Deals" },
    { id: 11, name: "Categories", hasChild: true },
    { id: 12, pid: 11, name: "Songs" },
    { id: 13, pid: 11, name: "Bestselling Albums" },
    { id: 14, pid: 11, name: "New Releases" },
    { id: 15, pid: 11, name: "Bestselling Songs" },
    { id: 16, name: "MP3 Albums", hasChild: true },
    { id: 17, pid: 16, name: "Rock" },
    { id: 18, pid: 16, name: "Gospel" },
    { id: 19, pid: 16, name: "Latin Music" },
    { id: 20, pid: 16, name: "Jazz" },
    { id: 21, name: "More in Music", hasChild: true },
    { id: 22, pid: 21, name: "Music Trade-In" },
    { id: 23, pid: 21, name: "Redeem a Gift Card" },
    { id: 24, pid: 21, name: "Band T-Shirts" },
    { id: 25, pid: 21, name: "Mobile MVC" }
];

$(function () {
    // initialize and bind the TreeView with local data
    $("#fullRowTree").ejTreeView({
        fullRowSelect: true, //enable full row selection in TreeView
        fields: {
            dataSource: localData, id: "id", parentId: "pid", text: "name",
            hasChild: "hasChild", expanded: "expanded", selected: "selected"
        }
    });
}); 

{% endhighlight %}

For more details about full row selection in TreeView, refer the sample [here](http://js.syncfusion.com/demos/web/#!/bootstrap/treeview/fullrowselect).

## Customization

You can customize the TreeView full row selection for template support by using [cssClass](https://help.syncfusion.com/api/js/ejtreeview#members:cssclass) property. Based on this custom class, you can customize the height of the highlighting TreeView node.

{% highlight html %}

<!--create the TreeView wrapper-->
<div id="fullRowTree"></div>

<script id="treeTemplate" type="text/x-jsrender">

    {{"{{"}}if !hasChild{{}}}}
    <span class="con-img {{"{{"}}>className{{}}}}"></span>
    {{"{{"}}/if{{}}}}
    {{"{{"}}>name{{}}}}

</script>

{% endhighlight %}

{% highlight js %}

var localData = [
    { id: 1, name: "Browsers", className: "browser", hasChild: true, expanded: true },
    { id: 2, pid: 1, name: "Internet Explorer", className: "ie-browser", selected: true },
    { id: 3, pid: 1, name: "Chrome", className: "chrome-browser" },
    { id: 4, pid: 1, name: "Firefox", className: "firefox-browser" },
    { id: 6, pid: 1, name: "Bitty", className: "bitty-browser" },
    { id: 7, pid: 1, name: "Opera", className: "opera-browser" }
];

$(function () {
    // initialize and bind the TreeView with local data
    $("#fullRowTree").ejTreeView({
        fullRowSelect: true, //enable full row selection in TreeView
        fields: {
            dataSource: localData, id: "id", parentId: "pid", text: "name",
            hasChild: "hasChild", expanded: "expanded", selected: "selected"
        },
        cssClass: "custom",
        template: "#treeTemplate"
    });
});
	
{% endhighlight %}

{% highlight css %}

<style>
	.custom .con-img {
		background-image: url("http://js.syncfusion.com/demos/web/images/toolbar/browserl.png");
		background-repeat: no-repeat;
		height: 32px;
		width: 32px;
		display: inline-block;
		overflow: hidden;
		background-repeat: no-repeat;
		text-align: center;
		vertical-align: middle;
	}
	
	.custom .e-li-active > .e-text-wrap .con-img {
		background-image: url("http://js.syncfusion.com/demos/web/images/toolbar/browserh.png");
	}

	.custom .e-li-hover > .e-text-wrap .con-img, .e-fullrow-wrap .e-li-focus > .e-text-wrap .con-img {
		background-image: url("http://js.syncfusion.com/demos/web/images/toolbar/browserl.png");
	}
	
	.custom .ie-browser {
		background-position: -84px 0px;
	}
	
	.custom .chrome-browser {
		background-position: -42px 0px;
	}
	
	.custom .firefox-browser {
		background-position: 0px 0px;
	}
	
	.custom .bitty-browser {
		background-position: -126px 0px;
	}
	
	.custom .opera-browser {
		background-position: -168px 0px;
	}

	/*customize the height of highlighting TreeView node*/
	.custom.e-fullrow-wrap .e-item ul .e-fullrow {
		margin-top: -36px;
		height: 36px;
	}
</style>

{% endhighlight %}

For more details about full row selection with template support in TreeView, refer the sample [here](http://jsplayground.syncfusion.com/Sync_1intlzxk).

