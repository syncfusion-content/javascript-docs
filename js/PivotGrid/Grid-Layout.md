---
layout: post
title: Grid-Layout
description: Layouts
platform: js
control: PivotGrid
documentation: ug
---

# Layouts

> **Note:** This feature is applicable only for OLAP datasource.

The four kinds of [Layouts](/js/api/ejPivotGrid#members:layout) supported by the **PivotGrid** are as follows:

 * Normal
 * Excel-like
 * Normal top summary
 * No summaries

##Normal

The **Normal** layout is the default Layout of the **PivotGrid** where the summary cells are positioned at the bottom of each parent member and child members appear next to their parent.

{% include image.html url="/js/PivotGrid/Grid-Layout_images/Grid-Layout_img1.png" %}

{% highlight js %}

$("#PivotGrid1").ejPivotGrid({ url: "../wcf/PivotGridService.svc",
layout: ej.PivotGrid.Layout.Normal });

{% endhighlight %}

##Excel-like Layout

In the **Excel-like** layout, the summary cells are positioned at the bottom of the **Grid** and the child members appear under their parent member with a small indent.

{% include image.html url="/js/PivotGrid/Grid-Layout_images/Grid-Layout_img2.png" %}

{% highlight js %}

$("#PivotGrid1").ejPivotGrid({ url: "../wcf/PivotGridService.svc",
layout: ej.PivotGrid.Layout.ExcelLikeLayout });


{% endhighlight %}

##Normal Top Summary

In the **Normal Top Summary** Layout, the summary cells are positioned at the top of each parent member and the child member appears next to their parent.

{% include image.html url="/js/PivotGrid/Grid-Layout_images/Grid-Layout_img3.png" %}

{% highlight js %}

$("#PivotGrid1").ejPivotGrid({ url: "../wcf/PivotGridService.svc", 
layout: ej.PivotGrid.Layout.NormalTopSummary });


{% endhighlight %}

##No Summaries

In **No Summaries** Layout, the summary cells are hidden and the child members appear next to their parent member.

{% include image.html url="/js/PivotGrid/Grid-Layout_images/Grid-Layout_img4.png" %}

{% highlight js %}

$("#PivotGrid1").ejPivotGrid({
    url: "../wcf/PivotGridService.svc",
    layout: ej.PivotGrid.Layout.NoSummaries
});

{% endhighlight %}

