---
layout: post
title: getting-started
description: getting started
platform: js
control: RichTextEditor
documentation: ug
---

# Getting Started

This section briefly describes how to create and use **RichTextEditor** control using **Javascript**, **MVC** and **ASP.NET** in your application.

## Create your first RichTextEditor in JavaScript

The **Essential JavaScript RichTextEditor (RTE)** control allows easily to edit contents, insert tables, images and to get the **HTML** content. In this section, you can learn how to use **RichTextEditor** for getting Feedback from the user. The following screenshot demonstrates how the **RTE** control is used in Feedback form.



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img1.png" Caption="Figure 2: RTE support with Feedback Form functionality"%}

In the above screenshot , the **RTE** consists of content editable area with feedback title when you click the Post Feedback toolbar item to send the feedback information.

### Create a RichTextEditor

**Essential JavaScript RTE** widget basically renders by using simple text area element. The following steps describe the creation of **RTE** control.  

* Create an **HTML** file and add the following template to it for **RTE** creation.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
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





* Add text area element within the body element for **RichTextEditor** rendering.



{% highlight html %}

<div>
       <textarea id="feedBackEditor"></textarea>       
</div>


{% endhighlight %}



* Initialize **RTE** in script.



{% highlight js %}

<script type="text/javascript">     
$(function () {
// document ready
// simple RTE creation
	$("#feedBackEditor").ejRTE();       
});
</script>



{% endhighlight %}



The following **RTE** screenshot is the output of above steps.



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img2.png" Caption="Figure 3: Empty RTE control"%}

### Configure the Toolbar

The **RichTextEditor** is used to configure the toolbar items to provide editing and styling functionality. In this scenario, use the default **RTE** toolbar item to provide feedback form. 

#### Add the Toolbar Item

The additional functionality toolbar item is necessary to perform the required operation. The **RTE** provides some additional toolbar items that are already predefined, but not rendered in without specifying the toolbar items. 

The following code example is used to render the additional in-built toolbar items to **RTE** toolbar list.

{% highlight js %}

    <script type="text/javascript">

        $(function () {

            $("#feedBackEditor").ejRTE({

                width: "100%",

                tools: {

//specify the font type, size, color and background color option for text

                    font: ["fontName", "fontSize", "fontColor", "backgroundColor"],

                }

            });

        });

    </script>


{% endhighlight %}



The following screenshot is the output of above steps:



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img3.png" Caption="Figure 4: RTE with adding inbuilt toolbar item"%}

#### Removing the ToolbarItem

You can remove the particular toolbar item using **remove ToolbarItem** method. 

Consider that the **“create table”** toolbar item is not necessary for the feedback scenario. To easily remove the **“create table”** toolbar item the following code example is used to remove the in-built toolbar items from **RTE** toolbar list.



{% highlight js %}

<script type="text/javascript">     
     var editorObj;
     $(function () {            
         $("#feedBackEditor").ejRTE();
         //create the editor object for removing the toolbar item   
         editorObj = $("#feedBackEditor").data('ejRTE'); 
         //remove the create table toolbar item by specifying the create table toolbar id   
         editorObj.removeToolbarItem("feedBackEditorcreateTable");
     });
</script>


{% endhighlight %}



The following screenshot is the output of above steps:



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img4.png" Caption="Figure 5: RTE support for removing toolbar item"%}

#### Configure Custom Toolbar item

To post the feedback directly you need additional toolbar item. The **RTE** control provides support to create the custom toolbar item for custom action. The following code example demonstrates the custom **toolbar** item creation in the **RTE** control.



{% highlight js %}

<script type="text/javascript" class="jsScript">     
    $(function () {
        $("#feedBackEditor").ejRTE({   
         tools: {        
           customTool: [{
                        name: "PostFeedBack", //Id for the newly added tool
                        tooltip: "Submit the feedback",// Shows the tooltip for custom tool
                        css: "FeedBack",
                        action: function () {
                            //when click the custom tool item, the event will triggered                             
                        }
                    }] 
                }
       });
       $("div.FeedBack").html("Post Feedback");       
 });
</script>


{% endhighlight %}



The following screenshot is the output of above steps:



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img5.png" Caption="Figure 6: RTE with Custom toolbar item"%}

### Validate the Content

To send the feedback form without contents you need to validate them before submitting the contents. To achieve this validation use **getText()** method in **RTE** control.

When the content area is empty, you set the notification message displayed in the &lt;div&gt; element area in order to alert the user. The following **HTML** code example is used to create the feedback form editor with support of **RTE** control.



{% highlight html %}

<div class="commentSection">
        <div class="titleSection">
            <label>Title:</label>
            <input type="text" class="input ejinput"/>
        </div>
        <!--textarea element section-->
        <textarea id="feedBackEditor" class="hide" rows="10" cols="30">            
        </textarea>
        <!-- validation message display area-->
        <div class="output"></div>
