---
layout: post
title: Toolbar-Customization
description: toolbar customization
platform: js
control: ReportViewer
documentation: ug
---

# Toolbar Customization

The **ReportViewer** has an option to show or hide items in the **toolbar**. To customize the **toolbar** items, use the **ReportViewer’s****ToolbarSettings** property. The **toolbar** template can also be customized by specifying custom template to **ReportViewer****toolbar**.

{% highlight js %}



$("#viewer").ejReportViewer(
                {
                    toolbarSettings: {
                        items: ej.ReportViewer.ToolbarItems.All & ~ej.ReportViewer.ToolbarItems.Parameters
                    }                });


{% endhighlight %}



