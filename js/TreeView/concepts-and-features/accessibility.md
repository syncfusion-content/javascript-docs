---
layout: post
title: accessibility
description: accessibility
platform: js
control: TreeView
documentation: ug
---

# Accessibility

**TreeView** provides full keyboard support. You can interact with the **TreeView** control using the keyboard. It is compatible with the standard keyboard navigation and you can focus on **TreeView** with a predefined Alt and Key combination. Also, you can navigate through the nodes, expand or collapse, select, check and uncheck nodes with the provided shortcut keys. You can access the **TreeView** with the shortcut keys by using the **allowKeyboardNavigation** property.

This feature is mainly useful for all the keyboard users to access the **TreeView** with the keyboard shortcut keys.

The following table showcases the various keyboard shortcuts available in the **TreeView** control. 

_Table_ _3__: Keyboard Shortcuts_

<table>
<tr>
<td>
<b>Keys </b></td><td>
<b>Functions</b></td></tr>
<tr>
<td>
<b>      Alt+j</b></td><td>
Focuses the control.</td></tr>
<tr>
<td>
<b>F2</b></td><td>
Edit the selected node. </td></tr>
<tr>
<td>
<b>Ctrl + X</b></td><td>
Cut the selected node.</td></tr>
<tr>
<td>
<b>Ctrl + C</b></td><td>
Copy the selected node.</td></tr>
<tr>
<td>
<b>Ctrl + V</b></td><td>
Paste the cut or copied nodes to selected node.</td></tr>
<tr>
<td>
<b>Delete key</b></td><td>
Delete the selected node.</td></tr>
<tr>
<td>
<b>Down</b></td><td>
Selected next node.</td></tr>
<tr>
<td>
<b>Up</b></td><td>
Selected previous node.</td></tr>
<tr>
<td>
<b>Right</b></td><td>
Expand selected node. </td></tr>
<tr>
<td>
<b>Left</b></td><td>
Collapse selected node.</td></tr>
<tr>
<td>
<b>Enter</b></td><td>
Select node.</td></tr>
<tr>
<td>
<b>Space</b></td><td>
Toggle Checks and Unchecks.</td></tr>
<tr>
<td>
<b>Home</b></td><td>
Selected first child node.</td></tr>
<tr>
<td>
<b>End</b></td><td>
Selected last child node.</td></tr>
</table>


The following steps explain how to enable the **allowKeyboardNavigation** property for **TreeView**.

* In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**

****

<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;        &lt;li class="expanded"&gt;            Favorites            &lt;ul&gt;                <li>Desktop</li>                <li>Downloads</li>                <li>Recent places</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li class="expanded"&gt;            Libraries            &lt;ul&gt;                &lt;li&gt;                    Documents                    &lt;ul&gt;                        <li>My Documents</li>                        <li>Public Documents</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Pictures                    &lt;ul&gt;                        <li>My Pictures</li>                        <li>Public Pictures</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Music                    &lt;ul&gt;                        <li>My Music</li>                        <li>Public Music</li>                    &lt;/ul&gt;                &lt;/li&gt;                <li>Subversion</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;            Computer            &lt;ul&gt;                <li>Folder(C)&lt;/li&gt;                <li>Folder(D)&lt;/li&gt;                <li>Folder(F)&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;</td></tr>
<tr>
<td>
            <b>[JavaScript]</b><b>// Enable allowKeyboardNavigation for TreeView control as follows.</b>     $(function () {        $("#treeView").ejTreeView({            showCheckbox: true,            allowEditing: true,            <b>allowKeyboardNavigation</b>:true        });        //Control focus key        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) {                // j- key code.                $("#treeView.e-treeview-wrap").focus();            }        });    });</td></tr>
</table>


