---
layout: post
title: Action Buttons in Dialog widget for Essential JS
description: How to enable the Interaction button like “Close”, “Minimize” and etc., in Dialog Widget. 
platform: js
control: Dialog
documentation: ug
keywords : ejdialog, js dialog, jquery dialog, dialog, dialog ui, web dialog, ej dialog, essential javascript dialog, dialog widget,
api: /api/js/ejdialog
---

# Action Buttons

The Dialog widget provides the following action buttons.

1. Close

2. Maximize

3. Minimize

4. Pin/Unpin

5. Collapse/Expand

You can display only the necessary buttons in the Dialog widget by configuring the [actionButtons](https://help.syncfusion.com/api/js/ejdialog#members:actionbuttons) property.

{% highlight javascript %}

           //create dialog widget
            $("#dialog").ejDialog({
                showOnInit: false,
                actionButtons: ["close", "maximize", "minimize"]
            });

{% endhighlight %}



![Action Buttons](action-buttons_images\action-buttons_img1.png)


## Customizing Action Buttons

We can customize the action buttons in dialog widget.

You can add new action button in the dialog widget by configuring the [actionButtonClick](https://help.syncfusion.com/api/js/ejdialog#events:actionbuttonclick) event.

{% highlight javascript %}

           //create dialog widget
            $("#dialog").ejDialog({
                showOnInit: false,
                actionButtons: ["close", "collapsible", "maximize", "minimize", "pin", "mediaplay", "search"],
				actionButtonClick: "playMedia"
            });
            function playMedia(args)
		    {
               console.log(args.buttonID);
            }
{% endhighlight %}



![Action Buttons](action-buttons_images\action-buttons_img2.png)
