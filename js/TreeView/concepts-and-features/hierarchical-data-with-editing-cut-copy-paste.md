---
layout: post
title: hierarchical-data-with-editing-cut-copy-paste
description: hierarchical data with editing-cut-copy-paste
platform: js
control: TreeView
documentation: ug
---

# Hierarchical data with Editing-cut-copy-paste

The **TreeView** control permits you to edit a node and also allows you to cut, copy and paste the node in **TreeView**. You can edit the tree node name when it is required. This is achieved by using the **allowEditing** property. By setting the property as **“tTrue”**, you can select a node and press F2 or double click the node to initiate editing.

The following steps explain how to enable the **allowEditing** property for **TreeView**.

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

**[JavaScript]**
**// Enable allowEditing for TreeView control as follows.**

            $("#treeView").ejTreeView({ **allowEditing**: true });



{% endhighlight %}





**[View]**

**\\ To configure TreeView in the CSHTML page**

@Html.EJ().TreeView("treeview").Items(items =>

    {

        items.Add().Text("Favorites").Expanded(true).Children(child =>

                   {

                       child.Add().Text("Desktop");

                       child.Add().Text("Downloads");

                       child.Add().Text("Recent places");

                   });

        items.Add().Text("Libraries").Expanded(true).Children(child =>

        {

            child.Add().Text("Documents").Children(child1 =>

                {

                    child1.Add().Text("My Documents");

                    child1.Add().Text("Public Documents");

                });

            child.Add().Text("Pictures").Children(child1 =>

            {

                child1.Add().Text("My Pictures");

                child1.Add().Text("Public Pictures");

            });

            child.Add().Text("Music").Children(child1 =>

            {

                child1.Add().Text("My Music");

                child1.Add().Text("Public Music");

            });

            child.Add().Text("Subversion");



        });

        items.Add().Text("Computer").Children(child =>

        {

            child.Add().Text("Folder(C)");

            child.Add().Text("Folder(D)");

            child.Add().Text("Folder(E)");

        });



    }).**AllowEditing(true)**







**[ASPX]**

**\\ Configure TreeView in the aspx page.**

&lt;ej:TreeView ID="treeview" runat="server" AllowEditing="true"&gt;

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



* The following screenshot displays the appearance of Editing-cut-copy-paste the node in **TreeView** component.



![](hierarchical-data-with-editing-cut-copy-paste_images\hierarchical-data-with-editing-cut-copy-paste_img1.png)

_Figure_ _1__4__0__:_ _Node Editing-cut-copy-paste_

