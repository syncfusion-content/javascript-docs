---
layout: post
title: rtl
description: rtl
platform: js
control: TreeView
documentation: ug
---

# RTL

**TreeView** supports right-to-left layout and the node text is displayed in the **RTL** languages. Arabic and Hebrew are languages written from right to left. When you desire to change the display of **TreeView** as right to left direction, you can do so by using the **enableRTL** property. To enable or disable this option, set the appropriate value for the **enableRTL** property. When **enableRTL** is enabled, the appearance of the **TreeView** is displayed in the right to left direction. You can display the **TreeView** as right to left direction by using this feature.

The following steps explain enabling the **enableRTL** property for **TreeView**.

* In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**

****

<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;        &lt;li class="expanded"&gt;            Favorites            &lt;ul&gt;                <li>Desktop</li>                <li>Downloads</li>                <li>Recent places</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li class="expanded"&gt;            Libraries            &lt;ul&gt;                &lt;li&gt;                    Documents                    &lt;ul&gt;                        <li>My Documents</li>                        <li>Public Documents</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Pictures                    &lt;ul&gt;                        <li>My Pictures</li>                        <li>Public Pictures</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Music                    &lt;ul&gt;                        <li>My Music</li>                        <li>Public Music</li>                    &lt;/ul&gt;                &lt;/li&gt;                <li>Subversion</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;            Computer            &lt;ul&gt;                <li>Folder(C)&lt;/li&gt;                <li>Folder(D)&lt;/li&gt;                <li>Folder(F)&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;</td></tr>
<tr>
<td>
            <b>[JavaScript]</b><b>// Enable the property enableRTL for TreeView control as follows.</b>           $("#treeView").ejTreeView(			{			    <b>enableRTL</b>: true,			});</td></tr>
</table>


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

}).**EnableRTL(true)**



**[ASPX]**

**\\ Configure TreeView in the aspx page.**

&lt;ej:TreeView ID="treeview" runat="server" EnableRTL="true"&gt;

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

    **&lt;/ej:TreeView&gt;**



The output for **TreeView** when **enableRTL** is set to “**True**” is as follows.

![](rtl_images\rtl_img1.png)

![](rtl_images\rtl_img2.png)

_Figure_ _21__53__: TreeView with_ _enableRTL_

