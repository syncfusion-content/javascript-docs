---
layout: post
title: Treeview-with-context-menu-support
description: treeview with context menu support
platform: js
control: TreeView
documentation: ug
---

### Treeview with context menu support

**TreeView** control is availed with the context menu options that open on right-click, over the node. Other than the default menu items available, you can add the new node dynamically in **TreeView** and also delete the item, enable and disable the item in **TreeView**. It is achieved by adding the **Context Menu** option to the **TreeView**.

#### Menu Item

By default, the context menu options are provided with four items namely: **Add New Item, Delete Item, Enable Item** and **Disable Item**. When you want to customize and use your own custom menu items, then you can customize the **TreeView** with the desired collections. 

The following code example illustrates how to configure the context menu elements for the **TreeView** and in the following example, you have to specify the menu type as **ej.MenuType.ContextMenu** and in the **menuClick** function, you can check the cases with add, delete, remove or enable item in **TreeView**. 

And each functionality in the context menu option is done by specific methods. For example, you have added the new item in **TreeView** by using the **addNode()** method, delete the item using **removeNode()** method, disable the item using **disableNode()** method and enable the item **enableNode()** method respectively.

The following steps explain how you can enable the **showCheckbox** property for **TreeView**.

* In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**

****

{% highlight html %}

**[HTML]**

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
<div>
        <ul id="treeviewMenu">
            <li><a href="#">Add New Item</a></li>
            <li><a href="#">Remove Item</a></li>
            <li><a href="#">Disable Item</a></li>
            <li><a href="#">Enable Item</a></li>
        </ul>
    </div>



{% endhighlight %}



* Add **ContextMenu** for **TreeView** control as follows.

****

{% highlight js %}

**[JavaScript]**
var tabIndex = 1;
$("#treeView").ejTreeView();
        $("#treeviewMenu").ejMenu({
            menuType: ej.MenuType.ContextMenu,
            openOnClick: false,
            contextMenuTarget: "#treeView",
            showArrow: true,
            click: "menuclick",
            beforeOpen: "beforeOpen"
        });
        treeviewObj = $("#treeView").data("ejTreeView");


{% endhighlight %}



* Define the events in the script as follows.



{% highlight js %}

function beforeOpen(args) {
        if (!$(args.target).hasClass("e-text"))
            args.cancel = true;
        else {
            selectedNode = args.target;
            treeviewObj.selectNode(selectedNode);
        }
    }
    function menuclick(args) {
        if (args.events.text == "Add New Item") {
            treeviewObj.addNode("Item" + tabIndex, selectedNode);
            tabIndex++;
        }
        else if (args.events.text == "Remove Item") {
            treeviewObj.removeNode(selectedNode);
        }
        else if (args.events.text == "Disable Item") {
            treeviewObj.disableNode(selectedNode)
        }
        else if (args.events.text == "Enable Item") {
            treeviewObj.enableNode(selectedNode)
        }
    }



{% endhighlight %}



{% include image.html url="/js/TreeView/How-To/Treeview-with-context-menu-support_images/Treeview-with-context-menu-support_img1.png" Caption=""%}

The output for the context menu for **TreeView** control is as follows.

























_Figure_ _2__9__: Context M__enu for TreeView_



