---
layout: post
title: Knockout-Support
description: knockout support
platform: js
control: TreeView 
documentation: ug
api: /api/js/
---

# Knockout Support

**Knockout support** allows you to bind the **HTML** elements against any of the available data models. It is of two types.

* One-way binding
* Two-way binding

##One-way binding

**One-way binding** refers to the process of applying observable values to all the available properties of the **TreeView** widget, but the changes made in **TreeView** widget are not reflected and triggered in turn to the observable collection. This kind of binding applies to all the properties of the **TreeView** widget.

The following example depicts the way to bind data to the **TreeView** widgets through **knockoutJS Support**.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <!-- Style sheet for default theme (flat azure) -->
    <link href=" http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>
</head>
<body>
    <div style="width: 250px; max-width:100%">
            <div id="treeview" data-bind="ejTreeView: {fields :{ dataSource: dataSource,id:'id',text:'name',hasChild:'hasChild',expanded:'expanded',parentId:'pid'}} "></div>
    </div>
    <script type="text/javascript">
        $(function () {
            var treeData = [
                        { id: 1, name: "Discover Music", hasChild: true, expanded: true },
                       { id: 2, pid: 1, name: "Hot Singles" },
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
                       { id: 25, pid: 21, name: "Mobile MVC" }];
            window.employeeView = {
                dataSource: ko.observableArray(treeData),
            };
            ko.applyBindings(employeeView);
        });
    </script>
</body>
</html>

{% endhighlight %}

For more details about one-way binding in TreeView, please refer the below online sample.

<http://js.syncfusion.com/demos/web/#!/bootstrap/treeview/KnockoutSupport>

##Two-way binding

TreeView data source supports two-way (bidirectional) binding modes when we specifying e-deepwatch attribute as true in TreeView control. It allows to synchronize the changes of the TreeView and data source.

When enable e-deepwatch support, if do any interaction (like drag and drop, edit, add, remove, selection, check, expand any node) in TreeView then mapped data source will be updated automatically. And also if do any changes in data source then TreeView will be updated automatically.

{% highlight html %}

<div style="width: 250px; max-width:100%">
      <div id="treeview" e-deepwatch="true" data-bind="ejTreeView: { showCheckbox: true, fields :{ dataSource: dataSource, id:'id',text:'name',hasChild:'hasChild',expanded:'expanded',parentId:'pid', isChecked : 'checked'}} "></div>
</div>

{% endhighlight %}

For more details about two-way binding in TreeView, refer the sample [here]( http://jsplayground.syncfusion.com/op0cfsz4)

For more information about the **knockout binding**, refer the following online documentation in the given link location,

<https://help.syncfusion.com/js/knockoutjs>

