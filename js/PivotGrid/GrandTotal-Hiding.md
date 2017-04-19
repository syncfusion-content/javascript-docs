---
layout: post
title:  GrandTotal Hiding
description: GrandTotal Hiding
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Grand Total Hiding

Grand Total Hiding can be classified into three categories.

* Row Grand Total Hiding
* Column Grand Total Hiding
* Both

## Row Grand Total Hiding

You can hide the **Grand Total** in row alone by setting the property [`enableRowGrandTotal`](/api/js/ejpivotgrid#members:enablerowgrandtotal) to `false`

{% highlight html %}

<script>
    $(function() {    
        $("#PivotGrid1").ejPivotGrid({
        //...
        enableRowGrandTotal: false
        });
    });
</script>

{% endhighlight %}

![](GrandTotal-Hiding_images/enableRowGrandTotal.png)

## Column Grand Total Hiding

You can hide the **Grand Total** in column alone by setting the property [`enableColumnGrandTotal`](/api/js/ejpivotgrid#members:enablecolumngrandtotal) to `false`


{% highlight html %}

<div id="PivotGrid1"></div>
<script>
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //...
            enableColumnGrandTotal: false
        });
    });
</script>

{% endhighlight %}

![](GrandTotal-Hiding_images/enableColumnGrandTotal.png)

## Both

You can hide the **Grand Total** in both row and column by setting the property [`enableGrandTotal`](/api/js/ejpivotgrid#members:enablegrandtotal) to `false`

{% highlight html %}

<div id="PivotGrid1"></div>

<script>
    $(function() {            
        $("#PivotGrid1").ejPivotGrid({
            //...
            enableGrandTotal: false
        });
    });
</script>

{% endhighlight %}

![](GrandTotal-Hiding_images/enableGrandTotal.png)