---
layout: post
title:  Column Resizing
description: column resizing
platform: js
control: PivotGrid
documentation: ug
---

# Column Resizing

Allows you to resize the column by changing its width while holding and dragging the column border using the mouse.

You can enable column resizing option in PivotGrid by setting the [`enableColumnResizing`](/js/api/ejpivotgrid#members:enablecolumnresizing) property to true.

{% highlight html %}

<div id="PivotGrid1"></div>

<script>
    $(function() {    
        $("#PivotGrid1").ejPivotGrid({
            //...
            enableColumnResizing : true
        });
    });
</script>

{% endhighlight %} 

![](Column-Resizing_images/columnresizing.png)