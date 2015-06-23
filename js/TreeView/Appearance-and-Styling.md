---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: TreeView
documentation: ug
---

# Appearance and Styling

## Css Class

Sets the root class for **TreeView** theme. This **cssClass** **API** helps you to use custom skinning option for **TreeView** control. By defining the root class using this API, you can include this root class in **CSS**.

The following steps explain enabling the **cssClass** property for **TreeView**.

In the **HTML** page, add &lt;ul&gt; and &lt;li&gt; elements to configure TreeView.

{% highlight html %}

<ul id="treeView">
    <li class="expanded">Favorites
            <ul>

                <li>Desktop</li>
                <li>Downloads</li>
                <li>Recent places</li>
            </ul>
    </li>
    <li class="expanded">Libraries
            <ul>
                <li>Documents
                    <ul>
                        <li>My Documents</li>
                        <li>Public Documents</li>
                    </ul>
                </li>
                <li>Pictures
                    <ul>
                        <li>My Pictures</li>
                        <li>Public Pictures</li>
                    </ul>
                </li>
                <li>Music
                    <ul>
                        <li>My Music</li>
                        <li>Public Music</li>
                    </ul>
                </li>
                <li>Subversion</li>
            </ul>
    </li>
    <li>Computer
            <ul>
                <li>Folder(C)</li>
                <li>Folder(D)</li>
                <li>Folder(F)</li>
            </ul>
    </li>
</ul>

{% endhighlight %}



Define CSS class for customizing the TreeView.

{% highlight css %}

<style>
    .customCss .e-treeview {
        background-color: #E0E0E0;
        /* Old browsers */
        color: white;
        border: 1px solid transparent;
        border-image: initial;
    }
</style>

{% endhighlight %}



Add the **cssClass** property to TreeView.

{% highlight js %}

    $("#treeView").ejTreeView({ cssClass: "customCss" });

{% endhighlight %}



The following screenshot displays the **TreeView** component, configured based on CSS class.

{% include image.html url="/js/TreeView/Appearance-and-Styling_images/Appearance-and-Styling_img1.png"%}

## Adjusting TreeView Size

You can **adjust** the **TreeView** size, height and width, by using the properties **width** and **height.**

### Height

You can customize the **Height** of the **TreeView** control by using the **height** property.

The following steps explain how to use the **height** property of **TreeVie**w.

In the **HTML** page, add &lt;ul&gt; and &lt;li&gt; elements to configure TreeView.

{% highlight html %}

<ul id="treeView">
    <li class="expanded">Favorites
        <ul>

            <li>Desktop</li>
            <li>Downloads</li>
            <li>Recent places</li>
        </ul>
    </li>
    <li class="expanded">Libraries
        <ul>
            <li>Documents
                <ul>
                    <li>My Documents</li>
                    <li>Public Documents</li>
                </ul>
            </li>
            <li>Pictures
                <ul>
                    <li>My Pictures</li>
                    <li>Public Pictures</li>
                </ul>
            </li>
            <li>Music
                <ul>
                    <li>My Music</li>
                    <li>Public Music</li>
                </ul>
            </li>
            <li>Subversion</li>
        </ul>
    </li>
    <li>Computer
        <ul>
            <li>Folder(C)</li>
            <li>Folder(D)</li>
            <li>Folder(F)</li>
        </ul>
    </li>
</ul>

{% endhighlight %}

{% highlight js %}

    $("#treeView").ejTreeView({ height: "75px" });

{% endhighlight %}

The following screenshot displays the appearance of **height** of the **TreeView** component.

{% include image.html url="/js/TreeView/Appearance-and-Styling_images/Appearance-and-Styling_img2.png"%}

### Width

You can customize the **width** of the **TreeView** control by using the **width** property. By specifying the **width** property, you can change the **width** value in the document.

The following steps explain how to use the **width** property for **TreeView**.

In the **HTML** page, add &lt;ul&gt; and &lt;li&gt; elements to configure TreeView.

{% highlight html %}

<ul id="treeView">
    <li class="expanded">Favorites
            <ul>

                <li>Desktop</li>
                <li>Downloads</li>
                <li>Recent places</li>
            </ul>
    </li>
    <li class="expanded">Libraries
            <ul>
                <li>Documents
                    <ul>
                        <li>My Documents</li>
                        <li>Public Documents</li>
                    </ul>
                </li>
                <li>Pictures
                    <ul>
                        <li>My Pictures</li>
                        <li>Public Pictures</li>
                    </ul>
                </li>
                <li>Music
                    <ul>
                        <li>My Music</li>
                        <li>Public Music</li>
                    </ul>
                </li>
                <li>Subversion</li>
            </ul>
    </li>
    <li>Computer
            <ul>
                <li>Folder(C)</li>
                <li>Folder(D)</li>
                <li>Folder(F)</li>
            </ul>
    </li>
</ul>

{% endhighlight %}

{% highlight js %}

    $("#treeView").ejTreeView({ width: 300 });

{% endhighlight %}


The following screenshot displays the appearance of width of the **TreeView** component.

{% include image.html url="/js/TreeView/Appearance-and-Styling_images/Appearance-and-Styling_img3.png"%}

