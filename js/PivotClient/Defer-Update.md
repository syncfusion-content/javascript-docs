---
layout: post
title: Defer-Update with PivotClient widget for Syncfusion Essential JS
description: defer update
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Defer Update

I> This feature is applicable only for OLAP data source bound from server-side.

Defer Update support allows the user to refresh the control on-demand and not during every user interaction. To enable this functionality, set the [`enableDeferUpdate`](/api/js/ejpivotclient#members:enabledeferupdate) property to true. By default, the value is set to false.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        url: "/OlapService",
        enableDeferUpdate: true
    });

{% endhighlight %}

After enabling this property, an icon for Defer Update will appear inside the toolbar.

![Defer update in JavaScript pivot client control](Defer-Update_images/Before-defer-update.png)

On clicking the icon, after making the necessary UI interactions, the PivotGrid and PivotChart controls will be updated according to the OlapReport available at that instant.

![Defer update view in JavaScript pivot client control](Defer-Update_images/after-defer-update.png)