</div>


{% endhighlight %}



When feedback is sent, you can validate whether the content area is empty or not. To achieve this validation use **RTE** client side events. In this **RTE**, it provides the “action” function for performing the client side events to custom tool.

You can specify the custom tool as previous script section with validation operations.

{% highlight js %}

        $(function () {
            $("#feedBackEditor").ejRTE({

                width: "98%",

                tools: {

                    customTool: [{

                        name: "PostFeedBack", //Id for the newly added tool

                        tooltip: "submit the feedback",// Shows the tooltip for the custom tool

                        css: "FeedBack",    // Css class for custom tool design purpose

                        action: function () {
                            var editorObj = $("#feedBackEditor").data("ejRTE");var editorObj = $("#feedBackEditor").ejRTE();
                            //support the client side validation for content present in the area or not

                            if (($.trim(editorObj.getText()).length < 1)) {

                                //the content area is empty

                                $(".output").html("The feedback content is empty");

                            } else {   //the content area contains information

                                $(".output").html("");

                                //custom code to send the feedback form contents

                                alert("The feedback content has been saved");

                            }

                        }

                    }]

                }

            });
        });
    </script>


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
            width: 10098%;
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



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img6.png" Caption="Figure 7: RTE content validation"%}

## Create your first RichTextEditor in MVC

The **ASP.NET MVC RichTextEditor (RTE)** control allows you to edit contents, insert tables, images and to get the HTML content. In this section you can learn how to use **RichTextEditor** in order to get **Feedback** from the user. 

The following screenshot demonstrates how the **RTE** control is used in **Feedback** form.



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img7.png" Caption="Figure 8: RTE support with Feedback Form functionality"%}

In the above screenshot , the **RTE** consists of content editable area with Feedback title.In this **RTE** application, you can click the **PostFeedback** toolbar item to send the Feedback information.

**Create a RichTextEditor** 

**ASP.NET MVC RTE** widget basically renders by using simple text area element. 

* You can create a **MVC** Project and add necessary Dll’s and scripts with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

Add the following code example to the corresponding view page to render **RichTextEditor**.





@Html.EJ().RTE("FeedbackEditor")



The following **RTE** screenshot renders the output of the above steps.



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img8.png" Caption="Figure 9: Empty RTE control"%}

**Configure the Toolbar**

The **RichTextEditor** configures the toolbar items to provide editing and styling functionalities. In this scenario, you can use the default **RTE** toolbar item to provide Feedback form support. 

**Add the Toolbar Item**

The additional functionality toolbar item is necessary to perform the required operation. The **RTE** provides some additional toolbar items that are predefined, but not rendered.  

The following code example renders the additional inbuilt toolbar items to **RTE** toolbar list.





@{

    List<string> font = new List<string>() { "fontName", "fontSize","fontColor"  };

}



@Html.EJ().RTE("FeedbackEditor").Tools(tool => tool.Font(font)) 





 The following screenshot displays the **RTE** with inbuilt toolbar item.



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img9.png" Caption="Figure 10: RTE supports inbuilt toolbar item"%}

**Remove the ToolbarItem**

Sometimes, an existing toolbar item is not necessary to perform the required operation. You can remove the particular toolbar item using **remove ToolbarItem** method. 

For example, consider ‘**create table**’ toolbar item is not necessary for the Feedback scenario. You can easily remove the ‘**create table**’ toolbar item using the following code example.



[CSHTML]

@Html.EJ().RTE("FeedbackEditor")





&lt;script type="text/javascript"&gt;

    var editorObj;

    $(function () {

        $("#FeedbackEditor").ejRTE();

        editorObj = $("#FeedbackEditor").data('ejRTE');

        //remove the create table toolbar item by specifying the create table toolbar id

        editorObj.removeToolbarItem("FeedbackEditorcreateTable");

    });



&lt;/script&gt;



The following screenshot displays ‘**create table**’ toolbar item is removed from the toolbar list.



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img10.png" Caption="Figure 11: RTE supports removing toolbar item"%}

**Configure Custom Toolbar item**

To post the Feedback directly, you need additional **Toolbar** item. The **RTE** control provides support to create the **custom toolbar item** for custom action. 

The following code example creates the **custom toolbar item** in the **RTE** control. 



@Html.EJ().RTE("FeedbackEditor").Width("820px").Tools(tool => tool.CustomTool(custom =>

                    custom.Name("PostFeedback").Tooltip("click to Post Feedback messages").Css("Feedback").Add()))





  Add the following styles for the **custom****toolbar****item**.

&lt;style&gt;

    .Feedback {

        height: 22px;

        width: 100px;

        display: block;

        text-align: center;

        font-weight: bold;

    }

