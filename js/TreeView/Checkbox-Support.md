---
layout: post
title: Checkboxes
description: checkboxes
platform: js
control: TreeView
documentation: ug
---

# Checkboxes

TreeView consists of in-build checkbox option and it can be displayed to the left of the tree node by setting the [showCheckbox](http://help.syncfusion.com/js/api/ejtreeview#members:showcheckbox) property as true. It allows you to select more than one node at a time. 

## Indeterminate Checkboxes

TreeView supports tristate checkboxes in addition with standard two state checkboxes. By default TreeView has been enabled with tristate in checkboxes. You can enable 2-state checkboxes by using [autoCheckParentNode](http://help.syncfusion.com/js/api/ejtreeview#members:autocheckparentnode) as false.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView"> </div>

{% endhighlight %}

{% highlight js %}

        $(function () {

            // initialize and bind the TreeView with local data

            $("#treeView").ejTreeView({

                showCheckbox: true, // shows each node with checkboxes

                autoCheckParentNode: false,// enable 2-state checkboxes

                fields: {
                    dataSource: [

                    {

                        text: "Item 1",

                        child: [

                        { text: "Item 1.1" },

                        { text: "Item 1.2" }

                        ]

                    },

                    { text: "Item 2" },

                    { text: "Item 3" }

                    ]

                }

            });

        });

{% endhighlight %}

## Auto Checkable

By default checkbox state of child nodes depends up on parent node checkbox state and also parent node state gets updated based on child nodes state. You can turn off this option by setting [autoCheck](http://help.syncfusion.com/js/api/ejtreeview#members:autocheck) as false to make independent parent and child nodes checkboxes.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView"> </div>

{% endhighlight %}

{% highlight js %}

        $(function () {

            // initialize and bind the TreeView with local data

            $("#treeView").ejTreeView({

                showCheckbox: true, // shows each node with checkboxes

                autoCheck: false,// turns off auto check of parent and child nodes

                fields: {
                    dataSource: [

                    {

                        text: "Item 1",

                        child: [

                        { text: "Item 1.1" },

                        { text: "Item 1.2" }

                        ]

                    },

                    { text: "Item 2" },

                    { text: "Item 3" }

                    ]

                }

            });

        });

{% endhighlight %}

## Check or Uncheck Node

Tree node can be checked or unchecked using [checkNode](http://help.syncfusion.com/js/api/ejtreeview#methods:checknode) and [uncheckNode](http://help.syncfusion.com/js/api/ejtreeview#methods:unchecknode) methods while [showCheckbox](http://help.syncfusion.com/js/api/ejtreeview#members:showcheckbox) property is enabled in TreeView. [nodeCheck](http://help.syncfusion.com/js/api/ejtreeview#events:nodecheck) and [nodeUncheck](http://help.syncfusion.com/js/api/ejtreeview#events:nodeuncheck) event occurs based on checkbox state.

{% highlight js %}

        //create an instance from an existing TreeView.

        // only after control creation we can get treeObj otherwise it throws exception.

        treeObj = $("#treeView").ejTreeView('instance');

        //to check node

        treeObj.checkNode("2");

        //to uncheck node

        treeObj.uncheckNode("2");

{% endhighlight %}


## Get Checked Nodes

To get checked nodes of TreeView, you can use [getCheckedNodes](http://help.syncfusion.com/js/api/ejtreeview#methods:getcheckednodes) method. It returns the collection of tree node.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView"> </div>

{% endhighlight %}

{% highlight js %}

        $(function () {

            // initialize and bind the TreeView with local data

            $("#treeView").ejTreeView({

                showCheckbox: true, // shows each node with checkboxes

                autoCheck: false,// turns off auto check of parent and child nodes

                fields: {
                    dataSource: [

                    {

                        text: "Item 1",

                        child: [

                        { text: "Item 1.1" },

                        { text: "Item 1.2" }

                        ]

                    },

                    { text: "Item 2" },

                    { text: "Item 3" }

                    ]

                }

            });

        });

        function onClick() {

            //create an instance from an existing TreeView.

            // only after control creation we can get treeObj otherwise it throws exception.

            treeObj = $("#treeView").ejTreeView('instance');

            //to get checked nodes

            treeObj.getCheckedNodes();

        }

{% endhighlight %}

