---
layout: post
title:  GrandTotal Hiding with PivotGrid widget for Syncfusion Essential JS
description: GrandTotal Hiding
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Grand Total Hiding

Grand total hiding can be classified into three categories.

* Row grand total hiding
* Column grand total hiding
* Both

## Row grand total hiding

You can hide the **Grand Total** in row alone by setting the [`enableRowGrandTotal`](/api/js/ejpivotgrid#members:enablerowgrandtotal) property to `false`.

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

![Hiding row totals in JavaScript pivot grid control](GrandTotal-Hiding_images/enableRowGrandTotal.png)

## Column grand total hiding

You can hide the **Grand Total** in column alone by setting the [`enableColumnGrandTotal`](/api/js/ejpivotgrid#members:enablecolumngrandtotal) property to `false`.


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

![Hiding column totals in JavaScript pivot grid control](GrandTotal-Hiding_images/enableColumnGrandTotal.png)

## Both

You can hide the **Grand Total** in both row and column by setting the [`enableGrandTotal`](/api/js/ejpivotgrid#members:enablegrandtotal) property to `false`.

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

![Hiding totals in JavaScript pivot grid control](GrandTotal-Hiding_images/enableGrandTotal.png)