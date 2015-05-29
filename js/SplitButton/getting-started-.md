---
layout: post
title: getting-started-
description: getting started 
platform: js
control: Split Button
documentation: ug
---

# Getting Started 

This section explains briefly about how to create a **Split Button** in your application with **JavaScript**. and **ASP.NET MVC**.

## Create your first Split Button in JavaScript

The **HTML** button element and the **&lt;UL&gt;, &lt;LI&gt;** are easily configured as **Essential JavaScript Split Button** control.  The basic rendering of **Essential JavaScript Split****Button** is achieved by using default functionality. Initially the **targetID** is a mandatory one, without this field it does not act as normal button on two sides.

### Control structure



{% include image.html url="\js\SplitButton\getting-started-_images\getting-started-_img1.png" Caption="Figure 1: Essential JavaScript Split Button"%}

### Split Button Creation

* Create an **HTML** file and add the following template to **HTML** file for **ejSplit Button** creation.

{% highlight html %}


<!doctype html>
DOCTYPE html>
<html>
<head>
<title>Getting Started Essential JS</title> 
      <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body><!--add button element here-->//add button element here</body>
</html>


{% endhighlight %}



* Adding button element and **&lt;UL&gt;, &lt;LI&gt;** element for **Split****Button** rendering.



{% highlight html %}

<button id="sbutton">Save</button>
<ul id="target">
    <li><a href="#">Open..</a></li>
    <li><a href="#">Save</a></li>
    <li><a href="#">Delete</a></li>
</ul>


{% endhighlight %}



* Initialization of **ejSplitButton** in script



{% highlight js %}

<script>
        $(function () {
            // simple control creation
            $("#sbutton").ejSplitButton({
                width: "120px",
                height: "50px",
                showRoundedCorner: true,
                targetID: "target"
            });
        });
    </script>$(function () {
        // document ready
// simple control creation
           $("#sbutton").ejSplitButton({
                width: "120px",
height: "50px",
                showRoundedCorner:true,
                targetID: "target"
            });
});


{% endhighlight %}



* Output of above steps



{% include image.html url="\js\SplitButton\getting-started-_images\getting-started-_img2.png" Caption="Figure 2: Split Button"%}



## Create your first Split Button in MVC

The **HTML** button element and the **&lt;UL&gt;, &lt;LI&gt;** can be easily configured as **Essential ASP.NET MVC Split Button** control.  The basic rendering of **Essential ASP.NET MVC Split Button** is achieved by using default functionality. Initially the **targetID** is a mandatory one, without this field it acts as normal button on two sides.

**Create Split Button Control in MVC**

**Essential ASP.NET MVC Split Button** control contains built-in features such as Click and different option choosing. You can easily create the **Split Button** control by using **HTML** helper as follows.

* You can create an **MVC** Project and add necessary assemblies, styles and scripts to it.  Refer [MVC-Getting Started.](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)

Add the following code to the corresponding view page to render **Split Button**.



@Html.EJ().SplitButton("sbutton").Text("Save").ShowRoundedCorner(true).Size(ButtonSize.Large).TargetID("target")



* Add the following **&lt;UL&gt;, &lt;LI&gt;** elements to render **Split Button** with popup option.



       &lt;ul id="target"&gt;

            &lt;li&gt;<span>Open..&lt;/span&gt;&lt;/li&gt;

            &lt;li&gt;<span>Save</span>&lt;/li&gt;

            &lt;li&gt;<span>Delete</span>&lt;/li&gt;

        &lt;/ul&gt;      



Output of the above steps.

The following screenshot illustrates the functionality of **Split Button** in login options.



{% include image.html url="\js\SplitButton\getting-started-_images\getting-started-_img3.png" Caption="Figure 3: Split Button with login options"%}

## Create your first Split Button in ASP.NET

You can add the items in **Split Button** that is displayed when you click the **Split Button**. Or it acts as a normal button on two sides.

**Control structure**



{% include image.html url="\js\SplitButton\getting-started-_images\getting-started-_img4.png" Caption="Figure 4: Essential ASP.NET Split Button"%}

**Split Button Creation**

**Essential ASP.NET Split Button** control contains built-in features such as Click and different display options. You can easily create the **Split Button** control by using **HTML** helper as follows.

* You can create a WEB Project and add necessary assemblies, styles and scripts to it. Refer[ASP-Getting Started.](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)

* Create an ASPX file and add the following code example to ASPX file for **ejSplitButton** creation.



**[ASPX]**

&lt;ej:SplitButton ID="ButtonSizeLarge" runat="server" Text="Save" Size="Large" ShowRoundedCorner="true"&gt;

        &lt;Items&gt;

            &lt;ej:SplitItem Text="Open.."&gt;&lt;/ej:SplitItem&gt;

            &lt;ej:SplitItem Text="Save"&gt;&lt;/ej:SplitItem&gt;

            &lt;ej:SplitItem Text="Delete"&gt;&lt;/ej:SplitItem&gt;

        &lt;/Items&gt;

    &lt;/ej:SplitButton&gt;





![C:\Users\labuser\Desktop\note.jpg](getting-started-_images\getting-started-_img5.jpeg)_**Note: Add menu items of Split Button inside of &lt;Items&gt; that is displayed when you click on split button**_



Output of above steps



{% include image.html url="\js\SplitButton\getting-started-_images\getting-started-_img6.png" Caption="Figure 5: Split Button"%}

