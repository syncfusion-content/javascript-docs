---
layout: post
title: right to left
description: right to left
platform: js
control: General Topics
documentation: ug
---

# Right To Left

All the **Essential JavaScript** **Widget** supports **RTL** option, when set to **true** will align the widget and its contents from **Right to Left**. The property **enableRTL** is used to handle this behaviour and is set to false by default for all the widgets. 

**Example**: To display the DatePicker control from Right-To-Left, we need to define its **enableRTL** property to **true** as depicted below,

N> Add and refer the necessary **Scripts** and **Stylesheets** to your sample application, before initializing any of the controls.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <title>My first HTML page</title>
        <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
        <script src="Scripts/jquery-1.10.2.min.js"></script>
        <script src="Scripts/jquery.easing.1.3.min.js"></script>
        <script src="Scripts/jsrender.min.js"></script>
        <script src="Scripts/ej/ej.web.all.min.js"></script>
        // Culture file reference to use the ar-DZ culture
        <script src="Scripts/cultures/ej/cultures/ej.culture.ar-DZ.min.js"></script>
    </head>
    <body>     
        <!--Container for ejDatePicker widget-->
        <input id="startDate" type="text" /> 

        <script type="text/javascript">
            $(function () {
                // initialization of ejDatePicker control with enableRTL property (Since the arabic script is the most widespread RTL writing system, therefore here we have showcased our datepicker control localized in one of the Arabic language.)
                $("#startDate").ejDatePicker({ locale: "ar-DZ", 
                      enableRTL: true,   
                      buttonText: "اليوم" 
                });
            });
        </script>
    </body>
</html>

{% endhighlight %}



The below screenshot displays the datepicker control from Right to left direction,

![](righttoleft_images\righttoleft_img1.png)





