---
layout: post
title: treeview-with-context-menu-support
description: treeview with context menu support
platform: js
control: TreeView
documentation: ug
---

# TreeView with Context Menu Support

**TreeView** control is available with context menu options that open when right clicked over the node. Other than the default menu items available, you can add the new node dynamically in **TreeView** or delete the item. You can also enable or disable the item in **TreeView**. It is achieved by adding the **Context Menu** option to the **TreeView**.

**Menu Item**

By default, the Context Menu options are provided with 4 items namely **Add New Item, Delete Item, Enable Item** and **Disable Item**. When you want to customize and use your own **Custom Menu items**, you can customize the **TreeView** with your desired collections. 

The following code sample illustrates how to configure the Context Menu elements for the TreeView and in the following example, you must specify the Menu type as **ej.MenuType.ContextMenu** and in the **menuClick** function, you can check the cases with add, delete, remove or enable item in **TreeView**. 

And each functionality in the context menu option is done by a specific method.For example, you can add a new item in TreeView by using the **addNode()** method, delete the item using **removeNode()** method, disable the item using **disableNode()** method and enable the item using **enableNode()** method respectively.

The following steps explain enabling the **showCheckbox** property for **TreeView**.

Configure **TreeView** in the **aspx** page as follows.



**[ASPX]**



&lt;div style="width: 250px"&gt;

   &lt;ej:TreeView ID="treeview" runat="server"&gt;

        &lt;Nodes&gt;

            &lt;ej:TreeViewNode Expanded="True" Text="Favorites"&gt;

                &lt;Nodes&gt;

                    &lt;ej:TreeViewNode Text="Desktop"&gt;&lt;/ej:TreeViewNode&gt;

                    &lt;ej:TreeViewNode Text="Downloads"&gt;&lt;/ej:TreeViewNode&gt;

                    &lt;ej:TreeViewNode Text="Recent places"&gt;&lt;/ej:TreeViewNode&gt;

                &lt;/Nodes&gt;

            &lt;/ej:TreeViewNode&gt;



            &lt;ej:TreeViewNode Expanded="True" Text="Libraries"&gt;

                &lt;Nodes&gt;

                    &lt;ej:TreeViewNode Text="Documents"&gt;

                        &lt;Nodes&gt;

                            &lt;ej:TreeViewNode Text="My Documents"&gt;&lt;/ej:TreeViewNode&gt;

                            &lt;ej:TreeViewNode Text="Public Documents"&gt;&lt;/ej:TreeViewNode&gt;

                        &lt;/Nodes&gt;

                    &lt;/ej:TreeViewNode&gt;

                    &lt;ej:TreeViewNode Text="Pictures"&gt;

                        &lt;Nodes&gt;

                            &lt;ej:TreeViewNode Text="My Pictures"&gt;&lt;/ej:TreeViewNode&gt;

                            &lt;ej:TreeViewNode Text="Public Pictures"&gt;&lt;/ej:TreeViewNode&gt;

                        &lt;/Nodes&gt;

                    &lt;/ej:TreeViewNode&gt;

                    &lt;ej:TreeViewNode Text="Music"&gt;

                        &lt;Nodes&gt;

                            &lt;ej:TreeViewNode Text="My Music"&gt;&lt;/ej:TreeViewNode&gt;

                            &lt;ej:TreeViewNode Text="Public Music"&gt;&lt;/ej:TreeViewNode&gt;

                        &lt;/Nodes&gt;

                    &lt;/ej:TreeViewNode&gt;

                &lt;/Nodes&gt;

            &lt;/ej:TreeViewNode&gt;

            &lt;ej:TreeViewNode Text="Computer"&gt;

                &lt;Nodes&gt;

                    &lt;ej:TreeViewNode Text="Folder(C)"&gt;&lt;/ej:TreeViewNode&gt;

                    &lt;ej:TreeViewNode Text="Folder(D)"&gt;&lt;/ej:TreeViewNode&gt;

                    &lt;ej:TreeViewNode Text="Folder(E)"&gt;&lt;/ej:TreeViewNode&gt;

                &lt;/Nodes&gt;

            &lt;/ej:TreeViewNode&gt;

        &lt;/Nodes&gt;

    &lt;/ej:TreeView&gt;

    &lt;/div&gt;

      &lt;div&gt;

        &lt;ej:Menu ID="treeviewMenu" MenuType="ContextMenu" ClientSideOnClick="menuclick" ClientSideOnBeforeContextOpen="beforeOpen" OpenOnClick="false" runat="server" ContextMenuTarget="#treeView"&gt;

            &lt;Items&gt;

                &lt;ej:MenuItem Text="Add New Item"&gt;&lt;/ej:MenuItem&gt;

            &lt;/Items&gt;

            &lt;Items&gt;

                &lt;ej:MenuItem Text="Remove Item"&gt;&lt;/ej:MenuItem&gt;

            &lt;/Items&gt;

            &lt;Items&gt;

                &lt;ej:MenuItem Text="Disable Item"&gt;&lt;/ej:MenuItem&gt;

            &lt;/Items&gt;

            &lt;Items&gt;

                &lt;ej:MenuItem Text="Enable Item"&gt;&lt;/ej:MenuItem&gt;

            &lt;/Items&gt;

        &lt;/ej:Menu&gt;

    &lt;/div&gt;



1. Define the events in the script as follows.



&lt;script type="text/javascript"&gt;

var tabIndex = 1, treeviewObj, selectedNode;

        $(function () {

            treeviewObj = $("#treeview").data("ejTreeView");

        });

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

                treeviewObj.addNode("Item" + tabIndex, null, selectedNode);

                tabIndex++;

            }

            else if (args.events.text == "Remove Item") {

                treeviewObj.removeNode(selectedNode);

            }

            else if (args.events.text == "Disable Item") {

                treeviewObj.disableNode(selectedNode);

            }

            else if (args.events.text == "Enable Item") {

                treeviewObj.enableNode(selectedNode);

            }

        }

&lt;/script&gt;



The output for the context menu for TreeView control is as follows.



{% include image.html url="\js\TreeView\concepts-and-features\treeview-with-context-menu-support_images\treeview-with-context-menu-support_img1.png" Caption="Figure 55: Context Menu Appearance"%}

