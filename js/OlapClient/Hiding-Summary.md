---
layout: post
title: Hiding-Summary
description: hiding summary
platform: js
control: OlapClient
documentation: ug
---

# Hiding Summary

By setting the “GridLayout” property as “NoSummaries”, the summary cells in PivotGrid control is hidden. By default, “Normal” layout is set.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
        url: "/OlapClient",
        title: "OLAP Browser",
        gridLayout: ej.PivotGrid.Layout.NoSummaries
    });
    
{% endhighlight %}

