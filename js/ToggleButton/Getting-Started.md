---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Toggle Button
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Toggle****Button** in your application with **JavaScript.**

## Create your first Toggle Button in JavaScript

The html checkbox element can be easily configured as **Essential JavaScript Toggle Button** control. The basic rendering of **Essential JavaScript Toggle Button** is achieved by using default functionality.

### Control structure

{% include image.html url="/js/ToggleButton/Getting-Started_images/Getting-Started_img1.png" Caption="Figure 1: Essential JavaScript Toggle Button in OFF state"%}



{% include image.html url="/js/ToggleButton/Getting-Started_images/Getting-Started_img2.png" Caption="Figure 2: Essential JavaScript Toggle Button in ON state"%}



### Toggle Button Creation



* Create an HTML file and paste the following template to html file for **ejToggleButton** creation.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<title>Getting Started Essential JS</title> 
    <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body><!--add Toggle Button element here--></body>
</html>


{% endhighlight %}



* Adding input Checkbox element for Toggle Button rendering.



{% highlight html %}

<input type="checkbox" id="tbutton"/>
<label for="tbutton">Play</label>


{% endhighlight %}



{% include image.html url="/js/ToggleButton/Getting-Started_images/Getting-Started_img3.jpeg" Caption=""%}_**Note: The advantages of using checkbox element and label element for the rendering of Toggle Button are as follows.**_



**Checkbox Element:**

The HTML checkbox element is made as the base for **Essential JavaScript Toggle Button**, because to provide convenient look and feel while building forms and support basic methods and its states.

**Label Element:**

A label element has to be explicitly associate a form control. A label is attached to a specific form control through the use of for attribute. The value of for attribute must be the same as the value of the id attribute of the form control. Clicking on the label or the control will activate the control in order to provide larger area of the control.



* Initialization of **ToggleButton** in script



{% highlight js %}

<script>
        $(function () {
            // simple control creation
            $("#tbutton").ejToggleButton({
                size:"small"
            });
        });
    </script>


{% endhighlight %}



* Output of above steps



{% include image.html url="/js/ToggleButton/Getting-Started_images/Getting-Started_img4.png" Caption="Figure 3: Toggle Button"%}



