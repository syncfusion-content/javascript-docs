---
layout: post
title: Grid-Layout
description: grid layout
platform: js
control: PivotGrid
documentation: ug
---

### Grid Layout

>_**Note: This feature is applicable only for OLAP datasource.**_

**Grid Layouts** customize the position of summary elements in the **PivotGrid** control. Summary elements can be positioned at the top or bottom of each parent member.

The four kinds of Layouts supported by the **PivotGrid** are as follows:

 * Normal

 * Excel-like

 * Normal top summary

 * No summaries

**Normal**

The **Normal** layout is the default Layout of the **PivotGrid** where the summary cells are positioned at the bottom of each parent member and child members appear next to their parent.

{% include image.html url="/js/PivotGrid/Concepts-and-Features/Grid-Layout_images/Grid-Layout_img1.png" Caption="PivotGrid in Normal Layout"%}

<br/>

{% highlight javascript %}

$("#PivotGrid1").ejPivotGrid({ url: "../wcf/PivotGridService.svc",
layout: ej.PivotGrid.Layout.Normal });

{% endhighlight %}


**Excel-like Layout**

In the **Excel-like** layout, the summary cells are positioned at the bottom of the **Grid** and the child members appear under their parent member with a small indent.

{% include image.html url="/js/PivotGrid/Concepts-and-Features/Grid-Layout_images/Grid-Layout_img2.png" Caption="PivotGrid in Excel-Like Layout"%}

<br/>

{% highlight javascript %}

$("#PivotGrid1").ejPivotGrid({ url: "../wcf/PivotGridService.svc",
layout: ej.PivotGrid.Layout.ExcelLikeLayout });


{% endhighlight %}

**Normal Top Summary**

In the **Normal Top Summary** Layout, the summary cells are positioned at the top of each parent member and the child member appears next to their parent.

{% include image.html url="/js/PivotGrid/Concepts-and-Features/Grid-Layout_images/Grid-Layout_img3.png" Caption="PivotGrid in Normal Top Summary Layout"%}

<br/>

{% highlight javascript %}

$("#PivotGrid1").ejPivotGrid({ url: "../wcf/PivotGridService.svc", 
layout: ej.PivotGrid.Layout.NormalTopSummary });


{% endhighlight %}

**No Summaries**

In **No Summaries** Layout, the summary cells are hidden and the child members appear next to their parent member.

{% include image.html url="/js/PivotGrid/Concepts-and-Features/Grid-Layout_images/Grid-Layout_img4.png" Caption="PivotGrid in No Summaries Layout"%}

<br/>

{% highlight javascript %}

$("#PivotGrid1").ejPivotGrid({ url: "../wcf/PivotGridService.svc", 
layout: ej.PivotGrid.Layout.NoSummaries });


{% endhighlight %}

