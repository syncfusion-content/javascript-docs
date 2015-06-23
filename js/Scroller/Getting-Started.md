---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Scroller
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Scroller** in your application with **JavaScript**.

## Create your first Scroller in JavaScript

**Essential JavaScript Scroller** control can be rendered based on the target panel height and width, and includes more customization options.

**Add Scroller Control to your JavaScript Application**

Create a HTML file and paste the following template to the HTML file to create the ejScroller.

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <title>Getting Started Essential JS</title>
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
               <h3>MVC </h3>
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



Initialize **ejScroller** in the target area in the script.

{% highlight js %}

    $(function() {
       // document ready
       // simple scroller creation
       $("#scrollcontent").ejScroller({
          height: 150,
          width: 300
       });
    });

{% endhighlight %}



Configure the styles.

{% highlight css %}
    
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



Scroller control is added to the application. 

{% include image.html url="/js/Scroller/Getting-Started_images/Getting-Started_img1.png"%}

