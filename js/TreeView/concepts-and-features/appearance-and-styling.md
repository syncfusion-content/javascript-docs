---
layout: post
title: appearance-and-styling
description: appearance and styling
platform: js
control: TreeView
documentation: ug
---

# Appearance and Styling

## Css Class

Sets the root class for **TreeView** theme. This **cssClass****API** helps you to use custom skinning option for **TreeView** control. By defining the root class using this API, you can include this root class in **CSS**.

The following steps explain enabling the **cssClass** property for **TreeView**.

* In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView**.

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



{% endhighlight %}



**[View]**

**\\ To configure TreeView in the CSHTML page.**

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



                }).**CssClass("customCss")**



**[ASPX]**

**\\Configure TreeView in the aspx page.**

    &lt;ej:TreeView ID="treeview" runat="server" CssClass="customCss"&gt;

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



* Define **CSS** class for customizing the **TreeView.**

****

{% highlight css %}

**[CSS]**
    .customCss .e-treeview {
        background-color: #E0E0E0;
        /* Old browsers */
        color: white;
        border: 1px solid transparent;
        border-image: initial;
    }



{% endhighlight %}



* Add the **cssClass** property to **TreeView**.



{% highlight js %}

    $("#treeView").ejTreeView({ cssClass: "customCss" });



{% endhighlight %}



The following screenshot displays the **TreeView** component, configured based on CSS class.



![](appearance-and-styling_images\appearance-and-styling_img1.png)

_Figure_ _26__59__: TreeView_ _based on CSS class_

## Adjusting TreeView Size

You can **adjust** the **TreeView** size, height and width, by using the properties **width** and **height.**

### Height

You can customize the **Height** of the **TreeView** control by using the **height** property.

The following steps explain how to use the **height** property of **TreeVie**w.

* In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**

****

<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;        &lt;li class="expanded"&gt;            Favorites            &lt;ul&gt;                <li>Desktop</li>                <li>Downloads</li>                <li>Recent places</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li class="expanded"&gt;            Libraries            &lt;ul&gt;                &lt;li&gt;                    Documents                    &lt;ul&gt;                        <li>My Documents</li>                        <li>Public Documents</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Pictures                    &lt;ul&gt;                        <li>My Pictures</li>                        <li>Public Pictures</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Music                    &lt;ul&gt;                        <li>My Music</li>                        <li>Public Music</li>                    &lt;/ul&gt;                &lt;/li&gt;                <li>Subversion</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;            Computer            &lt;ul&gt;                <li>Folder(C)&lt;/li&gt;                <li>Folder(D)&lt;/li&gt;                <li>Folder(F)&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;</td></tr>
<tr>
<td>
            <b>[JavaScript]</b><b>// Set height property for TreeView control as follows.</b>            $("#treeView").ejTreeView({ <b>height</b>: "75px" });</td></tr>
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



            }).**Height("75px")**





**[ASPX]**

**\\Configure TreeView in the aspx page.**

   &lt;ej:TreeView ID="treeview" runat="server" Height="300px"&gt;

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



The following screenshot displays the appearance of **height** of the **TreeView** component.

![](appearance-and-styling_images\appearance-and-styling_img2.png)











![](appearance-and-styling_images\appearance-and-styling_img3.png)

_Figure_ _60__27__: TreeView with height property_

### Width

You can customize the **width** of the **TreeView** control by using the **width** property. By specifying the **width** property, you can change the **width** value in the document.

The following steps explain how to use the **width** property for **TreeView**.

* In the **HTML** page, add **&lt;ul&gt;** and **&lt;li&gt;** elements to configure **TreeView.**



<table>
<tr>
<td>
<b>[HTML]</b>&lt;ul id="treeView"&gt;        &lt;li class="expanded"&gt;            Favorites            &lt;ul&gt;                <li>Desktop</li>                <li>Downloads</li>                <li>Recent places</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li class="expanded"&gt;            Libraries            &lt;ul&gt;                &lt;li&gt;                    Documents                    &lt;ul&gt;                        <li>My Documents</li>                        <li>Public Documents</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Pictures                    &lt;ul&gt;                        <li>My Pictures</li>                        <li>Public Pictures</li>                    &lt;/ul&gt;                &lt;/li&gt;                &lt;li&gt;                    Music                    &lt;ul&gt;                        <li>My Music</li>                        <li>Public Music</li>                    &lt;/ul&gt;                &lt;/li&gt;                <li>Subversion</li>            &lt;/ul&gt;        &lt;/li&gt;        &lt;li&gt;            Computer            &lt;ul&gt;                <li>Folder(C)&lt;/li&gt;                <li>Folder(D)&lt;/li&gt;                <li>Folder(F)&lt;/li&gt;            &lt;/ul&gt;        &lt;/li&gt;    &lt;/ul&gt;</td></tr>
<tr>
<td>
          <b>[JavaScript]</b><b>// Setting width property for TreeView control as follows.</b>          $("#treeView").ejTreeView({ <b>width</b>: 300 });</td></tr>
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



                }).**Width("300px")**





**[ASPX]**

**\\Configure TreeView in the aspx page.**

    &lt;ej:TreeView ID="treeview" runat="server" Width="400px" &gt;

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



The following screenshot displays the appearance of width of the **TreeView** component.



![](appearance-and-styling_images\appearance-and-styling_img4.png)



























![](appearance-and-styling_images\appearance-and-styling_img5.png)

_Figure_ _28__61__: TreeView with width_ _property_

