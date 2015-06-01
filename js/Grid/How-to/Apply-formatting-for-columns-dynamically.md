---
layout: post
title: Apply-formatting-for-columns-dynamically
description: apply formatting for columns dynamically
platform: js
control: Grid
documentation: ug
---

### Apply formatting for columns dynamically

Column format can be used dynamically to change data values format with the help of the public method. The following code example illustrates the **Essential JavaScript** with column formatting in public method.

{% highlight html %}

var grid = $("#Grid").data("ejGrid");
var column = grid.getColumnByField("fieldName");
column.format = **"{0:n2**}";
grid.refreshContent(true);


{% endhighlight %}



