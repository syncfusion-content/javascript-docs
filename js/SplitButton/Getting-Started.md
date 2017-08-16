---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: Split Button
documentation: ug
api: /api/js/ejsplitbutton
---

# Getting Started 

This section explains briefly about how to create a **Split Button** in your application with **JavaScript**.The **HTML** button element and the **&lt;UL&gt;, &lt;LI&gt;** are easily configured as **Essential JavaScript Split Button** control.  The basic rendering of **Essential JavaScript Split** **Button** is achieved by using default functionality. Initially the **targetID** is a mandatory one, without this field it does not act as normal button on two sides.


![](/js/SplitButton/Getting-Started_images/Getting-Started_img1.png)

**Split Button Creation**

Create an **HTML** file and add the following template to **HTML** file for **Split Button** creation.

{% highlight html %}

<!doctype html>
<html>
<head>
    <title>Getting Started Essential JS</title>
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!--add button element here-->
</body>
</html>


{% endhighlight %}

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.


Adding button element and **&lt;UL&gt;, &lt;LI&gt;** element for **Split** **Button** rendering.

{% highlight html %}


<button id="splitButton">Save</button>
<ul id="target">
    <li><a href="#">Open..</a></li>
    <li><a href="#">Save</a></li>
    <li><a href="#">Delete</a></li>
</ul>


{% endhighlight %}



Initialization of **ejSplitButton** in script

{% highlight javascript %}


        $(function () {
            // simple control creation
            $("#splitButton").ejSplitButton({
                width: "120px",
                height: "50px",
                showRoundedCorner: true,
                targetID: "target"
            });
        });
    


{% endhighlight %}



Output of above steps

![](/js/SplitButton/Getting-Started_images/Getting-Started_img2.png) 

