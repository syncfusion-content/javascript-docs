---
layout: post
title:  Frozen Header
description:  frozen header
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Frozen Header

Allows you to freeze the header of the grid. so, it will be always visible while scrolling the content with large number of rows or columns providing a precise view by this [`enableFrozenHeaders`](../api/ejpivotgrid#members:frozenheadersettings-enablefrozenheaders) property under the [`frozenheadersettings`](../api/ejpivotgrid#members:frozenheadersettings).

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

![](FrozenHeader_images/row_col_freeze.png)

You can also freeze the row/column headers individually by setting these properties [`enableFrozenRowHeaders`](../api/ejpivotgrid#members:frozenheadersettings-enablefrozenrowheaders)/[`enableFrozenColumnHeaders`](../api/ejpivotgrid#members:frozenheadersettings-enableFrozenColumnHeaders) under the [`frozenheadersettings`](../api/ejpivotgrid#members:frozenheadersettings).

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

![](FrozenHeader_images/row_freeze.png)

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

![](FrozenHeader_images/col_freeze.png)

You can also set the size of the scroller (horizontal and vertical) in the PivotGrid by using the [`scrollerSize`](../api/ejpivotgrid#members:frozenheadersettings-scrollersize) property under the [`frozenheadersettings`](../api/ejpivotgrid#members:frozenheadersettings).

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

![](FrozenHeader_images/scroll_size.png)