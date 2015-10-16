---
layout: post
title: Initialize-ejGrid
description: initialize ejgrid
platform: js
control: Grid
documentation: ug
---

### Initialize ejGrid

In this section, you can learn about **Grid’s** mandatory property to render a simple **Grid**. To initialize **Grid**, it needs two important properties. They are columns and its inner property field. [`columns`](/js/api/ejgrid#members:columns "columns") are used to define schema of **Grid** and [`field`](/js/api/ejgrid#members:columns-field "field") is mapping a name to the data source.

{% highlight js %}

$("#Grid").ejGrid({
     columns: [
        { field: "OrderID" },
        { field: "CustomerID" },
        { field: "EmployeeID" }
     ]
});


{% endhighlight %}



The following output is displayed as a result of the above code example.

![](/js/Grid/How-to/Initialize-ejGrid_images/Initialize-ejGrid_img1.png)

