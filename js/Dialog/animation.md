---
layout: post
title: Animation in Dialog widget for Essential JS
description: How to apply animation effects.
platform: js
control: Dialog
documentation: ug
keywords : ejdialog, js dialog, jquery dialog, dialog, dialog ui, web dialog, ej dialog, essential javascript dialog, dialog widget,
api: /api/js/ejdialog
---

# Animation

The Dialog widget can be animated by using [enableAnimation](https://help.syncfusion.com/api/js/ejdialog#members:enableanimation) property while opening and closing the dialog.

We can specify the effect and the duration for the [animation](https://help.syncfusion.com/api/js/ejdialog#members:animation). There are two types of effects. They are slide and fade. We can configure these settings separately for open and close dialog actions.

{% highlight javascript %}

            //create dialog widget
            $("#dialog").ejDialog({
                showOnInit: false,
                actionButtons: ["close", "maximize", "minimize", "collapsible"],
                enableAnimation: true,
                animation: {
                    //animation settings while opening the dialog
                    show: {
                        effect: "slide",
                        duration: 500
                    },
                    //animation settings while closing the dialog
                    hide: {
                        effect: "fade",
                        duration: 500
                    }
                }
            });

{% endhighlight %}

![Animation](animation_images\animation_img1.png)

