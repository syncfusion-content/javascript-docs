---
layout: post
title: getting-started
description: getting started
platform: js
control: Toggle Button
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Toggle****Button** in your application with **JavaScript** and **ASP.NET MVC.**

## Create your first Toggle Button in JavaScript

The html checkbox element can be easily configured as **Essential JavaScript JS Toggle Button** control. The basic rendering of **Essential JavaScript Toggle Button** is achieved by using default functionality.

### Control structure

{% include image.html url="\js\ToggleButton\getting-started_images\getting-started_img1.png" Caption="Figure 1: Essential JavaScript Toggle Button in OFF state"%}



{% include image.html url="\js\ToggleButton\getting-started_images\getting-started_img2.png" Caption="Figure 2: Essential JavaScript Toggle Button in ON state"%}



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
<body><!--add Toggle Button element here-->//add Toggle Button element here</body>
</html>


{% endhighlight %}



* Adding input Checkbox element for Toggle Button rendering.



{% highlight html %}

<input type="checkbox" id="tbutton"/>
<label for="tbutton">Play</label>


{% endhighlight %}



![C:\Users\labuser\Desktop\note.jpg](getting-started_images\getting-started_img3.jpeg)_**Note: The advantages of using checkbox element and label element for the rendering of Toggle Button are as follows.**_



**Checkbox Element:**

The HTML checkbox element is made as the base for **Essential JavaScript Toggle Button**, because to provide convenient look and feel while building forms and support basic methods and its states.

**Label Element:**

A label element has to be explicitly associate a form control. A label is attached to a specific form control through the use of for attribute. The value of for attribute must be the same as the value of the id attribute of the form control. Clicking on the label or the control will activate the control in order to provide larger area of the control.



* Initialization of **ejToggleButton** in script



{% highlight js %}

<script>
        $(function () {
            // simple control creation
            $("#tbutton").ejToggleButton({
                size:"small"
            });
        });
    </script>$(function () {
        // document ready
// simple control creation
       $("#tbutton").ejToggleButton();
});


{% endhighlight %}



* Output of above steps



{% include image.html url="\js\ToggleButton\getting-started_images\getting-started_img4.png" Caption="Figure 3: Toggle Button"%}{% include image.html url="\js\ToggleButton\getting-started_images\getting-started_img5.png" Caption="Figure 3: Toggle Button"%}



## Create your first Toggle Button in MVC

**ASP.NET MVC****Toggle Button** control allows you to perform the toggle option by using checked and unchecked state. **Toggle Button** helps you to check or uncheck their states. The **Toggle Button** control displays both text and images. The text displayed on the **Toggle Button** is contained in the Text property. The **Toggle Button** control display images using the **sprite Css****Class** and **ImagePosition** properties. The **Toggle Buttons** has theme support.

The following screenshot illustrates a **Toggle Button** control.



{% include image.html url="\js\ToggleButton\getting-started_images\getting-started_img6.png" Caption="Figure 4: Toggle Button in OFF state"%}



{% include image.html url="\js\ToggleButton\getting-started_images\getting-started_img7.png" Caption="Figure 5: Toggle Button in ON state"%}



**Create a Toggle Button**

**Essential Studio ASP.NET MVC Toggle Button** control has a built-in feature to customize both text and images.



1. Create an **MVC** Project and add required assemblies, scripts, and styles to it.  Refer [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code example to the corresponding view page to render the **Toggle Button**. 



@Html.EJ().ToggleButton("tbutton").Size(ButtonSize.Mini).ShowRoundedCorner(true).DefaultText("Play")



3. Output of the above steps.



{% include image.html url="\js\ToggleButton\getting-started_images\getting-started_img8.png" Caption="Figure 6: Toggle Button"%}



## Create your first Toggle Button in ASP.NET

The html checkbox element can be easily configured as **ASP.NET Toggle Button** control. The basic rendering of **ASP.NET Toggle Button** is achieved by using default functionality.

**Control structure**

{% include image.html url="\js\ToggleButton\getting-started_images\getting-started_img9.png" Caption="Figure 7: Essential ASP.NET Toggle Button in OFF state"%}



{% include image.html url="\js\ToggleButton\getting-started_images\getting-started_img10.png" Caption="Figure 8: Essential ASP.NET Toggle Button in ON state"%}



**Toggle Button Creation**

**Essential ASP.NET ToggleButton** control contains built-in features like Click and different display option. You can easily create the **ToggleButton** control by using **HTML** helper as follows.

1. You can create a WEB Project and add necessary assemblies, styles and scripts to it.  Refer [ASP-Getting Started.](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)

2. Create an aspx file and add the following code to aspx file for ejToggleButton creation.





**[ASPX]**

<ej:ToggleButton ID="ToggleButtonLarge" runat="server" Size="Large" ShowRoundedCorner="true"

        DefaultText="Play" ActiveText="Next">

    &lt;/ej:ToggleButton&gt;





3. Output of above steps



![](getting-started_images\getting-started_img11.png)

_Figure_ _9__: Toggle Button_