&lt;/style&gt; 



The following screenshot displays **RTE** with **custom toolbar item**.

{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img11.png" Caption="Figure 12: RTE with Custom toolbar item"%}

**Validate the Content**

In some cases, to send the Feedback form without contents you can validate them before submitting the Feedback contents. To achieve this validation, you can use **getText()** method in **RTE** control.

When the content area is empty, you can set the notification message displayed in the **&lt;div&gt;** element area in order to give an alert message. The following **HTML** code example creates the Feedback form editor with the support of **RTE** control.

During the Feedback sending time, you can validate whether the content area is empty or not. To achieve this validation, you can use **RTE** client-side events. **RTE** provides the ‘**action’** function to perform the client-side events to custom tool.

You can specify the custom tool same as previous section with validation operations.





&lt;div class="commentSection" style="width: 810px"&gt;

    &lt;div class="titleSection"&gt;

        <label>Title:&lt;/label&gt;

        &lt;input type="text" class="input ejinput" /&gt;

    &lt;/div&gt;

    &lt;!--RTE element section--&gt;



@Html.EJ().RTE("FeedbackEditor").Width("98%").ClientSideEvents(cs=>cs.Change("change")).Tools(tool => tool.CustomTool(custom =>

                    custom.Name("PostFeedback").Tooltip("click to Post Feedback messages").Css("Feedback").Action("validate").Add()))



&lt;!-- validation message display area--&gt;

        &lt;div class="output"&gt;&lt;/div&gt;

&lt;/div&gt;





&lt;script type="text/javascript"&gt;

function validate() {

        var editorObj = $("#FeedbackEditor").data('ejRTE');

        if (($.trim(editorObj.getText()).length < 1)) {

            //the content area is empty

            $(".output").html("The Feedback content is empty");

        } else {   //the content area contains information

            $(".output").html("");

            //custom code to send the Feedback form contents 

            alert("The Feedback content has been saved");

        }

    }

&lt;/script&gt;





You can add the following styles to achieve the Feedback form editor application.

&lt;style&gt;

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

            width: 100%;

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

&lt;/style&gt;



The following screenshot displays the Feedback sending without content.


{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img12.png" Caption="Figure 13: RTE support with Feedback Form functionality"%}

## Create your first RichTextEditor in ASP.NET

The **ASP.NET WebForms RichTextEditor (RTE)** control allows you to edit contents, insert tables, images and to get the **HTML** content. In this section you can learn how to use **RichTextEditor** in order to get **Feedback** from the user. 

The following screenshot demonstrates how the **RTE** control is used in **Feedback** form.



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img13.png" Caption="Figure 14: RTE support with Feedback Form functionality"%}

In the above screenshot , the **RTE** consists of content editable area with Feedback title.In this **RTE** application, you can click the **PostFeedback** toolbar item to send the Feedback information.

**Create a RichTextEditor** 

**ASP.NET WebForms RTE** widget basically renders by using simple text area element. 

* You can create an **ASP.NET****Web****F****orms** Project and add necessary Dll’s and scripts with the help of the given ASP.NET Webforms-Getting Started Documentation.

Add the following code example to the corresponding view page to render **RichTextEditor**.



**[ASPX]**



&lt;ej:RTE ID="FeedbackEditor" runat="server"&gt;

&lt;/ej:RTE&gt;



The following **RTE** screenshot renders the output of the above steps.

{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img14.png" Caption="Figure 15: Empty RTE control"%}

**Configure the Toolbar**

The **RichTextEditor** configures the toolbar items to provide editing and styling functionalities. In this scenario, you can use the default **RTE** toolbar item to provide Feedback form support. 

**Add the Toolbar Item**

The additional functionality toolbar item is necessary to perform the required operation. The **RTE** provides some additional toolbar items that are predefined, but not rendered.  

The following code example renders the additional inbuilt toolbar items to **RTE** toolbar list.

[ASPX]

&lt;ej:RTE ID="FeedbackEditor" runat="server"&gt;

    &lt;Tools Font="fontName,fontSize,fontColor,backgroundColor"&gt;

    &lt;/Tools&gt;

&lt;/ej:RTE&gt;



 The following screenshot displays the **RTE** with inbuilt toolbar item.

{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img15.png" Caption="Figure 16: RTE supports inbuilt toolbar item"%}

**Remove the ToolbarItem**

Sometimes, an existing toolbar item is not necessary to perform the required operation. You can remove the particular toolbar item using **removeToolbarItem** method. 

For example, consider ‘**create table**’ toolbar item is not necessary for the Feedback scenario. You can easily remove the ‘**create table**’ toolbar item using the following code example.

**[ASPX]**

&lt;ej:RTE ID="FeedbackEditor" runat="server"&gt;

&lt;/ej:RTE&gt;

 &lt;script type="text/javascript"&gt;



     window.onload = function () {

         $("#&lt;%=FeedbackEditor.ClientID%&gt;").ejRTE();

         var editorObj = $("#&lt;%=FeedbackEditor.ClientID%&gt;").data('ejRTE');

         //remove the create table toolbar item by specifying the create table toolbar id  

         editorObj.removeToolbarItem("<%=FeedbackEditor.ClientID%>createTable");

     };



&lt;/script&gt;





The following screenshot displays ‘**create table**’ toolbar item is removed from the toolbar list.



{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img16.png" Caption="Figure 17: RTE supports removing toolbar item"%}

**Configure Custom Toolbar item**

To post the Feedback directly, you need additional **Toolbar** item. The **RTE** control provides support to create the **custom toolbar item** for custom action. 

To Add Custom Toolbar to the **RTE** control, you can include **Syncfusion.JavaScript.Models** namespace in your **web.cofig** file. Include the following code example in **web.config** file under &lt;system.web&gt; section.

**[web.config]**



&lt;pages&gt;

      &lt;controls&gt;

        &lt;add  namespace="Syncfusion.JavaScript.Models" assembly="Syncfusion.EJ" tagPrefix="ej"/&gt;

       &lt;/controls&gt;

&lt;/pages&gt;



The following code example creates the **custom toolbar item** in the **RTE** control. 

**[ASPX]**



&lt;ej:RTE ID="FeedbackEditor" runat="server"&gt;

    &lt;Tools&gt;

        &lt;CustomTool&gt;

            &lt;ej:CustomTool Name="Post Feedback" Css="Feedback" Tooltip="click to Post Feedback messages" /&gt;

        &lt;/CustomTool&gt;

    &lt;/Tools&gt;

&lt;/ej:RTE&gt; 



  Add the following styles for the **custom****toolbar****item**.

&lt;style&gt;

    .Feedback {

        height: 22px;

        width: 100px;

        display: block;

        text-align: center;

        font-weight: bold;

    }

&lt;/style&gt; 



The following screenshot displays **RTE** with **custom toolbar item**.

{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img17.png" Caption="Figure 18: RTE with Custom toolbar item"%}

**Validate the Content**

In some cases, to send the Feedback form without contents you can validate them before submitting the Feedback contents. To achieve this validation, you can use **getText()** method in **RTE** control.

When the content area is empty, you can set the notification message displayed in the **&lt;div&gt;** element area in order to give an alert message. The following **HTML** code example creates the Feedback form editor with the support of **RTE** control.

During the Feedback sending time, you can validate whether the content area is empty or not. To achieve this validation, you can use **RTE** client-side events. **RTE** provides the ‘**action’** function to perform the client-side events to custom tool.

You can specify the custom tool same as previous section with validation operations.



[ASPX]

&lt;div class="commentSection"&gt;

    &lt;div class="titleSection"&gt;

        <label>Title:&lt;/label&gt;

        &lt;input type="text" class="input ejinput" /&gt;

    &lt;/div&gt;

    &lt;!--RTE element section--&gt;

    &lt;ej:RTE ID="FeedbackEditor" runat="server"&gt;

        &lt;Tools&gt;

            &lt;CustomTool&gt;

                &lt;ej:CustomTool Action="validate" Name="PostFeedback" Css="Feedback" Tooltip="click to Post Feedback messages" /&gt;

            &lt;/CustomTool&gt;

        &lt;/Tools&gt;

    &lt;/ej:RTE&gt;

    &lt;!-- validation message display area--&gt;

    &lt;div class="output"&gt;&lt;/div&gt;

&lt;/div&gt;

 &lt;script type="text/javascript"&gt;

     function validate() {

         var editorObj = $("#&lt;%=FeedbackEditor.ClientID%&gt;").data('ejRTE');

         if (($.trim(editorObj.getText()).length < 1)) {

             //the content area is empty

             $(".output").html("The Feedback content is empty");

         } else {   //the content area contains information

             $(".output").html("");

             //custom code to send the Feedback form contents

             alert("The Feedback content has been saved");

         }

     }

&lt;/script&gt;



You can add the following styles to achieve the Feedback form editor application.

&lt;style&gt;

    .commentSection {

        width: 786px;

        background: none repeat scroll 0 0 #f9f9f1;

        border: 1px solid #e9e9e1;

        padding: 10px;

    }



    .titleSection {

        text-indent: 20px;

        float: left;

        padding: 20px 0px;

        width: 100%;

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

&lt;/style&gt;





The following screenshot displays the Feedback sending without content.

{% include image.html url="\js\RichTextEditor\getting-started_images\getting-started_img18.png" Caption="Figure 19: RTE support with Feedback Form functionality"%}

