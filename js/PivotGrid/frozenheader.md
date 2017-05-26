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

Allows you to freeze the header of the Grid so that it will be always visible when scrolling the content with a large number of rows or columns providing a precise view.

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

We can also freeze the row/column headers individually by setting the below properties.

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

We can also set the size of the scroller (horizontal and vertical) in PivotGrid by using below property.

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