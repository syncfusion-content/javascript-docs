---
layout: post
title: Defer-Update
description: defer update
platform: js
control: OLAPClient
documentation: ug
---

# Defer Update

Defer Update support allows you to refresh the control only on-demand and not during every UI interaction.  To enable this functionality set the `enableDeferUpdate` property to "True".

The following code example explains how you can enable Defer Update in the OlapClient control.

{% highlight js %}

$(function()
{
    $("#OlapClient").ejOlapClient(
    {
        url: "../wcf/OlapClientService.svc",
        enableDeferUpdate: true,
        title: "OLAP Browser"
    });
});

{% endhighlight %}

![]("/js/OlapClient/Defer-Update_images/Defer-Update_images1.png" Caption="Before Defer Update")

![]("/js/OlapClient/Defer-Update_images/Defer-Update_images2.png" Caption="After Defer Update")




