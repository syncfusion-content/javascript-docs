---
layout: post
title: Grid-Layout
description: Layouts
platform: js
control: PivotGrid
documentation: ug
---

# Grid Layout

I> This feature is applicable only for OLAP datasource only at Server Mode.

## Normal Layout

A layout in which summary cells are positioned at the bottom of each parent member and their child members appear next to them. Normal layout is the default layout in PivotGrid control. The enumeration property [`layout`](/api/js/ejpivotgrid#members:layout) needs to be set to **"ej.PivotGrid.Layout.Normal"** in-order to view PivotGrid in normal layout. 

{% highlight js %}
	$("#PivotGrid1").ejPivotGrid({
      url: "/OLAPService",
     layout: ej.PivotGrid.Layout.Normal
}); 

{% endhighlight %}

![](Grid-Layout_images/layout-normal.png)

## No Summaries Layout
A layout in which summary cells are completely hidden and the child members appear next to their parent member.  The enumeration property [`layout`](/api/js/ejpivotgrid#members:layout) needs to be set to **"ej.PivotGrid.Layout.NoSummaries"** in-order to view PivotGrid without summaries.

{% highlight js %}

$("#PivotGrid1").ejPivotGrid({
      url: "/OLAPService",
     layout: ej.PivotGrid.Layout.NoSummaries
});

{% endhighlight %}
 
![](Grid-Layout_images/layout-nosummary.png)

## Excel-like Layout
A layout in which summary cells are positioned besides each parent member and their child members appear next to them. The enumeration property [`layout`](/api/js/ejpivotgrid#members:layout) needs to be set to **"ej.PivotGrid.Layout.ExcelLikeLayout"** in-order to view PivotGrid in excel-like layout.

{% highlight js %}

$("#PivotGrid1").ejPivotGrid({
    url: "/OLAPService",
    layout: ej.PivotGrid.Layout.ExcelLikeLayout
});

{% endhighlight %}

![](Grid-Layout_images/layout-excel.png)

## Top Summary Layout
A layout in which summary cells are positioned at the top of each parent member and their child members appear next to them. The enumeration property [`layout`](/api/js/ejpivotgrid#members:layout) needs to be set to **"ej.PivotGrid.Layout.NormalTopSummary"** in-order to view PivotGrid in top summaries layout.

{% highlight js %}

$("#PivotGrid1").ejPivotGrid({
     url: "/OLAPService",
     layout: ej.PivotGrid.Layout.NormalTopSummary
});

{% endhighlight %}

![](Grid-Layout_images/layout-top.png)

