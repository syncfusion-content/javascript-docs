---
layout: post
title: Getting-Started
description: getting started
platform: js
control: RichTextEditor
documentation: ug
---

# Getting Started

This section briefly describes how to create and use **RichTextEditor** control using **Javascript** in your application. The **Essential JavaScript RichTextEditor (RTE)** control allows easily to edit contents, insert tables, images and to get the **HTML** content. In this section, you can learn how to use **RichTextEditor** for getting Feedback from the user. The following screenshot demonstrates how the **RTE** control is used in Feedback form.

{% include image.html url="/js/RichTextEditor/Getting-Started_images/Getting-Started_img1.png"%}

In the above screenshot , the **RTE** consists of content editable area with feedback title when you click the Post Feedback toolbar item to send the feedback information.

## Create a RichTextEditor

**Essential JavaScript RTE** widget basically renders by using simple text area element. The following steps describe the creation of **RTE** control.  

Create an **HTML** file and add the following template to it for **RTE** creation.

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
      <!-- Style sheet for default theme (flat azure) -->
      <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <!--Scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
      <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!--add rich text element elememt here-->
   </body>
</html>

{% endhighlight %}

 Add text area element within the body element for **RichTextEditor** rendering.

{% highlight html %}

<div>
   <textarea id="feedBackEditor"></textarea>
</div>

{% endhighlight %}

Initialize **RTE** in script.

{% highlight js %}

    $(function () {
        // document ready
        // simple RTE creation
        $("#feedBackEditor").ejRTE();
    });

{% endhighlight %}

The following **RTE** screenshot is the output of above steps.

{% include image.html url="/js/RichTextEditor/Getting-Started_images/Getting-Started_img2.png"%}

## Configure the Toolbar

The **RichTextEditor** is used to configure the toolbar items to provide editing and styling functionality. In this scenario, use the default **RTE** toolbar item to provide feedback form. 

### Add the Toolbar Item

The additional functionality toolbar item is necessary to perform the required operation. The **RTE** provides some additional toolbar items that are already predefined, but not rendered in without specifying the toolbar items. 

The following code example is used to render the additional in-built toolbar items to **RTE** toolbar list.

{% highlight js %}

    $(function() {
       $("#feedBackEditor").ejRTE({
          width: "100%",
          tools: {
             //specify the font type, size, color and background color option for text
             font: ["fontName", "fontSize", "fontColor", "backgroundColor"],
          }
       });
    });

{% endhighlight %}

The following screenshot is the output of above steps:

{% include image.html url="/js/RichTextEditor/Getting-Started_images/Getting-Started_img3.png"%}

### Removing the ToolbarItem

You can remove the particular toolbar item using **remove ToolbarItem** method. 

Consider that the **“create table”** toolbar item is not necessary for the feedback scenario. To easily remove the **“create table”** toolbar item the following code example is used to remove the in-built toolbar items from **RTE** toolbar list.

{% highlight js %}

    var editorObj;
    $(function () {
        $("#feedBackEditor").ejRTE();
        //create the editor object for removing the toolbar item
        editorObj = $("#feedBackEditor").data('ejRTE');
        //remove the create table toolbar item by specifying the create table toolbar id
        editorObj.removeToolbarItem("feedBackEditorcreateTable");
    });

{% endhighlight %}

The following screenshot is the output of above steps:

{% include image.html url="/js/RichTextEditor/Getting-Started_images/Getting-Started_img4.png"%}

## Configure Custom Toolbar item

To post the feedback directly you need additional toolbar item. The **RTE** control provides support to create the custom toolbar item for custom action. The following code example demonstrates the custom **toolbar** item creation in the **RTE** control.

{% highlight js %}
    
    $(function() {
       $("#feedBackEditor").ejRTE({
          tools: {
             customTool: [{
                name: "PostFeedBack", //Id for the newly added tool
                tooltip: "Submit the feedback", // Shows the tooltip for custom tool
                css: "FeedBack",
                action: function() {
                   //when click the custom tool item, the event will triggered                             
                }
             }]
          }
       });
       $("div.FeedBack").html("Post Feedback");
    });

{% endhighlight %}

The following screenshot is the output of above steps:

{% include image.html url="/js/RichTextEditor/Getting-Started_images/Getting-Started_img5.png"%}

## Validate the Content

To send the feedback form without contents you need to validate them before submitting the contents. To achieve this validation use **getText()** method in **RTE** control.

When the content area is empty, you set the notification message displayed in the &lt;div&gt; element area in order to alert the user. The following **HTML** code example is used to create the feedback form editor with support of **RTE** control.

{% highlight html %}

<div class="commentSection">
   <div class="titleSection">
      <label>Title:</label>
      <input type="text" class="input ejinput" />
   </div>
   <!--textarea element section-->
   <textarea id="feedBackEditor" class="hide" rows="10" cols="30"></textarea>
   <!-- validation message display area-->
   <div class="output"></div>
</div>

{% endhighlight %}

When feedback is sent, you can validate whether the content area is empty or not. To achieve this validation use **RTE** client side events. In this **RTE**, it provides the “action” function for performing the client side events to custom tool.

You can specify the custom tool as previous script section with validation operations.

{% highlight js %}

    $(function() {
       $("#feedBackEditor").ejRTE({
          width: "98%",
          tools: {
             customTool: [{
                name: "PostFeedBack", //Id for the newly added tool
                tooltip: "submit the feedback", // Shows the tooltip for the custom tool
                css: "FeedBack", // Css class for custom tool design purpose
                action: function() {
                   var editorObj = $("#feedBackEditor").data("ejRTE");
                   //support the client side validation for content present in the area or not
                   if (($.trim(editorObj.getText()).length < 1)) {
                      //the content area is empty
                      $(".output").html("The feedback content is empty");
                   } else { //the content area contains information
                      $(".output").html("");
                      //custom code to send the feedback form contents
                      alert("The feedback content has been saved");
                   }
                }
             }]
          }
       });
    });

{% endhighlight %}

The following styles are used to achieve the feedback form editor application.

{% highlight css %}

<style>
    .commentSection {
        width: 60%;
        background: none repeat scroll 0 0 #f9f9f1;
        border: 1px solid #e9e9e1;
        padding: 10px;
    }
    .titleSection {
        text-indent: 20px;
        float: left;
        padding: 20px 0px;
        width: 98%;
        border: 1px solid #bbbcbb;
    }
    .output {
        height: 20px;
        padding: 5px;
        color: red;
    }
    .titleSection .level {
        margin: 15px 0px 5px 0px;
    }
    .input.ejinput {
        text-indent: 5px;
        height: 24px;
        width: 80%;
        margin-left: 5px;
    }
</style>


{% endhighlight %}

The output of the above steps is to send the feedback without content.

{% include image.html url="/js/RichTextEditor/Getting-Started_images/Getting-Started_img6.png" %}

