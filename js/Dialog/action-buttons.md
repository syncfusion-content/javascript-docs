---
layout: post
title: action-buttons
description: action buttons
platform: js
control: Dialog
documentation: ug
---

## Action Buttons

The Dialog widget provides the following action buttons.

1. Close

2. Maximize

3. Minimize

4. Pin/Unpin

5. Collapse/Expand

You can display only the necessary buttons in the Dialog widget by configuring the actionButtons property.

{% highlight html %}



           //create dialog widget
            $("#dialog").ejDialog({
                showOnInit: false,
                actionButtons: ["close", "maximize", "minimize"]
            });



{% endhighlight %}



![Alt text](Action-Buttons_Images\action-buttons_img1.png)

