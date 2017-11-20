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

## Column Width Based on Size

The property [`enableColumnResizing`](/api/js/ejpivotgrid#members:enablecolumnresizing) adjusts the width of each column based on size of the widget.

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


## Column Width Based on Text

The property [`resizeColumnsToFit`](/api/js/ejpivotgrid#members:resizecolumnstofit) automatically adjusts the width of each column based on the maximum content length available in the respective column.

{% highlight html %}

<div id="PivotGrid1"></div>

<script>
    $(function() {    
        $("#PivotGrid1").ejPivotGrid({
            //...
            resizeColumnsToFit: true
        });
    });
</script>

![](Column-Resizing_images/columnresizing.png)

{% endhighlight %} 