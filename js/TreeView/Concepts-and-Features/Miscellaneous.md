---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: TreeView
documentation: ug
---

# Miscellaneous

## Enabled

You can enable or disable the **TreeView** control by using the property **enabled**. You can enable the **TreeView** control by setting the property **enabled** to “**true**” and you can specify the property **enabled** in the script as follows.

{% highlight js %}

<script>
    // Initialize the TreeView with the enabled value specified.
    $("#treeView").ejTreeView({ **enabled**: true });
</script>


{% endhighlight %}

## Expanded Nodes

You can specify the **expanded****node** level in **TreeView** by using the property **expandedNodes**. **Expanded****nodes** index collection is given to integer array. Add the following code in your script section.

{% highlight js %}

<script>
    // Initialize the TreeView with the expandedNodes value specified.
    $("#treeView").ejTreeView({ **expandedNodes**: [0, 7] });
</script>


{% endhighlight %}

### Expand On

**Node** can be expanded for specified events. You can specify the property **expandOn** in **TreeView** control in the script as follows.

{% highlight js %}

<script>
    //Initialize the TreeView with the expandOn value specified
    $("#treeView").ejTreeView({ **expandOn**: 'dblclick' });
</script>


{% endhighlight %}



