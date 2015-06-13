---
layout: post
title: Synchronous-Upload
description: synchronous upload 
platform: js
control: Uploadbox
documentation: ug
---

# Synchronous Upload 

This features allow you to upload and remove the files **synchronously**. To achieve this, set the **asyncUpload** property to ‘**false**’. The data type is **Boolean.**

> _**Note: By default, Uploadbox widget works with asynchronous upload option only.**_



The following steps guide you in uploading the file **synchronously**.

* In the **HTML** page, create a form with action and post method and then add the **&lt;div&gt;** element into the form to configure the **Uploadbox** element.

{% highlight html %}

**[HTML]**

      <div class="control">
        <form id="upload" method="post" action="saveFiles.ashx">
            <div id="Uploadbox"></div>
            <input type="submit" value="submit" />
        </form> 
    </div>

{% endhighlight %}

{% highlight js %}

**[JavaScript]**  

// Initialize the control in JavaScript.

   <script type="text/javascript">
        $(function () {
//Declaration.
            $("#Uploadbox").ejUploadbox({
                asyncUpload: false
            });
        });
    </script>


{% endhighlight %}

* For **JS**, configure **saveFiles.ashx** and **removeFiles.ashx** files as mentioned in the Save file action and Remove file action respectively. 

Once the form is submitted by using **submit** button, it triggers the **saveFiles.ashx** handler. In the handler, save the files as usual.

The following screenshot displays the output.



{% include image.html url="/js/UploadBox/Concepts-and-features/Synchronous-Upload_images/Synchronous-Upload_img1.png" Caption="Uploadbox with synchronous option"%}

