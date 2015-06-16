---
layout: post
title: Checkbox-Support
description: checkbox support
platform: js
control: TreeView
documentation: ug
---

# Checkbox Support

**TreeView** allows you to check or uncheck the nodes. When you check the parent node of **TreeView**, the corresponding child nodes are automatically moved to checked state. A parent node check state is automatically set to indeterminate when it has checked and unchecked child nodes. To enable this feature, set the **showCheckbox** property to **“true”.**

The following steps explain how you can enable the **showCheckbox** property for **TreeView**.

1. In the HTML page, add &lt;ul&gt; and &lt;li&gt; elements to configure **TreeView**.

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

{% highlight js %}

[JavaScript]

// Enable showCheckbox for TreeView control as follows.
<script type="text/javascript">
    $("#treeView").ejTreeView({showCheckbox: true });
</script>

{% endhighlight %}


The following image is the output for TreeView when showCheckbox is set to “True”.

{% include image.html url="/js/TreeView/Concepts-and-Features/Checkbox-Support_images/Checkbox-Support_img1.png" Caption="TreeView with checkbox"%}

### Auto Check Parent Node

To overcome the default functionality of **TreeView**, when you don’t want the parent node check state being moved to indeterminate state and when you check the corresponding child node, you can enable the property **autoCheckParentNode**. By using this functionality, you can check the single parent node as well as the corresponding child nodes. You can specify the property **autoCheckParentNode** in **TreeView** as follows.

{% highlight js %}

**[JavaScript]**
<script type="text/javascript">
    $("#treeView").ejTreeView({ **autoCheckParentNode**: false,showCheckbox: true});
</script>

{% endhighlight %}

### Checked Nodes

You can specify the **Checked Nodes** in **TreeView** initially by using the property **checkedNodes**. **Checked Nodes** index collection is given to the integer array. You can specify the property **checkedNodes** in **TreeView** control in the script as follows.

{% highlight js %}

**[JavaScript]**
<script type="text/javascript">
    $("#treeView").ejTreeView({ showCheckbox: true, **checkedNodes**: [1, 2] });
</script>

{% endhighlight %}