<table>
<tr>
<td>
 <b>[View]</b><b>\\ To configure TreeView in the CSHTML page</b>@Html.EJ().TreeView("treeview").Items(items =>      {             items.Add().Text("Favorites").Expanded(true).Children(child =>             {                   child.Add().Text("Desktop");                   child.Add().Text("Downloads");                   child.Add().Text("Recent places");             });             items.Add().Text("Libraries").Expanded(true).Children(child =>             {                    child.Add().Text("Documents").Children(child1 =>                    {                                child1.Add().Text("My Documents");                                child1.Add().Text("Public Documents");                    });                    child.Add().Text("Pictures").Children(child1 =>                    {                            child1.Add().Text("My Pictures");                            child1.Add().Text("Public Pictures");                    });                    child.Add().Text("Music").Children(child1 =>                     {                            child1.Add().Text("My Music");                            child1.Add().Text("Public Music");                     });                     child.Add().Text("Subversion");              });              items.Add().Text("Computer").Children(child =>              {                     child.Add().Text("Folder(C)");                     child.Add().Text("Folder(D)");                     child.Add().Text("Folder(E)");               });     }).ShowCheckbox(true).AllowEditing(true).<b>AllowKeyboardNavigation(true)</b></td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;                    //Control focus key            $(document).on("keydown", function (e) {                if (e.altKey && e.keyCode === 74) {                    // j- key code.                    $(".e-treeview-wrap").focus();                }            });	    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
[ASPX]\\ Configure TreeView in the aspx page.&lt;ej:TreeView ID="treeview" runat="server" ShowCheckbox="true" AllowEditing="true" AllowKeyboardNavigation="true"&gt;        &lt;Nodes&gt;            &lt;ej:TreeViewNode Expanded="True" Text="Favorites"&gt;                &lt;Nodes&gt;                    &lt;ej:TreeViewNode Text="Desktop"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Downloads"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Recent places"&gt;&lt;/ej:TreeViewNode&gt;                &lt;/Nodes&gt;            &lt;/ej:TreeViewNode&gt;            &lt;ej:TreeViewNode Expanded="True" Text="Libraries"&gt;                &lt;Nodes&gt;                    &lt;ej:TreeViewNode Text="Documents"&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="My Documents"&gt;&lt;/ej:TreeViewNode&gt;                            &lt;ej:TreeViewNode Text="Public Documents"&gt;&lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                    &lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Pictures"&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="My Pictures"&gt;&lt;/ej:TreeViewNode&gt;                            &lt;ej:TreeViewNode Text="Public Pictures"&gt;&lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                    &lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Music"&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="My Music"&gt;&lt;/ej:TreeViewNode&gt;                            &lt;ej:TreeViewNode Text="Public Music"&gt;&lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                    &lt;/ej:TreeViewNode&gt;                &lt;/Nodes&gt;            &lt;/ej:TreeViewNode&gt;            &lt;ej:TreeViewNode Text="Computer"&gt;                &lt;Nodes&gt;                    &lt;ej:TreeViewNode Text="Folder(C)"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Folder(D)"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Folder(E)"&gt;&lt;/ej:TreeViewNode&gt;                &lt;/Nodes&gt;            &lt;/ej:TreeViewNode&gt;        &lt;/Nodes&gt;    &lt;/ej:TreeView&gt;</td></tr>
<tr>
<td>
[JavaScript]\\ Focus the TreeView in the script.&lt;script type="text/javascript"&gt;                    //Control focus key            $(document).on("keydown", function (e) {                if (e.altKey && e.keyCode === 74) {                    // j- key code.                    $(".e-treeview-wrap").focus();                }            });	    &lt;/script&gt;</td></tr>
</table>


* Define CSS class for customizing the TreeView.



**[CSS]**



&lt;style&gt;

    .Treeview {

        display: inline-block;

        float: left;

        width: 153px;

    }



&lt;/style&gt;



The output for **TreeView** when **allowKeyboardNavigation** is set to “**True**”.



![](accessibility_images\accessibility_img1.png)

![](accessibility_images\accessibility_img2.png)

_Figure_ _2__5__8__: TreeView with_ _allowKeyboardNavigation_

