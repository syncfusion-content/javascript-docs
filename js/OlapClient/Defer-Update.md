---
layout: post
title: Defer-Update
description: defer update
platform: js
control: OLAPClient
documentation: ug
---

# Defer Update

Defer Update support will allow user to refresh the control only on-demand and not during every UI interaction.  To enable this functionality set the `enableDeferUpdate` property to "true".

The following code example explains on how to enable Defer Update in the OlapClient control.

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

{% include image.html url="/js/OlapClient/Defer-Update_images/Defer-Update_images1.png" Caption="Before Defer Update"%}

{% include image.html url="/js/OlapClient/Defer-Update_images/Defer-Update_images2.png" Caption="After Defer Update"%}




