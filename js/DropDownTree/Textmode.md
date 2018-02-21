---
layout: post
title: Textmode with DropDownTree widget for Syncfusion Essential JS
description: Describes about Textmode functionalities in DropDownTree widget for Syncfusion Essential JS
platform: js
control: DropDownTree
documentation: ug
keywords: Textmode, dropdown,textModes, Delimiter
api: /api/js/ejDropDownTree
---

## textMode

You can get the node text or node with parent text in the value field by using the [`textMode`](https://help.syncfusion.com/api/js/ejdropdowntree#members:textMode) property.

To get the node with parent in the value field of the input element, set `textMode` to `fullPath`.
It's default value is `none`.

{% highlight html %}

    <input type="text" id="itemList" />
     
{% endhighlight %}

{% highlight javascript %}

   var localData = [
                    { id: 1, name: "Windows Team", hasChild: true, expanded: true },
                    { id: 2, pid: 1, name: "Clark" },
                    { id: 3, pid: 1, name: "Wright" },
                    { id: 4, pid: 1, name: "Lopez" },
                    { id: 6, pid: 1, name: "Anderson" },
                    { id: 7, name: "Web Team", hasChild: true, expanded: true },
                    { id: 8, pid: 7, name: "Joshua" },
                    { id: 9, pid: 7, name: "Matthew" },
                    { id: 10, pid: 7, name: "David" },
                    { id: 11, name: "Build Team", hasChild: true },
                    { id: 12, pid: 11, name: "Ryan" },
                    { id: 13, pid: 11, name: "Justin" },
                    { id: 14, pid: 11, name: "Robert" },
                    { id: 15, pid: 11, name: "Johnson" },
                    { id: 16, name: "WPF Team", hasChild: true },
                    { id: 17, pid: 16, name: "Rock" },
                    { id: 18, pid: 16, name: "Gospel" },
                    { id: 19, pid: 16, name: "Brown" },
                    { id: 20, pid: 16, name: "Miller" }];
        $(function () {
            $('#itemList').ejDropDownTree({
                treeViewSettings: {
                    showCheckbox: true,
                    fields: { id: "id", parentId: "pid", value: "id", text: "name", hasChild: "hasChild", dataSource: localData, expanded: "expanded" }
                },
                watermarkText: "Please select",
                textMode: "fullPath"
            });
        });

{% endhighlight %}

![](TextMode_images/fullpath.png)

## TextMode with fullPathDelimiter

Each selected item’s text is appended to the textbox with parent separated by delimiter “/”, by default. This is enabled by assigning `textMode` (enum). You can customize the delimiter option by using the [`fullPathDelimiter`](https://help.syncfusion.com/api/js/ejdropdowntree#members:fullpathdelimiter) property.

{% highlight html %}

<input type="text" id="itemList" />

{% endhighlight %}

{% highlight javascript %}

<script type="text/javascript">
        var localData = [
                    { id: 1, name: "Windows Team", hasChild: true, expanded: true },
                    { id: 2, pid: 1, name: "Clark" },
                    { id: 3, pid: 1, name: "Wright" },
                    { id: 4, pid: 1, name: "Lopez" },
                    { id: 6, pid: 1, name: "Anderson" },
                    { id: 7, name: "Web Team", hasChild: true, expanded: true },
                    { id: 8, pid: 7, name: "Joshua" },
                    { id: 9, pid: 7, name: "Matthew" },
                    { id: 10, pid: 7, name: "David" },
                    { id: 11, name: "Build Team", hasChild: true },
                    { id: 12, pid: 11, name: "Ryan" },
                    { id: 13, pid: 11, name: "Justin" },
                    { id: 14, pid: 11, name: "Robert" },
                    { id: 15, pid: 11, name: "Johnson" },
                    { id: 16, name: "WPF Team", hasChild: true },
                    { id: 17, pid: 16, name: "Rock" },
                    { id: 18, pid: 16, name: "Gospel" },
                    { id: 19, pid: 16, name: "Brown" },
                    { id: 20, pid: 16, name: "Miller" }];
        $(function () {
            $('#itemList').ejDropDownTree({
                treeViewSettings: {
                    fields: { id: "id", parentId: "pid", value: "id", text: "name", hasChild: "hasChild", dataSource: localData, expanded: "expanded" }
                },
                textMode: "fullPath",
                fullPathDelimiter: "->"
            });
        });
    </script>

{% endhighlight %}

![](TextMode_images/fullpath_with_delimeter.png)