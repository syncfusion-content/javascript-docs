---
layout: post
title:  Column Resizing
description: column resizing
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Resizing Column

Allows the user to change the column width by holding and dragging the column border using the mouse pointer.

You can enable the resizing option in PivotGrid by setting the [`enableColumnResizing`](/api/js/ejpivotgrid#members:enablecolumnresizing) property to true.

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


Additionally, the property [`resizeColumnsToFit`](/api/js/ejpivotgrid#members:resizecolumnstofit) automatically adjusts the width of each column based on the maximum content length available in the respective column.

{% highlight html %}

<div id="PivotGrid1"></div>

<script>
    $(function() {    
        $("#PivotGrid1").ejPivotGrid({
            //...
            enableColumnResizing : true,
            resizeColumnsToFit: true
        });
    });
</script>

{% endhighlight %} 