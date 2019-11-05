---
layout: post
title:  Frozen Header with PivotGrid widget for Syncfusion Essential JS
description:  This document illustrates that how to enable frozen header feature and its options in JavaScript PivotGrid control
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Frozen header

Allows you to freeze the header of the grid. so, it will be always visible while scrolling the content with large number of rows or columns providing a precise view by this [`enableFrozenHeaders`](/api/js/ejpivotgrid#members:frozenheadersettings-enablefrozenheaders) property under the [`frozenHeaderSettings`](/api/js/ejpivotgrid#members:frozenheadersettings).

{% highlight html %}

<div id="PivotGrid1"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //...
            frozenHeaderSettings : {enableFrozenHeaders : true}
        });
    });
</script>

{% endhighlight %}

![Frozen header, aka Freeze headers support in JavaScript pivot grid control](FrozenHeader_images/row_col_freeze.png)

You can also freeze the row/column headers individually by setting [`enableFrozenRowHeaders`](/api/js/ejpivotgrid#members:frozenheadersettings-enablefrozenrowheaders)/[`enableFrozenColumnHeaders`](/api/js/ejpivotgrid#members:frozenheadersettings-enablefrozencolumnheaders) properties under the [`frozenHeaderSettings`](/api/js/ejpivotgrid#members:frozenheadersettings).

{% highlight html %}

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //...
            frozenHeaderSettings : {
                enableFrozenRowHeaders : true      //To Freeze the Row headers only
            }
        });
    });
</script>

{% endhighlight %}

![Frozen row headers in JavaScript pivot grid control](FrozenHeader_images/row_freeze.png)

{% highlight html %}

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //...
            frozenHeaderSettings : {
                enableFrozenColumnHeaders : true  //To Freeze the Column headers only
            }
        });
    });
</script>

{% endhighlight %}

![Frozen column headers in JavaScript pivot grid control](FrozenHeader_images/col_freeze.png)

You can also set the size of the scroller (horizontal and vertical) in the pivot grid by using the [`scrollerSize`](../api/ejpivotgrid#members:frozenheadersettings-scrollersize) property under the [`frozenHeaderSettings`](../api/ejpivotgrid#members:frozenheadersettings).

{% highlight html %}

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //...
            frozenHeaderSettings : {
                scrollerSize : 18
            }
        });
    });
</script>

{% endhighlight %}

![Scroller size in JavaScript pivot grid control](FrozenHeader_images/scroll_size.png)