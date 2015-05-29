---
layout: post
title: checkbox-support
description: checkbox support
platform: js
control: TreeView
documentation: ug
---

# Checkbox Support

**TreeView** allows you to check or uncheck the nodes. When you check the parent node of **TreeView**, the corresponding child nodes are automatically moved to checked state. A parent node check state is automatically set to indeterminate when it has checked and unchecked child nodes. To enable this feature, set the **showCheckbox** property to **“tTrue”.**

The following steps explain how you can enable the **showCheckbox** property for **TreeView**.

* In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**



<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;        &lt;li class="expanded"&gt;            Favorites            &lt;ul&gt;                <li>Desktop</li>                <li>Downloads</li>                <li>Recent places</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li class="expanded"&gt;            Libraries            &lt;ul&gt;                &lt;li&gt;                    Documents                    &lt;ul&gt;                        <li>My Documents</li>                        <li>Public Documents</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Pictures                    &lt;ul&gt;                        <li>My Pictures</li>                        <li>Public Pictures</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Music                    &lt;ul&gt;                        <li>My Music</li>                        <li>Public Music</li>                    &lt;/ul&gt;                &lt;/li&gt;                <li>Subversion</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;            Computer            &lt;ul&gt;                <li>Folder(C)&lt;/li&gt;                <li>Folder(D)&lt;/li&gt;                <li>Folder(F)&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;</td></tr>
<tr>
<td>
            <b>[JavaScript]</b><b>// Enable showCheckbox for TreeView control as follows.</b>        $("#treeView").ejTreeView({<b>showCheckbox</b>: true });</td></tr>
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



    }).**ShowCheckbox (true)**





**[ASPX]**

**\\Configure TreeView in the aspx page.**



&lt;ej:TreeView ID="treeview" runat="server" ShowCheckbox="true"&gt;

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



The following image is the output for **TreeView** when **showCheckbox** is set to “**True**”.



![](checkbox-support_images\checkbox-support_img1.png)

_Figure_ _16__42__:_ _TreeView with checkbox_

### Auto Check Parent Node

To overcome the default functionality of **TreeView**, when you don’t want the parent node check state being moved to indeterminate state and when you check the corresponding child node, you can enable the property **autoCheckParentNode**. By using this functionality, you can check the single parent node as well as the corresponding child nodes. You can specify the property **autoCheckParentNode** in **TreeView** as follows.



{% highlight js %}

**[JavaScript]**

    $("#treeView").ejTreeView({ **autoCheckParentNode**: false,showCheckbox: true});



{% endhighlight %}



**[View]**

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



    }).**AutoCheckParentNode(true)**



[ASPX]    

&lt;ej:TreeView ID="treeview" runat="server" AutoCheckParentNode="true"&gt;

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

### Checked Nodes

You can specify the **Checked Nodes** in **TreeView** initially by using the property **checkedNodes**. **Checked Nodes** index collection is given to the integer array. You can specify the property **checkedNodes** in **TreeView** control in the script as follows.



{% highlight js %}

**[JavaScript]**

    $("#treeView").ejTreeView({ showCheckbox: true,  **checkedNodes**: [1, 2] });



{% endhighlight %}



**[View]**

@{List<int> nodes = new List<int>() { 0,4 }; }

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



    }).**CheckedNodes(nodes)**





<table>
<tr>
<td>
<b>[C#]</b>public partial class Checkbox : System.Web.UI.Page    {        protected void Page_Load(object sender, EventArgs e)        {            List<int> nodes = new List<int>() { 0, 4 };            this.treeview.<b>checkedNodes</b> = nodes;        }<b>    }</b></td></tr>
<tr>
<td>
<b>[ASPX]</b><b>\\ Configure TreeView in the aspx page.</b>&lt;ej:TreeView ID="treeview" runat="server" ShowCheckbox="true"&gt;        &lt;Nodes&gt;            &lt;ej:TreeViewNode Expanded="True" Text="Favorites"&gt;                &lt;Nodes&gt;                    &lt;ej:TreeViewNode Text="Desktop"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Downloads"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Recent places"&gt;&lt;/ej:TreeViewNode&gt;                &lt;/Nodes&gt;            &lt;/ej:TreeViewNode&gt;            &lt;ej:TreeViewNode Expanded="True" Text="Libraries"&gt;                &lt;Nodes&gt;                    &lt;ej:TreeViewNode Text="Documents"&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="My Documents"&gt;&lt;/ej:TreeViewNode&gt;                            &lt;ej:TreeViewNode Text="Public Documents"&gt;&lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                    &lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Pictures"&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="My Pictures"&gt;&lt;/ej:TreeViewNode&gt;                            &lt;ej:TreeViewNode Text="Public Pictures"&gt;&lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                    &lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Music"&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="My Music"&gt;&lt;/ej:TreeViewNode&gt;                            &lt;ej:TreeViewNode Text="Public Music"&gt;&lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                    &lt;/ej:TreeViewNode&gt;                &lt;/Nodes&gt;            &lt;/ej:TreeViewNode&gt;            &lt;ej:TreeViewNode Text="Computer"&gt;                &lt;Nodes&gt;                    &lt;ej:TreeViewNode Text="Folder(C)"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Folder(D)"&gt;&lt;/ej:TreeViewNode&gt;                    &lt;ej:TreeViewNode Text="Folder(E)"&gt;&lt;/ej:TreeViewNode&gt;                &lt;/Nodes&gt;            &lt;/ej:TreeViewNode&gt;        &lt;/Nodes&gt;<b>    &lt;/ej:TreeView&gt;</b></td></tr>
</table>


