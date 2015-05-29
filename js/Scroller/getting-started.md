---
layout: post
title: getting-started
description: getting started
platform: js
control: Scroller
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Scroller** in your application with **JavaScript,****ASP.NET MVC** and **ASP.NET**.

## Create your first Scroller in JavaScript

**Essential JavaScript Scroller** control can be rendered based on the target panel height and width, and includes more customization options.

### Add Scroller Control to your JavaScript Application

* Create a HTML file and paste the following template to the HTML file to create the ejScroller.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <title>Getting Started Essential JS</title> 
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
   <!--Target area to apply Scroller.-->
    <div id="scrollcontent">
        <div>
            <!--Wrapper div for Scroller.-->
            <div class="innercontent">
                <!--Content div-->
                <h3> MVC </h3>
                <p>
                    Model–view–controller (MVC) is a software architecture pattern which
                    separates the representation of information from the user's interaction
                    with it. The model consists of application data, business rules, logic, and
                    functions. A view can be any output representation of data, such as a chart
                    or a diagram.
                </p>
            </div>
        </div>
    </div>// Target area to apply Scroller.
   <div id="scrollcontent">
        <div> // Wrapper div for Scroller.
            <div class="innercontent"> // Content div
                <h3> MVC </h3>
                <p>
                 Model–view–controller (MVC) is a software architecture pattern which   
                 separates the representation of information from the user's interaction 
                 with it. The model consists of application data, business rules, logic, and 
                 functions. A view can be any output representation of data, such as a chart 
                 or a diagram. 
                </p>
</div>
</div>
   </div>   
</body>
</html>


{% endhighlight %}





* Initialize **ejScroller** in the target area in the script.



{% highlight js %}


<script>
        $(function () {
            // document ready
            // simple scroller creation
            $("#scrollcontent").ejScroller({ height: 150, width: 300 });
        });
    </script>$(function () {
// document ready
// simple scroller creation
$("#scrollcontent").ejScroller({ height: 150, width: 300 });
});


{% endhighlight %}



*  Configure the styles 


{% highlight css %}

**[CSS]**

<style type="text/css">

    #innercontent {
        width: 400px;
        padding: 15px;
    }

    #scrollcontent {
        border: 1px solid grey;
    }

</style>


{% endhighlight %}



* Scroller control is added to the application. 



{% include image.html url="\js\Scroller\getting-started_images\getting-started_img1.png" Caption="Figure 2: Target area with Scroller"%}

## Create your first Scroller in MVC

## ASP.NET MVC Scroller control allows you to slide document whose position corresponds to a value. The document has text, HTML content or images. Refer the following guidelines to create a Scroller control for horizontal and vertical Scrolling.

## Add Scroller Control to your MVC Application

## Essential Studio ASP.NET MVC Scoller control has a built-in feature to customize the resizing and changing the Scrollbar theme.

## Create an MVC Project and add required assemblies, scripts, and styles to it. Refer MVC-Getting Started Documentation.

## Add the following code example to the corresponding view page to render the Scroller. 

## 

###     &lt;div id="scrollcontent"&gt;

###         &lt;div&gt; @* Wrapper div for Scroller.*@

###             &lt;div class="innercontent"&gt; @* Content div*@

###                 &lt;h3&gt; MVC &lt;/h3&gt;

###                 &lt;p&gt;

###                  Model–view–controller (MVC) is a software architecture pattern which   

###                  separates the representation of information from the user's interaction 

###                  with it. The model consists of application data, business rules, logic, and 

###                  functions. A view can be any output representation of data, such as a chart 

###                  or a diagram. 

###                 &lt;/p&gt;

### 	     &lt;/div&gt;

### 	&lt;/div&gt;

### &lt;/div&gt;   

### 

###     @{ Html.EJ().Scroller("scrollcontent").Height(150).Width(300).Render(); }

### 

## 

## Add the following style in the view page to set the height and width of the Scroller.

## 

### &lt;style type="text/css" class="cssStyles"&gt;

###     .innercontent{

###         width: 400px;

###         padding:15px;

###     }

### &lt;/style&gt;

## Execute the above example code to get the following output. 

## 

## Figure 3: Target area with Scroller

## Create your first Scroller in ASP.NET

## ASP.NET Scroller control can be rendered based on the target panel height and width, and includes more customization options.

## Add Scroller Control to your ASP.NET Web Application

## You can create an ASP.NET Project and add necessary Dll and script with the help of the given ASP-Getting Started Documentation.

## You can add the following code example to the corresponding ASPX page to render Scroller.

## 

### [ASPX]

### &lt;div&gt;

###         &lt;div class="control"&gt;

###             &lt;div id="ScrollContent"&gt;

###                 &lt;div&gt;

###                     &lt;div class="sampleContent"&gt;

###                         &lt;h3 style="font-size: 15px;"&gt;

###                             MVC</h3>

###                         &lt;div&gt;

###                             &lt;p&gt;

###                                 Model–view–controller (MVC) is a software architecture pattern which separates the

###                                 representation of information from the user's interaction with it. The model consists

###                                 of application data, business rules, logic, and functions. A view can be any output

###                                 representation of data, such as a chart or a diagram. Multiple views of the same

###                                 data are possible, such as a bar chart for management and a tabular view for accountants.

###                                 The controller mediates input, converting it to commands for the model or view.The

###                                 central ideas behind MVC are code reusability and n addition to dividing the application

###                                 into three kinds of components, the MVC design defines the interactions between

###                                 them.

###                             &lt;/p&gt;

###                             &lt;ul&gt;

###                                 &lt;li&gt;<b>A controller </b>can send commands to its associated view to change the view's

###                                     presentation of the model (e.g., by scrolling through a document). It can also send

###                                     commands to the model to update the model's state (e.g., editing a document).

###                                 &lt;/li&gt;

###                                 &lt;li&gt;<b>A model</b> notifies its associated views and controllers when there has been

###                                     a change in its state. This notification allows the views to produce updated output,

###                                     and the controllers to change the available set of commands. A passive implementation

###                                     of MVC omits these notifications, because the application does not require them

###                                     or the software platform does not support them. &lt;/li&gt;

###                                 &lt;li&gt;<b>A view</b> requests from the model the information that it needs to generate

###                                     an output representation to the user. &lt;/li&gt;

###                             &lt;/ul&gt;

###                         &lt;/div&gt;

###                     &lt;/div&gt;

###                 &lt;/div&gt;

###             &lt;/div&gt;

###         &lt;/div&gt;

###         &lt;ej:Scroller ID="ScrollContent" runat="server" Height="150" Width="300"&gt;

###         &lt;/ej:Scroller&gt;

###     &lt;/div&gt;

## 

## Initialize Scroller with following styles.

## 

### [CSS]

###   &lt;style type="text/css" class="cssStyles"&gt;

###         .control

###         {

###             border: 1px solid #bbbcbb;

###             color: gray;

###             width: 300px;

###             margin: 0 auto;

###             height: 150px;

###         }

###         

###         .sampleContent

###         {

###             width: 350px;

###             padding: 7px;

###         }

###     &lt;/style&gt;

## 

## Output of the above steps. 

## 

## 

##  Figure 4: Target area with Scroller

