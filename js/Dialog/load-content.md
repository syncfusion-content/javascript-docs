---
layout: post
title: Content Loading in Dialog widget for Essential JS
description: How to load content to dialog widget either using the Ajax, iframe, and Image.
platform: js
control: Dialog
documentation: ug
keywords : ejdialog, js dialog, jquery dialog, dialog, dialog ui, web dialog, ej dialog, essential javascript dialog, dialog widget,
api: /api/js/ejdialog
---

# Load content

BY default, the content inside the Dialog element is considered as the content for the Dialog widget. 

Also, we can render the Dialog widget content through the following ways.

1. request through AJAX

2. request iframe content

3. request image content

This settings can be specified through [contentType](https://help.syncfusion.com/api/js/ejdialog#members:contenttype) property. 

{% highlight javascript %}

            $("#dialog").ejDialog({
                title: "Dialog",
               //create a HTML file (dialogContent.html) which contains the content for the dialog                        
                contentUrl: "dialogContent.html",
                contentType: "ajax"
            });



{% endhighlight %}



Here below the content of that HTML file.

{% highlight html %}

    <div id="content">
        This content is loaded via AJAX request.
    </div>


{% endhighlight %}



![Load content](load-content_images\load-content_img1.png)

We can handle the AJAX request’s success and failures through the events [ajaxSuccess](https://help.syncfusion.com/api/js/ejdialog#events:ajaxsuccess) and [ajaxError](https://help.syncfusion.com/api/js/ejdialog#events:ajaxerror) events respectively. See also ajaxSuccess and ajaxError

The previous example is modified as below to handle the success and failure events.

{% highlight javascript %}

            $("#dialog").ejDialog({
                title: "Dialog",
               //create a HTML file (dialogContent.html) which contains the content for the dialog                        
                contentUrl: "dialogContent.html",
                contentType: "ajax",
                ajaxSuccess: "onSuccess",
                ajaxError:"onError"
            });

        function onSuccess(args) {
            //handle success event
        }
        function onError(args) {
            //handle success event
        }

{% endhighlight %}



N>The same way we can render the iframe and image content for the Dialog widget by specifying the [contentType](https://help.syncfusion.com/api/js/ejdialog#members:contenttype) as “iframe” and “image” respectively and also by specifying the proper location in the [contentUrl](https://help.syncfusion.com/api/js/ejdialog#members:contenturl) property.  If you wish to dynamically change the dialog content, you can set the [`contentUrl`](https://help.syncfusion.com/api/js/ejdialog#members:contenturl) and the [`contentType`](https://help.syncfusion.com/api/js/ejdialog#members:contenttype) property through setModel on any action.