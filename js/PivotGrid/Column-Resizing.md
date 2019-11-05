---
layout: post
title:  Column Resizing with PivotGrid widget for Syncfusion Essential JS
description: This document illustrates that how to enable column resizing feature and its customization through API in JavaScript PivotGrid control
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Resizing Column

Allows you to change the column width by holding and dragging the column border using the mouse pointer.

## Column width based on size

The [`enableColumnResizing`](/api/js/ejpivotgrid#members:enablecolumnresizing) property adjusts the width of each column based on size of the widget.

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


## Column width based on text

The [`resizeColumnsToFit`](/api/js/ejpivotgrid#members:resizecolumnstofit) property automatically adjusts the width of each column based on the maximum content length available in the respective column.

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

{% endhighlight %}

![Column resizing in JavaScript pivot grid control](Column-Resizing_images/columnresizing.png)

