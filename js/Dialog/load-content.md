---
layout: post
title: Load-Content
description: load content
platform: js
control: Dialog
documentation: ug
---

# Load content

BY default, the content inside the Dialog element is considered as the content for the Dialog widget. 

Also, we can render the Dialog widget content through the following ways.

1. request through Ajax

2. request iframe content

3. request image content

This settings can be specified through “contentType” property. 

{% highlight js %}

            $("#dialog").ejDialog({
                title: "Dialog",
               //create a html file (dialogcontent.html) which contains the content for the dialog                        
                contentUrl: "dialogcontent.html",
                contentType: "ajax"
            });



{% endhighlight %}



dialogcontent.html

{% highlight html %}

    <div id="content">
        This content is loaded via AJAX request.
    </div>


{% endhighlight %}



![Load content](load-content_images\load-content_img1.png)

We can handle the AJAX request’s success and failures through the events “ajaxSuccess” and “ajaxError” events respectively. See also ajaxSuccess and ajaxError

The previous example is modified as below to handle the success and failure events.

{% highlight js %}

            $("#dialog").ejDialog({
                title: "Dialog",
               //create a html file (dialogcontent.html) which contains the content for the dialog                        
                contentUrl: "dialogcontent.html",
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



N>The same way we can render the iframe and image content for the Dialog widget by specifying the “__contentType__” as “iframe” and “image” respectively and also by specifying the proper location in the "__contentUrl__" property.

